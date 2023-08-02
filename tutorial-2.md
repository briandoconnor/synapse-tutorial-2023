# Tutorial 2: Programmatic Synapse Access

Everything we've done to this point has been through the Synapse web interface.  This is great since it's really easy to get started but when you try to use Synapse for large projects with thousands of files, things get overwhelming very quickly.

In this tutorial we'll look at using Synapse through programmatic interfaces, namely with the Synapse Python client. In this way, you can script things like file upload and annotation so you and your collaborators can use interfaces like the File View to explore your data without a ton or work to set it up.  Likewise, the Python client allows you to download files for use in your analysis pipelines and to upload the results and provenance back.  For the most part, whatever you can do in the web interface you can do through the API the client accesses.  The preferred client is Python-based but we have a version that can run in R as well.

## Setting up Mybinder.org

For this tutorial we'll work in a Juypter notebook using Python. If your forte is R don't worry, the code examples are very simple and the more extensive online documentation for Synapse does a great job of showing you how to code in either Python or R.  

You may have experience using Jupyter notebooks either on your own computer, a VM in the cloud, or on a hosted platform like Velsera, Cavatica, or Tera.  In this tutorial we'll go super simple, we'll use https://mybinder.org/, a service that provides free Jupyter notebook (Jupyter Labs) instances for lightweight compute and exploration.  Parenthetically, this is a great way to make the Notebooks you store in GitHub immediately usable by others.  We won't go into great details on the features of MyBinder but this is really worth some exploration if you're interested.  You can include a customized `environment.yml` file in your GitHub repository to specify library dependencies and other configuration.  See the [documentation](https://mybinder.readthedocs.io/en/latest/introduction.html) for more details.  Lucky for us, a stock MyBinder instance works just fine for this tutorial!

Start by going to https://mybinder.org/ and entering `https://github.com/briandoconnor/synapse-tutorial-2023` into the 'GitHub repository name or URL field':

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3782dbb7-b3f1-40fa-8846-57b3dadd287b">

You'll then click 'launch' and wait a couple of minutes to start.  You can follow the progress and eventually get something that looks like the following:

<img width="1049" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/442eecc0-9853-466a-8c03-1df7b604db6b">

This is extremely nifty, there are few places online where you can use a fully functioning notebook environment for free.  If you're interested, another good free Notebook environment is [Google Collab](https://colab.google/), which I confirmed worked with the tutorial below.  Alternatively, you could use a pay service like Cavatica/Velsera or Tera (which are commonly used system for NIH programs). Here's a screenshot from the Google Collab alternative service:

<img width="1690" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/38ee1fdb-dbc4-4b0b-98e4-1c628b981fc8">

## Installing the Synapse Python Client

Now that your Binder notebook server is running, click on 'Python 3 (ipykernel)' under the Notebook section.  You should be greeted with a very empty notebook, something that looks like this:

<img width="1690" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/8a716861-8659-42b7-b8fa-4262ea2b4ecd">

Our first task is going to be to install the Synapse Python client library.  Put the following in the first code field:

```
!pip3 install synapseclient
```

Hit `shift`+`enter` to execute the cell.  You should see something like the following:

<img width="1690" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/80e2fc55-7b93-4c05-8e5f-2ffdd42c75ce">

You should see a success, in which case you now have the Synapse client installed in the Python instance running this notebook.

> [!IMPORTANT]  
> __Assignment:__
> Give it a try! Start a mybinder.org Notebook instance and let it launch until you see the Jupyter Labs interface.  If you prefer, you can use Google Collab.  Install the python client and make sure you see a success message.

## Logging in to Synapse

Now we need to authenticate/authorize the Synapse client in this notebook to work on your behalf.  To do this, you need to setup a personal access token, see you Account Settings and look for this section:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/774989b0-f2b5-46c1-84c6-844b65f3aaa9">

Now create a new access token:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/87d5e5bd-b751-4acc-93ff-c77bec5a317f">

You need to save this access token somewhere safe, like 1Password or LastPass... once you close this window you can't get the access token again!!

Keep in mind, this access token is sensitive... don't check in your notebook into Github or another place where others can see it.  If you accidentally do, please immediately delete this access token from your account.  _Remember, you are responsible for keeping your Synapse account credentials safe._

The next step is to do the login, copy the following text to a new cell in the notebook, make sure you replace the '...' with your access token (single quoted, just replace ... with your access token):

```
import synapseclient
from synapseclient import Activity
from synapseclient import Entity, Project, Folder, File, Link
from synapseclient import Evaluation, Submission, SubmissionStatus
from synapseclient import Wiki
from synapseclient import Schema, Column, Table, Row, RowSet, as_table_columns


syn = synapseclient.Synapse()

# You need to login first. Replace '...' with your Synapse access token.
syn.login(authToken='...')

# Replace 'syn52190581' with your actual Synapse File ID (pick one).
synapse_id = 'syn52190581'
entity = syn.get(synapse_id)

print(entity)
```

When you've copied this into the notebook and replaced ... with your access token go ahead and run the cell with `shift`+`enter`.  Also, replace the `synapse_id` with a synapse ID from one of the files in your test project.  You should see something that looks like the following.  Note it says 'Welcome, <username>!' showing you've logged in and gives the details on the file whose Synapse ID you included:

<img width="1690" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/22e72351-159f-48c1-b376-dceb2035048a">

> [!IMPORTANT]  
> __Assignment:__
> Make sure you use your token and point to a Synapse ID for a file you own.  Give it a try!

## Upload files

Now that you're connected to Synapse via the Python client, it's time to do some basic operations.  We'll start with uploading a file, in this case a fake cram file that can be used in our file browser on our project.  Put the following in a new code cell:

```
!echo 'hi there, this is a fake cram file' > rna_seq_5.cram
```

And go ahead and execute it... it will create another fake cram file.  Make sure you pick a number/name that you haven't yet used in the previous tutorial.

Now we'll look up the project Synapse ID that you created in last tutorial, in my case the Synapse ID 'syn52134164'. Yours will be different:

<img width="618" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/baef7b6c-9bea-4d4f-8b29-f99b0ec21728">

We'll use that ID to attach the new file to the project as a parent, copy the code below, paste it in a new code cell, and update the specific Synapse ID to be your project:

```
project_entity = syn.get('syn52134164')

print (project_entity)

test_file = File('rna_seq_5.cram', description='A sample fake cram file', parent=project_entity, species='human', data_type='rnaseq')
test_file = syn.store(test_file)

print (test_file)
```

Notice the annotations are just extra parameters on the `File` object.  Simple!

You should see output similar to the following:

<img width="1656" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/feea825e-f2c9-4ffe-889a-b5b91dc432ab">

Now that you've done this, wait 30 seconds or so and then head back to your `test_table_view` that you created in the previous tutorial.  Notice that `rna_seq_5.cram` (or whatever you named the new file) is now listed?  

<img width="1490" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0fa75775-90ea-4e2b-9ac1-a417dc2adca6">

This may seem like a really trivial example, but it shows you how you could upload a file and annotations with just a couple of lines of code.  Remember how time intensive it was to do this by hand for even just a few files?  This programmatic approach means you can bulk upload hundreds or thousands of files for your project without having to manually upload and annotate them through the web interface.

> [!IMPORTANT]  
> __Assignment:__
> Make sure you use file names that work for you and you select the right project Synapse ID for use in this code.  Your goal is to have at least one new file uploaded including annotations as labels.

## Download files

This is very simple, you can use the same approach as above but instead of uploading we're going to download to the current directory.  Make sure you change the Synapse ID to one of your files, enter this in a new cell and execute.  Keep in mind, if you uploaded a real CRAM file (or any binary file) you may want to skip printing it's contents, you'll just get gibberish text:

```
# download file into current working directory
entity = syn.get('syn52190584', downloadLocation='.', version='1')
print(entity.name)
print(entity.path)

# now let's print that content out
with open(entity.path, 'r') as file:
    content = file.read()
print(content)
```

And here's what that looks like:

<img width="1328" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3f4b5c17-e380-408d-976e-515d4f8ecdc0">

In my case this just prints '1' since that's the content I put in this fake cram file.  Now, if this was a real CRAM file you might use a whole host of tools to explore and analyze the result.  But this code shows you how to pull data back from Synapse for whatever use you have in mind.

> [!IMPORTANT]  
> __Assignment:__
> Make sure you use file Synapse IDs that work for you and your project.  Your goal is to download at least one file.

## Editing Tables

File upload and download, including annotation setting and provenance recording, is a key function of the Python client.  But another area that will be very commonly used is querying tables and returning results as data frames.  Files are well and good, but many projects contain structured data in tables, so being able to manipulate those tables will be key. Tables can be built up by adding rows and queried with a SQL-like language.  Let's look at an example.  First, find the 'test_table' Synapse ID that you created in the previous tutorial.  In my case it's `syn52178128`.  

Let's try to add some data to this table, the schema we're using is identical to the annotations we applied to new files uploaded in the Files section.  But this table could just as easily be any schema you like.  For example, imaging storing all your files in the Files section, annotating them with key attributes, and then using a table with a schema that stores clinical or phenotypic data.  This is a very common use case for projects using Synapse.  In a new cell copy and paste the code below and update the Synapse ID to match your table.

```
import os.path

data = [[3, "human", "rna_seq", "syn52214733"],
            [4, "mouse", "wgs", "syn52190582"]]

# get the table schema
schema = syn.get('syn52228001')
print (schema)

# now store
row_reference_set = syn.store(RowSet(schema=schema, rows=[Row(r) for r in new_rows]))

```

And the result:

<img width="1317" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/d5b154fd-c8ba-4dc9-925e-5e35ecb0598e">

You can edit or delete rows using the Python client as well as create entirely new tables or uploading files directly into tables (as we did in the web interface).  You can find more information about using Tables in the Synapse Python client [here](https://python-docs.synapse.org/build/html/Table.html#module-synapseclient.table).

> [!IMPORTANT]  
> __Assignment:__
> Use your table's Synapse ID in the above and update the file Synapse IDs referenced in the table.  You should see new rows added to your table.

## Querying Tables

In addition to adding to a table, we can perform queries that use a SQL-like query language.  We'll start by installing [Pandas](http://pandas.pydata.org/), an excellent framework for working with tabular data.  Make a new cell with this content:

```
!pip3 install pandas
```

Run it, you should see something similar to 'Successfully installed pandas-2.0.3'.

Next, we're going to do a query on the table and return the result as a Pandas dataframe.  Create a new code cell and paste the following, make sure you change to use your Synapse ID for the table you created earlier:

```
import pandas as pd

query_results = syn.tableQuery('SELECT * FROM syn52228001')
df = query_results.asDataFrame()
print(df)
```

And you can see this returns a result that is a DataFrame, which can be manipulated with all the goodness Pandas provides:

<img width="1317" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0f581f63-934f-4dd0-a678-a72b73c4507c">

You can find more information about using Tables in the Synapse Python client [here](https://python-docs.synapse.org/build/html/Table.html#module-synapseclient.table).

> [!IMPORTANT]  
> __Assignment:__
> Try this out with a query from your table.  Make sure you use the right Synapse ID for your table.

## Next Steps

We explored file upload and download as well as table queries but there are many other ways to interact with Synapse through the Python client.  These examples including writing annotations to the file we uploaded (which saves a lot manual clicking in the web interface).  But you can use the client to automate other time consuming tasks such as filling out provenance information, changing permission, etc.  You can also interact with wiki content, datasets, tables, etc.  Generally speaking, what you can do in the web interface in Synapse can be automated in code with the R or Python clients.  If you do run into a situation where the functionality you're looking for isn't in the R or Python client, you can always directly code to the [Synapse REST API](https://rest-docs.synapse.org/rest/).  The API is documented in great detail and, while it is lower-level than the R or Python clients, it gives you full control over your projects in Synapse.  This is great if you want to use a language that doesn't support the R or Python clients (for example Java).  

Another approach that many users might find useful is the [Synapse command line tool](https://python-docs.synapse.org/build/html/CommandLineClient.html).  This lets you incorporate the use of Synapse within Bash and other scripts.   Users on a Mac or Linux environment might find this extremely useful and it's installed automatically when you install the Python client.

# Next Steps

> [!NOTE]  
> You can find my test project [here](https://www.synapse.org/#!Synapse:syn52134164/wiki/623112) (Synapse ID: syn52134164) in case you want to explore what it looks like by the end of a tutorial or if you want to use my mock files.  If you would like to add my account to your project (to help with debugging for example) my username is nimbusboconnor (a test account).

> [!NOTE]  
> There is a __ton__ of documentation on Synapse.org, take a look [here](https://help.synapse.org/docs/)!  We also have a [helpdesk](https://sagebionetworks.jira.com/servicedesk/customer/portal/9) that is a good way to get help if you don't find the answer in our docs.

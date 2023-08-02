# TODO:

* make sure I annotate files uploaded and tables created
* fill in the assignment sections
* fill in documentation links for more information
* have my own notebook on my laptop just in case mybinder or collab don't work
* spell check tutorial  

# Tutorial 1: Synapse Basics

In this tutorial we're going to learn about the Synapse web user interface (https://synapse.org) and it's most key features.  By the end of this tutorial you will have a Synapse account, be able to create projects, upload/download data, and create tables/datasets to store and share your results.  You can then use this account to collaborate with others and publish your research methods and results.  

Our free account has a recommended maximum total storage footprint of 100GB or less.  If you need high-performance storage for >100GB and/or one-on-one tech support, we have a "supported" plan that you can [contact us](https://sagebionetworks.jira.com/servicedesk/customer/portal/9) to learn more about.

> [!NOTE]  
> You can find my test project [here](https://www.synapse.org/#!Synapse:syn52134164/wiki/623112) (Synapse ID: syn52134164) in case you want to explore what it looks like by the end of a tutorial or if you want to use my mock files.  If you would like to add my account to your project (to help with debugging for example) my username is nimbusboconnor (a test account).

> [!NOTE]  
> There is a __ton__ of documentation on Synapse.org, take a look [here](https://help.synapse.org/docs/)!  We also have a [helpdesk](https://sagebionetworks.jira.com/servicedesk/customer/portal/9) that is a good way to get help if you don't find the answer in our docs.

## Getting an account

First, let's create your account.  If you've already setup a Synapse account you can skip this step.

Start by navigating to the [registration page](https://www.synapse.org/#!RegisterAccount:0)

You can setup an account with either a Google-based account ("Sign up with Google") or using an email and selecting a password.

Once you register, you'll get an email to verify your account, you can then follow the link to set your account password.

You then will need to take the "Synapse Pledge", which includes agreeing to governance policies, privacy policies, terms of service, etc.  Please review these carefully, you are responsible for safe data sharing on the Synapse platform.

<img width="1355" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/68c303b3-584e-49fd-8d0d-583e2a9fee48">

## Taking the quiz so you can upload

You need to become a "certified" user in order to upload data to Synapse.  You can do this by taking the quiz [here](https://www.synapse.org/#!Quiz:Certification)

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0b19c08b-68ee-4fc5-886d-80749a0814ee">

The quiz is just 15 questions and should take << 15 min to complete.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/1809b51a-e6d9-4048-88ce-5d3ce2204d2e">

> [!IMPORTANT]  
> __Assignment:__
> We'll pause here to let you finish registering and taking the Synapse quiz.  I can also answer any questions at this time.  Make sure you:
> - register for Synapse and verify your email
> - take the quiz and pass it

## Exploring Synapse

We'll start by taking a quick tour of some of the features of Synapse.  Follow along as I walk through the interface, you should see something very similar on your account.

### Projects

Projects are really the key concept in Synapse, most roads lead back to them.  You organize work into a project; it might be for your own lab work, for collaboration with another researcher, or even dataset upload for a large consortium.  You can have many projects and, for big efforts or collaborations, you may actually have many different projects to organize distinct studies or data types.  Ultimately, it's up to you on how you organize and share your projects.

### Favorites

Clicking on the star on the left menu will take you to a place where you can organize your favorite projects.  This is very handy if you have lots of projects.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/9c8542d2-e72e-4c72-a13a-32979ec891be">

### Teams

You can see the teams you own, manage, or are a part of here:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3aeb8a54-ac6a-4dc1-940d-003572d034b2">

You can also search teams to find ones you may want to join:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/efaa5c39-3f81-461b-8270-f2abd570ffc2">

Teams are a great way to organize large sets of collaborators.  These might be the other members of your researcher group, a collaboration you have with another lab, or working groups in a large consortium with many collaborators.  

Creating teams will make it much easier to manage access permissions which you'll see later in the tutorials.  You can give permissions to a team on many different projects and then, when a new person comes into the team or another leaves, you just have to add/remove them from the team.  This avoids having to add/remove individuals from a bunch of different projects.

### Challenges

You can see Challenges you've joined here:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/df30f8d4-dce8-4eed-a740-29ed58a7afe3">

Challenges are out of scope for today's tutorial but they are a really powerful way to participate in algorithm/analysis development with the wider community.  Many of the Challenges hosted by Sage are part of the DREAM Challenges effort, which regularly hosts challenges ranging from digital mammography classification to variant calling to machine learning methods testing.  Sage has hosted over 60 Challenges to date, resulting in hundreds of publications and thousands of participants!  Check it out!

### Download Cart

This is where you can collect data files on Synapse that you'd like to download.  It helps you organize your access requests for data that is controlled access as well:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/1118fc68-dce4-4ce4-996a-640ef2620089">

We won't work with this feature in today's tutorial but it's a great way to add data references to your cart as you explore Synapse projects and download in one go.  In the future watch this space, we're working on interoperability with Velsera/Cavatica, Terra, and other compute environments to make it easier to "send" data references from Synapse into those environments for analysis.

### Search

Allows you to find projects, files, datasets, etc of interest.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/1eccfb6c-48aa-4e87-9b84-5253faf4ae41">

The search functionality of Synapse is fairly simple and unstructured but it does let you locate key public projects and search through your projects that you have access to.

Sage has built many project data portals built on top of Synapse-based data.  These typically provide much more sophisticated ways of exploring data, for example, the AD Knowledge portal allows you to search for data files, publications, people, etc.  You can see highlights of available public portals on the [Synapse homepage](https://synapse.org).

In today's tutorial we will actually create a mini-data portal that you can share with your collaborators to make exploring your projects' data easier.

## Creating your first project

When you log into Synapse you will be dropped into your projects page, you'll see it's empty to start with.

Synapse projects are the main "containers" for information in Synapse.  They are workspaces where you can store data and share with other collaborators.  They start out as private and sharable with any other Synapse user but can, ultimately, be made public when it's time to share your results with the wider community.  Or you can keep them private and just share with specific collaborators or teams.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/ed7cf758-59f1-40d2-aea8-ed3e1803491f">

Click "Create a New Project", name it something meaningful to you, and you'll be taken to the new project page.  It looks pretty empty to start but we'll fix that soon!:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/54ba2c99-4458-4b23-add0-c1073a657d7b">

## Adding wiki space content

You can add content to your project in the form of wiki pages.  These are written in a simple language called Markdown and allow you to create simple (or complex!) web pages containing graphics and tables all using a simple syntax that anyone can master.

Start by clicking on the pencil icon to edit the wiki page.  You can then put in the following content:

```
## Test Project <-- Pick a better project name!!

This project space is a test

You can use simple formatting to make text **bold**, _italics_, or ~~strikethrough~~

You can make:

* bulleted lists

You can make:

0. numeric lists

You can even make tables:

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

Finally, you can make links, for example, here's more information on the [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) language that you can use in Synapse wiki pages.

```

You can see the result of this nicely formated when you save:

<img width="1192" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/f47d186d-e7fb-4f88-9305-1a35353332da">

The Synapse project space is much more than a single page.  You can create a bunch of different pages, all related to each other in a hierarchy.  This is useful if your trying to organize your research results in distinct topics or collaborate with others on different parts of a project.  You can think of these wiki pages as Google-doc like but organizable as a hierarchy with linking between them, much easier to explore than a bunch of shared Google doc links!  In that way, it's very akin to Wikipedia.

To create another page, click the "Wiki Tools" button and then click "Add Wiki Subpage":

<img width="1192" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/fa98cbd8-8ebe-48db-90a8-b14916002ddb">

You'll now see a new page (in this case I called it "Testing Page 2"... not very creative) appear in a navigation bar on the left.  In this way you can create multiple pages nested under each other, creating a potentially complex collection of pages with their own respective content.

<img width="1259" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/9b458883-6e74-4e60-a738-b8ec0f3300ba">

> [!IMPORTANT]  
> __Assignment:__
> Give it a try! Start by creating a wiki page in your new project and then add at least one sub-page.  Try experimenting with adding some Markdown content.

## Uploading some files

At its core, Synapse is a ___data sharing platform___ and the majority data is in the form of files.  You can think of Synapse as a DropBox or Google Drive but focused on the needs of researchers.  Because of that, the platform is focused on what you need for sharing and publishing on research results, namely data provenance and DOI minting.  Also keep in mind Synapse is hosted on the AWS cloud environment, so if you want to perform large-scale analysis on the cloud it's the perfect place to host your data.  Provenance means you can upload a file and then update it with a new version, all while maintaining the history.  DOIs are unique identifiers commonly used in publications to refer to data in a durable way.  You can create DOIs in the Synapse platform for _free_ and these can be made for individual files, elements like tables and datasets (more to come on these), or even whole project spaces.

Let's get started by uploading data...

We'll start simple with the drag and drop interface.

Start by clicking the upload arrow:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/21d1712b-82cf-4718-89dd-bf38593dc877">

You'll see an interface like the above.  Pick a file on your compute and try uploading it by dragging the file to the upload area.  __Make sure you don't upload anything sensitive!  No passports or credit cards please :-)__

If you want to follow along with my examples you can open a shell environment and execute the following to make some tiny files for testing purposes... these obviously aren't real CRAM files but they'll be useful placeholders:

```
echo '<html><body><h1>Testing</h2></body></html>' > index.html
for i in 1 2 3 4 5; do
  echo $i > rna_seq_$i.cram
  echo $i > wgs_$i.cram
done;
```

Just open the folder where you created the above in your file browser, select them, and drag-and-drop them to the upload window.

In the below, I uploaded a simple index.html file:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/e5be0815-9f6a-415d-b00b-abc63ce71e56">

When it finishes uploading, click on the `index.html` file and you'll get a bunch of information:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/17b53db2-39a8-4247-826b-ce294e282da4">

Things to think about:
- there is no upper limit of data you can upload but generally we ask you to upload <100GB when using our free accounts
- if you upload lots of data to our platform and then never access it, it might be moved to slower storage
- you can add annotations on files to organize them (we'll see this in a little bit) and use nested folder structures as well
- we use AWS in us-east-1 (east coast of the US) by default
- if you want to, you can "bring your own bucket".  This lets you own the storage yourself while managing it within Synapse.  Really useful if you want to store _a lot_ more than 100GB of data on the cloud and need to control it's location (e.g. Google, AWS, in a particular geographic region, etc).  The downside is it requires knowledge of how to set this up in the cloud and your own cloud account which not everyone has.

> [!IMPORTANT]  
> __Assignment:__
> Let's pause here to make sure everyone has caught up to this point.  I'd recommend you create the mock files above and upload them.  Feel free to upload your own files instead/in addition.  _At least make a simple index.html file since we'll use it below_.

## Sharing with others

So by this point you've created your Synapse project, you've added some documentation in the form of a wiki, and you uploaded some files.  Now it's time to share the project with another Synapse user so you can collaborate!

You'll start by clicking the "Project Tools" button on the project main page:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/12ccb9d4-91da-4172-86b4-af44638c6118">

Then click on "Project Sharing Settings", you see this dialog box:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b2153464-4420-4624-bb42-0921d16fb183">

Now it's time to turn to your neighbor and ask them for their Synapse ID!  You can then add them to your project, try giving them the ability to download from your project.  In this image I've added my other Synapse account (briandoconnor, my _real_ Synapse account) to my project:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/05f15ba5-d62b-4dbc-a0ef-61f054e425d3">

You can add as many users as you want.  But as your collaborations get large, you may want to organize your sharing with Teams.  In the following I'm creating a new team:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/fe4d34fd-81d3-49b4-9764-1a2fbe7d1236">

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/cda5c418-a8d3-49df-ad87-040b98967a85">

And now I can add people to the team, in my case, my other Synapse username `briandoconnor`.

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/345061cc-17a3-4f7b-8342-a39954a34340">

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/7e072165-7c90-4dd1-a3bc-3c23df4f7510">

The invited person will get an email that will allow them to accept (or reject) your team request.

You can also change some high-level team settings here:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/24673b09-bf96-4361-b05d-c8b19d2f0060">

Going back to the project space, you can share with Teams in addition to individuals:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/6a970985-2303-4072-96a7-f4db9b266a9c">

> [!IMPORTANT]  
> __Assignment:__
> Let's pause here to give you time to:
> - get your neighbor's Synapse ID
> - add them directly to your project
> - then ask another neighbor for their ID and make a team
> - invite both neighbors to your team and add that team to the project (you can remove the individual user you added previously, the team replaces it!)

## Uploading new versions of files

Now that you've shared your project, the next step is to upload another version of the file we uploaded earlier.  This is similar to you, or a collaborator, updating a shared result file with a new version after running an updated algorithm.

Start by navigating back to the `index.html` file you uploaded earlier, click on it and you should see something like the following:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/91aff570-a84b-4d13-a2e9-2b24c133a92f">

We need to update the `index.html` file's contents, you can just open the local copy of the file in a text editor or you can use the following command to update it:

```
echo '<html><body><h1>Testing V2</h2></body></html>' > index.html
```

Click on the up arrow, this will let you drag and drop the new version of the file to upload:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/84a4be97-dba2-4573-b870-0ad05f66f100">

_You need to upload a new version of the file, if the file is the same, a new version on Synapse won't get created.  So make sure you edit your local index.html before uploading._

I updated the `index.html` file to include a change, uploaded it again, and you can see in the result below the version is now V2:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/a5b7d56a-6e14-449a-9d6a-a8e106d32c15">

As a researcher, this easy ability to manage versions of your data is incredibly important.  Whether you're working as a team of researchers on a particular analysis or working independently, you will always have multiple iterations of result files that you will want to track and share.  

In this figure below I clicked on the version link under the name of the file, which opens a "Version History" that you can explore.  You can see there are two versions of this file, the only difference being the header was updated to "Test Summary v2" in my file.  I can download either version of the file, or create DOIs for my publication.  This is great since you can publish on a previous version of the file via a DOI and continue to upload newer versions as you perform subsequent rounds of analysis.

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/948316cb-6bd2-4f7d-b97f-05f148ef9ae2">

> [!IMPORTANT]  
> __Assignment:__
> Let's pause here to give you time to upload your new file version and see your index.html file now has multiple versions.

## Provenance

Provenance in Synapse refers to the tracking of file histories, how they related to each other, how the transformations between versions happened.

By default, when you upload a file (or new version of a file), you will see a very simple provenance graph.  But you can use this feature to describe how you arrived at a version of a file.  This process of documenting history is critical for science, it allows you to track the tools you used to create a result, the parameters you used, and the inputs among others.

On version 2 of the index.html file, click on the "File Tools" button and choose "Edit File Provenance".

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/ff1240cd-6ea2-4cad-9c92-47c1e66a6222">

You can then select the version 1 of the file in the "Used" section.  Click on "Add Synapse Reference":

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/ec46d4df-f006-4ebb-afea-094ebe0f6dae">

Select the index.html and "Version 1" in the pulldown.  This is the source file we used to create V2 of the file.

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/bb9ee3e7-7718-48b5-9bd2-5f50404beecc">

Under Executed, click on "Add External URL Reference", we're just going to put a URL to the editor I used:

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/de590450-bf2b-4576-9e6b-a6801655602f">

Now you can click on "Save":

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/cb720508-2a78-4cb3-a22d-2520b9691cef">

You can now see the version 2 of the index.html file has a clear relationship to version 1 and the process used (the text editor) to actual do the transformation.

<img width="284" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/78514e9d-3474-4d65-9408-1a0670464b42">

> [!IMPORTANT]  
> __Assignment:__
> OK, it's time for you to try this out.  Go ahead and follow the steps above to update the provenance of index.html V2 to show it's the result of V1 transformed by whatever editor you used.

## Using Tables

File support in Synapse is great to upload and organize results.  But often times, you may have tabular data that you want to share and make queryable (think clinical, biospecimen, phenotypic, or other data types).  In many ways, this functions as a database, allowing you to do powerful queries on your data directly (vs. just storing files that you need to download to actually search).

Table structure can be created from an Excel or Google Sheets document by first saving as a `.tsv` or `.csv` file.  You can then upload these to Synapse which will turn it into tables behind the scenes.  Below is a simple sample file, you can access it on Google [here](https://docs.google.com/spreadsheets/d/17Qef59nQL5r5FfR94QwNjCwtamAMbElG03BtyKu2jgY/edit#gid=0).  Open it and download it as a `.tsv` file:

<img width="550" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b565284d-0216-44da-86a3-2770577b29a4">

Now, in the table page, click the upload button to upload the `.tsv` version of this file.  Synpase will recognize it as a table and give you some options, we're going to stick with the defaults:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/7c3037fd-5b1d-47fa-90de-4c86ba9c3332">

You can then name it, I'll call it `test_table`:

<img width="1492" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3aa51557-7fea-4a2e-a173-3b643aa84564">

Synapse will guess the types of each column, but you can customize that by clicking on "Schema Options". Let's do that and change the file column to something easier to deal with (a String).  I'm also going to make the columns "bigger" since we want space to store species and data_types that are up to 256 characters long.  If you're following along with me, make your schema look like the following:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/c31dffed-5c24-49b1-9542-e9b143d2d943">

In this case, I changed the "file" column to be type "String" to make it easier to work with.

Now that the table was created, you can edit. Click on the table and, in the detail view, click on the pencil icon to edit the table:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/e9063d5e-6221-4e43-97e2-fee0f910076a">

Like files, tables can have wiki spaces, can be versioned, and can have DOIs created.

Tables can be complicated, have many columns, rows and be related to other tables.  When you publish on your data, you may wish to create a snapshot.  This allows you to crate a snapshot of tables at a specific moment in time, for referencing in publications and sharing.  Alternatively, you can use a Dataset to accomplish the same thing but with more flexibility with what you include in the snapshot.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b19efc35-9408-4e28-83e9-cee51cef6189">

> [!NOTE]  
> To learn more about Tables see the very detailed [Synapse documentation]( https://help.synapse.org/docs/Organizing-Data-With-Tables.2011038095.html)

> [!IMPORTANT]  
> __Assignment:__
> We've covered a lot of ground in this section and tables are very powerful with a lot of features we just scratched the surface on.  Take a few minutes to walk through the above and setup your table:
> - create the table from the .tsv file
> - customize it's schema with the sizes and file as a string example I gave
> - then go into the interface and edit it, try updating my Synapse file IDs to some of your file IDs for example

## Generating a File Browser

At this point, you've created a wiki space for the documentation on your project, you've uploaded a file(s) to the Files section, and you've created a table which works like a database and also includes references to some of your files.  In many ways, you have a collaborative Dropbox + Google Docs + Zenodo + MySQL database combination that's super flexible for your collaborations and let's you version data on the cloud and mint DOIs for just about everything in order to support publishing your awesome results!  And it's all free to use and ready to go!

But Synapse as another feature that I _really_ like that takes your collaborative environment to the next level.  Imagine, if you will, that your collaborative project generates 1,000+ files.  That can be really difficult to navigate, either on the Files tab or the Tables tab if you end up using that feature to organize files.

What we'd really like is a simple way to browse and facet search (think Amazon shopping interface) on files, whether this is used for publishing lots of data across teams for a collaboration or even just within your lab.

To get started doing this we're going to pick up where we left off with Tables and create something called a "File View".  Click on "Add New..." then click on "Add File View" and you will see the following, I named this "test_table_view" and selected both Files and Tables:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/29a8ae8e-978e-45df-9c2c-309dabb0ea1a">

Next you will need to set your Scope.  You can actually add files from multiple projects, really helpful if you're working in a large consortium that has many different projects that are each representing a working group or particular dataset and you want to create a file view across them all.  We're going to select the context of this current project, click the "Add container" button, navigate up to all your projects, and select the current project:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/f38e8170-4376-4ca1-8fbd-5d07a72829f3">

And you can see what that looks like when you finish your scope selection:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/7252c0b7-a113-49b8-81f1-a63f9b181612">

Click Next and now you can select the fields you want to be able to search on:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/793db782-53db-4d97-afe3-3c33fcbc8220">

Wow, there are a lot of fields!  These are all intrinsic metadata fields for the Synapse system... I selected a bunch above then used the trash icon to remove them since I didn't want them in my faceted browser.  You get down to something much more reasonable:

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/8673b7a4-b957-447a-aa2f-8e7581abb99f">

But I'm not done yet! Notice you son't see the columns in your table e.g. `data_type`, `species`, etc... strange!  Let's click on "Import Columns" and select the "test_table":

<img width="1225" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/af05d755-3018-4f55-a304-7dfcd006d5a5">

And now you see the columns we defined ourselves: species, data_type, my_id, and file.  I'll select those along with a few other fields that might be useful to search on.   Make sure you select "Facet" as "Values" for the `species` and `data_type` fields:

<img width="1245" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/d162f913-6785-4120-97b6-efdb6fa2bcac">

And here we go after making the changes:

<img width="1245" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/6264b8b3-2a50-4640-a47d-76d3e828908a">

Now click "Finish" and you'll see the following:

<img width="1245" alt="image" src="https://user-images.githubusercontent.com/1730584/257069000-e2e25431-4b89-4e7a-8e69-00a7727744b5.png">

You'll notice a few things:

1. the _content_ of the table "test_table" isn't being picked up, this view is created for the table as an entity as a whole
1. the table is missing "species" and "data_type"

The first items is by deisgn but let's fix the second.

Open the files browser.  We previously uploaded index.html, now we're going to upload some more fake RNASeq and WGS files (if you didn't already previously).

Drag and drop the files `wgs_1.cram` ... `wgs_3.cram` and `rna_seq_1.cram` ... `rna_seq_3.cram`.  Upload all those files you created earlier (if you haven't already).

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0c7feee9-7e01-4d9a-b747-dca33aa0ca61">

Now, for each file, click on it and then click on the label icon. Now you can edit the annotations assocaited with each file, add a `species` key with a value like mouse and a `data_type` key with a value of `html` for the index.html, `rnaseq` for RNASeq files, and `wgs` for WGS files.

You'll have to do this for each file you upload, in a future tutorial we'll use a Python script to do this.  If you have thousands of files you can see how this would be a big help!

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/c6fa6486-03d7-451b-bbaf-c6be415468a9">

For one of the WGS files:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3e5f9ce6-7ca4-46d7-83e4-16a74fdc9d2d">

Now if we take a look back at the file view we see the following:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/78651d0a-4838-4e1c-9b3e-5872176bbfe2">

So now we have the `species` and `data_type` facets that we can filter files on!  This is cool, you can quicky filter this file view for data that you're interested in based on file annotations.  Over time, you can add more files to your project and they will show up here.  This is designed to be a live view that can be dynamically added to over time.  It's a great way to be able to filter your active files quickly and easily.

For example, I uploaded another RNASeq file (`rna_seq_4.cram`), annotated it with the same attributes, and then it automatically shows up in the file view!

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/f3987b21-6a36-45f8-a246-5d20e354a6db">

This all might seem like a trvial thing, but when you're working on a large collaboration with thousands of files this is a great way to organize and slide-and-dice data between you and your collaborators.  Beyond just the simple folders and sub-folders approach often used in shared workspaces (and that doesn't really scale well when you have __lots__ of files).

> [!IMPORTANT]  
> __Assignment:__
> We've covered a lot of ground through the creation of a File View, annotating a bunch of files with Labels, and then using that to populate facets in the File View that you can search on.  Let's take a moment to get everyone caught up.  Make sure you have:
> - uploaded all those files we generated
> - annotate these files with labels, at least do a few files and include a `species` and `data_type` (make up the values)
> - setup your File View with the correct fields including `species` and `data_type`
> - show that you can facet search using these annotations in the File View
> - In the next tutorial we'll use a script to do all this heavy lifting which will make it possible to have very large File Views

## Publishing

Now that we've explored how you can use Synapse to work on your research and collaborate in small (or large) groups we will turn to how you can use the platform to publish data publicly.  

We'll walk through each of the following activities:
- Create a Dataset
- Mint a DOI for a file and the Dataset
- Make your data public

### Creating a Dataset

As you saw in the file view, when you add new data the file view is updated.  This is great when you are collaborting on analysis and new data is uploaded and shared.  But when you're getting ready to publish, you'll likely want some stable dataset that you can reference in your paper.  Datasets are the answer, they let you make a durable file view that can be published for others to use.

Navigate to the Datasets section of your project and click `Add New...` and `Dataset`:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/27f19545-3ccc-451f-bc2e-582cc9f7f175">

You'll then be greated with a draft dataset where you can publish your files.  In this case, I'm going to assume `rna_seq_3.cram` and `wgs_3.cram` are the final files we're going to publish on.  So lets add those:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/5af4f955-164d-4b72-b62d-fc0163bdc7af">

And add those files, and then click `Save`:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/8980861b-4418-497d-86d8-33f48c535c30">

We're not quite done yet, this is still a draft version of the dataset:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/fdbf0e24-e536-45d0-a84d-87e58497fc33">

Next we're going to click on the icon with the arrow and circles.  This is the "Create Stable Version" button:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/61d693a9-6b94-434e-b137-cb096ed7d4f4">

### Minting a DOI

DOIs are extremely useful when it comes time to publish.  For example, we can give the stable release of our dataset, which is now immutable, a DOI and then use that in our publication text.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/25f465af-38c3-4c45-89c4-bf4a935ef8c3">

We can now see the DOI was created:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/58b6f202-5042-453a-afb9-23b7d5909944">

You can drop in the URL: https://doi.org/10.7303/syn52190980.1 into your publication, most publishers recognize DOIs as a means of referencing data in a stable and durable way that is perfect for publications.

> [!IMPORTANT]  
> __Assignment:__
> Synapse supports DOI minting for Datasets, tables, files and handles versioning as well.  Give the following a try:
> - make a new Dataset using a few files, create a stable version from the draft, and assign it a DOI
> - pick a file and make a DOI for V1
> - look through the other entity times we crated today and see what you can mint DOIs for... they're everywhere which is great for citability!

### Sharing Data Publicly

One last task, it's great that we were able to create a Dataset and mint a DOI that could be used for publications.  But what about researchers actually accessing the files, for example `wgs_3.cram`?

We can easily share this Synapse project with particular Syanpse users directly or with any Synapse user.  Go back to the project main page and choose 'Project Sharing Settings' under 'Project Tools'.  From there you can add individual users or teams:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/e3b21c7a-66a3-45f8-9569-600116b91f7d">

If you want to make your project accessible anyone click the 'Make Public' button:

You'll notice a few things, 'All registered Synapse users' is now 'Can download' and 'Anyone on the web' is now 'Can view'.

You can't actually give download permissions to anyone on the web (e.g. no Synapse login required) since we don't want Synapse to be a general data hosting platform like Dropbox or Google Drive (since this is ripe for abuse).  However, we have a process to make your key, published datasets accessible to the public.  You can email `act@sagebase.org` and request that your project be made fully public, which is great for publications and efforts where you want to share data as widely as possible.

We can also make datasets available for anonymous reviewer access, making it possible to safely share data during the publication review process.  Reach out to us if you're interested!

> [!IMPORTANT]  
> __Assignment:__
> Give it a try, make your project public!

## Next Steps

We just really scratched the surface on the features of Synapse but we did go over some of the key ones for using the platform to collaborate.  In the [next Tutorial](tutorial-2.md) we'll explore how to do many of the same things but programmatically using Python.

> [!NOTE]  
> There is a __ton__ of documentation on Synapse.org, take a look [here](https://help.synapse.org/docs/)!  We also have a [helpdesk](https://sagebionetworks.jira.com/servicedesk/customer/portal/9) that is a good way to get help if you don't find the answer in our docs.

# TODO:

* remove "ID" from my upload table
* make sure I annotate files uploaded and tables created
* I think I want to upload some fake crams in the file upload step
* fill in the assignment sections
* fill in documentation links for more information 

# Tutorial 1: Synapse Basics

https://www.synapse.org/#!Synapse:syn52134164/wiki/623112 as nimbusboconnor

In this tutorial we're going to learn about Synapse and it's most basic features.

## Getting an account

First, let's create your account.  If you've already setup a Synapse account you can skip this step.

Start by navigating to the [registration page](https://www.synapse.org/#!RegisterAccount:0)

You can setup an account with either a Google-based account ("Sign up with Google") or using an email and selecting a password.

You'll get an email, you can then follow the link to set your account password.

You then will need to take the "Synapse Pledge", which includes agreeing to governance policies, privacy policies, terms of service, etc.

<img width="1355" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/68c303b3-584e-49fd-8d0d-583e2a9fee48">


## Taking the quiz so you can upload

You need to become a "certified" user.  You can do this by taking the quiz [here](https://www.synapse.org/#!Quiz:Certification)

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0b19c08b-68ee-4fc5-886d-80749a0814ee">

The quiz is just 15 questions and should take < 15 min.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/1809b51a-e6d9-4048-88ce-5d3ce2204d2e">

## Exploring Synapse

### Favorites

Clicking on the star on the left menu will take you to a place where you can organize your favorite projects

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/9c8542d2-e72e-4c72-a13a-32979ec891be">

### Teams

You can see the teams you own, manage, or are a part of here.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3aeb8a54-ac6a-4dc1-940d-003572d034b2">

You can also search teams to find ones you may want to join.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/efaa5c39-3f81-461b-8270-f2abd570ffc2">

### Challenges

You can see Challengs you've joined here:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/df30f8d4-dce8-4eed-a740-29ed58a7afe3">

### Download Cart

This is where you can collect data files on Synapse that you'd like to download.  It helps you organize your access requests for data that is controlled access as well.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/1118fc68-dce4-4ce4-996a-640ef2620089">

### Search

Allows you to find projects, files, datasets, etc of interest.

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/1eccfb6c-48aa-4e87-9b84-5253faf4ae41">

## Creating your first project

You will be dropped into your projects page, you'll see it's empty to start with.

Synapse projects are the main "containers" for information in Synapse.  They are workspaces where you can store data and share with other collaborators.  They start out as private and sharable with any other Synapse user but can, ultiamtely, be made public when it's time to share your results with the wider community.  

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/ed7cf758-59f1-40d2-aea8-ed3e1803491f">

Click create project, name it, and you'll be taken to the new project page:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/54ba2c99-4458-4b23-add0-c1073a657d7b">

## Adding wiki space content

You can add content to your project in the form of wiki pages.  These are written in a simple language called Markdown and allow you to create complex web pages containing graphics and tables using a simple syntax.

Start by clicking on the pencil icon to edit the wiki page.  You can then put in the following content:

```
## Test Project

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

Finally, you can make links, for example, here's more information on the [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) language.

```

You can see the result of this nicely formated when you save:

<img width="1192" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/f47d186d-e7fb-4f88-9305-1a35353332da">

The Synapse project space is much more than a single page.  You can create a bunch of different pages, useful if your trying to organize your research results in distinct topics or collaborate with others on different parts of a project.  

To create another page, click the "Wiki Tools" button and then click "Add Wiki Subpage":

<img width="1192" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/fa98cbd8-8ebe-48db-90a8-b14916002ddb">

You'll now see a new page (in this case "Testing Page 2") appear in a navigation bar on the left.  In this way you can create multiple pages nested under each other, creating a potentially complex collection of pages with their own respective content.

<img width="1259" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/9b458883-6e74-4e60-a738-b8ec0f3300ba">


> [!NOTE]  
> Give it a try, start by creating a few pages and then adding some Markdown content 

## Uploading some files

At its core, Synapse is a data sharing platform and the majority data is in the form of files.  You can think of Synapse as a DropBox or Google Drive but focused on the needs of researchers.  Because of that, the platform is focused on what you need for publishing on research results, namely provenance and DOI minting.  Provenance means you can upload a file and then update it with a new version, all while maintaing the history.  DOIs are unique identifiers commonly used in publications to refer to data in a durable way.  You can create DOIs in the Synapse platform for free and these can be made for individual files or whole project spaces.

Let's get started by uploading data...

We'll start simple with the drag and drop interface.

Start by clicking the upload arrow:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/21d1712b-82cf-4718-89dd-bf38593dc877">

You'll see an interface like the above.  Pick a file on your compute and try uploading it by dragging the file to the upload area.

In this case I uploaded a simple index.html file

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/e5be0815-9f6a-415d-b00b-abc63ce71e56">

When it finishes uploading, click on the file and you'll get a bunch of information

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/17b53db2-39a8-4247-826b-ce294e282da4">

Things to think about:
- there is no upper limit of data you can upload but generally we ask you to upload <100GB when using our free accounts
- if you upload lots of data to our platform and then never access it, it might be moved to slower storage
- you can add annotations on files
- we use AWS in us-east-1 (east coast of the US) by default
- if you want to, you can "bring your own bucket".  This lets you own the storage yourself while managing it within Synapse.  Really useful if you want to store a lot more than 100GB of data on the cloud and need to control it's location (e.g. Google, AWS, in a partiuclar region).  Downside is it requires knowledge of how to set this up in the cloud and your own cloud account which not everyone has.

## Sharing with others 

So by this point you've created your Synapse project, you've added some documentation in the form of a wiki, and you uploaded a file.  Now it's time to share the project with another Synapse user so you can collaborate.

You'll start by clicking the "Project Tools" button on the project main page:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/12ccb9d4-91da-4172-86b4-af44638c6118">

Then click on "Project Sharing Settings", you see this dialog box:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b2153464-4420-4624-bb42-0921d16fb183">

Now it's time to turn to your neighbor and ask them for their Synapse ID!  You can then add them to your project, try giving them the ability to download and upload to your project.  In this image I've added my other Synapse account (briandoconnor) to my project:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/05f15ba5-d62b-4dbc-a0ef-61f054e425d3">

You can add as many users as you want.  But as your collaborations get large, you may want to organize your sharing with Teams.  In the following I'm creating a new team:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/fe4d34fd-81d3-49b4-9764-1a2fbe7d1236">

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/cda5c418-a8d3-49df-ad87-040b98967a85">

And now I can add people to the team, such as my other Synapse username briandoconnor.

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/345061cc-17a3-4f7b-8342-a39954a34340">

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/7e072165-7c90-4dd1-a3bc-3c23df4f7510">

The invited person will get an email that will allow them to accept (or reject) your team request.

You can also change some high-level team settings here:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/24673b09-bf96-4361-b05d-c8b19d2f0060">

Going back to the project space, you can share with Teams in addition to individuals:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/6a970985-2303-4072-96a7-f4db9b266a9c">

## Uploading new versions of files

Now that you've shared your project, the next step is to upload another version of the file we uploaded earlier.  This is similar to you, or a collabortor, updating a shared result file with a new version.

Start by navigating back to the file you uploaded earlier, click on it and you should see the following:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/91aff570-a84b-4d13-a2e9-2b24c133a92f">

Click on the up arrow, this will let you drag and drop a new version of the file to upload:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/84a4be97-dba2-4573-b870-0ad05f66f100">

You need to upload a new version of the file, if the file is the same, a new version won't get creted.

I updated the index.html file to include a change, uploaded it, and you can see in the result below the version is now V2:

<img width="1311" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/a5b7d56a-6e14-449a-9d6a-a8e106d32c15">

As a researcher, this easy ability to manage versions of your data is incredibly important.  Whether you're working as a team or researchers on a particular analysis or working indepdently, you will always have multiple iterations of files and results that you will want to track and share.  

In this figure below I clicked on the version link under the name of the file, which opens a "Version History" that you can explore.  You can see there are two versions of this file, the only difference being the header was updated to "Test Summary v2".  I can download either version of the file, or create DOIs for my publication.  This is great since you can publish on a version of the file and continue to upload newer versions.

<img width="1484" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/948316cb-6bd2-4f7d-b97f-05f148ef9ae2">

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

## Using Tables

File support in Synapse is great to upload and orgnize results.  But often times, you may have tabular data that you want to share and make queriable.  In many ways, this functions as a database, allowing you to do powerful queries on your data directly (vs. just storing files that you need to download to actually search).

Table structure can be created from an Excel or Google Sheets document by first saving as a .tsv or .csv file.  You can then upload these to Synapse which will turn it into tables behind the scenes. 

<img width="519" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/df555d6e-de18-4d2b-ac6d-1c9e93f77c47">

Click the upload button to upload the .tsv version of this file:

<img width="1492" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/41886065-17af-49b2-8648-086816b8745e">

You can name it, I'll call it `test_table`:

<img width="1492" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3aa51557-7fea-4a2e-a173-3b643aa84564">

Synapse will guess the types of each column, but you can customize that by clicking on "Schema Options":

<img width="1492" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/d0ac2595-8e7f-4699-ac9c-17e8ab6bf695">

In this case, I changed the "file" column to be "File" type.

Now that the table was created, you can edit. Click on the table and, in the detail view, click on the pencil icon to edit the table:

<img width="1440" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/cd17e27f-4de0-4eab-a16c-1db4f48f603f">

I'll upload a mock RNAseq and WGS file for the files column in these rows.  Click on the upload icon to the right of the file field:

<img width="1440" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/5827645a-ced5-41a1-afd6-75bef077e4f4">

You can now see the full table populated including the file column containing `.cram` files.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/2a57779c-a9f7-47c6-b026-566559509d83">

Like files, tables can have wiki spaces, can be versioned, and can have DOIs created.

Tables can be complicated, have many columns, rows and be related to other tables.  When you publish on your data, you may wish to create a snapshot.  This allows you to crate a snapshot of tables at a specific moment in time, for referencing in publications and sharing.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b19efc35-9408-4e28-83e9-cee51cef6189">

> [!NOTE]  
> To learn more about Tables... https://help.synapse.org/docs/Organizing-Data-With-Tables.2011038095.html 

## Generating a File Browser 

At this point, you've created a wiki space for the documentation on your project, you've uploaded a file to the Files section, and you've created a table which works like a database and also includes additional files.  In many ways, you have a collaborative Dropbox + Google Docs + MySQL database combination that's super flexible for your collaborations and let's you version and mint DOIs for just about everything in order to support publishing your awesome results!  And it's all free to use and ready to go!

But Synapse as another feature that I really like that takes your collabortive environment to the next level.  Imagine, if you will, that your collaborative project generates 1,000 files.  That can be really difficult to navigate, either on the Files tab or the Tables tab if you end up using that feature to organize files.

What we'd really like is a simple way to browse and facet (think Amazon shopping interface) on files, whether this is used for publishing lots of data, across teams for a collaboration, or even just within your lab.

To get started doing this we're going to pick up where we left off with Tables.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/6f3918ec-154c-47ab-806a-fb833d2fc0c1">

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/67891602-17aa-440f-abac-e3f89604ce4b">


You can actually add files from multiple projects, really helpful if you're working in a large consortium that has many different projects and you want to create a file view across them.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/fbc98c26-6a61-4b06-9470-03500974150f">

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/ff0fd21f-d966-4fd9-90d9-3e50cbe0a8e3">

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b3485927-559d-4694-bbac-e9ebbab619ea">

Now you can select the fields you want to be able to search on:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/d56b97ee-fdde-42cf-8f43-6aa0e2f1f4d3">

Notice you son't see the columns in your table... strange!  Let's click on "Import Columns" and select the "test_table":

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/44b218d3-2492-4fe3-b570-3921bc7be8fa">

And now you see the columns we defined ourselves: species, data_type, and file.  I'll select those along with a fiew other fields that might be useful to search on.  I'll also remove the fields I don't need.  Make sure you select "Facet" as "Values" for the `species` and `data_type` fields:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/b4c4b54a-5189-469a-9c8e-0da183a5ba0d">

And here we go:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/e2e25431-4b89-4e7a-8e69-00a7727744b5">

You'll notice a few things:

1. the _content_ of the table "test_table" isn't being picked up, this view is created for the table as an entity as a whole
1. the table is missing "species" and "data_type"

The first items is by deisgn but let's fix the second.

Open the files browser.  We previously uploaded index.html, now we're going to upload some more fake RNASeq and WGS files.

Drag and drop the files `wgs_1.cram` ... `wgs_3.cram` and `rna_seq_1.cram` ... `rna_seq_3.cram`.

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0c7feee9-7e01-4d9a-b747-dca33aa0ca61">

Click on the label icon, now you can edit the annotations assocaited with each file, add a `species` key with a value like mouse and a `data_type` key with a value of `html` for the index.html, `rnaseq` for RNASeq files, and `wgs` for WGS files.

You'll have to do this for each file you upload, in a future tutorial we'll use a Python script to do this.  If you have thousands of files you can see how this would be a big help!

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/c6fa6486-03d7-451b-bbaf-c6be415468a9">

For one of the WGS files:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3e5f9ce6-7ca4-46d7-83e4-16a74fdc9d2d">

Now if we take a look back at the file view we see the following:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/78651d0a-4838-4e1c-9b3e-5872176bbfe2">

So now we have the `species` and `data_type` facets that we can filter files on!  This is cool, you can quicky filter this file view for data that you're interested in based on file annotations.  Over time, you can add more files to your project and they will show up here.  This is designed to be a live view that can be dynamically added to over time.  It's a great way to be able to filter your active files quickly and easily.

For example, I uploaded another RNASeq file (`rna_seq_4.cram`), annotated it with the same attributes, and then it automatically shows up in the file view!

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/f3987b21-6a36-45f8-a246-5d20e354a6db">

This all might seem like a trvial thing, but when you're working on a large collaboration with thousands of files this is a great way to organize and slide-and-dice data between you and your collaborators.  Beyond just the simple folders and sub-folders approach often used in shared workspaces.

## Publishing

Now that we've explored how you can use Synapse to work on your research and collaborate in small (or large) groups we will turn to how you can use the platform to publish.  

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

### Sharing Data Publicaly 

One last task, it's great that we were able to create a Dataset and mint a DOI that could be used for publications.  But what about researchers actually accessing the files, for example `wgs_3.cram`? 

We can easily share this Synapse project with particular Syanpse users directly or with any Synapse user.  Go back to the project main page and choose 'Project Sharing Settings' under 'Project Tools'.  From there you can add individual users or teams:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/e3b21c7a-66a3-45f8-9569-600116b91f7d">

If you want to make your project accessible anyone click the 'Make Public' button:

You'll notice a few things, 'All registered Synapse users' is now 'Can download' and 'Anyone on the web' is now 'Can view'.

You can't actually give download permissions to anyone on the web (e.g. no Synapse login required) since we don't want Synapse to be a general data hosting platform like Dropbox or Google Drive (since this is ripe for abuse).  However, we have a process to make your key, published datasets accessible to the public.  You can email `act@sagebase.org` and request that your project be made fully public, which is great for publications and efforts where you want to share data as widely as possible.

We can also make datasets available for anonymous reviewer access, making it possible to safely share data during the publication review process.  Reach out to us if you're interested!

## Assignment

- Give them a problem scenario to solve 

# Tutorial 2: Programmatic Access 

Everything we've done to this point has been through the Synapse web interface.  This is great since it's really easy to get started but when you try to use Synapse for large projects with thousands of files, things get overwhelming very quickly.

In this tutorial we'll look at using Synapse through programmatic interfaces, namely with the Synapse Python client. In this way, you can script things like file upload and annotation so you and your collaborators can use interfaces like the File View to explore your data without a ton or work to set it up.  Likewise, the Python client allows you to download files for use in your analysis pipelines and to upload the results and provenance back.  For the most part, whaterver you can do in the web interface you can do through the API the client accesses.  The prefered client is Python-based but we have a version that can run in R as well.

## Setting up Mybinder.org

For this tutorial we'll work in a Juypter notebook using Python. If your forte is R don't worry, the code examples are very simple and the more extensive online documenation for Synapse does a great job of showing you how to code in either Python or R.  

You may have experience using Jupyter notebooks either on your own computer, a VM in the cloud, or on a hosted platform like Velsera, Cavatica, or Tera.  In this tutorial we'll go super simple, we'll use https://mybinder.org/, a service that provides free Jupyter notebook (Jupyter Labs) instances for lightweight compute and exploration.  Parentetically, this is a great way to make the Notebooks you store in GitHub immediately usable by others.  We won't go into great details on the features of MyBinder but this is really worth some exploration if you're intersted.  You can include a customized `environment.yml` file in your GitHub repository to specify library dependencies and other configuation.  See the [documentation](https://mybinder.readthedocs.io/en/latest/introduction.html) for more details.  Lucky for us, a stock MyBinder instance works just fine for this tutorial!

Start by going to https://mybinder.org/ and entering `https://github.com/briandoconnor/synapse-tutorial-2023` into the 'GitHub repository name or URL field':

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/3782dbb7-b3f1-40fa-8846-57b3dadd287b">

You'll then click 'launch' and wait a couple of minutes to start.  You can follow the progress and eventually get something that looks like the following:

<img width="1049" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/442eecc0-9853-466a-8c03-1df7b604db6b">

This is extremely nifty, there are few places online where you can use a fully functioning notebook environment for free.  If you're interested, another good free Notebook environment is [Google Collab](https://colab.google/), which I confirmed worked with the tutorial below.  Here's a screenshot from that alternative service:

<img width="1690" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/38ee1fdb-dbc4-4b0b-98e4-1c628b981fc8">

## Installing the Synapse Python Client 

Now that your Binder notebook server is running, click on 'Python 3 (ipykernel)' under the Notebook section.  

## Logging in to Synapse

You need to setup a personal access token, see you Account Settings and look for this section:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/774989b0-f2b5-46c1-84c6-844b65f3aaa9">

Now create a new access token:

<img width="1496" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/87d5e5bd-b751-4acc-93ff-c77bec5a317f">

You need to save this access token somewhere safe, like 1Password or LastPass... once you close this window you can't get the access token again!!

```
import synapseclient
syn = synapseclient.Synapse()

# You need to login first. Replace '...' with your Synapse access token.
syn.login(authToken='...'

# Replace "syn123" with your actual Synapse ID.
synapse_id = 'syn52190581'
entity = syn.get(synapse_id)

print(entity)
```


## Upload files

## Download files

## Query table 

## Graph something 

## Assignment 

## Tutorial 3: Data Submission for INCLUDE

# Cleanup

Delete your project

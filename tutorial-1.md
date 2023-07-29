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

## Generating a File Browser 

## Publishing

- Mint a DOI
- make the data public 
- DOI
- public data

## Assignment

- Give them a problem scenario to solve 

# Tutorial 2: Programmatic Access 

Programmatic access

## Setting up Mybinder.org

## Installing the Synapse Python Client 

## Logging in to Synapse

## Upload files

## Download files

## Query table 

## Graph something 

## Assignment 

## Tutorial 3: Data Submission for INCLUDE

# Cleanup

Delete your project

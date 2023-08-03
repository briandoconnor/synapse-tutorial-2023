# Demo: INCLUDE DCC Submission

This demo walks you through the process that data submitters to the [INCLUDE DCC](http://includedcc.org) follow in order to share data through the portal.  The goal is to give you an overview of the process, we'll work with you directly when it comes time to submit your data to INCLUDE.  [Contact us](https://app.smartsheet.com/b/form/514745159a004c2e987fff0aa16ceaac) to learn more!

## Submitter Instructions

The first place to stop is the [INCLUDE Data Contributor Guide](https://docs.google.com/spreadsheets/d/1omhtVW51noNfNfX_wiu-9HEyQ7t9Df297oub8YoDq7k/edit#gid=2131231137), a Google doc prepared by the project to walk you through the process as a data submitter.

<img width="1074" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/7c15dba5-109c-494f-b3b2-aae8178abc7c">

The submission process starts with a submitter interview by the DCC team to explain the guide and setup a Synapse Project for your files.

## Submitter Synapse Project

Here's an [example Synapse Project](https://www.synapse.org/#!Synapse:syn52171867/files/) that would be setup for a data submitter in INCLUDE.

<img width="1432" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/0b73c14a-cc5d-4153-b433-2188b49ba0d1">

## Upload Data 

The process of submitting starts with uploading data files to your Synapse Project.  This includes files like RNASeq, WGS, etc, whatever data files you will ultimately be submitting to the project.  In some cases, submitters might only have clinical, phenotypic, or biospecimen annotations to upload and may not have data files per se.  That's OK!

Also, if you are submitting a bunch of files, very large files, or need to transfer from a cloud VM, we recommend you use the Synapse command line or Python/R client library.  See [tutorial-2.md](tutorial-2.md) for much more info on this.

Here's an example uploading a bunch of cram files to a direcotry in the [example Synapse Project](https://www.synapse.org/#!Synapse:syn52171867/files/):

<img width="1256" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/4c2350a2-3ec4-4180-9c7a-3e8c7de9e66b">
<img width="1256" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/ead72cf4-0c15-417e-9002-2f7389891b33">

_In the rest of the demo below I'm going to upload biospecimen annotations, so I won't use these files.  But I wanted to show you how this is done._

## Submit and Validate Data via DCA

The [Data Curator App (DCA)](https://dca.app.sagebionetworks.org/) is a tool developed at Sage to ensure that data submitted for a project like INCLUDE complies with the data model developed for the project.  More simply, it's making sure people don't forget to fill in required columns for the information they're submitted to INCLUDE.

For this demo, we're going to submit some [Biospecimen](https://docs.google.com/spreadsheets/d/1omhtVW51noNfNfX_wiu-9HEyQ7t9Df297oub8YoDq7k/edit#gid=1910032073) data to INCLUDE via the [example Synapse Project](https://www.synapse.org/#!Synapse:syn52171867/files/) and validated using DCA.

<img width="1432" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/91cdcda3-b5a7-410f-a3cd-34329207e93a">

Click next

<img width="1432" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/a8a4c28c-8dbd-406a-9b2f-a6e4271e2efd">

Click next

Select the lung biospecimen folder:

<img width="1432" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/5ff8f30b-10a0-4dad-8b97-b9ab9ea8b600">

Click next

Select biospecimen template:

<img width="1432" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/4dc1ccc5-b5b3-407a-b79f-1de2463bfd5f">

It generates a template for you to submit data. You fill in this google sheet and download as CSV... note I left out a required field:

<img width="539" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/c598bc47-0c20-47a4-a3aa-25dfffee281a">

You then upload this back to DCA, you'll see a summary and option to validate:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/84ba3472-f16e-4e9f-95c9-306bd183c1aa">

Click "Validate Metadata"

It tells you there's an error:

<img width="1431" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/8f16e423-ee8d-4bc5-af6d-aac34ac78d50">

I'll correct the error and redownload as CSV:

<img width="452" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/94eb2bfd-6a00-4983-aba7-80586f035fb2">

Now I'll reupload to DCA and click the validate button again:

<img width="1430" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/84d8b551-de8e-4836-9f51-e1ebfdec9bbc">

This time it passes validation and I'm giving the option to "Submit data":

<img width="1430" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/937e59a0-6a7b-472f-abbf-1f92af12a108">

<img width="1430" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/633cf7e5-8c69-48a1-82a2-a89be427a5b4">

And you get a success message along with a link to where in Synapse the file was submitted to:

<img width="1430" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/92ff6b25-f154-49a5-a4c5-f02b622d935a">

And you can see the manifest stored on Synapse:

<img width="1430" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/57923fe2-d473-4230-ac5f-1f5dfec89cb4">

## Data Release to Portal

And that's really it for you!  Behind the scenes the INCLUDE team takes these submitted and validated files, transforms them to FHIR (a data exchange standard), and populates the portal on a regular basis.

Not every field that is submitted is currently in the portal but, over time, we will add more and more data to the portal.

<img width="1256" alt="image" src="https://github.com/briandoconnor/synapse-tutorial-2023/assets/1730584/d9970fe0-d261-4a5f-94e9-7292784a221a">


## Live Demo Instructions

* Open Synapse and show the [INCLUDE Test Project C](https://www.synapse.org/#!Synapse:syn52171867/files/) - which can represent an INCLUDE Contributor site 
* Navigate to DCA ([this is the production instance](https://dca.app.sagebionetworks.org/))
* Within DCA use the DCA Demo DCC - this is equivalent to an INCLUDE DCC Hub 
* Select the INCLUDE Test Project C 
* Find the Biospecimen_Heart folder - it should be empty.  
* Select the Biospecimen Template
* Download - and in here you add a few lines of metadata - you can start with a blank space in the Tissue Status column (see screen shot) to show an error during validation
* Download as a CSV
* Navigate back to DCA - browse and upload the CSV you just saved
* Click Validate - show the error that you get.  
* Navigate back to the Google sheet and correct the error, save as CSV, upload, validate and submit.
* At this point you can go back to the Synapse project and show that the CVS has been submitted.  

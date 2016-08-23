# project-convert-a-card

This is the template for the Convert-a-Card projects seen on LibCrowds.


## Supported languages

The following languages (or writing systems) are currently supported:

- Pinyin
- Indonesian
- Urdu

To add support for another language update the `libs` variable and `getLibs()`
function in [template.html](template.html) and add a descriptive paragraph
to the bottom of [long_description.md](long_description.md).

## Workflow

The workflow established for Convert-a-Card projects is as follows:

#### 1. Create a new project

The following steps describe how to create a new project using
[pybossa-github-builder](https://github.com/alexandermendes/pybossa-github-builder):

1. Create a new project.
    - **Important:** The short name must start with one of the supported languages listed above, in lower case.
2. Select Dashboard from the side menu then Sync with GitHub.
3. Enter the URL of this page (https://github.com/LibCrowds/project-convert-a-card) and click Continue.
4. On the following page, click Update.
5. Select Dashboard from the side menu then Import Tasks.
6. Select the Flickr importer and, if necessary, log in using the LibCrowds Flickr credentials.
7. Select your album and click Import.
    - **Important:** If importing a large number of tasks, wait for the email to let you know that the import has finished before proceeding.
8. From the Dashboard click Task Redundancy.
9. Enter **3** and click Set Redundancy.
10. To publish the project visit the Dashboard again and click Publish.

Note that there are various other ways to create new projects, all of which are
described in the [PyBossa documentation](http://docs.pybossa.com/en/latest/user/overview.html).


#### 2. Analyse the results

For all tasks where two or more contributors submitted the same answer, for both
the WorldCat record and the shelfmark, the final result will automatically be set
to that answer. For those tasks where no contributors were able to find a matching
WorldCat record the final result will be set to a blank field for the WorldCat
record and the shelfmark. For all other tasks, human intervention will be required.

1. Sign in and select Open Project from the menu at the top right of the screen. Here 
   you will see all projects for which you are the project owner.
2. Open the project then from the left-hand menu click Analysis. If there are tasks pending analysis you will 
   be presented with a card and all associated answers. Otherwise, a message will be displayed
   saying that there are no unanalysed results to process.
    - When you first visit the analysis application you'll be asked for a username and password, which can
      be supplied by a LibCrowds administrator.
    - Users other than the project owner can also help analyse results by visiting the following URL directly: `https://analyse.libcrowds.com/<project_short_name>`
3. To spot check results open the project as above then click results from the left-hand menu.

**Important:** Once a project has been completed ensure that all results are analysed by either clicking through
to the analysis application, as in step 3, or by downloading the relevant CSV file from the [LibCrowds Data](https://www.libcrowds.com/data/) page
and ensuring that there are no rows with 'Unanalysed' in the *info* column.


#### 3. Submit the data

1. Download the results CSV file for the project from the [LibCrowds Data](http://www.libcrowds.com/data) page.
2. Check the *info_oclc* and *info_shelfmark* columns for things like duplicates or poorly formatted shelfmarks.
3. If you do notice any errors visit `https://analyse.libcrowds.com/<project_short_name>/<result_id>` to edit the result.
4. Once all discrepencies have been dealt with download the updated CSV file once again.
5. Submit this file to metadata services.
    - The Work Request Number for printed books in the oriental collections is 15.045.

**Important:** If any changes are subsequently made, for example, if certain records are not able to be
ingested, the associated results should be updated on the system as in step 3. This ensures that we can
later identify the cards that still need to be processed by alternative means.


## Downloading images

The analysis application can be used to download sets of images from Flickr by listing their
task IDs in the form at `https://analyse.libcrowds.com/<project_short_name>/download`. You can
visit this URL by clicking the Download Input menu link in your project dashboard. The
task IDs can be found in the results CSV file for your project.

So, to download all images for which a WorldCat record was not found just filter the
*info_oclc* column to show blank cells only then copy the contents of the *task_id* column
into the form. As all of the images need to be downloaded from Flickr it may take a few
minutes for the resulting zip file to be prepared.

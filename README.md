# project-convertacard

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

1. Visit the [Create Project from GitHub](https://www.libcrowds.com/github/project/new) page.
2. Enter the URL of this page (https://github.com/LibCrowds/project-convert-a-card) and click Search.
3. Modify the name and short name (e.g. to *Pinyin Card Catalogue: Drawer One* and *pinyincardcatalogue_d1*).
    - **Important:** The short name must start with one of the supported languages listed above, in lower case.
4. Click Create.
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

1. From the Dashboard click Analysis.
    - If there are tasks pending analysis you will be presented with the card and all submitted answers.
    - Use the radio buttons to select the correct answer.
    - If no answers are acceptable, select the free text fields and leave them blank.
    - The free text fields can also be used to specify any other answer.
2. Once a project has been completed, ensure that all tasks have been analysed.
    - A notification label next to the Analysis menu option shows how many tasks are pending analysis.
    - On clicking the link a message will also be displayed if there are no pending tasks.
3. From the Dashboard click Results.
    - This view allows you to scroll through the final results for the purpose of spot checking.

**Note:** All of the above can be performed at any time, as the project is ongoing.


#### 3. Submit the data

1. From the LibCrowds [About](http://www.libcrowds.com/about) page, download the results CSV file.
2. Check the *info_oclc* and *info_shelfmark* columns for things like duplicates or poorly formatted shelfmarks.
3. If you do notice any errors you can visit the `/<project_short_name>/<result_id>` to edit the result.
4. Once all discrepencies have been dealt with download the updated CSV file once again.
5. Submit this file to metadata services.
    - The Work Request Number for printed books in the oriental collections is 15.045.
**Important:** If any changes are subsequently made, for example, if certain records are not able to be ingested, the results should be updated on the system as in part 4. This ensures that we can later identify the cards that still need to be processed by alternative means.

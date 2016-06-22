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

1. Visit the [Create Project from GitHub](http://www.libcrowds.com/github/new_project) page.
2. Enter the URL of this page (https://github.com/LibCrowds/project-convert-a-card) and click Search.
3. Modify the name and short name (e.g. to *Pinyin Card Catalogue: Drawer One* and *pinyincardcatalogue_d1*).
    - **Important:** The short name must start with one of the supported languages listed above, in lower case.
4. Click Create.
5. Select Dashboard from the side menu then Import Tasks.
6. Select the Flickr importer and, if necessary, log in using the LibCrowds Flickr credentials.
7. Select your album and click Import.
    - **Important:** Wait for an email to let you know that all tasks are imported, before proceeding to the next step.
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
3. If you do notice any errors visit the analysis application to edit the result.
    - Copy the *id* from the relevant row of the spreadsheet.
    - Append this ID to the root URL of the analysis application, followed by /edit (e.g. `https://{root-url}/<id>/edit`).
    - Here you can edit the result info directly (e.g. by deleting the values for oclc and shelfmark).
    - **Note:** While it would be possible to edit the spreadsheet directly, following the above method ensures
      that the final result is stored permentantly in the main database. Apart from being safer (this database is
      backed up daily), this means that the downloadable final result data is kept in line with what was actually
      submitted to metadata services.
4. Once all discrepencies have been dealt with download the updated CSV file.
5. Submit this file to metadata services.
    - The Work Request Number for printed books in the oriental collections is 15.045.

# Questionnaires

* [Overview](#overview)
* [Minimal Questionnaire](#minimal-form)
* [Standard Questionnaire](#standard-form)
* [Customizing Your Questionnaire](#customizing-your-questionnaire)

### Overview {#overview}

Every data project is different - starting with the questions being asked. These questions shape everything about the project- including the fields for data collection.

The Cadasta platform allows you to define your own data collection schema, so you can tailor your data collection around the specific questions your asking. These questions could include contact details, geographic place names or how the land was acquired.

The underlying technology that enables this comes from [XLSForm](http://xlsform.com). XLSForm is a form standard based on authoring forms using a spreadsheet. The forms (or questionnaires) are easy to use, while also allowing for more complexity as needed.

The two questionnaires you can start with are:

* [The minimal questionnaire](https://docs.google.com/spreadsheets/d/1gB7lcz4Dr6aqdW_Oesuum2pbI8lzs6EYTLpVZGQMhcQ/edit#gid=2006567796) for the bare minimum of data needed by the platform; and

* [The standard questionnaire](https://docs.google.com/spreadsheets/d/1QsqMTLlPH5KVbBcgnh6MHWkIR0pIFchVzkqBSoL92fA/edit#gid=2006567796) - which is the starting point for many of our partners.

You can use either of these forms as a starting points for your project. You can also modify parts of these forms to fit your data collection needs.

To use them, follow the links above to your desired questionnaire. Then, download your very own .xlsx form.

![](/assets/download-as-xlsx.png)

If you have questions about how to use these questionnaire forms, [contact us](cadasta.org/contact/) at any time.

### The Minimal Questionnaire {#minimal-form}

[The minimal form](https://docs.google.com/spreadsheets/d/1gB7lcz4Dr6aqdW_Oesuum2pbI8lzs6EYTLpVZGQMhcQ/edit#gid=2006567796) has the essential fields you need to collect your data.

This form has three tabs:

* Survey
* Choices, and
* Settings.

The **survey** tab shows the overall data collection schema.

> Check information about first two columns: `type` and `name`

![](/assets/minimal-survey.png)

* The areas in gray are fields that the Cadasata platform requires to work. Some of them \(like `deviceid`\) you'll never see . 
* The first two columns - `type` and `name` - relate to the type of data being collected, and the name it's given.
* The areas in white indicate the questions that will show up on the form. \(Note the `image` options only show up with mobile data collectors [ODK](odkcollect.md) & [GeoODK](06-geoodkcollect.md), allowing you to take a pictures of the location or party you're documenting.

The **choices** tab is where the choices for any drop-down menus are stored.

![](/assets/minimal-choices.png)

For example, the `respondent` entries in A2 - A4 correspond with this dropdown menu in the Add Relationship popup:

![](/assets/relationship-dropdown.png)

The **settings** tab shows you the `form_id` and title of the questionnaire. You'll use this ID when you set up data collection with ODK and GeoODK.

### The Standard Questionnaire {#standard-form}

[The standard form](https://docs.google.com/spreadsheets/d/1QsqMTLlPH5KVbBcgnh6MHWkIR0pIFchVzkqBSoL92fA/edit#gid=2006567796) has all the same questions as the mininimal version, with quite a few added. You can see many of these choices indicated in the **survey** tab. 

![](/assets/standard-survey.png)

The image above shows some fields that have been added in addition to the minimal information. These fields are organized by section:

* Location Attributes (rows 22-28)
* Default Party Attributes (rows 20-32)
* Individual Party Attributes (rows 34-38)
* Group Party Attributes (rows 40-43)
* Party Relationship Attributes (45-47)
* Tenure Relationship Attributes (49-51)

The **choices** tab also shows some additional choice options for your dropdown menus. 

![](/assets/standard-choices-more.png)

For example, rows 38-47 show the choices for the different types of location acquisitions. 

The **settings** tab of the standard questionnaire is exactly the same as it is in the minimal version - providing the `form_id`. 

![](/assets/standard-settings.png)

### Customizing Your Questionnaire {#customizing-your-questionnaire} 

If you need to collect different data than what's in the standard questionnaire, you can customize it to meet your needs. Any field with a white background can be modified. Fields with a gray background need to remain as they are in order for the questionnaires to work with the Cadasta Platform. 

#### Deleting Unnecessary Fields

If there's a field that you don't want to include, simply delete its row from survey tab of the questionnaire. To do this in Excel, right click the row and then select Delete. 

#### Editing Drop-Down Fields

To edit a field in a drop-down menu, navigate to the choices tab. There, you can modify the `name` and `label` of the fields as needed. 

For example, to add a new field to the location acquisition dropdown (`l_acquired_how`):

* Add a new row, and give it a `list name` of `l_acquired_how`.
* Add a new name and label.

In the example below, a new category for the dropdown ("Unknown") has been added to the questionnaire. 

![](/assets/land-acquision-new-row.png)

Once that questionnaire is saved and loaded into the project, the new "Unknown" option will appear in the dropdown under, "How was this location acquired?"

![](/assets/standard-new-field.png)

#### Creating a New Dropdown Menu

#### Data Types

* `text`
* `gender`
* `date`
* `select-one`
* `select-one` `yes_no`



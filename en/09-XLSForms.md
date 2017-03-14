# Cadasta XLSForms & Custom Data Collection

> need:
* Final one-to-many form from David
* Replace all images (based on Form)
* Links to all revised forms as Excel Spreadsheets, hosted on Amazon server

> Questions
* Do we want partners to mess with geopoint, geotrace, geoshape? Same with the geopoint, geotrace, geoshape dropdowns?

//


* [Overview](#overview)
* [Types of Cadasta Template Forms](#types)
* [Parts of a Cadasta Form](#parts)
	* [Survey Tab](#survey-tab)
	* [Choices Tab](#choices-tab)
	* [Settings Tab](#settings-tab)
* [Customizing Your XLSForm for Cadasta](#customizing-your-xlsform)
* [Troubleshooting](#troubleshooting)

### Overview {#overview}

Every data collection project is different - starting with the questions you're asking. These questions shape everything about the project- including the entry fields for data collection.

The Cadasta Platform allows you to define your own data collection schema, so you can tailor it around the specific questions you're asking. These questions could include contact details, geographic place names or how the land was acquired.

In the Cadasta Platform, the underlying technology that enables this comes from [XLSForm](http://xlsform.org/). XLSForm is a form standard that allow you to create forms using a spreadsheet. The forms are low-fi alternatives to a database. They are also designed to handle information of varying degrees of complexity.  

In this section, you'll learn about how to use XLSForms designed specifically for use with the Cadasta system. 

### Types of Cadasta Template Forms {#types}

When it comes to data schemas, land rights documentation often falls into one of three different categories:

> need project example for Standard Questionnaire

* One person (or group of people) using one piece of land ([project example - ]()),
* Many different people (or groups of people) using one piece of land ([project example - Urban Informal Settlements]()), and
* One person (or group of people) using many pieces of land ([project example - Smallholder Agriculture]()). 

Cadasta has designed a template form for each of these use cases, which you can download here: 

> Katrina - please check links below. Are they correct still?

* [Standard Form(also knows as a One-to-One Form)](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx)
* [One-to-Many Form](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/multiple_party_standard_cadasta_questionnaire.xlsx)
* [Many-to-One Form](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/multiple_location_standard_cadasta_questionnaire.xlsx)

**These forms should be the starting point of any Cadasta project.** Keep reading to learn about how they work and how to customize them.

> Link to customization.

### Parts of a Cadasta Form {#parts}

Each Cadasta form follows a similar structure. Here, we're looking at the [One-to-Many Form](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/multiple_party_standard_cadasta_questionnaire.xlsx). 

#### Form Tabs

There are 3 tabs. 

* **Survey** shows all of the survey questions you’re asking. 
* **Choices** lists all of the choices that appear in multiple choice questions or drop-down menus. 
* And finally, **Settings** has some basic information about the form and its default language.


#### Survey Tab {#survey-tab}

> Section notes:
* Indicate required and nonrequired fees.

> [add image]

The Survey Tab shows all of the survey questions you're asking. This section outlines everything you need to know about this important tab.

##### **Sections & Color Coding**

In Cadasta’s structure, the questions are divided into four parts, each with its own color coding:

* **Mandatory Fields**, which house some of the required meta information as well as geographic data collection options. These fields cannot be modified.
* **Location Information**, for collecting basic information such as how the land is used or whether there has been recent flooding.
* **Party Information**, for information about people using the location.
* **Relationship information**, describing the kind relationship (or tenure) between the land and the people who use it.

> link to Project Resources

Any photos, videos or audio collected are stored as **Project Resources** 


##### **Headings**

The Survey tab includes some important column headers you need to know about.

> link to relevant tables, esp. `required`

| Item | Description | Synonyms | Notes |
|`type` | defines the type of question it is, like a text, date, integer, or multiple choice question.| ||
|`name`| gives a database-readable name to the question. || It must start with a letter only be made of letters, numbers, and underscores.|
|`label`| where you write the question you want to actually show up on the survey.|`label::[language]`|To add a language, append `label::` with the desired <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
" target="_blank">2-digit ISO country code</a>. e.g. `fr` is French|
|`required`| indicates whether a question is required | bind:required| Allowed values: yes, no, TRUE, FALSE, true(), false(); or a statement that evaluates as true or false. Note that Some fields must be marked as required in order to work. (See table below)|
|`hint`|Optional.  This column allows you to give additional information to the person filling out the form.|||
|`default`| A default value that is pre-filled before the user gets to the question ||In the above example, in line 22, the default selection is set to `renter`.|
|`relevant`| adds visibility logic. In other words, it allows you to show or hide questions based on an answer to another question. |||

> add example of visibility logic (David)

##### **Data Entry Types**

The `type` field can take many different data entry types. 

These data entry types go with **meta questions**. These questions are hidden to the user.

| Item | Description | Synonyms | Notes |
| `start` | Records when the form was loaded| | |
| `end` | Records when the form was finished| | |
| `today` | Records the date the form was loaded| | |
| `deviceid` | Get the device ID (for Android devices) | | |

The below data entry types go with **regular questions**, which do appear to the user. 

| Item | Description | Synonyms | Notes |
| `select_one` `[list_name]` `[or_other]`  | User can choose one of several choices| | Must be set to Required to work|
| `select_multiple` `[list_name]` `[or_other]`  | User can choose one or more of several choices| | Must be set to Required to work|
| `text`  | User can enter a text response| | |
| `integer`  | User can enter an integer| | |
| `decimal`  | User can enter a decimal number | | |
| `date`  | User can enter a date| | Must be set to Required to work|
| `image`  | User can take or attach a picture| `photo`| |
| `audio`  | User can record or attach audio | | |
| `video`  | User can record or attach video| | |
| `note`  | User is shown a note (no response possible)| | |
| `geopoint`  | Collects a single point of data based on the user's GPS coordinates.| | |
| `geoshape`  | records a polygon made of multiple GPS coordinates, which are drawn on-screen. | | |
| `geotrace`  | records a line of two or more GPS coordinates.  | |Location pins are added based on the user's GPS coordinates. 


##### **Groups**

> David, is this a sufficient description of Groups?

Groups contain one or more questions or other nested groups. Some of may repeat, which is described in the next section.

| Item | Description | Synonyms | Notes |
| `begin_group` | Sets the beginning of a group | | Do not edit this row! |
| `end_group` | Sets the beginning of a group | | Do not edit this row!|



##### **Repeats**

> [add image]

Both the Many-to-One and One-to-Many (shown above) forms make use of Repeats. Repeats allow you the option of repeating a section of questions without having to start the whole survey all over again. 

In GeoODK, for example, a repeat gives you a screen like the one shown below. 

You have the option to repeat the section or not. This is the feature that allows you to collect information for many people associated with a single location, or for many locations associated with a single person or group of people.

| Item | Description | Synonyms | Notes | 
| `begin_repeat` | Sets the beginning of a repeat group | | Do not edit this row! |
| `end_repeat` | Ends the repeat group| | Do not edit this row!|

####Choices Tab {#choices-tab}

The Choices tab is where you enter choices for your multiple choice survey questions. These are the headers required on this tab: 

| Item | Description | Synonyms | Notes |
|`list_name` | defines the type of question it is, like a text, date, integer, or multiple choice question.| ||
|`name`| gives a database-readable name to the question. || It must start with a letter only be made of letters, numbers, and underscores.|
|`label`| choice that the user sees|label::[language]| Add different language options by appending the header `label::` with a <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
" target="_blank">2-digit ISO country code</a>, e.g. `label::fr`|

To get your multiple choice options to show up on the form, add the `list_name` to the `type` field in the survey tab, following either a `select_one` or `select_multiple` type. 

> Edit based on final form

For example, you can see `main_use` listed by `select_one` on row 14:

> [add image]

Which looks like this in GeoODK:

> [add image]

#### Settings Tab {#settings-tab}

> [add image]

The Settings tab is devoted to a few special settings. 

* `form_id` provides a unique ID for this form. Make sure that you have a different ID for each of your Cadasta projects!
* `title` is what shows up on ODK or GeoODK when you load the form. 
* `default_language` shows the default language being used on the form, indicated by the <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
" target="_blank">2-digit ISO country code</a>. Here, we’ve marked the default language as English.


### Customizing Your XLSForm for Cadasta {#customizing-your-xlsform}

#### Steps to Creating Your Custom Cadasta Form

The first thing you need to do is think through the questions you'll be asking in your data collection.

1. Identify your questions. What information do you need to collect in your project? 

2. Identify where each question should go. Is this question about a party, location, relationship, or something else?

3. Identify each question's data entry type. What kind of  entry would work best for each question - a date? A text field? A drop-down or multiple choice?

4. Choose your starter template form based on your use case:
Are you documenting one group of people per location? Or many different groups in a single location? Or how one group of people uses many different locations? 

Once you've thought this through, you can start adding your questions to their appropriate section.

#### Basic Customization

##### Rows that Can & Cannot Be Edited

> David, what else can't be edited?

Before editing your form, it's important to note that some rows cannot be edited. Changing them in any way will cause the form to break and result in errors. 

Areas that cannot be edited or deleted:
* Any field in gray
* Pre-loaded header rows (except for `label::[language]`; that column can be deleted if it won't be used).

Everything else is up for grabs.

##### Adding New Questions

To add a new question, create a new row. 

From there, the easiest way to create a new question is to copy and paste a row with the same question `type`. From there, you can edit the `name`, `label`, and other fields as needed. 

##### Editing Multiple Choice Options

> Beth update based on final form

To edit a field in a multiple choice question, navigate to the Choices tab. There, you can modify the `name` and `label` of the fields as needed.

For example, to add a new field to the location acquisition dropdown \(`l_acquired_how`\):

* Add a new row, and give it a `list_name` of `l_acquired_how`.
* Add a new name and label.

In the example below, a new category for the dropdown \("Unknown"\) has been added to the Cadasta Form.

![](/assets/land-acquision-new-row.png)

Once that form is saved and loaded into the project, the new "Unknown" option will appear in the dropdown under, "How was this location acquired?"

![](/assets/standard-new-field.png)

##### Attachment of Multiple Resources

If you need to attach multiple resources during your data collection in the field, you can do so using a few special codes:

* `tenure_resource_*`, for uploading multiple resources related to relationships, 

* `party_resource_*`, for uploading multiple resources related to the party, and

* `location_resource_*`, for uploading multiple resources related to a location. 

Here's an example of these codes at work in a form, under `name` in rows 11, 12, 19, 20, 31, 32, and 33:

![](/assets/questionnaire-mulitiple-resource-example.png)

The codes can be used multiple times in your form, preceding unique words like `_pic1` and `_pic2`. 

#### Advanced Customization

> David, what else cannot be edited or deleted??

If you need to do more than simply edit a few existing fields, then advanced customization may be for you.

Remember, when it comes to editing forms, some of the fields cannot be modified.

Areas that cannot be edited or deleted:
* Any field in gray
* Pre-loaded header rows (except for `label::[language]`; that column can be deleted if it won't be used).


##### Editing Form Sections

![](/assets/standard-survey.png)

The customizable portion of the form has been organized into the following sections: 

In Cadasta’s structure, the questions are divided into four parts, each with its own color coding:

* **Mandatory Fields**, which house some of the required meta information as well as geographic data collection options. These fields cannot be modified.

* **Location Information**, for collecting basic information such as how the land is used or whether there has been recent flooding.

* **Party Information**, for information about people using the location.

* **Relationship information**, describing the kind relationship (or tenure) between the land and the people who use it.

Each of these sections relates to a piece of the Cadasta Platform's internal workings. In order for your questions to appear in the platform, they need to be in one of these sections.

It is possible to create new sections, as another Cadasta partner has done below. Here, they've added a section on witnesses:

![](/assets/example-xls-2.png)

##### Dropdown with All GeoTypes (GeoTrace, GeoPoint & GeoShape)

> David, is this something that we want partners to mess with?

In some cases, you may want to give your data collectors the option to choose collecting data using GeoTrace, GeoPoint or GeoShape. If you do, you can modify to your form to make this possible. Alternatively, you can build out your questionnaire [starting from this one](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx). 

If you'd like to update an existing questionnaire, here's what you need to do. 

In the **Survey tab** of your questionnaire, add three rows just below row 11. 

![](/assets/allgeo-modify-1.png)

Then, copy and paste the below into rows 11 - 14. 

<table>
<tbody>
<tr>
    <td>select_one geo_type</td>
    <td>geo_type</td>
    <td>Select type of geo collection</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td>geoshape</td>
    <td></td>
</tr>
<tr>
    <td>geoshape</td>
    <td>location_geoshape</td>
    <td>Draw the location boundaries on the map	</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td></td>
    <td>${geo_type}='geoshape'</td>
</tr>
<tr>
    <td>geotrace</td>
    <td>location_geotrace</td>
    <td>Please, walk through the location boundaries</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td></td>
    <td>${geo_type}='geoshape'</td>
</tr>
<tr>
    <td>geopoint</td>
    <td>location_geopoint</td>
    <td>Please, select a point</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td></td>
    <td>${geo_type}='geoshape'</td>
</tr>
</tbody>
</table>


Note that you may need to use the _Paste Special_ option and select Text in the pop-up window that follows.

![](/assets/allgeo-modify-2.png)

Next, you'll need to add the following options to the the Choices tab of your spreadsheet. Again, you may need to paste this using the _Paste Special_ option. 

<table>
<tbody>
<tr>
    <td>geo_type</td>
    <td>geoshape</td>
    <td>Drawing coordinates on a map</td>
</tr>
<tr>
    <td>geo_type</td>
    <td>geotrace</td>
    <td>Walking around the boundaries</td>
</tr>
<tr>
    <td>geo_type</td>
    <td>geopoint</td>
    <td>Select a location point</td>
</tr>
</tbody>
</table>

In the image below, the fields above have been pasted into a minimum questionnaire. 

![](/assets/allgeo-modify-3.png)

Now, when data collectors are collecting data in the field, they can choose which data collection method is best: GeoTrace, GeoPoint or GeoShape.

### Troubleshooting {#troubleshooting}

> David & Katrina, what should be edited here?

Before uploading your form to your project, check to make sure that:

* all of your data entry `types` match those listed in the table above and and are spelled correctly. 
* all of your `names` are lowercase and contain no spaces. 
* all of your `list_names` in the Choices tab match the name you've given to your dropdowns in the Survey tab.
* all of your `form_ids` are distinct, contain no spaces, and start with a lowercase letter.

Simple misspellings and formatting inconsistencies can cause errors when it's time to collect data. For this reason, we highly recommend testing your data collection before heading out to the field. 

If you're having trouble with your form, please don't hesistate to [contact us](http://cadasta.org/contact/) at any time - we're here to help you get your data collection just right.

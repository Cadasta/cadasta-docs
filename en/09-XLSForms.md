# Cadasta XLSForms & Custom Data Collection

> redo table of contents

* [Overview](#overview)
* Parts of a Cadasta Form
	* Survey Tab
	* Choices Tab
	* Settings Tab
* Data Entry Types
* Customizing Your Form

### Overview {#overview}

Every data collection project is different - starting with the questions you're asking. These questions shape everything about the project- including the entry fields for data collection.

The Cadasta Platform allows you to define your own data collection schema, so you can tailor it around the specific questions you're asking. These questions could include contact details, geographic place names or how the land was acquired.

In the Cadasta Platform, the underlying technology that enables this comes from [XLSForm](http://xlsform.org/). XLSForm is a form standard that allow you to create forms using a spreadsheet. The forms \(which we call questionnaires\) are low-fi alternatives to a database. They are also designed to handle information of varying degrees of complexity.  

In this section, you'll learn about how to use XLSForms designed specifically for use with the Cadasta system. 

### Types of Cadasta Template Forms

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

### Parts of a Cadasta Form

Each Cadasta form follows a similar structure. Here, we're looking at the [One-to-Many Form](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/multiple_party_standard_cadasta_questionnaire.xlsx). 

#### Form Tabs

There are 3 tabs. 

* **Survey** shows all of the survey questions you’re asking. 
* **Choices** lists all of the choices that appear in multiple choice questions or drop-down menus. 
* And finally, **Settings** has some basic information about the form and its default language.


#### Survey Tab

> Section notes:
* Indicate required and nonrequired fees.

> [add image]

The survey tab includes some important column headers you need to know about.

##### **Sections & Color Coding**

In Cadasta’s structure, the questions are divided into four parts, each with its own color coding:

* **Mandatory Fields**, which house some of the required meta information as well as geographic data collection options. These fields cannot be modified.
* **Location Information**, for collecting basic information such as how the land is used or whether there has been recent flooding.
* **Party Information**, for information about people using the location.
* **Relationship information**, describing the kind relationship (or tenure) between the land and the people who use it.

> link to Project Resources

Any photos, videos or audio collected are stored as **Project Resources** 

> QUESTION FOR PROGRAMS TEAM: do any of the below sections still apply? I like the less technical sounding wording above. 

##### Form Sections

![](/assets/standard-survey.png)

The customizable portion of the questionnaire has been organized into the following sections: 

* **Location Attributes** relate to to information about the location - like its name and boundaries. 

* **Default Party Attributes** specify the information that you collect about any party, be it an individual, group, or corporation.

* **Individual Party Attributes** and **Group Party Attributes** each provide information specific to whether a party is an individual or group.

* **Party Relationship Attributes** is for information specific to the relationship between a party and the location. 

* **Tenure Relationship Attributes** specify information about a party's tenure on the land.

##### **Headings**

* `type` defines the type of question it is, like a text, date, integer, or multiple choice question. 
* `name`  gives a database-readable name to the question. It must start with a letter only be made of letters, numbers, and underscores.
* `label` is where you write the question you want to actually show up on the survey. 
* `label::fr` is an optional column for adding additional languages to your survey. To add a language, append `label::` with the desired <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
" target="_blank">2-digit ISO country code</a>. Here, FR means French.
* `required` indicates whether a question is required. Please note that some fields must be marked as required in order to work. See the table below for more info. 

> link table 

* `default` is where you can indicate a default response to multiple choice questions. In the above example, in line 22, the default selection is set to `renter`.
* `relevant` adds visibility logic. In other words, it allows you to show or hide questions based on an answer to another question.  

> add example of visibility logic (David)

##### **Repeats**

> [add image]

Both the Many-to-One (shown above) and One-to-Many forms make use of Repeats. Repeats allow you the option of repeating a section of questions without having to start the whole survey all over again. 

In GeoODK, for example, a repeat gives you a screen like the one shown below. 

You have the option to repeat the section or not. This is the feature that allows you to collect information for many people associated with a single location, or for many locations associated with a single person or group of people.

**Important**! `begin repeat` and `end repeat` separate the questions that repeat from the ones that don't, and they **should not** be edited or modified! 

To change what data type you're collecting, modify cell A11 on either your standard or minimum questionnaire. 

####Choices Tab

> [add image]

The Choices tab is where you enter choices for your multiple choice survey questions. 

* `list_name` gives the set of responses a database-readable name. 
* `name` is the database-readable version of a possible answer. 
* `label` is choice that the user sees. Like in the survey tab, you can add a column for different language options by appending the header `label::` with a <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
" target="_blank">2-digit ISO country code</a>.

To get your multiple choice options to show up on the form, add the `list_name` to the `type` field in the survey tab, following either a `select_one` or `select_multiple` type. 

For example, you can see `main_use` listed by `select_one` on row 14:

> [add image]

Which looks like this in GeoODK:

> [add image]

#### Settings Tab

> [add image]

The Settings tab is devoted to a few special settings. 

* `form_id` provides a unique ID for this form. Make sure that you have a different ID for each of your Cadasta projects!
* `title` is what shows up on ODK or GeoODK when you load the form. 
* `default_language` shows the default language being used on the form, indicated by the <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes
" target="_blank">2-digit ISO country code</a>. Here, we’ve marked the default language as English.

### Data Entry Types

Here is a table with all of the data entry types:

> Insert Table


#### GeoTrace, GeoShape and GeoPoint {#geo}

In your location data collection, you may choose to collect point, line, or polygon data. In both the standard and minimum questionnaires, you have the option to choose one of these using `geopoint`, `geotrace`, or `geoshape`. 

* `geotrace` records a line of two or more GPS coordinates. It's also the default setting of both the minimum and standard questionnaires. With `geotrace`, location pins are added based on the user's GPS coordinates. 

* `geoshape` records a polygon made of multiple GPS coordinates, which are drawn on-screen. 

* `geopoint` collects single points of data based on the user's GPS coordinates


### Customizing Your Questionnaire {#customizing-your-questionnaire}

If you need to collect different data than what's in the standard questionnaire, and more than what's in the minimum questionnaire, you can customize these forms to meet your needs. Any entry with a white background can be modified. Fields with a gray background need to remain as they are in order for everything to work.

#### Basic Customization

##### Deleting Unnecessary Fields

If there's a field that you don't want to include, simply delete its row from the survey tab of the questionnaire. To do this in Excel, right-click the row and then select Delete.

Fields that can be deleted:

* Fields in white (all forms)
* Darker colored fields (repeating forms only)

Fields that **cannot** be deleted: 
* Fields in gray cannot (all forms)
* Fields in lighter colors (repeating forms only)


##### Editing Drop-Down Fields

To edit a field in a drop-down menu, navigate to the Choices tab. There, you can modify the `name` and `label` of the fields as needed.

For example, to add a new field to the location acquisition dropdown \(`l_acquired_how`\):

* Add a new row, and give it a `list_name` of `l_acquired_how`.
* Add a new name and label.

In the example below, a new category for the dropdown \("Unknown"\) has been added to the Cadasta Form.

![](/assets/land-acquision-new-row.png)

Once that form is saved and loaded into the project, the new "Unknown" option will appear in the dropdown under, "How was this location acquired?"

![](/assets/standard-new-field.png)

##### Attachment of Multiple Resources

> David, does this still apply to forms?

If you need to attach multiple resources during your data collection in the field, you can do so using two special codes:

* `tenure_resource_*`, for uploading multiple resources related to relationships, 

* `party_resource_*`, for uploading multiple resources related to the party, and

* `location_resource_*`, for uploading multiple resources related to a location. 

Here's an example of these codes at work in a form, under `name` in rows 11, 12, 19, 20, 31, 32, and 33:

![](/assets/questionnaire-mulitiple-resource-example.png)

The codes can be used multiple times in your form, preceding unique words like `_pic1` and `_pic2`. 

#### Advanced Customization

If you need to do more than simply edit a few existing fields, then advanced customization may be for you.

Remember, when it comes to editing forms, only some fields that can be modified.

Fields that can be modified:

* Fields in white (all forms)
* Darker colored fields (repeating forms only)

Fields that **cannot** be modified: 
* Fields in gray cannot (all forms)
* Fields in lighter colors (repeating forms only)

##### Data Entry Types {#data-types}

To fully take advantage of customizing your Cadasta Form, it's important to figure out which data entry type will work best for the kind of information you're collecting. Some of the most common ones that you'll use are:

* `text` - which specifies that you're collecting basic text.
* `date` - which specifies that you're logging the date.
* `select_one` - which specifies that you're using a dropdown menu

![](/assets/standard-survey-example.png)

You can see each of these at work in the above example, taken from the survey tab of the standard form.

Notice that `select_one` - the dropdown option - requires identifying a set of choices to go with it. In the example above, the first dropdown menu specifies that cell A24 is linked to the choices tagged `l_quality_choices`. In the Choices tab, you can see the different options for `l_quality_choices`:

![](/assets/standard-choices-example.png)

_Note that using `select_multiple` follows the same logic; only rather than selecting a single item from a dropdown, it allows the user to select multiple items._

These options will appear in the dropdown when it's selected.

In addition to these basic data types, [XLSForm offers many different data types for you to choose from](http://xlsform.org/#question-types).

![](/assets/xls-form-question-types.png)

The type you need depends on the kinds of questions you need to ask. For example, if you need to collect an audio sample from an interviewee, you could select `audio`, which will prompt you to take an audio recording.

##### Form Sections

![](/assets/standard-survey.png)

The customizable portion of the form has been organized into the following sections: 

* **Location Attributes** relate to to information about the location - like its name and boundaries. 

* **Default Party Attributes** specify the information that you collect about any party, be it an individual, group, or corporation.

* **Individual Party Attributes** and **Group Party Attributes** each provide information specific to whether a party is an individual or group.

* **Party Relationship Attributes** is for information specific to the relationship between a party and the location. 

* **Tenure Relationship Attributes** specify information about a party's tenure on the land.

Each of these sections relates to a piece of the Cadasta Platform's internal workings. In order for your questions to appear in the platform, they need to be in one of these sections.

The below image is taken from a custom form used by one of our partners. Here, they've added a number of custom fields in the `party_attributes_default` section:

![](/assets/example-xls-1.png)

It is possible to create new sections, as another Cadasta partner has done below. Here, they've added a section on witnesses:

![](/assets/example-xls-2.png)

##### Dropdown with All GeoTypes (GeoTrace, GeoPoint & GeoShape)

// David, is this something that we want partners to mess with?

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

##### Steps to Creating Your Custom Cadasta Form

The first thing you need to do is think through the questions you'll be asking in your data collection.

1. Identify your questions. What information do you need to collect in your project? 

2. Identify where each question should go. Is this question about a party, location, relationship, or something else?

3. Identify each question's data entry type. What kind of  entry would work best for each question - a date? A text field? A drop-down or multiple choice?

4. Choose your starter template form based on your use case:
Are you documenting one group of people per location? Or many different groups in a single location? Or how one group of people uses many different locations? 

> add links to forms


Once you've thought this through, you can start adding your questions to their appropriate section.

Before uploading your form to your project, check to make sure that:

* all of your data entry `types` match those listed in the table above and and are spelled correctly. 
* all of your `names` are lowercase and contain no spaces. 
* all of your `list_names` in the Choices tab match the name you've given to your dropdowns in the Survey tab.
* all of your `form_ids` are distinct, contain no spaces, and start with a lowercase letter.

Simple misspellings and formatting inconsistencies can cause errors when it's time to collect data. For this reason, we highly recommend testing your data collection before heading out to the field. 

If you're having trouble with your form, please don't hesistate to [contact us](http://cadasta.org/contact/) at any time - we're here to help you get your data collection just right.

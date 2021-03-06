# Cadasta XLSForms & Custom Data Collection

_Note: Check out our [Cadasta XLSForm video here](https://www.youtube.com/watch?v=m3vg7mxJjNM)._

* [Overview](#overview)
* [Types of Cadasta Template Forms](#types)
* [Parts of a Cadasta Form](#parts)
	* [Survey Tab](#survey-tab)
	* [Choices Tab](#choices-tab)
	* [Settings Tab](#settings-tab)
* [Cadasta XLSForm & Language](#xlsform-language)
* [Customizing Your XLSForm for Cadasta](#customizing-your-xlsform)
* [Troubleshooting](#troubleshooting)

## Overview {#overview}

Each data collection project is different - starting with the goal of the survey. The format, order and structure of the questions you ask make a huge difference in the field and when you are conducting analysis on the data later.

The Cadasta Platform allows you to define your own data collection schema. You can customize your survey around specific themes that you are aiming to uncover through specific questions. These questions can include anything from text field of thea respondent's contact details to a drop down list of village names to a multiple select option of how the land was acquired.

The underlying technology in the Cadasta Platform is [XLSForm](http://xlsform.org/). XLSForm is a form standard that allows you to create a custom questionaire using a spreadsheet (or Google sheet)-- instead of a clunky database. With XLSForm, you can add various types of fields, like integers, radio questions, checkbox questions, text fields, etc. You can also add default values or logic that will show certain questions depending on the answers of previous questions. The forms are low-fi alternatives to a database. They are also designed to handle information of varying degrees of complexity.  

The Cadasta Platform uses a subset of features from XLSForm so that users are able to focus on custom questions they want to ask in the field and on the web. In this section, you will learn about how to use XLSForms designed specifically for use with the Cadasta system. 
  

## Types of Cadasta Template Forms {#types}


Since Cadasta XLSForms are the basis for all Cadasta projects, Cadasta has designed a variety of template forms for you to start from. Each starter form maps to a common land rights documentation use case. 

To get started, choose the form that most closely matches your documentation needs. If you need help or have questions, [please contact us](http://cadasta.org/contact/).

* The [Customary Rights Form](https://docs.google.com/spreadsheets/d/1MHg6iok4SkDxN2NdMVt3P2W9UZe81VxH6CpAz_eUtOY/pub?output=xlsx) is designed for documenting the rights of a single group of people who are using a single parcel or piece of land, like in this [Customary Rights project in Ghana](https://demo.cadasta.org/organizations/cadasta-demo-organization/projects/customary-rights-ghana/). 
* The [Sustainable Sourcing Form](https://docs.google.com/spreadsheets/d/1hyF_uxZb4959lxD6vDMM574cQEFTyq636VAS7n3e0MA/pub?output=xlsx) is for documenting land that's being used for sustainable agricultural production.
* The [Smallholder Agriculture Form](https://docs.google.com/spreadsheets/d/1HKal7WyNSji80cg7ID9FnXh9-4dFvjSuqHJKu4_vxxI/pub?output=xlsx) is designed for documenting a farmer's rights to use one or more plots of land. See this [Smallholder Farming project](https://demo.cadasta.org/organizations/cadasta-demo-organization/projects/smallholder-farmers-india/) as an example. 
* The [Urban Informal Settlements Form](https://docs.google.com/spreadsheets/d/1iORFg75ofq-QzLB5x-WvuggEZN6JaE0iS6yqc7dE1Y0/pub?output=xlsx) is for documenting many people who may be living in a very small urban area, like in [this Urban Informal Settlements project](https://demo.cadasta.org/organizations/cadasta-demo-organization/projects/urban-informal-settlement-enumeration/).  

To view the example projects listed above, visit <a href="https://demo.cadasta.org/dashboard/" target="_blank">demo.cadasta.org</a>. There you can create an account or log in using the following credentials:

* user: `demo`
* pass: `password`

**These forms are the starting point of any Cadasta project.** Keep reading to learn about how they work and [how to customize them](#customizing-your-xlsform).

## Parts of a Cadasta Form {#parts}

Each Cadasta form follows a similar structure. This guide will walk you through the [Smallholder Agriculture (1:Many) Form](https://docs.google.com/spreadsheets/d/1HKal7WyNSji80cg7ID9FnXh9-4dFvjSuqHJKu4_vxxI/pub?output=xlsx). 


### Form Tabs

There are 3 tabs. 

* **Survey** shows all of the survey questions. 
* **Choices** lists all of the choices that appear in single-choice (dropdown) or multiple-choice (checkboxes) questions.
* And finally, **Settings** has the required form name and language information.

A Reference Table tab has been added, as well, to make it convinent to look up the fields and syntax required by the form. 

### Survey Tab {#survey-tab}

![survey tab](/assets/xls-01-survey-tab.png)

The Survey Tab shows all of the survey questions you're asking. This section outlines everything you need to know about this important tab.

#### Sections & Color Coding

In Cadasta’s structure, the questions are divided into four parts, each with its own color coding:

* **Mandatory Fields**, at the top, houses the required meta information. These fields cannot be modified.
* **Location Information**, for collecting basic information such as how the land is used or whether there has been recent flooding.
* **Party Information**, for information about people using the location.
* **Relationship information**, describing the kind relationship (or tenure) between the land and the people who use it.

**Areas that cannot be edited are given a grey or colorful background.** Areas in white can be edited.

Any photos, videos or audio collected are stored as **[Project Resources](/04-records.md)**. 

#### Tips Column

The first column in the Survey tab provides tips about the form, such as notes about how to format different fields. 

If it gets in your way, feel free to hide the column at any time.

Additional information can be found in the Reference Tables tab.

#### Headings

The Survey tab includes some important column headers you need to know about.

| Item | Description | Synonyms | Notes |
|:--------|:--------|:--------|:--------|
|`type` | Defines the type of question it is, like a text, date, integer, or multiple choice question.| ||
|`name`| Gives a database-readable name to the question. || It must start with a letter only be made of letters, numbers, and underscores.|
|`label`| Where you write the question you want to actually show up on the survey.|`label::[language]`|To add a language, append `label::` with the desired 2-digit ISO country code. e.g. `fr` is French. You can find a list of ISO codes here: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes|
|`required`| indicates whether a question is required | `bind:required`| Allowed values: `yes`, `no`, `TRUE`, `FALSE`, `true()`, `false()`; or a statement that evaluates as true or false. The following [data entry types](#data-entry-types) must be set to `required`in order to work: `select_one`, `select_multiple`, and `date`. |
|`hint`|_Optional._  This column allows you to give additional information to the person filling out the form.|||
|`default`| A default value that is pre-filled before the user gets to the question ||In the above example, in line 22, the default selection is set to `renter`.|
|`relevant`| adds visibility logic. In other words, it allows you to show or hide questions based on an answer to another question. ||||


#### Data Entry Types{#data-entry-types}

The `type` field can take many different data entry types. 

These data entry types go with **meta questions**. These questions are hidden to the user, but required for the form to work.

| Item | Description | Synonyms | Notes |
|:--------|:--------|:--------|:--------|
| `start` | Records when the form was loaded| | |
| `end` | Records when the form was finished| | |
| `today` | Records the date the form was loaded| | |
| `deviceid` | Gets the device ID (for Android devices) | | | | |
 
The below data entry types go with **regular questions**, which do appear to the user. 

| Item | Description | Synonyms | Notes |
|:--------|:--------|:--------|:--------|
| `select_one` `[list_name]` `[or_other]`  | User can choose one of several choices| | Must be set to `required` to work|
| `select_multiple` `[list_name]` `[or_other]`  | User can choose one or more of several choices| | Must be set to `required` to work|
| `text`  | User can enter a text response| | |
| `integer`  | User can enter an integer| | |
| `decimal`  | User can enter a decimal number | | |
| `date`  | User can enter a date| | Must be set to `required` to work|
| `image`  | User can take or attach a picture| `photo`| |
| `audio`  | User can record or attach audio | | |
| `video`  | User can record or attach video| | |
| `note`  | User is shown a note (no response possible)| | |
| `geopoint`  | Collects a single point of data based on the user's GPS coordinates.| | |
| `geoshape`  | Records a polygon made of multiple GPS coordinates, which are drawn on-screen. | | |
| `geotrace`  | Records a line of two or more GPS coordinates.  | |Location pins are added based on the user's GPS coordinates. 


#### Groups

Groups contain one or more questions or other nested groups. Some of may repeat, which is described in the next section.

| Item | Description | Synonyms | Notes |
|:--------|:--------|:--------|:--------|
| `begin_group` | Sets the beginning of a group | | Do not edit this row! |
| `end_group` | Sets the beginning of a group | | Do not edit this row!|

It's important to include the groups section headers. This ensures the information inside shows up in the right section of the platform, as well as in GeoODK and ODK.

#### Repeats

![](/assets/xls-02-repeats.png)

Both the Urban Informal Settlements and Smallholder Agriculture forms make use of Repeats. Repeats allow you the option of repeating a section of questions without having to start the whole survey all over again. 


| Item | Description | Synonyms | Notes | 
|:--------|:--------|:--------|:--------|
| `begin_repeat` | Sets the beginning of a repeat group | | Do not edit this row! |
| `end_repeat` | Ends the repeat group| | Do not edit this row!|

#### Form Variable References

Form Variables create conditional logic in the form. They can be used in the `relevant` field.

| Item | Description | Synonyms | Notes | 
|:--------|:--------|:--------|:--------|
| `${variable_name}` | Reference another question (can be used in skip logic condition [relevant], validation, inside another question or hint label| | |
| `.` | Current question| | | |

### Choices Tab {#choices-tab}

![](/assets/xls-03-choices-tab.png)

The Choices tab is where you enter choices for your multiple choice survey questions. These are the headers required on this tab: 

| Item | Description | Synonyms | Notes |
|:--------|:--------|:--------|:--------|
|`list_name` | defines the type of question it is, like a text, date, integer, or multiple choice question.| ||
|`name`| gives a database-readable name to the question. || It must start with a letter only be made of letters, numbers, and underscores.|
|`label`| choice that the user sees|`label::[language]`| Add different language options by appending the header `label::` with a 2-digit ISO country code, e.g. `label::fr`. List of ISO codes here: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes|

To get your multiple choice options to show up on the form, add the `list_name` to the `type` field in the survey tab, following either a `select_one` or `select_multiple` type. 

For example, you can see `spoken_languages` listed by `select_multipe` on row 20:

![](/assets/xls-04-select-multiple.png)

On the choices tab, you can see all of the `spoken_languages` attribute.

![](/assets/xls-05-list-name.png)

### Settings Tab {#settings-tab}

The Settings tab is devoted to a few special settings. 

| Item | Description | Synonyms | Notes |
|:--------|:--------|:--------|:--------|
| `form_id`| Provides a unique ID for this form. | | Make sure that you have a different ID for each of your Cadasta projects!|
| `title`| What shows up on ODK or GeoODK when you load the form | | |
| `default_language`| Shows the default language being used on the form. | | Use the 2-digit ISO country code to choose your language. For example, `en` sets the form to English. You can find the ISO codes listed here: https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes|


## Cadasta XLSForm & Language {#xlsform-language}

You can add one or more language options to your Cadasta XLSForm, making it possible to collect survey data in a variety of languages.

To add a new language, create a new `label` column in the Survey tab, and give it a title like `label::fr`. Here, `fr` is the <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes" target="_blank">two-digit ISO code</a> for French, but you can choose any language you like. 

In your new `label::[language]` column, provide translations for each label line by line. 

Similarly, in the `choices` tab, add a `label::[language]` column for multiple choice selections you'd like to see in a different language. 

On the Platform, you can toggle language options in the upper right: 

![](/assets/translation-01-xlsform.png)

Note that the language selected on the upper right only changes the language of the survey questions and answers, not the whole platform. Similarly, the language selected on the lower right does not change the language shown on the


## Customizing Your XLSForm for Cadasta {#customizing-your-xlsform}

### Steps to Creating Your Custom Cadasta Form

The first thing you need to do is think through the questions you'll be asking in your data collection.

1. Identify your questions. What information do you need to collect in your project? 

2. Identify where each question should go. Is this question about a party, location, relationship, or something else?

3. Identify each question's data entry type. What kind of  entry would work best for each question - a date? A text field? A drop-down or multiple choice?

4. Choose your starter template form based on your use case. Is it most like a sustainable sourcing project? Or smallholder agriculture documentation? Or something else?

Once you've thought this through, you can start adding your questions to their appropriate section.

### Rows that Can & Cannot Be Edited

Before editing your form, it's important to note that some rows cannot be edited. Changing them in any way will cause the form to break and result in errors. 

Areas that cannot be edited or deleted:
* Any field with a gray or colorful background.
* Pre-loaded header rows (except for `label::[language]`; that column can be renamed to indicate an added language, or deleted if it won't be used).

All fields in white **can** be edited.

### Adding New Questions

To add a new question, create a new row. 

From there, the easiest way to create a new question is to copy and paste a row with the same question `type`. From there, you can edit the `name`, `label`, and other fields as needed. 

### Editing Multiple Choice Options

To edit a field in a multiple choice question, navigate to the Choices tab. There, you can modify the `name` and `label` of the fields as needed.

For example, to add a new field to the spoken languages options \(`spoken_languages\):

* Add a new row, and give it a `list_name` of `spoken_languages`.
* Give it a new name and fill in the labels.

Once that form is saved and loaded into the project, the new option will appear in the appropriate dropdown or multiple choice selection.

### Attachment of Multiple Resources

If you need to attach multiple resources during your data collection in the field, you can do so using a few special codes:

* `tenure_resource_*`, for uploading multiple resources related to relationships, 

* `party_resource_*`, for uploading multiple resources related to the party, and

* `location_resource_*`, for uploading multiple resources related to a location. 

The codes can be used multiple times in your form, preceding unique words like `_pic1` and `_pic2`. 


## Troubleshooting {#troubleshooting}

Before uploading your form to your project, check to make sure that:

* all of your data entry `types` match those listed in the table above and and are spelled correctly. 
* all of your `names` are lowercase, start with a letter, and are made of letters, numbers and underscores. 
* all of your `list_names` in the Choices tab match the name you've given to your dropdowns in the Survey tab.
* all of your `form_ids` are distinct, contain no spaces, and start with a lowercase letter.
* all of your photos are smaller than 10MB. 
* none of mandatory fields have been edited or deleted.

Simple misspellings and formatting inconsistencies can cause errors when it's time to collect data. For this reason, we highly recommend testing your data collection before heading out to the field. 

If you're having trouble with your form, please don't hesistate to [contact us](http://cadasta.org/contact/) at any time - we're here to help you get your data collection just right.

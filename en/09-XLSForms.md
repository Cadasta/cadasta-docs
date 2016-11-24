# Questionnaires & Custom Data Collection

* [Overview](#overview)
* [Minimum Questionnaire](#minimal-form)
* [Standard Questionnaire](#standard-form)
* [Multiple Location Questionnaires](#multiple-location-questionnaires)
* [Multiple Party Questionnaires](#multiple-party-questionnaires)
* [Customizing Your Questionnaire](#customizing-your-questionnaire)

### Overview {#overview}

Every data collection project is different - starting with the questions you're asking. These questions shape everything about the project- including the entry fields for data collection.

The Cadasta Platform allows you to define your own data collection schema, so you can tailor it around the specific questions you're asking. These questions could include contact details, geographic place names or how the land was acquired.

In the Cadasta Platform, the underlying technology that enables this comes from [XLSForm](http://xlsform.org/). XLSForm is a form standard that allow you to create forms using a spreadsheet. The forms \(which we call questionnaires\) are low-fi alternatives to a database. They are also designed to handle information of varying degrees of complexity.  

> David, would love your insight on how to make this a little bit more intuitive. 

You can start your project with one of the following ready-to-go questionnaires. They fall into two categories:

* Non-Repeating Questionnaires
* Repeating Questionnaires

The difference is based on whether or not you want the options for some questions to repeat during your data collection. For example, you may need to collect data for multiple locations that all have the same relationship to a certain party. In that case, you would want to use a repeating questionnaire. If not, you'd want a non-repeating questionnaire. 

Non-Repeating Questionnaires:

> 11.23.2016 - all links need to be replaced

* [The minimum questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx) creates a schema for the bare minimum of data needed by the platform; and

* [The standard questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx) is the starting point for many of our partners. It includes the same entry fields as the minimum questionnaire, with some added. 

Repeating Questionnaires:

> Add links to the below questionnaires

* [The multiple location questionnaire]() lets you collect data for multiple locations that all relate to a single party, but may have different relationships to each one. For example, a community group may hold a lease for one property and have right-of-way access for another. If a party has the same relationship to all the locations, then a similar, alternative form is available - the [multiple location, single relationship questionnaire](). Both of these forms have many of the same fields as the minimum questionnaire. 

* [The multiple party questionnaire]() lets you collect data for multiple parties that may have relationships with a single location. For example, a building may be leased by many tenants and owned by another individual. In the event that the parties all have the same relationship with the location, then an alternative is available: the [multiple party, single relationship questionnaire](). Like the other repeating questionnaires, these forms have many of the same fields as the minimum questionnaire. 

You can use any of these forms as starting points for your project. You can also modify parts of these forms to fit your data collection needs. 

If you need to significantly modify these data entry fields, see the section on [customizing your questionnaire](#customizing-your-questionnaire). 

_**Important note:** You can make small changes to your questionnaire - such as adding a row - and reupload it to an existing project. However, if your questionnaire changes significantly, you may need to start a new project._

If you have questions about how to use these questionnaires, [contact us](http://cadasta.org/contact/) at any time.

### The Minimum Questionnaire {#minimal-form}

[The minimum questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx) has the essential fields you need for data collection using the Cadasta Platform.

This questionnaire has three tabs:

* Survey
* Choices, and
* Settings.

The **Survey** tab shows the overall data collection schema.

![](/assets/minimum-survey.png)

The areas in gray are fields that the Cadasta platform requires to work. Some of them \(like `deviceid`\) are used behind the scenes, so you'll never see them in the Platform, ODK, or GeoODK. _(Note! Do not tamper with any of the gray fields!)_

The first three columns are important ones for you to know about:
* `type` specifies the type of entry you're adding - be it text, a date, a dropdown or something else. 
* `name` specifies the variable used for that entry. No two names can be the same!
* `label` shows the text that will actually be seen on the form. Fields in white can be modified as needed.

The **Choices** tab is where the choices for all the drop-down menus are stored.

![](/assets/minimum-choices.png)

For example, the `respondent` entries Group, Individual and Corporation (A2 - A4 in the image above) correspond with this dropdown menu in the Add Relationship popup:

![](/assets/relationship-dropdown.png)

The **Settings** tab shows you the `form_id`, the title of the questionnaire, and the default language. 

You'll use the `form_id` when you set up data collection with ODK and GeoODK. 

Each form ID in your organization needs to be unique. Make sure all of the questionnaires follow this rule. Otherwise, they won't load, and you'll default to using the original form with that ID. Also be sure to create names that start with lowercase letters and contain no spaces.


### The Standard Questionnaire {#standard-form}

[The standard questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx) has most of the same questions as the minimal version, with quite a few added. You can see many of these choices indicated in the **Survey** tab.

In the required fields, at the top of the survey above the yellow lines, one section that's different from the minimal questionnaire can be seen on rows 13-16: the selection of `geoshape`, `geotrace`, and `geopoint`.

![](/assets/new-standard-01.png)

This setting allows data collectors to choose how they'd like to log their location while they're in the field. 

_[Read more about GeoTrace, GeoShape, and GeoPoint here](#geo)_

Another important difference is can be seen in column D: the use of a different language. 

If you need to use other languages in your questionnaire (such as a combination of Spanish and English), you can indicate the preferred language in the column header in your form questionnaire using a notation like this:

```
label::es
```

To make this work, you'll need to add a third column to the Settings tab and give it the heading `default_language`.

![](/assets/new-standard-02.png)

This indicates the default language you prefer for your data collection. It's set using <a href="https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes" target="_blank">two-letter ISO 639-1 codes</a>. For example, to set the default language to Swahili, you would use the abbreviation `sw`. 

![](/assets/new-standard-03.png)

Let's walk through some of the other columns you'll see in the standard questionnaire (shown above). 

* Images and audio recordings (rows 20-23)
* Location Attributes \(rows 27-32\)
* Default Party Attributes \(rows 34-36\)
* Individual Party Attributes \(rows 38-43\)
* Group Party Attributes \(rows 45-48\)
* Tenure Relationship Attributes \(50-52\)

Each of these sections relates to a data collection window in the Cadasta platform.

The **Choices** tab has the same options as the minimal questionnaire, with some additional drop-down choices as well.  

![](/assets/new-standard-04.png)

For example, rows 41-44 show the choices for the different types of location problems, which correspond with row 30 on the Survey tab. Additionally, you'll notice the choices for `geo_type`, and the inclusion of a column for answers in Spanish.   

The **Settings** tab of the standard questionnaire is similar to how it is in the minimal version - providing the title and `form_id`, which is your identifier for the questionnaire in ODK or GeoODK. The only difference is the addition of the `default_language` section, which provides the default language for the questionnaire.

![](/assets/new-standard-02.png)

**Important!** Make sure all of the questionnaires in your organization have unique form IDs. Otherwise, they won't load in ODK or GeoODK. Also be sure to create names that start with lowercase letters and contain no spaces. 

### Multiple Location Questionnaires {#multiple-location-questionnaires}

If you are collecting data for multiple locations as they relate to a single party, then one of these two multiple location questionnaires may be for you:

* [The multiple location questionnaire](), and 
* [the multiple location, single relationship questionnaire](). 

The first questionnaire lets you collect data for multiple locations that all relate to a single party, but may have different relationships to each one. For example, a community group may hold a lease for one property and have right-of-way access for another. 

The second questionnaire is better if you're collecting data for a party that has the same relationship to all the locations. For example, if an individual inherited a number of buildings and properties, then the second questionnaire will be better. 

Both of these forms have many of the same fields as the minimum questionnaire, but they are formatted a little bit differently.

![](/assets/repeating-01-location.png)

In the above image, there are two important things to note:

* **`begin repeat` and `end repeat`. These rows separate the questions that repeat from the ones that don't, and they **should not** be edited or modified.  

* **Light and dark colors for each question group.** These indicate the questions that can be modified or edited (darker colors), and which ones can't (lighter colors). For example, rows 18 and 19 can be edited, and more questions can be added there. _See [customizing your questionnaire](#customizing-your-questionnaire) for more information about how to do that._

The multiple location, single relationship questionnaire works similarly. The difference is simply in the location of the the `begin repeat` and `end repeat` rows. 

![](/assets/repeating-02-location-one-rel.png)

As with the standard and minimal questionnaires, fields in gray should not be edited or moved: they are required for the forms to work. 


###Multiple Party Questionnaires 
{#multiple-party-questionnaires}

If you are collecting data for multiple parties as they relate to a single location, then one of these two multiple party questionnaires may be for you:

* [The multiple party questionnaire](), and 
* [the multiple party, single relationship questionnaire](). 

The first questionnaire lets you collect data for multiple parties that may have relationships with a single location. For example, a building may be leased by many tenants and owned by another individual. 

In the event that the parties all have the same relationship with the location, then you may want to use the second questionnaire. 

Both of these forms have many of the same fields as the minimum questionnaire. 

![](/assets/repeating-02-party.png)

In the above image, there are two important things to note:

* **`begin repeat` and `end repeat`. These rows separate the questions that repeat from the ones that don't, and they **should not** be edited or modified.  

* **Light and dark colors for each question group.** These indicate the questions that can be modified or edited (darker colors), and which ones can't (lighter colors). For example, rows 18 and 19 can be edited, and more questions can be added there. _See [customizing your questionnaire](#customizing-your-questionnaire) for more information about how to do that._

The multiple location, single relationship questionnaire works similarly. The difference is simply in the location of the the `begin repeat` and `end repeat` rows. 

![](/assets/repeating-02-party-one-rel.png)

As with the standard and minimal questionnaires, fields in gray should not be edited or moved: they are required for the forms to work. 


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

In the example below, a new category for the dropdown \("Unknown"\) has been added to the questionnaire.

![](/assets/land-acquision-new-row.png)

Once that questionnaire is saved and loaded into the project, the new "Unknown" option will appear in the dropdown under, "How was this location acquired?"

![](/assets/standard-new-field.png)

#### GeoTrace, GeoShape and GeoPoint {#geo}

In your location data collection, you may choose to collect point, line, or polygon data. In both the standard and minimum questionnaires, you have the option to choose one of these using `geopoint`, `geotrace`, or `geoshape`. 

* `geotrace` records a line of two or more GPS coordinates. It's also the default setting of both the minimum and standard questionnaires. With `geotrace`, location pins are added based on the user's GPS coordinates. 

* `geoshape` records a polygon made of multiple GPS coordinates, which are drawn on-screen. 

* `geopoint` collects single points of data based on the user's GPS coordinates. 

To change what data type you're collecting, modify cell A11 on either your standard or minimum questionnaire. 

##### Attachment of Multiple Resources

If you need to attach multiple resources during your data collection in the field, you can do so using two special codes:

* `tenure_resource_*`, for uploading multiple resources related to relationships, 

* `party_resource_*`, for uploading multiple resources related to the party, and

* `location_resource_*`, for uploading multiple resources related to a location. 

Here's an example of these codes at work in a questionnaire, under `name` in rows 11, 12, 19, 20, 31, 32, and 33:

![](/assets/questionnaire-mulitiple-resource-example.png)

The codes can be used multiple times in your questionnaire, preceding unique words like `_pic1` and `_pic2`. 

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

To fully take advantage of customizing the questionnaire, it's important to figure out which data entry type will work best for the kind of information you're collecting. Some of the most common ones that you'll use are:

* `text` - which specifies that you're collecting basic text.
* `date` - which specifies that you're logging the date.
* `select_one` - which specifies that you're using a dropdown menu

![](/assets/standard-survey-example.png)

You can see each of these at work in the above example, taken from the survey tab of the standard questionnaire.

Notice that `select_one` - the dropdown option - requires identifying a set of choices to go with it. In the example above, the first dropdown menu specifies that cell A24 is linked to the choices tagged `l_quality_choices`. In the Choices tab, you can see the different options for `l_quality_choices`:

![](/assets/standard-choices-example.png)

_Note that using `select_multiple` follows the same logic; only rather than selecting a single item from a dropdown, it allows the user to select multiple items._

These options will appear in the dropdown when it's selected.

In addition to these basic data types, [XLSForm offers many different data types for you to choose from](http://xlsform.org/#question-types).

![](/assets/xls-form-question-types.png)

The type you need depends on the kinds of questions you need to ask. For example, if you need to collect an audio sample from an interviewee, you could select `audio`, which will prompt you to take an audio recording.

##### Questionnaire Sections

![](/assets/standard-survey.png)

The customizable portion of the questionnaire has been organized into the following sections: 

* **Location Attributes** relate to to information about the location - like its name and boundaries. 

* **Default Party Attributes** specify the information that you collect about any party, be it an individual, group, or corporation.

* **Individual Party Attributes** and **Group Party Attributes** each provide information specific to whether a party is an individual or group.

* **Party Relationship Attributes** is for information specific to the relationship between a party and the location. 

* **Tenure Relationship Attributes** specify information about a party's tenure on the land.

Each of these sections relates to a piece of the Cadasta Platform's internal workings. In order for your questions to appear in the platform, they need to be in one of these sections.

The below image is taken from a custom questionnaire used by one of our partners. Here, they've added a number of custom fields in the `party_attributes_default` section:

![](/assets/example-xls-1.png)

It is possible to create new sections, as another Cadasta partner has done below. Here, they've added a section on witnesses:

![](/assets/example-xls-2.png)

If you'd like to create new sections or significantly customize your questionnaire, we highly recommend that you [contact us](http://cadasta.org/contact/) first. We're here to help! 

##### Dropdown with All GeoTypes (GeoTrace, GeoPoint & GeoShape)

In some cases, you may want to give your data collectors the option to choose collecting data using GeoTrace, GeoPoint or GeoShape. If you do, you can modify to your form to make this possible. Alternatively, you can build out your questionnaire [starting from this one](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire-all-geo.xlsx). 

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

##### Steps to Creating Your Custom Questionnaire

The first thing you need to do is think through the questions you'll be asking in your data collection.

1. Identify your questions. What information do you need to collect in your project? 

2. Identify each question's data entry type. What kind of  entry would work best for each question - a date? A text field? A drop-down or multiple choice?

3. Identify where each question should go. Is this question about a party, location, relationship, or something else?

Once you've thought this through, you can start adding your questions to their appropriate section.

Before uploading your questionnaire to your project, check to make sure that:

* all of your data entry `types` match those listed on [XLSForm](http://xlsform.org/#question-types) and are spelled correctly. 
* all of your `names` are lowercase and contain no spaces. 
* all of your `list_names` in the Choices tab match the name you've given to your dropdowns in the Survey tab.
* all of your `form_ids` are distinct, contain no spaces, and start with a lowercase letter.

Simple misspellings and formatting inconsistencies can cause errors when it's time to collect data. For this reason, we highly recommend testing your data collection before heading out to the field. 

If you're having trouble with your questionnaires, don't hesistate to [contact us](http://cadasta.org/contact/) at any time - we're here to help you get your data collection just right.

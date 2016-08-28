# Questionnaires & Custom Data Collection

* [Overview](#overview)
* [Minimal Form](#minimal-form)
* [Standard Form](#standard-form)
* [Customizing Your Questionnaire](#customizing-your-questionnaire)

### Overview {#overview}

Every data project is different - starting with the questions being asked. These questions shape everything about the project- including the fields for data collection.

The Cadasta platform allows you to define your own data collection schema, so that you can tailor your data collection around the specific questions your asking.  

Our platform structurea the data around three core entities: 
* the **Party** \(a person, family, community or organization\), 
* the **Place** and 
* the **Relationship** \(rights, restrictions and responsibilities connecting the Party to the Place\).

Within this framework you have the ability to add as many fields as you need, customized to your project's local context.  These could include fields for contact details, names of family members, geographic place names, how the land was aquired, or even information more relevant for a census, such as information on health, education or public services.

The underlying technology that enables this comes from [XLSForm](http://xlsform). XLSForm is a form standard based on authoring forms using a spreadsheet. The forms are easy to use, while also allowing for more complexity as needed.  

The two forms you can start with are:

* [The minimal form](https://docs.google.com/spreadsheets/d/1gB7lcz4Dr6aqdW_Oesuum2pbI8lzs6EYTLpVZGQMhcQ/edit#gid=2006567796) for the bare minimum of data needed by the platform; and

* [The standard form](https://docs.google.com/spreadsheets/d/1QsqMTLlPH5KVbBcgnh6MHWkIR0pIFchVzkqBSoL92fA/edit#gid=2006567796) - which is the starting point for many of our partners.

You can use either of these forms as a starting points for your project. You can also modify parts of these forms to fit your data collection needs. 

To use them, follow the links above to your desired form. Then, download your very own .xlsx form. 

> add image

If you have questions about how to use these questionnaire forms, [contact us](cadasta.org/contact/) at any time. 

### The Minimal Form {#minimal-form}

[The minimal form](https://docs.google.com/spreadsheets/d/1gB7lcz4Dr6aqdW_Oesuum2pbI8lzs6EYTLpVZGQMhcQ/edit#gid=2006567796) has the essential fields you need to collect your data.

This form has three tabs: 
* Survey
* Choices, and
* Settings.

![](/assets/minimal-survey.png)

The **survey** tab shows the overall data collection schema. 

![](/assets/minimal-survey.png)

* The areas in gray are fields that the Cadasata platform requires to work. Some of them (like `deviceid`) you'll never see . 
* The first two columns - `type` and `name` - are 
* The areas in white indicate the questions that will show up on the form. (Note the `image` options only show up with mobile data collectors [ODK](odkcollect.md) & [GeoODK](06-geoodkcollect.md), allowing you to take a pictures of the location or party you're documenting.

The *choices* tab is where the choices for any drop-down menus are stored. 

![](/assets/minimal-choices.png)

For example, the `respondent` entries in A2 - A4 correspond with this dropdown menu:

> add image from Parties view

The *settings* tab shows you the `form_id` and title of the questionnaire. You'll use this ID when you set up data collection with ODK and GeoODK. 

### The Standard Form {#standard-form}

[The standard form](https://docs.google.com/spreadsheets/d/1QsqMTLlPH5KVbBcgnh6MHWkIR0pIFchVzkqBSoL92fA/edit#gid=2006567796) has all the same questions as the mininimal version, with quite a few added. 

![](/assets/standard-survey.png)

![](/assets/standard-choices.png)

![](/assets/standard-settings.png)

### Customizing Your Questionnaire {#customizing-your-questionnaire}



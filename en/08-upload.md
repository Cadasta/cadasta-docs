#Importing Data

* [Overview](#overview)
* [Setting Up](#setting-up)
* [Importing Data](#importing-data)

### Overview{#overview}

If you've already been collecting data in another system and are switching to the Cadasta Platform, you can import your data in a .csv. This can be useful if you have many questionnaires to import, whether you have 10 or 10,000.

Data importing is also a relatively new feature. We recommend that you <a href="http://http://cadasta.org/contact/" target="_blank">reach out to us</a> so that we can help you through the process. 

### Setting Up{#setting-up}

Before importing your data, you'll want to make sure that the structure of your dataset matches the structure of the [questionnaire](#09-XLSForms.md) that you're using for your project. 

In this example, you can see a .csv of responses:

![](/assets/upload-sample-csv.png)

Each of these fields corresponds with entries in this customized questionnaire:

> add image

If you have questions about whether your questionnaire matches your data set, or if you need to create a questionnaire to match your data, please don't hesitate to <a href="http://http://cadasta.org/contact/" target="_blank">reach out to us</a> for assistance. 

### Importing Data {#importing-data}

To import your data this, navigate to the main project page. There, select the three dots on the upper right, and then Import Data. 

![](/assets/upload-01.png)

Next, you'll come to a page where you can give the file a name and select your .csv for uploading. You can also select whether or not you'd like to add your .csv as a project resource, which may be helpful for archival purposes. 

![](/assets/upload-02.png)

On the page that follows, you'll be asked to select your input fields. 

![](/assets/upload-03.png)

Note that grayed-out checkboxes indicate required questions in your questionnaire (i.e. questions marked `yes` in the `required` column). They must be included with the file upload. 

At the bottom of this page, you may see some notes like `The following fields have no corresponding attribute` and `These attributes exist in your schema but not in your import`. 

![](/assets/upload-04.png)

> David, what is meant here?

The first message indicates [not sure, David?]

The second message indicates fields that exist in your questionnaire that do no appear in your .csv.

On the next page, you'll need to configure a couple types of fields. 

![](/assets/upload-05.png)

One type is for selecting the type of default party name and party type (individual, group, or corporation). The other is for selecting the type of location, geometry, and geometry field.

_Please note that this section will likely change as of December 2016. In the meantime, please <a href="http://http://cadasta.org/contact/" target="_blank">reach out to us</a> for guidance.

When you're done, select **Import Data** from the bottom right. Note that this might take a few moments. If the upload takes more than a minute, then you will get a timeout and need to try again. If the problem persists, try splitting your one .csv into two. 

If the uploaded is completed successfully, you'll be able to see all of the records you've imported from the project location overview page. 

![](/assets/upload-07.png)


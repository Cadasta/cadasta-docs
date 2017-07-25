#Importing Data

* [Overview](#overview)
* [Setting Up](#setting-up)
* [Importing Data](#importing-data)
* [Troubleshooting](#troubleshooting)

## Overview{#overview}

If you've already been collecting data in another system and are switching to the Cadasta Platform, you can import your data in a .csv. This can be useful if you have many completed Cadasta XLSForms to import, whether you have 10 or 10,000.

Data importing is also a relatively new feature. We recommend that you <a href="http://cadasta.org/contact/" target="_blank">reach out to us</a> so that we can help you through the process. 

##Setting Up{#setting-up}

Before importing your data, you'll want to make sure that the structure of your dataset matches the structure of the [Cadasta XLSForm](09-XLSForms.md) that you're using for your project. 

In this example, you can see a .csv of responses:

![](/assets/import-00-example.png)

Which works with this form:

![](/assets/import-01-form.png)

Here you can see that: 

* each header in the data corresponds with a `name` in the form. 

* all of the required fields – all marked in gray - are preserved, even if there is no corresponding data or fields in the .csv. 

If you look at the `choices` tab of the form, you can also see that the options in the `name` column match entries in the .csv. Note that these options need to match exactly in both spelling and format. 

![](/assets/import-02-choices.png)

If you have questions about whether your form matches your data set, need to create a form to match your data set, or are having trouble importing data from your .csv, please don't hesitate to <a href="http://cadasta.org/contact/" target="_blank">reach out to us</a> for assistance. 

## Importing Data {#importing-data}

To import your data, navigate to the main project page. There, select the **More actions** button on the upper right, and then Import Data. 

![](/assets/import-0724t.png)

Next, you'll come to a page where you can give the file a name and select your .csv for uploading. 

![](/assets/import-05.png)

Note that here you need to select whether you'll be uploading an Excel file or a CSV. Make sure that the selected file type matches the one of the file being uploaded.

On the page that follows, you'll be shown some messages indicating required fields in the Cadasta XLSForm that do not have corresponding fields in the data. Just click Next to get to the next stage.

On the next page, you'll need to configure a couple types of fields. 

One type is for selecting the type of default people / party name and type (individual, group, or corporation). The other is for selecting the type of location and geometry field. These simply create default inputs for required fields not shown in the .csv.

When you're done, select **Finish** from the bottom right. Note that this might take a few moments. If the upload takes more than a minute, then you'll likely get a timeout message and need to try again. If the problem persists, try splitting your .csv into two smaller files and uploading them one at a time.

If the upload is completed successfully, you'll be able to see all of the records you've imported from the project location overview page. 

## Troubleshooting {#troubleshooting}

If you're getting an error with your import, make sure that:

* **The import is the right size.** The platform can import up to 10 MB at a time. 
* **Your field headers are spelled correctly.** If the headers on your import don't match the headers of the Cadasta XLSForm used to create your project, the import will not work. 
* **Choice options align between your import and your Cadasta XLSForm.** The choices entered on your import must match the choice options in the choice tab of the Cadasta XLSForm used to create your project. 
* **Columns match up.** The columns in both spreadsheets must be in the same order. 
* **The geography sections are formatted correctly.** [See one of our sample forms](https://docs.cadasta.org/en/09-XLSForms.html#types) for more information. 
* **All required fields are present.** Examples are `location_type` `party_name` and `tenure_type`. Again, [see one of our sample forms](https://docs.cadasta.org/en/09-XLSForms.html#types) for more information. 

If you're importing a CSV, also be sure to format `select_multiple` options with quotes around them, like this:

```
select_multiple: "optionA, optionB"
```
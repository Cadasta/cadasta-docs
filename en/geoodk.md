# Open Data Kit \(ODK\) Collect User Guide

Field data collection is an important part of the land and resource rights documentation process. The Cadasta Platform is designed to easily accommodate a variety of tools for data collection, allowing for ingestion of data. This guide will show you how to use ODK for data collection and to streamline the process of getting accurate geospatially enabled data into the platform.

ODK is a free, open source mobile data collection application for Android devices \(sorry Apple fans\). To get started, please [download ODK.](/ http://geomarvel-projects.s3.amazonaws.com/cadasta/collect-cadasta-dev.apk

## **Initial Setup**

If this is the first time you have used ODK with the Cadasta Platform, you will need to configure ODK for direct syncing with the  Platform. In order to do this, you will first need to setup your Cadasta account if you haven't already \(see getting started\).

1. Once you have installed ODK, please open the application.
2. Select **General Settings** from the home page using the menu key.

  ![](/assets/odk_homepage.png)

3. Now click **Configure Platform Settings**_._

  ![](/assets/odk_generalsettings_marked.png)

4. On this screen you will need to enter the necessary URL:
  1. http://platform.cadasta.org/collect \(if for production\); or
  2. http://demo.cadasta.org/collect  \(if for testing\)

5. Please also enter the Username and Password utilized with the Cadasta platform

6. Select the Back button two times to return to the ODK Main Menu.


Now ODK is configured for data collection that will feed directly to the Cadasta Platform.

## Loading your Form

Now we need to load the forms posted to the Cadasta Platform to the device.

1. Select **Get Blank Form** from the home page.

  ![](/assets/odk_homepage_getblankform2.png)

2. Enter the Cadasta Platform Username and Password if prompted.

3. Place a checkmark next to the form you would like to download and select **Get Selected**.

![](/assets/odk_get_forms.png)

## Data Collection

Now it’s time to collect some data!

1. From the ODK Main Menu select **Fill Blank Form**.

![](/assets/odk_homepage_fill_blank_form.png)

2. Select the relevant form for data collection
3. Swipe left twice to get started completing the form
4. Continue answering all the survey questions until you reach the "End of survey" message
5. Select **Mark Form as Finalized** checkbox
6. Click **Save Form and Exit**

![](/assets/odk_questionnaire_marked.png)

7. When ready to submit data \(via WiFi or over the mobile network\), click **Send Finalized Form**.

![](/assets/odk_send_form_marked.png)

8. After data is confirmed as sent, and you have received a confirmation message, the used form can be deleted.



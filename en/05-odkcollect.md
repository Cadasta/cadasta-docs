# Collecting Data with Open Data Kit \(ODK Collect\)

* [Overview](#overview)
* [Initial Setup](#initial-setup)
* [Loading Your Questionnaire](#loading-your-form)
* [Data Collection](#data-collection)
* [Uploading Data](#uploading-data)
* [Collecting Location Data: GeoTrace, GeoPoint and GeoShape](#geotracing)
* [Editing Data](#editing-data)
* [Deleting Questionnaires](#deleting-questionnaires)
* [GeoODK Troubleshooting](#geoodk-troubleshooting)


###Overview {#overview}

Field data collection is an important part of the land and resource rights documentation process. The Cadasta Platform is designed to easily accommodate a variety of tools for data collection, allowing for ingestion of data. One of those tools is Open Data Kit, or ODK Collect (which we refer to as ODK for short).

ODK is a free, open source mobile data collection application for Android devices \(sorry Apple fans\). To get started, please [download ODK Collect](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en) from the Google Play Store, or wherever you acquire your applications.

This guide will show you how to use ODK Collect for data collection and to streamline the process of getting accurate geospatially enabled data directly into the platform.

### Initial Setup {#initial-setup}

To get started, [download ODK from the Google Play Store](https://play.google.com/store/apps/details?id=com.geoodk.collect.android), or wherever you acquire your applications.

If this is the first time you've used ODK with the Cadasta Platform, you'll need to configure ODK for direct syncing. To do this, you'll need to set up your Cadasta account if you haven't already \(see [Getting Started](01-gettingstarted.md)\).

1. Once you've installed ODK, open the application.

2. From the opening screen (the Main Menu), tap the three dots in the upper right, then select **General Settings**, then **Configure Platform Settings**. 

    > new image 
    ![](/assets/geo-odk-1-configure-settings.png)

3. On this screen, enter the Platform URL along with your a username and password. The username and password do not have to be the same as they are on your Cadasta account, and the URL you need should be similar to the one you used when you signed up for your Cadasta account. 

    * https://platform.cadasta.org/collect \(if for active projects\); or

    * https://demo.cadasta.org/collect  \(if for testing\)

    > new image
    ![](/assets/geo-odk-2-url.png)

You now have an ODK account that's synced with the Cadasta Platform.

Click the back button twice to return to the main menu.

## Loading your Questionnaire {#loading-your-form}

Once you've connected ODK with Cadasta, the next thing you need to do is load the questionnaire you're using for your data collection project.


1. From the main menu, select **Get Blank Form**.

    >new image
    ![](/assets/odk_homepage_getblankform2.png)

2. At this stage, you may be asked to provide your Cadasta username and password. Enter this information and then wait a few minutes to be connected to the server.

    > add image

3. In the page that follows, you'll see a list of questionnaires that have been loaded for your organization's projects. Place a checkmark next to the form you would like to download and tap **Get Selected**.
    
    >new image
    ![](/assets/odk_get_forms2.png)

Now, ODK is configured to record data using the questions in your questionnaire.

## Data Collection

Now it’s time to collect some data!

1. From the ODK Main Menu select **Fill Blank Form**.

![](/assets/odk_homepage_fill_blank_form2.png)


2. Select the relevant form for data collection
3. Swipe left twice to get started completing the form
4. Continue answering all the survey questions until you reach the "End of survey" message
5. Select **Mark Form as Finalized** checkbox
6. Click **Save Form and Exit**


![](/assets/odk_questionnaire_marked2.png)

7. When ready to submit data \(via WiFi or over the mobile network\), click **Send Finalized Form**.

![](/assets/odk_send_form_marked2.png)

8. After data is confirmed as sent, and you have received a confirmation message, the used form can be deleted.



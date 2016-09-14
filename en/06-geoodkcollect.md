# Geographical Open Data Kit \(GeoODK\) Collect User Guide

* Overview [#overview]
* Initial Setup [#initial-setup]
* Loading Your Questionnaire[#loading-your-form]
* Data Collection[#data-collection]
* Uploading Data [#uploading-data]
* Editing Data [#editing-data]
* GeoODK Troubleshooting[#geoodk-troubleshooting]

###Overview {#overview}

Geographical Open Data Kit \(GeoODK\) is a data collection application for Android devices (unfortunately not yet available for Apple devices). Like ODK Collect, GeoODK can be used for data collection for projects in the Cadasta Platform. 

This section provides an overview of how GeoODK works with the Cadasta Platform. 

1. First, you'll [set up GeoODK](#initial-setup) on an Android device.
2. Then you'll [load the questionnaire](#loading-your-form) you want to use for data collection.
3. Finally, it's time to [collect your data](#data-collection)! 
4. When you're back to WiFi, [upload your data](#upload-data) to the Cadasta Platform.

**Important!** Steps 1, 2, and 4 require being near WiFi. You may also want to test step 3 before heading out into the field, just in case you need to make any changes. 

For more information and documentation about GeoODK generally, visit [geoodk.com](http://geoodk.com/).

### Initial Setup {#initial-setup}

To get started, [download GeoODK Collect from the Google Play Store](https://play.google.com/store/apps/details?id=com.geoodk.collect.android) or wherever you acquire your applications.

If this is the first time you've used GeoODK with the Cadasta Platform, you'll need to configure GeoODK for direct syncing. To do this, you'll need to set up your Cadasta account if you haven't already \(see [Getting Started](01-gettingstarted.md)\).

1. Once you've installed GeoODK, open the application.
2. From the map screen, hit the button with the four squares on the right. Then select **Settings** from the Main Menu, then **General Settings**, then **Configure Platform Settings**. 

    >insert image

3. On this screen, enter the Platform URL, along with your Cadasta Platform username and password.
    * https://platform.cadasta.org/collect \(if for active projects\); or
    * https://demo.cadasta.org/collect  \(if for testing\)

    > add image

GeoODK is now connected to your Cadasta account, and making it possible for your data collection to feed directly to the Cadasta Platform!

Click the back button 3 times to return to the main menu.

### Loading your Questionnaire {#loading-your-form}

Once you've connected GeoODK with your Cadasta account, the next thing you need to do is load the form you're using for your data collection project. 

1. From the Main Menu, select **Settings, then **Form Management**. 

    > add image

2. At this stage, you may be asked to provide your Cadasta username and password. Enter this information and then wait a few minutes to be connected to the server. _Having trouble with this step? See [GeoODK Troubleshooting](#geoodk-troubleshooting)._

    > add image

3. In the page that follows, you'll see a list of questionnaires that have been loaded for your organization's projects. Place a checkmark next to the form you would like to download and select **Get Selected**.

    > add image

Now, GeoODK is configured to ask questions in your questionnaire. 

### Data Collection {#data-collection}

Once you've initialized GeoODK and loaded your questionnaire, now it’s time to collect some data!

Specifically, you're recording location data. Each 

1. From the Main Menu select **Collect Data**, then the questionnaire that you want to use. 

    > add image

2. Swipe left twice to get started completing the form.
3. Continue answering all the survey questions until you reach the "End of survey" message. During this step, swipe left after the end of each question. 
    * During this section, you'll likely be asked to geotrace your data. For more information about how this works, see [Geotracing](#geotracing).
4. When all of your questions are completed, select the **Mark Form as finalized** checkbox and **Save Form and Exit**. 

    > add image

### Uploading Data {#uploading-data}

When you get 
7. When ready to submit data \(via WiFi or over the mobile network\), click **Send Data** and then confirm the form sending. 

![](/assets/geoodk_home_screen_send_data.png)

8. After data is confirmed as sent, and you have received a confirmation message, the used form can be deleted.

### Editing Data {#editing-data}

### Geotracing {#geotracing}

Automatic

Manual


click back to get out of the map and back to the questinnoinnaire. Notice GeoODK calls it a parcel regardless of what kind of location it is.


### GeoODK Troubleshooting {#geoodk-troubleshooting}

 

#### Loading Your Questionnaire

##### I can't connect to the Cadasta server because my username and password aren't working. (And yes, I've checked to make sure it's correct!)

The easiest thing to do here is to go to the Cadasta platform and change your password. Then, return to GeoODK and load your password there.  

##### I'm getting a message that says to "Wait a moment," but it's been more than a few moments.

> add image

If the above screen is taking longer than you think it should, hit Cancel. You may be correctly connected, or you may be asked to enter your username and password again. 






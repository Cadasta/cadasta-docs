# Collecting Data with Geographical Open Data Kit \(GeoODK\) 

* [Overview](#overview)
* [Initial Setup](#initial-setup)
* [Loading Your Questionnaire](#loading-your-form)
* [Data Collection](#data-collection)
* [Uploading Data](#uploading-data)
* [Editing Data](#editing-data)
* [Deleting Questionnaires](#deleting-questionnaires)
* [GeoODK Troubleshooting](#geoodk-troubleshooting)

###Overview {#overview}

Geographical Open Data Kit \(GeoODK\) is a data collection application for Android devices (unfortunately not yet available for Apple devices). Like ODK Collect, GeoODK can be used for data collection for projects in the Cadasta Platform. 

This section provides an overview of how GeoODK works with the Cadasta Platform. 

1. First, you'll [set up GeoODK](#initial-setup) on an Android device.
2. Then you'll [load the questionnaire](#loading-your-form) you want to use for data collection.
3. Finally, it's time to [collect your data](#data-collection)! 
4. When you're back to WiFi, [upload your data](#upload-data) to the Cadasta Platform.

**Important!** Steps 1, 2, and 4 require being near WiFi. You may also want to test step 3 before heading out into the field, just in case you need to [troubleshoot](#geoodk-troubleshooting) or make any changes. 

For more information and documentation about GeoODK generally, visit [geoodk.com](http://geoodk.com/).

### Initial Setup {#initial-setup}

To get started, [download GeoODK Collect from the Google Play Store](https://play.google.com/store/apps/details?id=com.geoodk.collect.android) or wherever you acquire your applications.

If this is the first time you've used GeoODK with the Cadasta Platform, you'll need to configure GeoODK for direct syncing. To do this, you'll need to set up your Cadasta account if you haven't already \(see [Getting Started](01-gettingstarted.md)\).

1. Once you've installed GeoODK, open the application.
2. From the map screen, hit the button with the four squares on the right. Then select **Settings** from the Main Menu, then **General Settings**, then **Configure Platform Settings**. 

    ![](/assets/geo-odk-1-configure-settings.png)

3. On this screen, enter the Platform URL, along with your Cadasta Platform username and password.
    * https://platform.cadasta.org/collect \(if for active projects\); or
    * https://demo.cadasta.org/collect  \(if for testing\)

    ![](/assets/geo-odk-2-url.png)

GeoODK is now connected to your Cadasta account, and making it possible for your data collection to feed directly to the Cadasta Platform!

Click the back button 3 times to return to the main menu.

### Loading your Questionnaire {#loading-your-form}

Once you've connected GeoODK with your Cadasta account, the next thing you need to do is load the form you're using for your data collection project. 

1. From the Main Menu, select **Settings, then **Form Management**. 

    ![](/assets/geo-odk-3-form-management.png)

2. At this stage, you may be asked to provide your Cadasta username and password. Enter this information and then wait a few minutes to be connected to the server. _Having trouble with this step? See [GeoODK Troubleshooting](#geoodk-troubleshooting)._

    ![](/assets/geo-odk-4-user-pass.png)

3. In the page that follows, you'll see a list of questionnaires that have been loaded for your organization's projects. Place a checkmark next to the form you would like to download and select **Get Selected**.

    ![](/assets/geo-odk-5-questionnaire-list.png)

Now, GeoODK is configured to ask questions in your questionnaire. 

### Data Collection {#data-collection}

Once you've initialized GeoODK and loaded your questionnaire, now it’s time to collect some data!

Specifically, you're recording location data. Each 

1. From the Main Menu select **Collect Data**, then the questionnaire that you want to use. 

    ![](/assets/geo-odk-6-collect-data.png)

2. Swipe left twice to get started completing the form.
3. Continue answering all the survey questions until you reach the "End of survey" message. During this step, swipe left after the end of each question. 
    * During this section, you'll likely be asked to geotrace your data. For more information about how this works, see [Geotracing](#geotracing).
4. When all of your questions are completed, select the **Mark Form as finalized** checkbox and **Save Form and Exit**. 

    ![](/assets/geo-odk-7-finalized-form.png)

### Uploading Data {#uploading-data}

When you get back to WiFi or a mobile network, you can upload your completed questionnaires to Cadasta. 

From the main menu, click **Send Data** and then check off all the forms that you want to upload (using the **Toggle All** button to select all questionnaires). Then select **Send Selected**.

![](/assets/geo-odk-8-send-data.png)

Next, you'll get a confirmation message confirming that the data has been sent. 

![](/assets/geo-odk-9-confirmation.png)

It's also a good idea to confirm that you see the data on the Cadasta Platform, and then [delete any completed questionnaires](#deleting-questionnaires) from your Android device.

### Editing Data {#editing-data}

GeoODK makes editing your forms relatively easy. From the main menu, select **Edit Data**, then the form you want to edit. When you're done, save your changes.

### Deleting Questionnaires {#deleting-questionnaires}

You can easily delete unwanted questionnaires by selecting **Delete Data** from the main menu. On the page that follows, you can toggle between Saved Forms and Blank Forms to delete either one. 

### Geotracing {#geotracing}

During [data-collection](#data-collection), you'll be asked to geotrace a location. Using GPS data from your Android device, geotracing follows your specific location and then records it in GeoODK. You can use geotracing to walk the perimeter of a building (creating a polygon), walk along a river or road (creating a line), or drop a pin directly where you're standing (creating a point).

To start geotracing, hit the Play button in the upper right:

![](/assets/geo-odk-geotrace-1-play.png)

From there, you'll be asked to select either Automatic or Manual mode. 

![](/assets/geo-odk-geotrace-2-manual-automatic.png)

**Manual mode** allows you to record your geotrace manually. Every time you want to drop a pin, click the **Record Location Point** button at the top of the map.

![](/assets/geo-odk-geotrace-3-record-location-point.png)

**Automatic mode** records your location at set intervals, such as once every 20 seconds. This mode is helpful if you're recording a large amount of space. 

> Kate: please check the suggested interval times below.

The amount of time you should set for your interval depends on how you're collecting the data. For example, if you're driving, you may want to set the interval to be once every 5 seconds. If you're walking, you may want to record once every 20-30 seconds. 

Automatic mode also lets you collect a point manually if you need to. For example, if you're automatically geotracing a rectangular plot of land, be sure to pause and record your location at each corner to ensure they are recorded.

For either automatic or manual mode, keep in mind that the more points you record, the bigger your data file will be and the harder it will be to upload when you return to WiFi or you mobile network.

When you're done geotracing, hit the pause button. You'll then be asked to save your information as a polyline or polygon.

![](/assets/geo-odk-geotrace-4-save-geotrace.png)

If you've recording a point or line, choose polyline. If you've recording an area and created a closed shape, choose polygon.

Finally, you'll be brought to a confirmation screen where you can view your geotrace. 

![](/assets/geo-odk-geotrace-5-confirmation.png)

Note that GeoODK calls a geotrace a parcel regardless of what kind of location it is.

### GeoODK Troubleshooting {#geoodk-troubleshooting}

If you're having trouble using GeoODK, the answer to your question may be here. If not, please [contact us](cadasta.org/contact/) and we'll do our best to help you work through the issue.

#### Loading Your Questionnaire

##### I can't connect to the Cadasta server because my username and password aren't working. (And yes, I've checked to make sure it's correct!)

The easiest thing to do here is to go to the Cadasta platform and change your password. Then, return to GeoODK and load your password there.  

##### I'm getting a message that says to "Wait a moment," but it's been more than a few moments.

![](/assets/geo-odk-error-1-wait-a-moment-forever.png)

If the above screen is taking longer than you think it should, hit Cancel. You may be correctly connected, or you may be asked to enter your username and password again. 

#### Uploading Completed Questionnaires

##### I'm getting an error when I upload my completed questoinnaires.

> Kate, see below. I got this error and then this is how I fixed it.

If you're having trouble uploading your questionnaires, the most likely culprit is collecting data using a questionnaire that doesn't exactly match the questionnaire loaded on the Cadasta Platform. This can happen if you modify your questionnaire, load it to Cadasta, and then continue collecting data using an older version. 

Unfortunately, the easiest way to fix this is to uninstall the old form and completed questionnaire and start over. This is why we recommend that you test GeoODK before heading out into the field. 

If you've collected too much data to start over, please [contact us](cadasta.org/contact/). 



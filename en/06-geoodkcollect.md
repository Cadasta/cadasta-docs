# Collecting Data with GeoODK Collect (Geographical Open Data Kit) 

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

Geographical Open Data Kit \(GeoODK Collect\) is a data collection application for Android devices (unfortunately not yet available for Apple devices). Like Open Data Kit (ODK Collect), GeoODK can be used for data collection projects in the Cadasta Platform. 

This section provides an overview of how GeoODK and Cadasta work together:

1. First, you'll [set up GeoODK](#initial-setup) on an Android device.
2. Then you'll [load the questionnaire](#loading-your-form) you want to use for data collection.
3. Finally, it's time to [collect your data](#data-collection)! 
4. When you're back to WiFi, [upload your data](#upload-data) to the Cadasta Platform.

**Important!** Steps 1, 2, and 4 require being near WiFi. You may also want to test step 3 before heading out into the field, just in case you need to [troubleshoot](#geoodk-troubleshooting) or make any changes. 

For more information and documentation about GeoODK generally, visit [geoodk.com](http://geoodk.com/).

### Initial Setup {#initial-setup}

To get started, [download GeoODK from the Google Play Store](https://play.google.com/store/apps/details?id=com.geoodk.collect.android), or wherever you acquire your applications.

If this is the first time you've used GeoODK with the Cadasta Platform, you'll need to configure GeoODK for direct syncing. To do this, you'll need to set up your Cadasta account if you haven't already \(see [Getting Started](01-gettingstarted.md)\).

1. Once you've installed GeoODK, open the application.
2. From the map screen, hit the button with the four squares on the right. Then select **Settings** from the Main Menu, then **General Settings**, then **Configure Platform Settings**. 

    ![](/assets/geo-odk-1-configure-settings.png)

3. On this screen, enter the Platform URL along with your a username and password. The username and password do not have to be the same as they are on your Cadasta account, and the URL you need should be similar to the one you used when you signed up for your Cadasta account. 
    * https://platform.cadasta.org/collect \(if for active projects\); or
    * https://demo.cadasta.org/collect  \(if for testing\)

    ![](/assets/geo-odk-2-url.png)

You now have a GeoODK account that's synced with the Cadasta Platform.

Click the back button 3 times to return to the main menu.

### Loading your Questionnaire {#loading-your-form}

Once you've connected GeoODK with Cadasta, the next thing you need to do is load the questionnaire you're using for your data collection project. 

1. From the Main Menu, select **Settings**, then **Form Management**. 

    ![](/assets/geo-odk-3-form-management.png)

2. At this stage, you may be asked to provide your Cadasta username and password. Enter this information and then wait a few minutes to be connected to the server. _Having trouble with this step? See [GeoODK Troubleshooting](#geoodk-troubleshooting)._

    ![](/assets/geo-odk-4-user-pass.png)

3. In the page that follows, you'll see a list of questionnaires that have been loaded for your organization's projects. Place a checkmark next to the form you would like to download and tap **Get Selected**.

    ![](/assets/geo-odk-5-questionnaire-list.png)

Now, GeoODK is configured to record data using the questions in your questionnaire. 

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

### Collecting Location Data: GeoTrace, GeoShape, and GeoPoint {#geotracing}

During [data-collection](#data-collection), you'll be asked to collect data specifying your location using one of the following options:

* **GeoTrace** creates lines, collections of two or more GPS coordinates. It's also the default option provided in both the standard and minimal questionnaires. 

* **GeoShape** creates polygons, or closed shapes. To create a geoshape, you need to end your shape on the same point where you started. Using this feature, you can either draw or walk to create your shape.

* **GeoPoint** creates points, or single GPS coordinates. 

To learn more about how to configure these options in your questionnaire, see the [Questionnaires & Custom Data Collection](XLSForms.md).

#### GeoTrace

To start geotracing, hit the Play button in the upper left:

![](/assets/geo-odk-geotrace-1-play.png)

From there, you'll be asked to select either Automatic or Manual mode. 

![](/assets/geo-odk-geotrace-2-manual-automatic.png)

**Manual mode** allows you to record your geotrace manually. Every time you want to drop a pin, click the **Record Location Point** button at the top of the map.

![](/assets/geo-odk-geotrace-3-record-location-point.png)

**Automatic mode** records your location at set intervals, such as once every 20 seconds. This mode is helpful if you're recording a large amount of space. 

The amount of time you should set for your interval depends on how you're collecting the data. For example, if you're driving, you may want to set the interval to be once every 5 seconds. If you're walking, you may want to record once every 20-30 seconds. 

If you know you need to record the corners of a large area, then you might want to try manual mode. Or, if you're using automatic mode, pause on the corner long enough for the pin to drop. Alternatively, in automatic mode, you can also select Record Location Point to manually drop a pin.

For either automatic or manual mode, keep in mind that the more points you record, the bigger your data file will be and the harder it will be to upload when you return to WiFi or you mobile network. Collect all the points you need - and only the points you need!

When you're done geotracing, hit the pause button. You'll then be asked to save your information as a polyline or polygon.

![](/assets/geo-odk-geotrace-4-save-geotrace.png)

If you've recording a point or line, choose polyline. If you've recording an area and created a closed shape, choose polygon.

Finally, you'll be brought to a confirmation screen where you can view your geotrace. 

![](/assets/geo-odk-geotrace-5-confirmation.png)

Note that GeoODK calls a geotrace a parcel regardless of what kind of location it is.

#### GeoShape

> Note: I don't have this working on my phone. Please check for accuracy!

GeoShape is designed for making shapes on a location. For example, you can use Geoshape to draw a boundary around a building or land area. 

![](/assets/geo-odk-geoshape-1.png)

You can collect location data with GeoShape comes in two ways: by walking around an area, or by drawing it on the map. Before collecting data, you'll be prompted to either draw your coordinates on the map, or walk around the boundaries.

![](/assets/geo-odk-geoshape-2.png)

If you choose walking mode, you can use either the automatic or manual mode as described in the GeoTrace section. 

#### GeoPoint

> Note: I don't have this working on my phone. Please check for accuracy!

You'll use GeoPoint to collect single GPS coordinates

First you'll come to a screen asking you to record the location of your parcel. Click **Record Location**. 

![](/assets/geoodk-geopoint-1.png)

In the screen that follows, you'll see a map with your location. To save your pin location, hit the **Save** icon in the upper left. Also note the GPS accuracy logged at the top of the screen. 

![](/assets/geoodk-geopoint-2.png)

When you're done, you'll come to a screen that looks like the one below. You can use this screen to view or edit your recording.

![](/assets/geoodk-geopoint-3.png)


### Uploading Data {#uploading-data}

When you get back to WiFi or a mobile network, you can upload your completed questionnaires to the Cadasta Platform. 

From the main menu, click **Send Data** and then check off all the forms that you want to upload (using the **Toggle All** button to select all questionnaires). Then select **Send Selected**.

![](/assets/geo-odk-8-send-data.png)

Next, you'll get a confirmation message confirming that the data has been sent. 

![](/assets/geo-odk-9-confirmation.png)

It's also a good idea to confirm that you see the data on the Cadasta Platform, and then [delete any completed questionnaires](#deleting-questionnaires) from your Android device.

### Editing Data {#editing-data}

GeoODK makes editing your forms relatively easy. From the main menu, select **Edit Data**, then the form you want to edit. When you're done, save your changes.

### Deleting Questionnaires {#deleting-questionnaires}

You can also easily delete unwanted questionnaires by selecting **Delete Data** from the main menu. On the page that follows, you can toggle between Saved Forms and Blank Forms to delete either one. 


### GeoODK Troubleshooting {#geoodk-troubleshooting}

If you're having trouble using GeoODK, the answer to your question may be here. If not, please [contact us](cadasta.org/contact/) and we'll do our best to help you work through the issue.

#### Trouble Loading Your Questionnaire

##### I can't connect to the Cadasta server because my username and password aren't working. (And yes, I've checked to make sure they're correct!)

The easiest thing to do here is to go to the Cadasta platform and change your password. Then, return to GeoODK and load your password there.  

##### I'm getting a message that says to "Please wait a few moments," but it's been much much longer than that.

![](/assets/geo-odk-error-1-wait-a-moment-forever.png)

If the above screen is taking longer than you think it should, hit Cancel. You may be correctly connected, or you may be asked to enter your username and password again. 

#### Trouble Uploading Completed Questionnaires

##### I'm getting an error when I upload my completed questoinnaires.

If you're having trouble uploading your questionnaires, the most likely culprit is collecting data using a questionnaire that doesn't exactly match the questionnaire loaded on the Cadasta Platform. This can happen if you modify your questionnaire, load it to Cadasta, and then continue collecting data using an older version. 

Unfortunately, the easiest way to fix this is to uninstall the old form and completed questionnaire and start over. This is why we recommend that you test GeoODK before heading out into the field. We also recommend refreshing your questionnaire before heading out to the field if you think that it might have changed. 

If you've collected too much data to start over, please [contact us](cadasta.org/contact/). 



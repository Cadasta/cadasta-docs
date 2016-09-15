# Collecting Data with Open Data Kit \(ODK Collect\)

* [Overview](#overview)
* [Initial Setup](#initial-setup)
* [Loading Your Questionnaire](#loading-your-form)
* [Data Collection](#data-collection)
* [Uploading Data](#uploading-data)
* [Collecting Location Data: GeoTrace, GeoPoint and GeoShape](#geotracing)
* [Editing Data](#editing-data)
* [Deleting Questionnaires](#deleting-questionnaires)


###Overview {#overview}

Field data collection is an important part of the land and resource rights documentation process. The Cadasta Platform is designed to easily accommodate a variety of tools for data collection, allowing for ingestion of data. One of those tools is Open Data Kit, or ODK Collect (which we refer to as ODK for short).

ODK is a free, open source mobile data collection application for Android devices \(sorry Apple fans\). To get started, please [download ODK Collect](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en) from the Google Play Store, or wherever you acquire your applications.

This section provides an overview of how ODK and Cadasta work together:

1. First, you'll [set up ODK](#initial-setup) on an Android device.
2. Then you'll [load the questionnaire](#loading-your-form) you want to use for data collection.
3. Finally, it's time to [collect your data](#data-collection)! 
4. When you're back to WiFi, [upload your data](#upload-data) to the Cadasta Platform.

**Important!** Steps 1, 2, and 4 require being near WiFi. You may also want to test step 3 before heading out into the field, just in case you need to troubleshoot or make any changes. 

For more information and documentation about GeoODK generally, visit [geoodk.com](http://geoodk.com/).


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

### Loading your Questionnaire {#loading-your-form}

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

### Data Collection {#data-collection}

Once you've initialized GeoODK and loaded your questionnaire, now it’s time to collect some data!

1. From the ODK Main Menu select **Fill Blank Form**, then the questionnaire that you want to use. 

    >new image
    ![](/assets/odk_homepage_fill_blank_form2.png)

2. Swipe left twice to get started completing the form
3. Continue answering all the survey questions until you reach the "End of survey" message. During this step, swipe left after the end of each question. 
    * During this section, you'll likely be asked to GeoTrace your location data, or add a GeoShape or GeoPoint. For more information about how this works, see [Collecting Location Data: GeoTrace, GeoPoint and GeoShape](#geotracing).
4. When all of your questions are completed, select the **Mark Form as finalized** checkbox and **Save Form and Exit**. 

    >new image
    ![](/assets/geo-odk-7-finalized-form.png)

### Collecting Location Data: GeoTrace, GeoShape, and GeoPoint {#geotracing}

> This information to be updated with 9.19 release

During [data-collection](#data-collection), you'll be asked to collect data specifying your location using one of the following options.

* **GeoTrace** creates lines, collections of two or more GPS coordinates. It's also the default option provided in both the standard and minimal questionnaires. 

* **GeoShape** creates polygons, or closed shapes. To create a geoshape, you need to end your shape on the same point where you started. Using this feature, you can either draw or walk to create your shape.

* **GeoPoint** creates points, or single GPS coordinates. 

To learn more about how to configure these options in your questionnaire, see the [Questionnaires & Custom Data Collection](XLSForms.md).

#### GeoTrace

To start geotracing, hit the Play button in the upper left:

> add image with 9.19 release

From there, you'll be asked to select either Automatic or Manual mode. 

> add image with 9.19 release

**Manual mode** allows you to record your geotrace manually. Every time you want to drop a pin, click the **Record Location Point** button at the top of the map.

> add image with 9.19 release

**Automatic mode** records your location at set intervals, such as once every 20 seconds. This mode is helpful if you're recording a large amount of space. 

The amount of time you should set for your interval depends on how you're collecting the data. For example, if you're driving, you may want to set the interval to be once every 5 seconds. If you're walking, you may want to record once every 20-30 seconds. 

If you know you need to record the corners of a large area, then you might want to try manual mode. Or, if you're using automatic mode, pause on the corner long enough for the pin to drop. Alternatively, in automatic mode, you can also select Record Location Point to manually drop a pin.

For either automatic or manual mode, keep in mind that the more points you record, the bigger your data file will be and the harder it will be to upload when you return to WiFi or you mobile network. Collect all the points you need - and only the points you need!

When you're done geotracing, hit the pause button. You'll then be asked to save your information as a polyline or polygon.

> add image with 9.19 release 

If you've recording a point or line, choose polyline. If you've recording an area and created a closed shape, choose polygon.

Finally, you'll be brought to a confirmation screen where you can view your geotrace. 

> add image with 9.19 release

Note that GeoODK calls a geotrace a parcel regardless of what kind of location it is.

#### GeoShape

> add more info with 9.19 release

GeoShape is designed for making shapes on a location. For example, you can use Geoshape to draw a boundary around a building or land area. 


> add image with 9.19 release

You can collect location data with GeoShape comes in two ways: by walking around an area, or by drawing it on the map. Before collecting data, you'll be prompted to either draw your coordinates on the map, or walk around the boundaries.

![](/assets/geo-odk-geoshape-2.png)

If you choose walking mode, you can use either the automatic or manual mode as described in the GeoTrace section. 

#### GeoPoint

> Add info with 9.19 release


###Uploading Data {#uploading-data}

When you get back to WiFi or a mobile network, you can upload your completed questionnaires to the Cadasta Platform. 

From the main menu, click **Send Finalized Form** and then check off all the forms that you want to upload (using the **Toggle All** button to select all questionnaires). Then select **Send Selected**.

> add image: send finalized form

Finally, you'll get a confirmation message confirming that the data has been sent. 

It's also a good idea to confirm that you see the data on the Cadasta Platform, and then [delete any completed questionnaires](#deleting-questionnaires) from your Android device.

### Editing Data {#editing-data}

GeoODK makes editing your forms relatively easy. From the main menu, select **Edit Data**, then the form you want to edit. When you're done, save your changes.

### Deleting Questionnaires {#deleting-questionnaires}

You can also easily delete unwanted questionnaires by selecting **Delete Data** from the main menu. On the page that follows, you can toggle between Saved Forms and Blank Forms to delete either one. 

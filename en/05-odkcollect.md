# Collecting Data with ODK Collect (Open Data Kit) 

* [Overview](#overview)
* [Initial Setup](#initial-setup)
* [Loading Your Cadasta XLSForm](#loading-your-form)
* [Data Collection](#data-collection)
* [Uploading Data](#uploading-data)
* [Collecting Location Data: GeoTrace, GeoPoint and GeoShape](#geotracing)
* [Editing Data](#editing-data)
* [Deleting Forms](#deleting-questionnaires)
* [ODK Troubleshooting](#odk-troubleshooting)


##Overview {#overview}

Field data collection is an important part of the land and resource rights documentation process. The Cadasta Platform is designed to accommodate a couple of tools for data collection, allowing for ingestion of data. One of those tools is Open Data Kit, or ODK Collect (which we refer to as ODK for short).

ODK is a free, open source mobile data collection application for Android devices \(sorry Apple fans\). To get started, [download ODK Collect from the Google Play Store](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en), or wherever you acquire your applications.

This section provides an overview of how ODK and Cadasta work together:

1. First, you'll [set up ODK](#initial-setup) on an Android device.
2. Then you'll [load the Cadasta XLSForm](#loading-your-form) you want to use for data collection.
3. Finally, it's time to [collect your data](#data-collection)! 
4. When you're back to WiFi, [upload your data](#uploading-data) to the Cadasta Platform.

**Important!** Steps 1, 2, and 4 require being near WiFi. You may also want to test step 3 before heading out into the field, just in case you need to [troubleshoot](#odk-troubleshooting) or make any changes. 

For more information and documentation about ODK generally, visit [opendatakit.org](https://opendatakit.org/).

## Initial Setup {#initial-setup}

_**Note:** This step requires being near WiFi!_

To get started, [download ODK from the Google Play Store](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en), or wherever you acquire your applications.

If this is the first time you've used ODK with the Cadasta Platform, you'll need to configure ODK for direct syncing. To do this, you'll need to set up your Cadasta account if you haven't already \(see [Getting Started](01-gettingstarted.md)\).

1. Once you've created your account and installed ODK, open the application.

2. From the opening screen (the Main Menu), tap the **three dots**  in the upper right, then select **General Settings**, then **Server**. 

    ![](/assets/new-odk-01.png)

3. On this screen, enter you'll need to change some settings. Change the `Type` field to `Other`. Then you'll need to enter a specific URL: 

    * https://platform.cadasta.org/collect \(if for active projects\); or

    * https://demo.cadasta.org/collect  \(if for testing\)

    ![](/assets/new-odk-02.png)

_**Important!** Notice the `s` at the end of `https` in the URLs above. That's an important part of our URLs! Forgetting it will produce an error. `https` provides authentication of the website and associated web server, meaning that the information being sent and received is more secure than it would be as just `http`. <a href="https://en.wikipedia.org/wiki/HTTPS" target="_blank">Read more.</a> _
Here, you'll also want to enter your Cadasta username and password. This will connect you to your Cadasta account, where you can access your questionnaires for data collection.


Click the back button twice to return to the main menu.

## Loading your Cadasta XLSForms {#loading-your-form}

_**Note:** This step requires being near WiFi!_

Once you've connected ODK with Cadasta, the next thing you need to do is load the forms you're using for your data collection project.

1. From the main menu, select **Get Blank Form**.

    ![](/assets/new-odk-03.png)

2. At this stage, you may be asked to provide your Cadasta username and password. Enter this information and then wait a few moments to be connected to the server.

3. In the page that follows, you'll see a list of questionnaires that have been loaded for your organization's projects. Place a checkmark next to the form you'd like to use and tap **Get Selected**.

Now, ODK is configured to record data using the questions in your form. You can select which form you want to use in a later step.

## Data Collection {#data-collection}

Once you've initialized ODK and loaded your Cadasta XLSForm, now it’s time to collect some data!

For this step, make sure that GPS is enabled on your device and turned on.

1. From the ODK Main Menu select **Fill Blank Form** then the form that you want to use. 

    ![](/assets/new-odk-04.png)

2. Swipe left twice to get started completing the form. 

	![](/assets/new-odk-05.png)

3. Continue answering all the survey questions until you reach the "End of survey" message. During this step, swipe left after you've answered each question. 
    * During this section, you'll likely be asked to GeoTrace your location data, or add a GeoShape or GeoPoint. For more information about how this works, see [Collecting Location Data: GeoTrace, GeoPoint and GeoShape](#geotracing).
4. When all of your questions are completed, select the **Mark Form as finalized** checkbox and **Save Form and Exit**. 

###Collecting Data in Multiple Languages

If you need to collect data in multiple languages, you can set it up in your Cadasta XLSform. _[Learn how.](09-XLSForms.md)_

Once you've chosen your default language and set up your questions in all the languages you need, you'll be able to toggle between the languages during data collection. Select the **More actions** button in the upper right, then **Change Language**, then the language of your choice. 

![](/assets/multi-lang-odk.png)


##Collecting Location Data: GeoTrace, GeoShape, and GeoPoint {#geotracing}

During [data collection](#data-collection), you'll be asked to collect data specifying your location using one of the following options.

![](/assets/new-odk-geoshape-geotrace-geopoint.png)

* **[GeoTrace](#geotrace)** gives you the option of creating polylines or polygons based on your location. In other words, you can use GeoTrace to walk an area, using automatic or manual mode. GeoTrace is the default option provided. _**Important!** If you get to the screen below, be sure to select the Polygon option if you are trying to map an enclosed area._

![](/assets/geo-odk-10-polyline-polygon.png)

* **[GeoShape](#geoshape)** creates polygons (closed shapes). To create a GeoShape, you can use your finger to draw a shape on the map.  

* **[GeoPoint](#geopoint)** creates points (single GPS coordinates) based on your location. 

### GeoTrace {#geotrace}

![](/assets/new-odk-geotrace.png)

When it's time to start your GeoTrace, you'll be prompted to **Start GeoTrace**.

In the next screen, you'll be asked to **Zoom to Current Location**.

![](/assets/odk-geotrace-2.png)

Once your location is identified, you'll be asked to select either Automatic or Manual mode.  

![](/assets/odk-geotrace-3.png)

**Manual mode** allows you to record your geotrace manually. Every time you want to drop a pin, click the **Record Location Point** button at the top of the map. For example, it's common practice to drop pins at each corner of a location. 

![](/assets/odk-geotrace-5.png)

**Automatic mode** records your location at set intervals, for example once every 20 seconds. This mode is helpful if you're recording a large area. 

The amount of time you should set for your interval depends on how you're collecting the data. For example, if you're driving, you may want to set the interval to be once every 5 seconds. If you're walking, you may want to record once every 20-30 seconds. 

If you know you need to record the corners of a large area, then you might want to try manual mode. Or, if you're using automatic mode, pause on the corner long enough for the pin to drop. Alternatively, in automatic mode, you can also use the **Record Location Point** button to manually drop a pin.

For either automatic or manual mode, keep in mind that the more points you record, the bigger your data file will be and the harder it will be to upload when you return to WiFi or you mobile network. Collect all the points you need - and only the points you need!

![](/assets/odk-geotrace-4.png)

When you're done with your GeoTrace, hit the pause button. You'll then be asked to save your information as a polyline or polygon.

If you've recording a point or line, choose polyline. If you've recording an area and created a closed shape, choose polygon.

Finally, you'll be brought to a confirmation screen where you can view your GeoTrace. 

_Note that ODK calls a geotrace a parcel regardless of what kind of location it is._

### GeoShape {#geoshape}

GeoShape is designed for making shapes (or polygons) to represent a specific location. For example, you can use GeoShape to draw a boundary around a building or land area. 

![](/assets/new-odk-geoshape.png)

If you're collecting data using GeoShape, you'll first be asked to zoom to your current location or to a saved feature. 

![](/assets/odk-geoshape-1.png)

In the next screen, you'll be able to start making your shape. Press the screen to place markers around your location, and notice the red lines that are created between each marker. To close your polygon, press on the same point where the polygon began.

![](/assets/odk-geoshape-2.png)

When you're ready to save your GeoShape, hit the **Save** icon on the right. If you wish to discard it, you can also hit the **Trash** button above it.

### GeoPoint {#geopoint}

To collect single GPS coordinates, you can use GeoPoint. GeoPoint only works by tracking your specific location (drawing with your finger is not available).

![](/assets/new-odk-geopoint.png)

When it's time to collect your GeoPoint, it will first load your location. This may take a few minutes. 

![](/assets/odk-geopoint-1.png)

Next it will give you some GPS accuracy information. Here, the accuracy is within a 24-meter radius of where the user is standing. 

![](/assets/odk-geopoint-2.png)

Once the location and accuracy information is loaded, you're ready to save your GeoPoint.

![](/assets/odk-geopoint-3.png)

##Uploading Data {#uploading-data}

When you get back to WiFi or a mobile network, you can upload your completed forms to the Cadasta Platform. 

From the main menu, click **Send Finalized Form** and then check off all the forms that you want to upload (use the **Toggle All** button to select all forms). Then select **Send Selected**.

![](/assets/new-odk-06.png)

Finally, you'll get a confirmation message confirming that the data has been sent. 

It's a good idea to confirm that you see the data on the Cadasta Platform. Then you can [delete any completed XLSForms](#deleting-questionnaires) from your Android device.

## Editing Data {#editing-data}

ODK makes editing your forms relatively easy. From the main menu, select **Edit Data**, then the form you want to edit. When you're done, save your changes.

## Deleting Cadasta XLSForms {#deleting-questionnaires}

You can also delete unwanted forms by selecting **Delete Data** from the main menu. On the page that follows, you can toggle between Saved Forms and Blank Forms to delete either one. 

## ODK Troubleshooting {#odk-troubleshooting}

If you're having trouble using ODK, the answer to your question may be here. If not, please [contact us](http://cadasta.org/contact/) and we'll do our best to help you work through the issue.

### Trouble Loading Your Cadasta XLSForm

##### ISSUE: I can't connect to the Cadasta server because my username and password aren't working. (And yes, I've checked to make sure they're correct!)

The easiest thing to do here is to go to the Cadasta platform and change your password. Then, return to ODK and enter your new password there.  

##### ISSUE: I'm getting a message that says to "Please wait a few moments," but it's been much much longer than that.

If the above screen is taking longer than you think it should, hit Cancel. You may be correctly connected, or you may be asked to enter your username and password again.

##### ISSUE: I'm getting an error that my file is too big. 

ODK cannot upload files that are bigger than 10 MB. Usually, the culprit is a high-resolution photograph. To resolve the issue, find the photograph (or other large file), remove it, and re-attach it with a lower-resolution version. 

### Difficulty Adding Location Data

##### ISSUE: ODK won't let me add any location data. 

![](/assets/odk-trouble-1.png)

If you get the screen like the one above, unfortunately it's a known (and frustrating!) bug. Cadasta is aware that some Android devices simply refuse to log their GPS data with ODK. Our team is working to resolve the issue.

In the meantime, here are some alternatives:

1. Try using another Android device. This mysterious bug does not appear on all of them.
2. Try using GeoODK, which works very similarly to ODK. _[Learn more about how to use GeoODK with Cadasta](06-odkcollect.md)._

# Using External Antennas with ODK:

### Trimble Catalyst Set-Up:

![](/assets/catalyst/catalyst.png)

Let’s walk through how to set it up… 

What you will need to get started:
1. An Android smartphone or tablet that has a data plan (this is a potential weakness of the Trimble device - GPS corrections require an available network, which isn’t always possible in remote areas);
2. A Trimble Catalyst antenna;

![](/assets/catalyst/2m-accuracy.png)

3. The Trimble Catalyst and Trimble Mobile Manager application (which can be downloaded from the Google Play Store);
4. Your own Trimble account; 
5. Enabled “Developer Tools” on the Android device to change the phone from using the native GPS receiver to using the Catalyst device. (You can enable developer tools on your Android by going to Settings > About phone > Build. Click “Build” seven times and the developer mode will be enabled.); and
6. (Optional) A rod/tripod to mount the antenna for stability/accuracy.  
7. (Optional) An extra battery or power bank for your phone as the Catalyst can quickly drain a phone battery.

How to Use the Catalyst with OpenDataKit:

Open the Trimble Mobile Manager application to log in to the Trimble Catalyst app. This app is used to manage the antennae and the Catalyst subscription.

Plug the Catalyst into USB charger/accessory port of your phone and wait for the Catalyst to pick up the satellites. The satellite icon will appear green (as shown below) when coverage is sufficient. 

![](/assets/catalyst/developer-options-3.png)

Now for the trickiest part, click the “Setup” section in the app to view the instructions that describes how you can reprogram your phone to read the Catalyst coordinates instead of the smart phone receiver. This is when you will need to have the Developer Options enabled. 

![](/assets/catalyst/developer-options-2.png)

To do so, you need to start by going to “Settings”, scroll down to “System”, click on “Developer Options” and scroll down until you find “Select mock location app”.  Once clicked, you should see “Trimble Mobile Manager” listed. 

![](/assets/catalyst/developer-options-3.png)

Choose that option so that ODK can use the Catalyst to collect two to three meter accuracy.

![](/assets/catalyst/2m-accuracy.png)


And finally, start mapping!

You will know if it is working by the Catalyst icon on the top of your screen and when you collect a point with ODK Collect and see that you have two meter accuracy!  Woot woot!

##### Troubleshooting:
1. When first connecting with satellites, you need to be outside with a clear view of the sky. Once the satellites are engaged, you can work under canopies or in between buildings.
2. Subscribe before you set-up. You cannot change your subscription settings from the app so we recommend that you subscribe before you going into the field. 
3. Make sure your phone is sufficiently connected to data. The centimeter level accuracy only works when you have cellular data. 
4. Make sure you are using the correct type of phone. The Catalyst, like ODK Collect and GeoODK, is only supported on Androids.




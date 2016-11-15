# Mengumpulkan Data dengan GeoODK Collect (Geographical Open Data Kit) 

* [Ringkasan](#overview)
* [Pemasangan Awal](#initial-setup)
* [Memuat Kuesioner Anda](#loading-your-form)
* [Pengumpulan Data](#data-collection)
* [Mengupload Data](#uploading-data)
* [Mengumpulkan Data Lokasi : GeoTrace, GeoPoint and GeoShape](#geotracing)
* [Mengubah Data](#editing-data)
* [Menghapus Kuesioner](#deleting-questionnaires)
* [GPenyelesaian Masalah GeoODK](#geoodk-troubleshooting)

###Overview {#overview}

Geographical Open Data Kit \(GeoODK Collect\) adalah aplikasi pengumpulan data untuk perangkat Android (sayangnya belum tersedia untuk perangkat Apple). Seperti Open Data Kit (ODK Collect), GeoODK dapat digunakan untuk proyek pengumpulan data di Platform Cadasta. 

Bagian ini menjelaskan secara ringkat bagaimana GeoODK dan Cadasta dapat bekerja sama: 

1. Pertama, Anda perlu [memasang GeoODK](#initial-setup) pada sebuah perangkat Android.
2. Kemudian Anda akan [memuat kuesioner](#loading-your-form) yang Anda inginkan untuk pengumpulan data. 
3. Terakhir, saatnya untuk [mengumpulkan data Anda](#data-collection)! 
4. Ketika Anda sudah memiliki jaringan WiFi, [upload data Anda](#uploading-data) ke Platform Cadasta.

**Penting!** Langkah 1, 2, dan 4 membutuhkan jaringan WiFi. Anda juga mungkin ingin melakukan ujio coba langkah ke-3 sebelum keluar lapangan, untuk menjaga apabila Anda perlu [menyelesaikan masalah](#geoodk-troubleshooting) atau membuat perubahan. 

Untuk informasi dan dokumentasi terkait GeoODK secara umum, kunjungi [geoodk.com](http://geoodk.com/).

### Pemasangan Awal {#initial-setup}


Untuk segera memulai, [download GeoODK dari the Google Play Store](https://play.google.com/store/apps/details?id=com.geoodk.collect.android), atau dari sumber manapun dimana Anda memperoleh aplikasi Anda. 

Jika ini adalah pertama kali Anda menggunakan GeoODK dengan Platform Cadasta, Anda perlu untuk mengatur GeoODK untuk sinkronisasi langsung. Untuk melakukan ini, Anda memerlukan perngaturan akun Cadasta Anda, jika Anda belum punya, silahkan \(lihat [Mulai Menggunakan](01-gettingstarted.md)\).


1. Setelah Anda membuat akun dan memasang GeoODK, buka aplikasi GeoODK.
2. Dari tampilan peta, sentuh tombol dengan empat persegi di sebelah kanan. Kemudian pilih  **Settings** dari menu utama, kemudian **General Settings**, kemudian **Configure Platform Settings**. 

    ![](/assets/geo-odk-1-configure-settings.png)

3. Pada layar ini, masukan URL Platform dengan nama pengguna Anda dan kata kunci. Nama pengguna dan kata kunci tidak harus sama dengan akun Cadasta Anda, tetapi akan lebih membantu apabila mereka konsisten. Untuk URL, Anda harus menyesuaikan dengan yang Anda gunakan saat Anda mendaftar akun Cadasta Anda.  

    * https://platform.cadasta.org/collect \(untuk proyek aktif\); atau

    * https://demo.cadasta.org/collect  \(untuk uji coba\)

    ![](/assets/geo-odk-2-url.png)

Sekarang Anda telah memiliki akun GeoODK yang akan tersinkronisasi dengan Platform Cadasta. 

Klik tombol kembali tiga kali untuk kembali ke menu utama. 

### Loading your Questionnaire {#loading-your-form}

Once you've connected GeoODK with Cadasta, the next thing you need to do is load the questionnaire you're using for your data collection project. 

1. From the Main Menu, select **Settings**, then **Form Management**. 

    ![](/assets/geo-odk-3-form-management.png)

2. At this stage, you may be asked to provide your Cadasta username and password. Enter this information and then wait a few moments to be connected to the server. _Having trouble with this step? See [GeoODK Troubleshooting](#geoodk-troubleshooting)._

    ![](/assets/geo-odk-4-user-pass.png)

3. In the page that follows, you'll see a list of questionnaires that have been loaded for your organization's projects. Place a checkmark next to the form you'd like to download and tap **Get Selected**.

    ![](/assets/geo-odk-5-questionnaire-list.png)

Now, GeoODK is configured to record data using the questions in your questionnaire. 

### Data Collection {#data-collection}

Once you've initialized GeoODK and loaded your questionnaire, now it’s time to collect some data!

1. From the Main Menu select **Collect Data** then the questionnaire that you want to use. 

    ![](/assets/geo-odk-6-collect-data.png)

2. Swipe left twice to get started completing the form.
3. Continue answering all the survey questions until you reach the "End of survey" message. During this step, swipe left after you've answered each question. 
    * During this section, you'll likely be asked to GeoTrace your location data, or add a GeoShape or GeoPoint. For more information about how this works, see [Collecting Location Data: GeoTrace, GeoPoint and GeoShape](#geotracing).
4. When all of your questions are completed, select the **Mark Form as finalized** checkbox and **Save Form and Exit**. 

    ![](/assets/geo-odk-7-finalized-form.png)

### Collecting Location Data: GeoTrace, GeoShape, and GeoPoint {#geotracing}

During [data collection](#data-collection), you'll be asked to collect data specifying your location using one of the following options.

* **[GeoTrace](#geotrace)** creates lines  (collections of two or more GPS coordinates) based on your location. It's also the default option provided in both the standard and minimum questionnaires. 

* **[GeoShape](#geoshape)** creates polygons (closed shapes). To create a GeoShape, you can use your finger to draw a shape on the map.  

* **[GeoPoint](#geopoint)** creates points (single GPS coordinates) based on your location. 

To learn more about how to configure these options in your questionnaire, see the [Questionnaires & Custom Data Collection](08-XLSForms.md).

#### GeoTrace {#geotrace}

To start geotracing, hit the Play button in the upper left:

![](/assets/geo-odk-geotrace-1-play.png)

From there, you'll be asked to select either Automatic or Manual mode. 

![](/assets/geo-odk-geotrace-2-manual-automatic.png)

**Manual mode** allows you to record your geotrace manually. Every time you want to drop a pin, click the **Record Location Point** button at the top of the map. For example, it's common practice to drop pins at each corner of a location. 

![](/assets/geo-odk-geotrace-3-record-location-point.png)

**Automatic mode** records your location at set intervals, such as once every 20 seconds. This mode is helpful if you're recording a large area. 

The amount of time you should set for your interval depends on how you're collecting the data. For example, if you're driving, you may want to set the interval to be once every 5 seconds. If you're walking, you may want to record once every 20-30 seconds. 

If you know you need to record the corners of a large area, then you might want to try manual mode. Or, if you're using automatic mode, pause on the corner long enough for the pin to drop. Alternatively, in automatic mode, you can also use the **Record Location Point** button to manually drop a pin.

For either automatic or manual mode, keep in mind that the more points you record, the bigger your data file will be and the harder it will be to upload when you return to WiFi or you mobile network. Collect all the points you need - and only the points you need!

When you're done geotracing, hit the pause button. You'll then be asked to save your information as a polyline or polygon.

![](/assets/geo-odk-geotrace-4-save-geotrace.png)

If you've recording a point or line, choose polyline. If you've recording an area and created a closed shape, choose polygon.

Finally, you'll be brought to a confirmation screen where you can view your GeoTrace. 

![](/assets/geo-odk-geotrace-5-confirmation.png)

_Note that GeoODK calls a geotrace a parcel regardless of what kind of location it is._

#### GeoShape {#geoshape}

GeoShape is designed for making shapes (or polygons) to represent a specific location. For example, you can use GeoShape to draw a boundary around a building or land area.  

![](/assets/geo-odk-geoshape-1.png)

To collect location data with GeoShape, you can use your finger to draw a shape on the map. 

To create the shape, press and hold your finger on a point on the map until a marker appears. Then, hold your finger on another point. You'll see a red line appear between the two points. 

Keep placing markers on key points around your polygon. When it's time to complete the polygon, press the **Polygon** button in the upper right. 

![](/assets/geoodk-geoshape-4.png)

This will connect the last and first marker you drew, creating a complete and closed polygon.

When you're done, tap the **Save button** and continue your data collection.

#### GeoPoint {#geopoint}

To collect single GPS coordinates, you can use GeoPoint. GeoPoint only works by tracking your specific location (drawing with your finger is not available).

First you'll come to a screen asking you to record the location of your parcel. Click **Record Location**. 

![](/assets/geoodk-geopoint-1.png)

In the screen that follows, you'll see a map with your location. To save your pin location, hit the **Save** icon in the upper right. Also note the GPS accuracy logged at the top of the screen. 

![](/assets/geoodk-geopoint-2.png)

When you're done, you'll come to a screen that looks like the one below. You can use this screen to view or edit your recording.

![](/assets/geoodk-geopoint-3.png)

### Uploading Data {#uploading-data}

When you get back to WiFi or a mobile network, you can upload your completed questionnaires to the Cadasta Platform. 

From the main menu, click **Send Data** and then check off all the forms that you want to upload (use the **Toggle All** button to select all questionnaires). Then select **Send Selected**.

![](/assets/geo-odk-8-send-data.png)

Next, you'll get a confirmation message confirming that the data has been sent. 

![](/assets/geo-odk-9-confirmation.png)

It's a good idea to confirm that you see the data on the Cadasta Platform. Then you can [delete any completed questionnaires](#deleting-questionnaires) from your Android device.

### Editing Data {#editing-data}

ODK makes editing your forms relatively easy. From the main menu, select **Edit Data**, then the form you want to edit. When you're done, save your changes.

### Deleting Questionnaires {#deleting-questionnaires}

You can also easily delete unwanted questionnaires by selecting **Delete Saved Form** from the main menu. On the page that follows, you can toggle between Saved Forms and Blank Forms to delete either one. 

### GeoODK Troubleshooting {#geoodk-troubleshooting}

If you're having trouble using GeoODK, the answer to your question may be here. If not, please [contact us](http://cadasta.org/contact/) and we'll do our best to help you work through the issue.

#### Trouble Loading Your Questionnaire

##### ISSUE: I can't connect to the Cadasta server because my username and password aren't working. (And yes, I've checked to make sure they're correct!)

The easiest thing to do here is to go to the Cadasta platform and change your password. Then, return to GeoODK and enter your new password there.  

##### ISSUE: I'm getting a message that says to "Please wait a few moments," but it's been much much longer than that.

![](/assets/geo-odk-error-1-wait-a-moment-forever.png)

If the above screen is taking longer than you think it should, hit Cancel. You may be correctly connected, or you may be asked to enter your username and password again. 

#### Trouble Uploading Completed Questionnaires

##### ISSUE: I'm getting an error when I upload my completed questionnaires.

If you're having trouble uploading your questionnaires, the most likely culprit is collecting data using a questionnaire that doesn't exactly match the questionnaire loaded on the Cadasta Platform. This can happen if you modify your questionnaire, load it to Cadasta, and then continue collecting data using an older version. 

Unfortunately, the easiest way to fix this is to uninstall the old form and completed questionnaire and start over. This is why we recommend that you test GeoODK before heading out into the field. We also recommend refreshing your questionnaire before heading out to the field if you think that it might have changed. 

If you've collected too much data to start over, please [contact us](http://cadasta.org/contact/). 



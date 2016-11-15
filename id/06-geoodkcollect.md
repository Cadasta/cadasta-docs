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

### Memuat Kuesioner Anda {#loading-your-form}

Setelah GeoODK dan Cadasta Anda terhubung, hal selanjutnya yang perlu Anda lakukan adalah memuat kuesioner yang akan Anda gunakan untuk proyek pengumpulan data.

1. Dari menur utama, pilih **Settings**, kemudian **Form Management**. 

    ![](/assets/geo-odk-3-form-management.png)

2. Pada tahap ini, Anda akan diminta untuk memasukan nama pengguna dan kata kunci dari akun Cadasta Anda. Masukan informasi tersebut kemudian tunggu beberapa saat untuk terhubung ke server. _Anda mengalami masalah di langkah ini? Lihat [Penyelesaian Masalah GeoODK](#geoodk-troubleshooting)._

    ![](/assets/geo-odk-4-user-pass.png)

3. Pada halaman yang telah Anda ikuti, Anda akan melihat sebuah daftar kuesioner yang telah dimuat untuk proyek organisasi Anda. Centang atau tandai pada formulir yang ingin Anda gunakan, dan sentuh **Get Selected**.

    ![](/assets/geo-odk-5-questionnaire-list.png)

Sekarang, GeoODK telah terkonfigurasi untuk mencatat data dengan menggunakan pertanyaan yang terdapat pada kuesioner Anda. 

### Pengumpulan Data {#data-collection}

Setelah Anda menyiapkan GeoODK dan memuat kuesioner Anda, saatnya untuk mengumpulkan beberapa data! 

1. Dari menu utama, pilih **Collect Data** kemudian pilih kuesioner yang ingin Anda gunakan. 

    ![](/assets/geo-odk-6-collect-data.png)

2. Geser ke kiri dua kali untuk mulai mengisi formulir tersebut. 
3. Lanjutkan untuk menjawab seluruh pertanyaan survey hingga Anda menemukan pesan "End of survey" yang menandakan survey telah selesai. Pada langkah ini, geser ke kiri setelah Anda menjawab setiap pertanyaan. 
    * Saat bagian ini, Anda akan ditanyakan untuk mencatat data lokasi dengan GeoTrace, atau menambahkan sebuah GeoShape atau GeoPoint. Informasi lebih lanjut terkait bagaimana mereka bekerja, lihat [Mengumpulkan Data Lokasi: GeoTrace, GeoPoint and GeoShape](#geotracing).
4. Ketika semua pertanyaan telah selesai, pilih **Mark Form as finalized** dan **Save Form and Exit**. 

    ![](/assets/geo-odk-7-finalized-form.png)

### Mengumpulkan Data Lokasi: GeoTrace, GeoShape, and GeoPoint {#geotracing}

Saat [pengumpulan data](#data-collection), Anda akan diminta untuk memperoleh data yang menunjukan lokasi Anda dengan menggunakan beberapa pilihan sebagai berikut. 

* **[GeoTrace](#geotrace)** membuat garis (kumpulan dua koordinat GPS atau lebih) berdasarkan lokasi Anda. Pilihan ini merupakan pilihan standar yang tersedia pada kuesioner standar dan minimal. 

* **[GeoShape](#geoshape)** membuat bentuk (bentuk tertutup). Untuk membuat sebuah GeoShape, Anda dapat menggunakan jari Anda untuk menggambar sebuah bentuk pada peta.   

* **[GeoPoint](#geopoint)** membuat titik (satu koordinat GPS) berdasarkan lokasi Anda. 

Untuk mempelajari lebih lanjut bagaimana mengatur pilihan-pilihan tersebut dalam kuesioner Anda, lihat [Kuesioner & Pengumpulan Data yang Disesuaikan](08-XLSForms.md).

#### GeoTrace {#geotrace}

Untuk memulai GeoTrace, sentuh tombol Play (mulai) di sebelah kiri atas: 

![](/assets/geo-odk-geotrace-1-play.png)

Selanjutnya, Anda akan diminta untuk memilih mode Automatic atau Manual. 

![](/assets/geo-odk-geotrace-2-manual-automatic.png)

**Manual mode** memperbolehkan Anda untuk merekam GeoTrace secara manual. Setiap kali Anda menentukan sebuah pin, klik pada tombol **Record Location Point** pada bagian atas peta. Sebagai contoh, idealnya pin dapat diletakan di setiap sudut dari sebuah lokasi. 

![](/assets/geo-odk-geotrace-3-record-location-point.png)

**Automatic mode** merekam lokasi Anda pada jangkauan waktu tertentu, misalnya setiap 20 detik. Mode ini akan berguna jika Anda merekam sebuah wilayah yang luas. 

Jangkauan waktu yang ditentukan seharusnya diatur sesuai dengan bagaimana Anda mengumpulkan data. Misalnya, jika Anda menggunakan kendaraan, Anda mungkin ingin mengatur interval setiap 5 detik. Jika Anda berjalan kaki, Anda mungkin ingin mengatur jangkauan waktu setiap 20-30 detik. 

Jika Anda tahu bahwa Anda memerlukan untuk merekam sebuah wilayah yang luas, Anda mungkin dapat mencoba mode manual. Atau jika Anda menggunakan mode Automatic, Anda dapat berhenti sejenak di bagian sudut wilayah untuk menandakannya dengan sebuah pin. Sebagai alternatif, pada mode Automatic, Anda juga dapat menggunakan tombol **Record Location Point** untuk menandakan sebuah lokasi secara manual.

Baik mode automatic maupun manual, mohon perhatikan bahwa semakin banyak titik yang Anda rekam, semakin besar berkas data Anda dan akan semakin sulit untuk diupload ketika menggunakan WiFi atau jaringan seluler Anda. Kumpulkan titik-titik seperlunya - dan hanya tambahkan titik-titik yang Anda butuhkan. 

Saat Anda telah selesai dengan GeoTrace, tekan tombol Pause. Anda akan ditanyakan untuk menyimpan informasi Anda sebagai garis atau bentuk. 

![](/assets/geo-odk-geotrace-4-save-geotrace.png)

Jika Anda merekam sebuah titik atau garis, pilih polyline. Jika Anda merekam sebuah wilayah dan membuat bentuk tertutup, pilih polygon.

Akhirnya, Anda akan dibawa ke layar konfirmasi dimana Anda dapat melihat GeoTrace Anda. 

![](/assets/geo-odk-geotrace-5-confirmation.png)

_Catatan bahwa GeoODK akan menyebut sebuah parsel dengan geotrace tanpa menghiraukan jenis lokasi tersebut._

#### GeoShape {#geoshape}

GeoShape dirancang untuk membuat bentuk (atau polygon) untuk menggambarkan sebuah lokasi spesifik. Misalnya, Anda dapat menggunakan GeoShape untuk menggambar sebuah batas di sekeliling bangunan atau wilayah tanah. 

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



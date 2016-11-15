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

Untuk memperoleh dat alokasi dengan GeoShape, Anda dapat menggunakan jari Anda untuk menggambar sebuah bentuk pada peta. 

Untuk membuat bentuk, sentuh dan tahan jari Anda pada sebuah titik hingga sebuah penanda muncul. Kemudian, tahan jari Anda pada sebuah titik yang lain. Anda akan melihat sebuah garis berwarna merah diantara kedua titik. 

Taruh beberapa penanda pada titik-titik utama disekitar wilayah Anda. Jika sudah waktunya untuk menyelesaikan bentuk wilayah Anda, tekan tombol **Polygon** di sebelah kanan atas.

![](/assets/geoodk-geoshape-4.png)

Ini akan menghubungkan penanda terakhir dengan penanda awal yang Anda gambar, membuat sebuah bentuk yang tertutup dengan sempurna. 

Jika Anda sudah selesai, sentuh **Save button** dan lanjutkan pengumpulan data Anda. 

#### GeoPoint {#geopoint}

Untuk mengumpulkan sebuah koordinat GPS, Anda dapat menggunakan GeoPoint. GeoPoint hanya bekerja dengan menandakan lokasi spesifik Anda (menggambarkan lokasi dengan jari tidak tersedia).

Pertama-tama Anda akan melihat tampilan layar yang menanyakan ASnda untuk merekam lokasi parsel Anda. Klik **Record Location**. 

![](/assets/geoodk-geopoint-1.png)

Pada tampilan layar berikutnya, Anda akan melihat sebuah peta lokasi Anda. Untuk menyimpan penanda lokasi, sentuh ikon **Save** di sebelah kanan atas. Mohon perhatikan bahwa akurasi GPS tercantum di bagian atas layar. 

![](/assets/geoodk-geopoint-2.png)

Jika Anda telah selesai, Anda akan melihat tampilan layar seperti di bawah ini. Anda dapat melihat atau mengubah titik lokasi Anda di tampilan ini. 

![](/assets/geoodk-geopoint-3.png)

### Uploading Data {#uploading-data}

Ketika Anda kembali mendapatkan jaringan WiFi atau jaringan seluler, Anda dapat mengupload kuesioner yang telah diisi ke Platform Cadasta.

Dari menu utama, klik **Send Data** dan tandai seluruh formulir yang ingin Anda upload (gunakan tombol **Toggle All** untuk memilih seluruh kuesioner). Kemudian pilih **Send Selected**.

![](/assets/geo-odk-8-send-data.png)

Terakhir, Anda akan mendapatkan sebuah pesan konfirmasi bahwa data Anda sudah terkirim. 

![](/assets/geo-odk-9-confirmation.png)

Sebaiknya Anda memeriksa untuk melakukan konfirmasi bahwa data Anda sudah tersedia di Platform Cadasta. Kemudian Anda dapat [menghapus seluruh kersioner yang terisi](#deleting-questionnaires) dari perangkat Android Anda.

### Mengubah Data {#editing-data}

GeoODK dapat membuat perubahan formulir Anda menjadi mudah. Dari menu utama, pilih **Edit Data**, kemudian pilih formulir yang ingin Anda ubah. Jika Anda sudah selesai, simpan perubahan Anda. 

### Deleting Questionnaires {#deleting-questionnaires}

Anda juga dapat menghapus kuesioner yang tidak dibutuhkan dengan memilih **Delete Saved Form** dari menu utama. Pada halaman selanjutnya, Anda dapat beralih antara Saved Forms dan Blank Forms untuk menghapus salah satunya. 

### Penyelesaian Masalah GeoODK {#geoodk-troubleshooting}

Jika Anda memiliki masalah menggunakan GeoODK, Anda mungkin akan menemukan jawaban di sini. Jika tidak, mohon [hubungi kami](http://cadasta.org/contact/) dan kami akan melakukan yang terbaik untuk membantu menyelesaikan permasalahan Anda. 

#### Trouble Loading Your Questionnaire

##### Masalah: Saya tidak dapat terhubung dengan server Cadasta karena nama pengguna dan kata kunci saya tidak bekerja. (Dan ya, saya telah memeriksanya untuk memastikan keduanya benar!)

Hal yang paling mudah adalah pergi ke Platform Cadasta dan ubah kata kunci Anda. Kemudian, kembali ke ODK dan masukan kata kunci Anda yang baru.   

##### Masalah: Saya mendapatkan pesan "Please wait a few moments," tetapi pesan tersebut muncul lebih lama dari biasanya. 

![](/assets/geo-odk-error-1-wait-a-moment-forever.png)

Jika Anda mendapatkan respon lebih lama dari biasanya, sentuh Cancel. Anda mungkin sudah terhubung secara benar, atau Anda mungkin ingin mencoba kembali memasukan nama pengguna dan kata kunci Anda.

#### Trouble Uploading Completed Questionnaires

##### Masalah: Saya mendapatkan pesan kesalahan ketika mengupload kuesioner yang telah diisi. 

Jika Anda memiliki masalah untuk mengupload kuesioner Anda, kemungkinan penyebab utamanya adalah jika Anda mengumpulkan data dengan kuesioner yang tidak sama dengan kuesioner yang dimuat di Platform Cadasta. Ini dapat terjadi jika Anda memodifikasi 
kuesioner Anda, memuatnya di Cadasta, dan melanjutkan pengumpulan data dengan versi kuesioner yang lama. 

Sayangnya, hal yang termudah untuk memperbaiki hal ini adalah membuang formulir beserta kuesioner yang telah terisi dan memulai dari awal. Inilah mengapa kami merekomendasikan Anda untuk melakukan uji coba GeoODK sebelum pergi ke lapangan. Kami juga merekomendasikan Anda untuk memperbarui kuesioner sebelum pergi ke lapangan jika Anda berpikir ada perubahan. 

Jika Anda telah terlanjur mengumpulkan banyak data kemudian perlu mengulang, mohon [hubungi kami](http://cadasta.org/contact/). 



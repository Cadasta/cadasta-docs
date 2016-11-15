# Mengumpulkan Data dengan ODK Collect (Open Data Kit) 

* [Ringkasan](#overview)
* [Pemasangan Awal](#initial-setup)
* [Memuat Kuesioner Anda](#loading-your-form)
* [Pengumpulan Data](#data-collection)
* [Mengupload Data](#uploading-data)
* [Mengumpulkan Data Lokasi: GeoTrace, GeoPoint dan GeoShape](#geotracing)
* [Mengubah Data](#editing-data)
* [Menghapus Kuesioner](#deleting-questionnaires)
* [Penyelesaian Masalah ODK](#odk-troubleshooting)


### Ringkasan {#overview}

Pengumpulan data lapangan merupakan salah satu bagian yang penting dalam proses pencatatan hak-hak atas tanah dan sumber daya. Platform Cadasta dirancang untuk menyediakan beberapa alat untuk pengumpulan data, dan memproses data-data tersebut. Salah satu alat ini disebut Open Data Kit, atau biasa disingkat dengan ODK Collect. 

ODK adalah perangkat lunak terbuka (open source) dan gratis untuk pengumpulan data secara mobile khusus perangkat Android \(maaf fans Apple)\. Untuk memulai, [download ODK Collect dari Google Play Store](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en), atau dari sumber manapun dimana Anda memperoleh aplikasi Anda. 

Bagian ini menjelaskan secara ringkas bagaimana ODK Collect dan Cadasta dapat bekerja sama: 

1. Pertama, Anda perlu [memasang ODK](#initial-setup) pada sebuah perangkat Android. 
2. Kemudian Anda akan [memuat kuesioner](#loading-your-form) yang Anda ingin gunakan untuk pengumpulan data. 
3. Terakhir, saatnya untuk [mengumpulkan data Anda](#data-collection)! 
4. Ketika Anda sudah memiliki jaringan WiFi, [upload data Anda](#uploading-data) ke Platform Cadasta.

**Penting!** Langkah 1, 2, dan 4 membutuhkan jaringan WiFi. Anda juga mungkin ingin melakukan ujio coba langkah ke-3 sebelum keluar lapangan, untuk menjaga apabila Anda perlu [menyelesaikan masalah](#odk-troubleshooting) atau membuat perubahan. 

Untuk informasi dan dokumentasi terkait ODK secara umum, kunjungi [opendatakit.org](https://opendatakit.org/).

### Pemasangan Awal {#initial-setup}

Untuk segera memulai, [download ODK dari Google Play Store](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en), atau dari sumber manapun dimana Anda memperoleh aplikasi Anda. 

Jika ini adalah pertama kali Anda menggunakan ODK dengan Platform Cadasta, Anda perlu untuk mengatur ODK untuk sinkronisasi langsung. Untuk melakukan ini, Anda memerlukan perngaturan akun Cadasta Anda, jika Anda belum punya, silahkan \(lihat [Mulai Menggunakan](01-gettingstarted.md)\).

1. Setelah Anda membuat akun dan memasang ODK, buka aplikasi ODK.

2. Dari layar pembuka (Menu Utama), sentuh tiga titik di kanan atas, kemudian pilih **General Settings**, kemudian **Configure Platform Settings**. 

    ![](/assets/odk-1-setup.png)

3. Pada layar ini, masukan URL Platform dengan nama pengguna Anda dan kata kunci. Nama pengguna dan kata kunci tidak harus sama dengan akun Cadasta Anda, tetapi akan lebih membantu apabila mereka konsisten. Untuk URL, Anda harus menyesuaikan dengan yang Anda gunakan saat Anda mendaftar akun Cadasta Anda.  

    * https://platform.cadasta.org/collect \(untuk proyek aktif\); atau

    * https://demo.cadasta.org/collect  \(untuk uji coba\)

    ![](/assets/odk-2-account-info.png)

Sekarang Anda telah memiliki akun ODK yang akan tersinkronisasi dengan Platform Cadasta. 

Klik tombol kembali dua kali untuk kembali ke menu utama. 

### Memuat Kuesioner Anda {#loading-your-form}


Setelah ODK dan Cadasta Anda terhubung, hal selanjutnya yang perlu Anda lakukan adalah memuat kuesioner yang akan Anda gunakan untuk proyek pengumpulan data. 

1. Dari menu utama, pilih **Get Blank Form**.

    ![](/assets/odk-3-get-blank-form.png)

2. Pada tahap ini, Anda akan diminta untuk memasukan nama pengguna dan kata kunci dari akun Cadasta Anda. Masukan informasi tersebut kemudian tunggu beberapa saat untuk terhubung ke server. 

3. Pada halaman yang telah Anda ikuti, Anda akan melihat sebuah daftar kuesioner yang telah dimuat untuk proyek organisasi Anda. Centang atau tandai pada formulir yang ingin Anda gunakan, dan sentuh **Get Selected**.

    ![](/assets/odk-4-get-blank-form.png)

Sekarang, ODK telah terkonfigurasi untuk mencatat data dengan menggunakan pertanyaan yang terdapat pada kuesioner Anda. 

### Pengumpulan Data {#data-collection}

Setelah Anda menyiapkan ODK dan memuat kuesioner Anda, saatnya untuk mengumpulkan beberapa data! 

1. Dari Menu Utama ODK, pilih **Fill Blank Form** kemudian pilih kuesioner yang ingin Anda gunakan.

    ![](/assets/odk-5-fill-blank-form.png)

2. Geser ke kiri dua kali untuk mulai mengisi formulir tersebut. 
3. Lanjutkan untuk menjawab seluruh pertanyaan survey hingga Anda menemukan pesan "End of survey" yang menandakan survey telah selesai. Pada langkah ini, geser ke kiri setelah Anda menjawab setiap pertanyaan. 
    * Saat bagian ini, Anda akan ditanyakan untuk mencatat data lokasi dengan GeoTrace, atau menambahkan sebuah GeoShape atau GeoPoint. Informasi lebih lanjut terkait bagaimana mereka bekerja, lihat [Mengumpulkan Data Lokasi: GeoTrace, GeoPoint dan GeoShape](#geotracing).
4. Ketika semua pertanyaan telah selesai, pilih **Mark Form as finalized** dan **Save Form and Exit**. 

### Mengumpulkan Data Lokasi: GeoTrace, GeoShape, dan GeoPoint {#geotracing}

Saat [pengumpulan data](#data-collection), Anda akan diminta untuk memperoleh data yang menunjukan lokasi Anda dengan menggunakan beberapa pilihan sebagai berikut. 

* **[GeoTrace](#geotrace)** membuat garis (kumpulan dua koordinat GPS atau lebih) berdasarkan lokasi Anda. Pilihan ini merupakan pilihan standar yang tersedia pada kuesioner standar dan minimal. 

* **[GeoShape](#geoshape)** membuat bentuk (bentuk tertutup). Untuk membuat sebuah GeoShape, Anda dapat menggunakan jari Anda untuk menggambar sebuah bentuk pada peta.   

* **[GeoPoint](#geopoint)** membuat titik (satu koordinat GPS) berdasarkan lokasi Anda. 

Untuk mempelajari lebih lanjut bagaimana mengatur pilihan-pilihan tersebut dalam kuesioner Anda, lihat [Kuesioner & Pengumpulan Data yang Disesuaikan](08-XLSForms.md).

#### GeoTrace {#geotrace}

Ketika Anda mulai menggunakan GeoTrace, Anda akan mendapat pemberitahuan **Start GeoTrace**:

![](/assets/odk-geotrace-1.png)

Pada tampilan layar selanjutnya, Anda akan ditanya untuk **Zoom to Current Location**.

![](/assets/odk-geotrace-2.png)


Setelah lokasi teridentifikasi, Anda akan ditanyakan untuk memilih mode Automatic atau Manual.  

![](/assets/odk-geotrace-3.png)

**Manual mode** memperbolehkan Anda untuk merekam GeoTrace secara manual. Setiap kali Anda menentukan sebuah pin, klik pada tombol **Record Location Point** pada bagian atas peta. Sebagai contoh, idealnya pin dapat diletakan di setiap sudut dari sebuah lokasi. 

![](/assets/odk-geotrace-5.png)

**Automatic mode** merekam lokasi Anda pada jangkauan waktu tertentu, misalnya setiap 20 detik. Mode ini akan berguna jika Anda merekam sebuah wilayah yang luas. 

Jangkauan waktu yang ditentukan seharusnya diatur sesuai dengan bagaimana Anda mengumpulkan data. Misalnya, jika Anda menggunakan kendaraan, Anda mungkin ingin mengatur interval setiap 5 detik. Jika Anda berjalan kaki, Anda mungkin ingin mengatur jangkauan waktu setiap 20-30 detik. 

Jika Anda tahu bahwa Anda memerlukan untuk merekam sebuah wilayah yang luas, Anda mungkin dapat mencoba mode manual. Atau jika Anda menggunakan mode Automatic, Anda dapat berhenti sejenak di bagian sudut wilayah untuk menandakannya dengan sebuah pin. Sebagai alternatif, pada mode Automatic, Anda juga dapat menggunakan tombol **Record Location Point** untuk menandakan sebuah lokasi secara manual.

Baik mode automatic maupun manual, mohon perhatikan bahwa semakin banyak titik yang Anda rekam, semakin besar berkas data Anda dan akan semakin sulit untuk diupload ketika menggunakan WiFi atau jaringan seluler Anda. Kumpulkan titik-titik seperlunya - dan hanya tambahkan titik-titik yang Anda butuhkan. 

![](/assets/odk-geotrace-4.png)

Saat Anda telah selesai dengan GeoTrace, tekan tombol Pause. Anda akan ditanyakan untuk menyimpan informasi Anda sebagai garis atau bentuk.

Jika Anda merekam sebuah titik atau garis, pilih polyline. Jika Anda merekam sebuah wilayah dan membuat bentuk tertutup, pilih polygon.

Akhirnya, Anda akan dibawa ke layar konfirmasi dimana Anda dapat melihat GeoTrace Anda. 

_Catatan bahwa ODK akan menyebut sebuah parsel dengan geotrace tanpa menghiraukan jenis lokasi tersebut._

#### GeoShape {#geoshape}

GeoShape dirancang untuk membuat bentuk (atau polygon) untuk menggambarkan sebuah lokasi spesifik. Misalnya, Anda dapat menggunakan GeoShape untuk menggambar sebuah batas di sekeliling bangunan atau wilayah tanah.

Jika Anda mengumpulkan data menggunakan GeoShape, pertama-tama Anda akan diminta untuk memperbesar ke lokasi Anda saat itu atau ke fitur yang telah disimpan. 

![](/assets/odk-geoshape-1.png)

Pada layar selanjutnya, Anda dapat mulai membuat bentuk Anda. Sentuh layar untuk menempatkan penanda di sekeliling lokasi, dan perhatikan garis merah yang dibuat diantara setiap penanda. Untuk menutup polygon Anda, sentuh pada titik yang sama dimana polygon tersebut dimulai. 

![](/assets/odk-geoshape-2.png)

Ketika Anda siap untuk menyimpan GeoShape Anda, sentuh ikon **Save** di sebelah kanan. Jika Anda ingin membuangnya, Anda juga dapat menyentuh tombol **Trash** di atasnya. 

#### GeoPoint {#geopoint}

Untuk mengumpulkan sebuah koordinat GPS, Anda dapat menggunakan GeoPoint. GeoPoint hanya bekerja dengan menandakan lokasi spesifik Anda (menggambarkan lokasi dengan jari tidak tersedia).

Ketika Anda memulai mengumpulkan GeoPoint Anda, pertama-tama aplikasi akan memuat lokasi Anda. Hal ini akan memakan waktu beberapa menit. 

![](/assets/odk-geopoint-1.png)

Selanjutnya, aplikasi akan menginformasikan tingkat ketelitian GPS. Di sini digambarkan bahwa akurasi kurang-lebih dalam radius 24-meter dimana pengguna berdiri. 

![](/assets/odk-geopoint-2.png)

Setelah informasi akurasi dan lokasi terlampir, Anda siap untuk menyimpan GeoPoint Anda. 

![](/assets/odk-geopoint-3.png)

###Mengupload Data {#uploading-data}

Ketika Anda kembali mendapatkan jaringan WiFi atau jaringan seluler, Anda dapat mengupload kuesioner yang telah diisi ke Platform Cadasta.

Dari menu utama, klik **Send Finalized Form** dan tandai seluruh formulir yang ingin Anda upload (gunakan tombol **Toggle All** untuk memilih seluruh kuesioner). Kemudian pilih **Send Selected**.

![](/assets/odk-send-finalized-form.png)

Terakhir, Anda akan mendapatkan sebuah pesan konfirmasi bahwa data Anda sudah terkirim. 

Sebaiknya Anda memeriksa untuk melakukan konfirmasi bahwa data Anda sudah tersedia di Platform Cadasta. Kemudian Anda dapat [menghapus seluruh kuesioner yang terisi](#deleting-questionnaires) dari perangkat Android Anda.

### Mengubah Data {#editing-data}

ODK dapat membuat perubahan formulir Anda menjadi mudah. Dari menu utama, pilih **Edit Data**, kemudian pilih formulir yang ingin Anda ubah. Jika Anda sudah selesai, simpan perubahan Anda. 

### Menghapus Kuesioner {#deleting-questionnaires}

Anda juga dapat menghapus kuesioner yang tidak dibutuhkan dengan memilih **Delete Data** dari menu utama. Pada halaman selanjutnya, Anda dapat beralih antara Saved Forms dan Blank Forms untuk menghapus salah satunya. 

### Penyelesaian Masalah ODK {#odk-troubleshooting}

Jika Anda memiliki masalah menggunakan ODK, Anda mungkin akan menemukan jawaban di sini. Jika tidak, mohon [hubungi kami](http://cadasta.org/contact/) dan kami akan melakukan yang terbaik untuk membantu menyelesaikan permasalahan Anda. 

#### Masalah Saat Memuat Kuesioner Anda

##### Masalah: Saya tidak dapat terhubung dengan server Cadasta karena nama pengguna dan kata kunci saya tidak bekerja. (Dan ya, saya telah memeriksanya untuk memastikan keduanya benar!)

Hal yang paling mudah adalah pergi ke Platform Cadasta dan ubah kata kunci Anda. Kemudian, kembali ke ODK dan masukan kata kunci Anda yang baru.   

##### Masalah: Saya mendapatkan pesan "Please wait a few moments," tetapi pesan tersebut muncul lebih lama dari biasanya. 

Jika Anda mendapatkan respon lebih lama dari biasanya, sentuh Cancel. Anda mungkin sudah terhubung secara benar, atau Anda mungkin ingin mencoba kembali memasukan nama pengguna dan kata kunci Anda.

#### Masalah Menambahkan Data Lokasi

##### Masalah: ODK tidak dapat menambahkan data lokasi apapun. 

![](/assets/odk-trouble-1.png)

Jika Anda mendapatkan pemberitahuan seperti atas, sayang sekali bahwa ini adalah masalah yang seringkali terjadi (dan membuat semuanya frustasi!). Cadasta telah mengetahui bahwa beberapa perangkat Android menolak untuk mencatat lokasi data GPS dengan ODK. Tim kami sedang bekerja untuk menyelesaikan masalah ini. 

Saat ini, silahkan coba beberapa alternatif: 

1. Coba gunakan perangkat Android yang lain. Masalah misterius ini tidak selalu muncul di setiap perangkat Android. 
2. Coba gunakan GeoODK, yang bekerja kurang lebih sama seperti ODK. _[Pelajari lebih lanjut tengang bagaimana menggunakan GeoODK dengan Cadasta](06-odkcollect.md)._


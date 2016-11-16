# Kuesioner & Pengumpulan Data yang Disesuaikan

* [Ringkasan](#overview)
* [Kuesioner Minimal](#minimal-form)
* [Kuesioner Standar](#standard-form)
* [Menyesuaikan Kuesioner Anda](#customizing-your-questionnaire)

### Ringkasan {#overview}

Setiap proyek pengumpulan data dapat berbeda - dimulai dari pertanyaan yang Anda tanyakan. Pertanyan-pertanyaan ini dapat membentuk proyek yang terbentuk - termasuk kolom isian untuk pengumpulan data.

Platform Cadasta memfasilitasi Anda untuk menetukan skema pengumpulan data Anda sendiri, sehingga Anda dapat menyesuaikannya sesuai dengan pertanyaan yang Anda ajukan. Pertanyaan-pertanyaan ini dapat termasuk rincian kontak, nama tempat, atau bagaimana tanah tersebut diakuisisi.

Pada Platform Cadasta, prinsip teknologi seperti ini diperoleh dari [XLSForm](http://xlsform.org/). XLSForm adalah formulir isian standar yang memfasilitasi Anda untuk membuat formulir isiang menggunakan sebuah tabel. Formulit ini \(atau yang kita sebut dengan kuesioner\) merupakan alternatif sebuah database yang sederhana. Tetapi mereka juga dirancang untuk mengelola informasi dengan berbagai tingkat kompleksitas. 

Anda dapat memulai proyek Anda dengan salah satu dari dua kuesioner yang telah disiapkan:

* [Kuesioner minimal](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx) - dimana membuat sebuah skema minimal untuk data yang dibutuhkan oleh platform; dan 

* [Kuesioner standar](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx) - dimana merupakan sebuah titik awal untuk rekan-rekan kami. Kuesioner ini termasuk kolom isian yang ada di kuesioner minimum, dengan beberapa tambahan. 

Anda dapat menggunakan kedua formulir ini sebagai titik awal untuk proyek Anda. Anda juga dapat memodifikasi bagian dari formulir ini untuk menyesuaikan kebutuhan koleksi data Anda. 

Jika Anda membutuhkan modifikasi yang signifikan dari kolom isian kuesioner, lihat bagian [menyesuaikan kuesioner Anda](#customizing-your-questionnaire). 

_**Catatan penting:** Anda dapat melakukan perubahan kecil pada kuesioner Anda - misalnya menambahkan baris - dan mengupload ulang pada proyek yang tersedia sebelumnya. Bagaimanapun, jika kuesioner Anda berubah secara signifikan, Anda mungkin harus memulai sebuah proyek baru._

Jika Anda memiliki pertanyaan tentang bagaimana untuk menggunakan kuesioner ini, silahkan [hubungi kami](http://cadasta.org/contact/) kapanpun.

### Kuesioner Minimal {#minimal-form}

[Kuesioner minimal](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx) memiliki kolom isian yang penting untuk pengumpulan data menggunakan Platform Cadasta. 

Kuesioner ini memiliki tiga tab:

* Survey
* Choices, dan
* Settings.

Tab **Survey** menunjukan skema pengumpulan data secara menyeluruh.

![](/assets/minimum-survey.png)

Area yang berwarna abu-abu adalah kolom isian pada Platform Cadasta yang akan bekerja. Beberapa dari kolom isian tersebut \(contohnya `deviceid`\) digunakan dibalik proses, sehingga Anda tidak akan melihatnya di dalam Platform, ODK, atau GeoODK. _(Catatan! Jangan mengubah apapun yang ada di dalam kotak abu-abu!)_

Penting bagi Anda untuk mengetahui tiga kolom pertama: 
* `type` menentukan tipe data yang Anda tambakan - misalnya teks, tanggal, sebuah pilihan, atau lainnya. 
* `name` menentukan variabel yang digunakan untuk pemasukan data. Tidak boleh ada dua nama yang sama! 
* `label` menunjukan teks yang akan dilihat pada formulir. Kolom isian yang berwarna putih dapat dimodifikasi sesuai kebutuhan. 

Tab **Choices** merupakan pilihan dimana menu pilihan ganda akan disimpan. 

![](/assets/minimum-choices.png)

Sebagai contoh, `respondent` terdiri dari Grup, Individual dan Korporat (A2 - A4 pada gambar di atas) berkaitan dengan menu pilihan pada jendela Tambah Hubungan:

![](/assets/relationship-dropdown.png)

Tab **Settings** menunjukan `form_id` dan judul kuesioner Anda. Anda akan menggunakan ID ini ketika Anda memasang pengumpulan data dengan ODK dan GeoODK. 

Pastikan seluruh kuesioner pada organisasi Anda memiliki ID formulir yang unik. Karena jika tidak, kuesioner Anda tidak akan termuat, dan Anda akan terpaksa menggunakan form yang asli dengan ID tersebut. Sebagai tambahan, pastikan ketika membuat nama dimulai dengan huruf kecil dan tidak memiliki spasi. 

### Kuesioner Standar {#standard-form}

[Kuesioner standar](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx) memiliki pertanyaan yang sama dengan versi minimal, dengan beberapa sedikit tambahan. Anda dapat melihat pilihan yang lebih banyak pada tab **Survey**.

![](/assets/standard-survey.png)

Gambar di atas menunjukan seluruh pemasukan data yang akan dikumpulkan dan ditambahkan pada informasi minimal. The image above shows all the entries that will be collected in addition to the minimal information. Pemasukan data tersebut diorganisir berdasarkan bagian: 

* Atribut Lokasi \(baris 22-28\)
* Atribut Kelompok Standar \(baris 20-32\)
* Atribut Kelompok Individual \(baris 34-38\)
* Atribut Kelompok Grup \(baris 40-43\)
* Atribut Hubungan Kelompok \(baris 45-47\)
* Atribut Hubungan Kepemilikan \(baris 49-51\)

Setiap bagian ini berhubungan dengan jendela pengumpulan data di Platform Cadasta. 

Tab **Choices** memiliki pilihan yang sama dengan kuesioner minimal, dengan tambahan pilihan. 

![](/assets/standard-choices-2.png)

Sebagai contoh, baris 38-47 menunjukan pilihan untuk berbagai macam tipe akuisisi lokasi, yang terhubung dengan baris 25 pada tab Survey (atas).

Tab **Settings** pada kuesioner standar sama dengan versi minimal - menyediakan `form_id`, untuk mengidentifikasi kuesioner Anda pada ODK atau GeoODK. 

![](/assets/standard-settings.png)

Pastikan seluruh kuesioner pada organisasi Anda memiliki ID formulir yang unik. Karena jika tidak, kuesioner Anda tidak akan termuat, dan Anda akan terpaksa menggunakan form yang asli dengan ID tersebut. Sebagai tambahan, pastikan ketika membuat nama dimulai dengan huruf kecil dan tidak memiliki spasi. 

### Menyesuaikan Kuesioner Anda {#customizing-your-questionnaire}

Jika Anda akan mengumpulkan data yang berebda dengan apa yang ada di dalam kuesioner standar, dan lebih daripada yang terdapat di kuesioner minimal, Anda dapat mengubah formulit ini untuk menyesuaikan dengan kebutuhan Anda. Apapun yang terdapat pada kolom isian berwarna putih dapat dimodifikasi. Kolom isian dengan warna abu-abu harus tetap sama agar semuanya tetap bekerja. 

#### Penyesuaian Dasar

##### Menghapus Kolom Isian yang Tidak Diperlukan

Jika ada sebuah kolom isian yang tidak ingin Anda masukan, Anda dapat menghapus baris kolom isian tersebut dari tab survey pada kuesioner. Untuk melakukan ini di Excel, klik kanan pada baris kemudian klik Delete. 

_**Catatan Penting!** Ingat bahwa kolom isian yang berwarna abu-abu tidak dapat dihapus atau dimodifikasi; Anda hanya dapat menghapus baris yang seluruhnya berlatar belakang putih._

##### Mengubah Menu Pilihan Ganda

Untuk mengubah sebuah menu pilihan ganda, arahkan ke tab choices. Di sana, Anda dapat memodifikasi kolom isian `name` dan `label` sesuai kebutuhan.

Sebagai contoh, untuk menambahkan sebuah kolom isian pada menu pilihan lokasi akusisi \(`l_acquired_how`\):

* Tambahkan sebuah garis baru, beri nama `list_name` dari `l_acquired_how`.
* Tambahkan sebuah nama dan label.

Pada contoh di bawah ini, sebuah kategori untuk menu pilihan \("Tidak Diketahui"\) telah ditambahkan pada kuesioner. 

![](/assets/land-acquision-new-row.png)

Saat kuesioner telah disimpan dan dimuat ke dalam proyek, pilihan "Tidak Diketahui" yang baru dimasukan akan muncul pada menu pilihan di bagian, "Bagaimana lokasi ini diakusisi?"

![](/assets/standard-new-field.png)

#### GeoTrace, GeoShape dan GeoPoint

Pada lokasi pengumpulan data Anda, Anda dapat memilih di antara data titik, garis, atau bentuk. Pada kedua kuesioner baik standar maupun minimal, Anda memiliki pilihan untuk menggunakan salah satu diantara pilihan berikut `geopoint`, `geotrace`, atau `geoshape`. 

* `geotrace` merekam sebuah garis dari dua koordinat GPS atau lebih. Ini merupakan pengaturan standar baik di dalam kuesioner minimal maupun standar. Dengan `geotrace`, lokasi ditandai berdasarkan koordinat GPS penggguna.

* `geoshape` merekam sebuah bentuk yang dibuat dari sejumlah koordinat GPS, yang digambar pada layar. 

* `geopoint` memperoleh satu titik data berdasarkan koordinat GPS pengguna. 

Untuk merubah tipe data apa yang Anda kumpulkan, Anda dapat memodifikasi sel A11 baik di kuesioner minimal maupun standar. 

#### Penyesuaian Tingkat Lanjut

Jika Anda memerlukan perubahan kolom isian yang lebih banyak, makan penyesuaian tingkat lanjut ini mungkin berguna untuk Anda. 

##### Tipe Pemasukan Data {#data-types}

Untuk memanfaatkan penyesuaian kuesioner, sangat penting untuk mengetahui tipe pemasukan daya yang terbaik untuk tipe informasi yang Anda kumpulkan. Beberapa yang paling umum yang akan Anda gunakan contohnya: 

* `text` - dimana menentukan bahwa Anda akan memperoleh teks dasar. 
* `date` - dimana menentukan bahwa Anda mencatat tanggal. 
* `select_one` - dimana menentukan bahwa Anda menggunakan sebuah menu pilihan ganda. 

![](/assets/standard-survey-example.png)

Anda dapat melihat masing-masing tipe pada contoh di atas, yang diambil dari tab survey pada kuesioner standar. 

Perhatikan bahwa `select_one` - menu pilihan ganda - memerlukan identifikasi sebuah set pilihan yang terkait. Pada contoh di atas, menu pilihan ganda yang pertama menentukan bahwa sel A24 terkait dengan pilihan yang diberi nama `l_quality_choices`. Pada tab Choices, Anda dapat melihat berbagai macam pilihan untuk `l_quality_choices`:

![](/assets/standard-choices-example.png)

Pilihan ini akan muncul pada menu pilihan ganda setelah dipilih. 

Sebagai tambahan untuk tipe data dasar ini, [XLSForm menawarkan berbagai macam tipe data yang dapat Anda pilih](http://xlsform.org/#question-types).

![](/assets/xls-form-question-types.png)

Tipe yang Anda pilih bergantung pada jenis pertanyaan yang Anda ajukan. Contohnya, jika Anda perlu mengumpulkan sebuah sampel suara dari sebuah interview, Anda dapat memilih `audio`, dimana akan memberi tahu Anda untuk merekam suara. 

##### Bagian Kuesioner

![](/assets/standard-survey.png)

Bagian kuesioner yang dapat disesuaikan telah diorganisir berdasarkan bagian-bagian berikut: 

* **Atribut Lokasi** berhubungan dengan informasi tentang lokasi, misalnya nama lokasi dan batas lokasi. 

* **Atribut Kelompok Standar** menentukan informasi yang Anda kumpulkan tentang kelompok apapun, baik individual, grup, maupun korporat. 

* **Atribut Kelompok Individual** dan **Atribut Kelompok Grup** masing-masing menyediakan informasi spesifik untuk apakah kelompok tersebut merupakan satu individu atau grup.

* **Atribut Hubungan Kelompok** merupakan informasi spesifik untuk hubungan antar sebuah kelompok terhadap satu lokasi.  

* **Atribut Hubungan Kepemilikan** menentukan informasi terkait tentang suatu kepemilikan kelompok pada sebuah bidang tanah.

Setiap bagian-bagian ini berhubungan dengan sebagian dasar internal Platform Cadasta. Agar pertanyaan Anda dapat muncul di platform, mereka harus berada dalam salah satu bagian ini. 

Gambar di bawah ini diambil dari sebuah kuesioner yang disesuaikan dari salah satu rekan kerja kami. Di sini, mereka menambahkan sejumlah kolom isian yang disesuaikan pada bagian `party_attributes_default`:

![](/assets/example-xls-1.png)

Menambahkan bagian baru juga memungkinkan, dimana contoh di bawah ini merupakan salah satu contoh yang pernah dilakkan oleh salah satu rekan kerja Cadasta. Di sini mereka menambahkan sebuah bagian pada saksi: 

![](/assets/example-xls-2.png)

Jika Anda ingin membuat sebuah bagian baru atau menyesuaiakan kuesioner Anda secara signifikan, kami sangat merekomendasikan Anda untuk [menghubungi kami](http://cadasta.org/contact/) pertama kali. Kami di sini untuk membantu! 

##### Menu Pilihan Ganda dengan Semua GeoTypes (GeoTrace, GeoPoint & GeoShape)

Pada kasus tertentu, Anda mungkin ingin memberikan pilihan bagi data kolektor Anda untuk mengumpulkan data menggunakan GeoTrace, GeoPoint atau GeoShape. Jika demikian, Anda dapat memodifikasi formulir Anda. Cara alternatif, Anda juga dapat membuat kuesioner Anda [dimulai dari kuesioner ini](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire-all-geo.xlsx). 

Jika Anda ingin memperbarui kuesioner sebelumnya, berikut adalah hal yang perlu Anda lakukan. 

Pada **tab Survey** dari kuesioner Anda, tambahkan tiga baris di bawah bari ke-11. 

![](/assets/allgeo-modify-1.png)

Kemudian, copy dan paste informasi di bawah ini pada baris ke-11 hingga baris ke-14. 

<table>
<tbody>
<tr>
    <td>select_one geo_type</td>
    <td>geo_type</td>
    <td>Select type of geo collection</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td>geoshape</td>
    <td></td>
</tr>
<tr>
    <td>geoshape</td>
    <td>location_geoshape</td>
    <td>Draw the location boundaries on the map	</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td></td>
    <td>${geo_type}='geoshape'</td>
</tr>
<tr>
    <td>geotrace</td>
    <td>location_geotrace</td>
    <td>Please, walk through the location boundaries</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td></td>
    <td>${geo_type}='geoshape'</td>
</tr>
<tr>
    <td>geopoint</td>
    <td>location_geopoint</td>
    <td>Please, select a point</td>
    <td></td>
    <td>yes</td>
    <td></td>
    <td></td>
    <td></td>
    <td>${geo_type}='geoshape'</td>
</tr>
</tbody>
</table>


Catatan bahwa Anda mungkin perlu menggunakan pilihan _Paste Special_ dan pilih Text pada jendela selanjutnya. 

![](/assets/allgeo-modify-2.png)

Selanjutnya, Anda perlu menambahkan pilihan berikut pada tab Choices dari lembar kerja Anda. Anda mungkin perlu menyalin teks dibawah ini menggunakan pilihan _Paste Special_ .

<table>
<tbody>
<tr>
    <td>geo_type</td>
    <td>geoshape</td>
    <td>Drawing coordinates on a map</td>
</tr>
<tr>
    <td>geo_type</td>
    <td>geotrace</td>
    <td>Walking around the boundaries</td>
</tr>
<tr>
    <td>geo_type</td>
    <td>geopoint</td>
    <td>Select a location point</td>
</tr>
</tbody>
</table>

Pada gambar di bawah ini, kolom isian di atas telah disalin pada sebuah kuesioner minimal. 

![](/assets/allgeo-modify-3.png)

Sekarang, ketika kolektor data mengumpulkan data di lapangan, mereka dapat memilih metode pengumpulan data yang terbaik: GeoTrace, GeoPoint or GeoShape.

##### Langkah-Langkah Membuat Kuesioner yang Disesuaikan oleh Anda

Hal pertama yang perlu Anda lakukan adalah memikirkan pertanyaan yang akan Anda ajukan pada saat mengumpulkan data. 

1. Identifikasi pertanyaan Anda. Informasi apa yang Anda butuhkan untuk dikumpulkan dalam proyek Anda? 

2. Identifikasi setiap tipe data dari tiap pertanyaan Anda. Tipe data seperti apa yang cocok untuk setiap pertanyaan - sebuah tanggal? Isian teks? Atau pilihan berganda? 

3. Identifikasi kemana setiap pertanyaan akan diajukan. Apakah pertanyaan tersebut terkait dengan sebuah kelompok, lokasi, hubungan, atau hal yang lain? 

Setelah Anda memikirkan hal-hal tersebut, Anda dapat memulai menambahkan pertanyaan Anda pada bagian yang sesuai. 

Sebelum mengupload kuesioner Anda ke dalam proyek, pastikan bahwa: 

* seluruh  `types` (tipe pemasukan data) Anda sama dengan yang terdaftar pada XLSForm dan memiliki ejaan yang benar. 
* seluruh `names` ditulis dalam huruf kecil dan tidak mengandung spasi. 
* seluruh `list_names` pada tab Choices sama dengan nama yang Anda berikan pada pilihan ganda Anda di tab Survey. 
* seluruh `form_ids` berbeda (unik), tidak memiliki spasi, dan dimulai dengan sebuah huruf kecil. 

Salah ejaan dan format yang tidak konsisten dana menyebabkan kesalahan saat Anda mengumpulkan data. Untuk itulah kami sangat merekomendasikan Anda untuk melakukan uji coba pengumpulan data sebelum pergi ke lapangan. 

Jika Anda memiliki permasalahan dengan kuesioner Anda, jangan ragu untuk [menghubungi kami](http://cadasta.org/contact/) kapanpun - kami hadir untuk membantu pengumpulan data Anda.
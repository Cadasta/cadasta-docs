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

##### Dropdown with All GeoTypes (GeoTrace, GeoPoint & GeoShape)

In some cases, you may want to give your data collectors the option to choose collecting data using GeoTrace, GeoPoint or GeoShape. If you do, you can modify to your form to make this possible. Alternatively, you can build out your questionnaire [starting from this one](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire-all-geo.xlsx). 

If you'd like to update an existing questionnaire, here's what you need to do. 

In the **Survey tab** of your questionnaire, add three rows just below row 11. 

![](/assets/allgeo-modify-1.png)

Then, copy and paste the below into rows 11 - 14. 

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


Note that you may need to use the _Paste Special_ option and select Text in the pop-up window that follows.

![](/assets/allgeo-modify-2.png)

Next, you'll need to add the following options to the the Choices tab of your spreadsheet. Again, you may need to paste this using the _Paste Special_ option. 

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

In the image below, the fields above have been pasted into a minimum questionnaire. 

![](/assets/allgeo-modify-3.png)

Now, when data collectors are collecting data in the field, they can choose which data collection method is best: GeoTrace, GeoPoint or GeoShape.

##### Steps to Creating Your Custom Questionnaire

The first thing you need to do is think through the questions you'll be asking in your data collection.

1. Identify your questions. What information do you need to collect in your project? 

2. Identify each question's data entry type. What kind of  entry would work best for each question - a date? A text field? A drop-down or multiple choice?

3. Identify where each question should go. Is this question about a party, location, relationship, or something else?

Once you've thought this through, you can start adding your questions to their appropriate section.

Before uploading your questionnaire to your project, check to make sure that:

* all of your data entry `types` match those listed on [XLSForm](http://xlsform.org/#question-types) and are spelled correctly. 
* all of your `names` are lowercase and contain no spaces. 
* all of your `list_names` in the Choices tab match the name you've given to your dropdowns in the Survey tab.
* all of your `form_ids` are distinct, contain no spaces, and start with a lowercase letter.

Simple misspellings and formatting inconsistencies can cause errors when it's time to collect data. For this reason, we highly recommend testing your data collection before heading out to the field. 

If you're having trouble with your questionnaires, don't hesistate to [contact us](http://cadasta.org/contact/) at any time - we're here to help you get your data collection just right.

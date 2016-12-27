# Catatan Proyek: Lokasi, Kelompok, Hubungan, dan Sumber Daya

* [Ringkasan](#overview)
* [Lokasi Proyek, Tipe Lokasi, dan Perolehan Lokasi](#project-locations)    
* [Kelompok dan Hubungan Mereka pada sebuah Lokasi](#location-relationships)
* [Sumber Daya Proyek](#project-resources)

### Ringkasan {#overview}

Dalam sebuah proyek apapun, Anda dapat bekerja dengan jumlah [lokasi](#project-locations) yang berbeda. Sebagai contoh, dalam sebuah wilayah hutan, mungkin terdapat beberapa batas taman nasional dan juga sebuah bangunan yang mungkin perlu Anda lacak. 

Setiap lokasi ini mungkin telah memiliki [hubungan](#relationships) dengan salah satu [kelompok](#parties) atau lebih. Sebagai contoh, sebuah taman kemungkinan dapat dimiliki oleh pemerintah, tetapi satu grup komunitas mungkin memiliki akses khusus pada taman tersebut. Setiap kelompok ini memiliki hubungan terhadap sebagian tanah. Hubungan ini dikenal sebagai [kepemilikan](#tenure) mereka. Seringkali terdapat banyak [sumber daya](#project-resources) untuk melacak hubungan kepemilikan tersebut, seperti foto, surat, dan akte.

Platform Cadasta dirancang untuk menghadapi kompleksitas ini. Bagian ini menjelaskan bagaimana Platform ini dapat mengatur pelacakan lokasi, kelompok, hubungan, dan seluruh sumber daya yang terkait. 

### Lokasi Proyek, Tipe Lokasi, dan Perolehan Lokasi {#project-locations}

#### Menambah sebuah lokasi {#adding-a-location}

Dari halaman utama proyek, pilih **Tambah lokasi** atau **Tambah sebuah lokasi**: 

![](/assets/add-project-location.png)

Pada halaman selanjutnya, Anda akan ditanyakan untuk menggambar lokasi Anda pada peta sebagai sebuah titik, garis, bentuk, atau persegi. 

![](/assets/project-location-info.png)

Di dini, Anda juga akan diminta untuk meyediakan informasi terkait lokasi Anda (ditunjukan di sebelah kanan). Jika Anda menggunakan [kuesioner minimal](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx), Anda hanya perlu untuk menentukan tipe lokasi. 

Jika Anda menggunakan [kuesioner standar](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx), Anda akan ditanyakan untuk menetukan hal-hal berikut (seperti yang ditunjukan di atas):

* [Tipe lokasi](#location-types)
* Nama lokasi
* Kualitas Unit Spasial
* [Bagaimana lokasi diperoleh](#location-acquisition), 
* Kapan lokasi tersebut diperoleh, dan
* Catatan lokasi.

Ketika Anda selesai, simpan lokasi Anda. 

Untuk mengakses lokasi ini, klik pada lokasi tersebut pada halaman utama proyek. 

![](/assets/access-project-location.png)

#### Tipe Lokasi {#location-types}

Tipe lokasi menentukan tipe lokasi yang akan Anda upload. Berikut ini adalah tipe lokasi yang termasuk dalam [kuesioner standar](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx):

* **Parsel** - sebuah plot tanah.
* **Batas Komunitas** - sebuah batas resmi atau tidak resmi antara dua kelompok masyarakat.
* **Bangunan** - jenis struktur apapun.
* **Apartment** - sebuah apartemen atau bangunan apartemen. 
* **Jangkauan Proyek** - batas proyek keseluruhan. 
* **Hak Pakai** - sebuah hak yang memperbolehkan seseorang atau sekelompok masyarakat untuk melalui tanah pihak lain.
* **Koridor Utilitas** - sebuah jalur, baik di atas tanah maupun di bawah tanah, yang diperuntukan untuk jalur utilitas seperti listrik dan air. 
* **Batas Taman Nasional** - batas di antara sebuah taman nasional dan jenis tanah lainnya.
* **Lain-lain** - tipe lokasi lainnya yang tidak termasuk dalam kategori Anda. 

Untuk mengubah tipe lokasi yang Anda gunakan, [ubah kuesioner Anda](08-XLSForms.md). 

#### Perolehan Lokasi {#location-acquisition}

Jika Anda menggunakan kuesioner standar untuk pengumpulan data Anda, Anda akan diminta untuk menentukan bagaimana lokasi diperoleh. Anda dapat memilih salah satu dari kategori berikut ini: 

* BH - Kontaktual Bagi Hasil
* PA - Pengaturan Adat
* HB - Hibah
* RT - Rumah Tinggal
* PI - Penghuni Informal
* WA - Warisan
* KO - Kontrak 
* HM - Pembelian Hak Milik
* SW - Sewa
* LA - Lainnya

### Kelompok dan Hubungan Mereka pada sebuah Lokasi {#location-relationships}

#### Kelompok{#Parties}

Kelompok merupakan kumpulan individu, grup ata korporat yang memiliki hubungan pada satu lokasi atau lebih pada proyek Anda. 

* **Individual** adalah satu orang, misalnya seorang pemilik lahan atau penyewa. 

* **Grup** adalah kumpulan dari orang-orang yang mungkin tidak memiliki organisasi resmi yang tercatat, misalnya suku, grup komunitas atau keluarga. 

* **Korporat** adalah organisasi seperti perusahaan, misalnya organisasi bukan pemerintah, atau organisasi pemerintahan. 


#### Hubungan {#relationships}

Lokasi apapun memiliki sebuah hubungan dengan sejumlah [kelompok](#parties). Misalnya, sebuah kecamatan mungkin memiliki sebuah koridor utilitas, dimana komunitas lokal mungkin menggunakannya sebagai suatu hak pakai.


#### Menambahkan sebuah Hubungan {#adding-a-new-relationship}

Untuk menambahkan sebuah hubungan baru dari satu lokasi proyek, klik pada tab Hubungan. Kemudian, klik pada **Tambah hubungan**. 

![](/assets/add-location-relationship.png)

Pada jendela yang muncul, pertama Anda akan ditanyakan untuk memilih salah satu kelompok yang tersedia atau membuat sebuah kelompok baru. 

![](/assets/add-new-relationship-popup.png)

Jika Anda membuat sebuah kelompok baru, maka Anda harus memasukan: 

* Nama kelompok, 
* Tipe kelompok (individual, grup, atau korporat), dan
* Catatan kelompok. 

Selanjutnya, Anda akan ditanyakan untuk menambah rincian hubungan: [tipe kepemilikan](#tenure-type) dan catatan terkait kepemilikan. 

Ketika Anda selesai menambahkan catatan terkait hubungan, klik simpan. 

#### Tipe Kepemilikan {#tenure-type}

**Tipe kepemilikan** menunjukan tipe dari kepemilikan atau hak yang dimiliki sebuah kelompok terkait satu lokasi. Pada Platform Cadasta, Anda dapat menentukan kepemilikan dari sebuah kelompok dalam sejumlah cara. 

* Hak Karbon
* Hak Konsesi
* Hak Adat
* Hak Pakai (Easement)
* Hak Pakai (Equitable Servitude)
* Hak Milik
* Hak Guna Usaha (Ternak)
* Hak Guna Usaha (Berburu/Memancing/Pertanian)
* Hak Atas Tanah Adat
* Hak Bersama
* Kontrak
* Kontrak Jangka Panjang
* Hak Mineral
* Kependudukan (Tanpa Dokumen Hak)
* Kontrak (Sub-kontrak Terdaftar)
* Hak Milik (Bersama)
* Hak Milik Bersama (Tak Terbagi)
* Hak Air

Untuk mempelajari lebih lanjut mengenai istilah tersebut, lihat glosarium dari [Focus on Land di Africa](http://www.focusonland.com/resources/glossary/#e). 

### Sumber Daya {#project-resources}

Proyek hak tanah dapat terdiri dari seluruh jenis pencatatan - misalnya dokumen resmi, surat, gambar, dan sebagainya. Beberapa dokumen pencatatan mungkin dapat terkait dengan beberapa lokasi dalam sebuah proyek, atau satu lokasi, atau mungkin hanya terkait proyek secara umum. 

Platform Cadasta memiliki rancangan untuk mengatur kompleksitas ini dengan mengatur sumber daya ke dalam beberapa jenis:

* Sumber daya berkaitan dengan satu lokasi spesifik, 
* Sumber daya berkaitan dengan satu kelompok, dan
* Sumber daya berkaitan dengan proyek pada umumnya. 


####Menambahkan sebuah Sumber Daya Baru {#adding-new-resource}

Terdapat beberapa cara untuk menambahkan sebuah sumber daya baru, bergantung pada hal yang terkait sumber daya tersebut.

Jika Anda menambahkan sebuah **sumber daya lokasi proyek**, pilih **Tab sumber daya** dari halaman rincian lokasi, kemudian **Tambah sumber daya** 

![](/assets/add-location-resource.png)

Untuk menambahkan sebuah **sumber daya yang terkait dengan satu kelompok tertentu**, arahkan ke **Tab hubungan** dari halaman rincian lokasi. Kemudian, pilih kelompok yang Anda ingin tambahkan pada sebuah sumber daya.

![](/assets/resource-party-1.png)

Pada bagian bawah halaman kelompok tersebut, pilih tombol **Lampirkan** dan upload sumber daya Anda.

![](/assets/resource-party-2.png)

Untuk menambahkan sebuah **sumber daya yang terkait dengan proyek pada umumnya**, arahkan ke halaman rincian proyek dengan mengklik **Ringkasan**. Kemudian klik **Sumber Daya.** 

![](/assets/resources-from-overview.png)

Dengan mengklik pada sumber daya dari halaman rincian proyek akan membawa Anda ke koleksi proyek, dimana koleksi proyek akan memiliki seluruh sumber daya yang terkait pada proyek Anda.

![](/assets/project-library.png)

Untuk menambah sebuah sumber daya saat Anda berada dalam katalog, klik **Tambah** pada kanan atas. 

Kemudian, Anda akan dipandu oleh sebuah jendela yang akan muncul. Di sini, Anda akan diminta untuk meng-upload sebuah berkas, dan memberikan berkas tersebut nama beserta deskripsinya.

![](/assets/project-library.png)

Tipe berkas yang diterima adalah:

* .pdf
* .mp3
* .mp4
* .doc
* .docx
* .jpg
* .png
* .gif
* .tiff
* .xls
* .xlsx
* .xml (Tipe berkas ini akan berguna jika Anda ingin mengupload dokumen .gpx; Anda hanya perlu untuk mengubah ekstensi berkas dari .gpx ke .xml)
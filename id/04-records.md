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

#### Location Acquisition {#location-acquisition}

If you're using the standard questionnaire for your data collection, you'll be asked to define how your location was acquired. You can choose from one of the following categories:

* CS - Contractual Share Crop
* CA - Customary Arrangement
* GF - Gift
* HS - Homestead
* IO - Informal Occupant
* IN - Inheritance
* LH - Leasehold 
* PF - Purchased Freehold
* RN - Rental
* OT - Other

### Parties and Their Relationship to a Location{#location-relationships}

#### Parties{#Parties}

Parties are the individuals, groups or corporations who have a relationship to one or more of the locations in your project.

* **Individuals** are single people, like a landowner or lessee.

* **Groups** are collections of people who may not have an officially documented organization, such as a tribe, community group or family.

* **Corporations** are organizations like companies, NGOs, or government bodies.


#### Relationships {#relationships}

Any given location has a relationship to a number of [parties](#parties). For example, a municipality may own a utility corridor, which a local community may use as a right-of-way. 


#### Adding a New Relationship {#adding-a-new-relationship}

To add a new relationship for a project location, clik on the Relationships tab. Then, click on **Add relationship**. 

![](/assets/add-location-relationship.png)

In the pop-up that follows, you'll be first asked to either choose from an existing party or add a new one. 

![](/assets/add-new-relationship-popup.png)

If you're adding a new one, you'll need to provide:

* Party name, 
* Party type (individual, group, or corporation), and
* Party notes. 

Next, you'll be asked to add relationship details: including the [tenure type](#tenure-type) and notes about the tenure. 

When you're done adding notes about the relationship, click save. 

#### Tenure Type {#tenure-type}

**Tenure type** refers to the type of ownership or right that a party may have with regards to a location. In the Cadasta Platform, you can define a party's tenure type in a variety of ways. 

* Carbon Rights
* Concessionary Rights
* Customary Rights
* Easement
* Equitable Servitude
* Freehold
* Grazing Rights
* Hunting / Fishing / Harvest rights
* Indigneous Land Rights
* Joint Tenancy
* Leasehold
* Longterm Leasehold
* Mineral Rights
* Occupancy (No documented rights)
* Tenancy (Documented Sub-Lease)
* Tenancy in Common
* Undivided Co-Ownership
* Water Rights

To learn more about many of these terms, see the glossary from [Focus on Land in Africa](http://www.focusonland.com/resources/glossary/#e). 

### Resources {#project-resources}

Land rights projects can come with all kinds of documentation - like legal documents, letters, pictures and more. Some of that documentation may relate to multiple locations within a project, or to one location, or it may just relate to the project in general.

The Cadasta Platform is set up to handle this kind of complexity, organizing resources into three different types:

* Resources pertaining a specific location,
* Resources pertaining to a party, and
* Resources pertaining to the project generally.


####Adding a New Resource {#adding-new-resource}

There are a few ways to add a new resource, depending on what it pertains to.

If you're adding a **project location resource**, select the **Resources tab** from the location overview page, and then **Add resource.**

![](/assets/add-location-resource.png)

To add a **resource that pertains to a certain party**, go to the **Relationships tab** from the location overview page. Then, select the party you'd like to add a resource for.

![](/assets/resource-party-1.png)

At the bottom of that party's page, select the **Attach** button and upload your resource.

![](/assets/resource-party-2.png)

To add a **resource that pertains to the overall project**, go to the project's overview page by clicking **Overview**. Then, click **Resources.** 

![](/assets/resources-from-overview.png)

Clicking on resources from the project overview page will take you to your project library, which will have all of the resources related to your project.

![](/assets/project-library.png)

To add a resource while you're in the the library, click **Add** on the upper right.

From any of these starting points, you'll be led to a pop-up window. Here, you'll be asked to upload a file, and give it a name and description. 

![](/assets/project-library.png)

Acceptable file types are:

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
* .xml (This file type is particularly useful if you need to upload a .gpx document; just change the file extension from .gpx to .xml)
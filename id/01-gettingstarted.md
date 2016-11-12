# Mulai Menggunakan

* [Tentang Struktur Cadasta](#how-cadasta-is-organized)
* [Panduan Cepat untuk Mulai Menggunakan](#quick-guide-to-getting-started)
* [Membuat Akun Baru](#createnewaccount)

### Tentang Struktur Cadasta {#how-cadasta-is-organized}

Meski siapapun dapat menggunakan Platform Cadasta, platform ini dirancang terutama bagi organisasi yang mencatat hak-hak atas tanah beserta sumber daya dari individu dan komunitas. Struktur dari platform ini disamakan dengan rancangan tersebut. 

Sebelum memulai, sangat penting untuk memahami struktur ini dan bagaimana mereka bekerja secara keseluruhan. 

![](/assets/diagram-organizations-projects-members-orig.png)

* Inti dari platform Cadasta adalah sejumlah **[proyek](03-projects.md)**. Sebuah proyek melingkupi satu wilayah geografi yang spesifik, dari sebuah parsel kecil lahan hingga keseluruhan dunia. Dalam wilayah proyek yang ditentukan, terdapat sejumlah **lokasi** proyek. Sebuah proyek juga memiliki sejumlah **anggota proyek**, dimana setiap anggota akan memiliki perizinan tertentu pada proyek tersebut. 

* Setiap proyek harus dimiliki oleh sebuah **[organisasi](02-organizations.md)**. Sebuah organisasi mewakili satu badan organisasi masyarakat dengan tujuan tertentu. Kebanyakan organisasi adalah organisasi-organisasi bukan pemerintah yang membantu komunitas untuk mencatat hak-hak tanah mereka. Dalam sistem Cadasta, orang-orang yang mewakili satu organisasi yang disebut **anggota organisasi**.

* Struktur data yang Anda kumpulkan dalam proyek Anda bergantung pada bagaimana Anda menyusun **kuesioner** Anda, dimana dibutuhkan untuk menyiapkan proyek Anda. 

![](/assets/diagram-resources.png)

* Sebagai tambahan untuk menyimpan data geografis, setiap proyek juga berhak untuk menyimpang sejumlah **arsip**. Arsip-arsip ini dapat termasuk **sumber daya** terkait lokasi, misalnya dokumen yang di-scan, gambar, video, suara testimoni atau apapun yang dapat membantu dalam pencatatan hak-hak tanah. Seluruh lokasi sumber daya akan disimpan dalam **koleksi** proyek. Sebagai tambahan, setiap proyek juga dapat menandai **hubungan** dalam berbagai **kelompok** yang mungkin berhubungan dengan satu lokasi atau lebih. 

Jika Anda melihat bagian-bagian ini secara ringkas, bagian-bagian tersebut akan terlihat seperti berikut ini: 

* Organisasi
  * Anggota Organisasi
  * Proyek
    * Anggota Proyek
    * Kuesioner (yang akan menentukan struktur pengumpulan data Anda)
    * Lokasi Proyek
      * Hubungan
      * Sumber Daya


Pada umumnya, data untuk setiap proyek dikumpulkan di lapangan. Hal tersebut pada umumnya dapat diselesaikan menggunakan aplikasi mobile, kuesioner kertas, atau aplikasi seperti Field Papers. Platform Cadasta saat ini mendukung dua platform pengumpulan data mobile, dimana keduanya tersedia untuk digunakan di Android:

* **[Open Data Kit \(ODK Collect\)](05-odkcollect.md)**, dan
* **[Geographical Open Data Kit \(GeoODK Collect\)](06-geoodkcollect.md)**.

Kedua aplikasi tersebut terintegrasi dengan kuesioner yang Anda gunakan untuk pengumpulan data dan memungkinkan data tersebut disimpan dalam platform Cadasta. 

Kapanpun Anda membutuhkan data dan sumber daya keluar dari platform, yang Anda lakukan hanyalah  **[men-download](07-download.md)** data tersebut.

### Quick Guide to Getting Started {#quick-guide-to-getting-started}

To get started, follow the steps below! For more information and images, follow the links on each step.* 

1. **[Create your new account](#createnewaccount)** by clicking **register** and entering your name, email, and a few other key pieces of information. _Note that you have up to 48 hours to verify your account using the verification link sent to your registered email address._

2. Next, you need to be added to an organization. To do this, contact your organization's administrator to add you as an organization member. Note that you can be added to multiple organizations in the Cadasta sytem.  

    * If you're going to be the administrator of a new organization in Cadasta, you can **[create your organization](02-organizations.md)** by selecting the **Organizations** button and then **Add**. You'll be asked to enter some basic information about your organization and save it. The person who creates an organization becomes the organization's administrator by default. Note that most users will not create their own organizations; instead they will be added to one. 

3. Next, you need to be added to a project by your organization or project administrator. Administrators can also **[create new projects](03-projects.md)** and add members to it. As part of the project creation process, you'll be asked to upload a questionnaire, which creates the structure for your data collection. You can use either the [minimum questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/minimum_cadasta_questionnaire.xlsx) or the [standard questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx), or modify one of them to meet your needs. You'll also need to add project members, project locations, and project resources as needed. 

4. Once you have an account, organization, and project, it's time to start gathering data! If you need to collect data in the field, you can use either [ODK Collect](/en/05-odkcollect.md) or [GeoODK Collect](/en/06-geoodkcollect.md), which are both applications for Android. If you don't need to be in the field, you can use the Cadasta Platform directly.

_* For printed versions, go to the associated section in the document._

### **Creating a New Account** {#createnewaccount}

![](/assets/sign-in-register-arrow.png)

To get started with Cadasta, the first thing you need to do to is create a user account.

1. If you're just trying out the Platform, navigate to [demo.cadasta.org](https://demo.cadasta.org). Partners with live projects should create accounts at [platform.cadasta.org](https://platform.cadasta.org).
2. Select **Register** from the upper right of the screen. 
3. Input a username, valid email address, password and your full name.
4. Select **Register**.

After a successful login, you'll return to the home screen, where you can view public projects and organizations.


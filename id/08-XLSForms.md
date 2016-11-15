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
* Pilihan, dan
* Pengaturan.

Tab **Survey** menunjukan skema pengumpulan data secara menyeluruh.

![](/assets/minimum-survey.png)

Area yang berwarna abu-abu adalah kolom isian pada Platform Cadasta yang akan bekerja. Beberapa dari kolom isian tersebut \(contohnya `deviceid`\) digunakan dibalik proses, sehingga Anda tidak akan melihatnya di dalam Platform, ODK, atau GeoODK. _(Catatan! Jangan mengubah apapun yang ada di dalam kotak abu-abu!)_

Penting bagi Anda untuk mengetahui tiga kolom pertama: 
* `tipe` menentukan tipe data yang Anda tambakan - misalnya teks, tanggal, sebuah pilihan, atau lainnya. 
* `nama` menentukan variabel yang digunakan untuk pemasukan data. Tidak boleh ada dua nama yang sama! 
* `label` menunjukan teks yang akan dilihat pada formulir. Kolom isian yang berwarna putih dapat dimodifikasi sesuai kebutuhan. 

Tab **Pilihan** tab is where the choices for all the drop-down menus are stored.

![](/assets/minimum-choices.png)

For example, the `respondent` entries Group, Individual and Corporation (A2 - A4 in the image above) correspond with this dropdown menu in the Add Relationship popup:

![](/assets/relationship-dropdown.png)

The **Settings** tab shows you the `form_id` and title of the questionnaire. You'll use this ID when you set up data collection with ODK and GeoODK.

Make sure all of the questionnaires in your organization have unique form IDs. Otherwise, they won't load, and you'll default to using the original form with that ID. Also be sure to create names that start with lowercase letters and contain no spaces.

### The Standard Questionnaire {#standard-form}

[The standard questionnaire](https://s3-us-west-2.amazonaws.com/cadasta-resources/sample-forms/standard_cadasta_questionnaire.xlsx) has all the same questions as the mininimal version, with quite a few added. You can see many of these choices indicated in the **Survey** tab.

![](/assets/standard-survey.png)

The image above shows all the entries that will be collected in addition to the minimal information. These entries are organized by section:

* Location Attributes \(rows 22-28\)
* Default Party Attributes \(rows 20-32\)
* Individual Party Attributes \(rows 34-38\)
* Group Party Attributes \(rows 40-43\)
* Party Relationship Attributes \(45-47\)
* Tenure Relationship Attributes \(49-51\)

Each of these sections relates to a data collection window in the cadasta platform.

The **Choices** tab has the same options as the minimal questionnaire, with some additional drop-down choices as well.  

![](/assets/standard-choices-2.png)

For example, rows 38-47 show the choices for the different types of location acquisitions, which correspond with row 25 on the Survey tab (above).

The **Settings** tab of the standard questionnaire is exactly the same as it is in the minimal version - providing the `form_id`, which is your identifier for the questionnaire in ODK or GeoODK.

![](/assets/standard-settings.png)

Make sure all of the questionnaires in your organization have unique form IDs. Otherwise, they won't load, and you'll default to using the original form with that ID. Also be sure to create names that start with lowercase letters and contain no spaces. 

### Customizing Your Questionnaire {#customizing-your-questionnaire}

If you need to collect different data than what's in the standard questionnaire, and more than what's in the minimum questionnaire, you can customize these forms to meet your needs. Any entry with a white background can be modified. Fields with a gray background need to remain as they are in order for everything to work.

#### Basic Customization

##### Deleting Unnecessary Fields

If there's a field that you don't want to include, simply delete its row from the survey tab of the questionnaire. To do this in Excel, right-click the row and then select Delete.

_**Important note!** Remember that fields in gray cannot be deleted or modified; only delete rows that have completely white backgrounds._

##### Editing Drop-Down Fields

To edit a field in a drop-down menu, navigate to the Choices tab. There, you can modify the `name` and `label` of the fields as needed.

For example, to add a new field to the location acquisition dropdown \(`l_acquired_how`\):

* Add a new row, and give it a `list_name` of `l_acquired_how`.
* Add a new name and label.

In the example below, a new category for the dropdown \("Unknown"\) has been added to the questionnaire.

![](/assets/land-acquision-new-row.png)

Once that questionnaire is saved and loaded into the project, the new "Unknown" option will appear in the dropdown under, "How was this location acquired?"

![](/assets/standard-new-field.png)

#### GeoTrace, GeoShape and GeoPoint

In your location data collection, you may choose to collect point, line, or polygon data. In both the standard and minimum questionnaires, you have the option to choose one of these using `geopoint`, `geotrace`, or `geoshape`. 

* `geotrace` records a line of two or more GPS coordinates. It's also the default setting of both the minimum and standard questionnaires. With `geotrace`, location pins are added based on the user's GPS coordinates. 

* `geoshape` records a polygon made of multiple GPS coordinates, which are drawn on-screen. 

* `geopoint` collects single points of data based on the user's GPS coordinates. 

To change what data type you're collecting, modify cell A11 on either your standard or minimum questionnaire. 

#### Advanced Customization

If you need to do more than simply edit a few existing fields, then advanced customization may be for you.

##### Data Entry Types {#data-types}

To fully take advantage of customizing the questionnaire, it's important to figure out which data entry type will work best for the kind of information you're collecting. Some of the most common ones that you'll use are:

* `text` - which specifies that you're collecting basic text.
* `date` - which specifies that you're logging the date.
* `select_one` - which specifies that you're using a dropdown menu

![](/assets/standard-survey-example.png)

You can see each of these at work in the above example, taken from the survey tab of the standard questionnaire.

Notice that `select_one` - the dropdown option - requires identifying a set of choices to go with it. In the example above, the first dropdown menu specifies that cell A24 is linked to the choices tagged `l_quality_choices`. In the Choices tab, you can see the different options for `l_quality_choices`:

![](/assets/standard-choices-example.png)

These options will appear in the dropdown when it's selected.

In addition to these basic data types, [XLSForm offers many different data types for you to choose from](http://xlsform.org/#question-types).

![](/assets/xls-form-question-types.png)

The type you need depends on the kinds of questions you need to ask. For example, if you need to collect an audio sample from an interviewee, you could select `audio`, which will prompt you to take an audio recording.

##### Questionnaire Sections

![](/assets/standard-survey.png)

The customizable portion of the questionnaire has been organized into the following sections: 

* **Location Attributes** relate to to information about the location - like its name and boundaries. 

* **Default Party Attributes** specify the information that you collect about any party, be it an individual, group, or corporation.

* **Individual Party Attributes** and **Group Party Attributes** each provide information specific to whether a party is an individual or group.

* **Party Relationship Attributes** is for information specific to the relationship between a party and the location. 

* **Tenure Relationship Attributes** specify information about a party's tenure on the land.

Each of these sections relates to a piece of the Cadasta Platform's internal workings. In order for your questions to appear in the platform, they need to be in one of these sections.

The below image is taken from a custom questionnaire used by one of our partners. Here, they've added a number of custom fields in the `party_attributes_default` section:

![](/assets/example-xls-1.png)

It is possible to create new sections, as another Cadasta partner has done below. Here, they've added a section on witnesses:

![](/assets/example-xls-2.png)

If you'd like to create new sections or significantly customize your questionnaire, we highly recommend that you [contact us](http://cadasta.org/contact/) first. We're here to help! 

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

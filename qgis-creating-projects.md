
## Creating Projects {#creating}

_Please note that this feature is in development. At the moment, you can only upload the required Cadasta fields, geometries and location attributes (no party or relationship attributes)._

In addition to downloading an existing project from the Cadasta platform, you can create new Cadasta projects using QGIS as well. 

Creating a project with QGIS allows quite a bit of flexibility when it comes to using different data formats. You can upload common layer types, such as: 

* Shapefiles, 
* Geojson, 
* KML,
* GPX, 
* CSV,
* Database layers, like SpatialLite, postGres

And any other layer that is supported by QGIS. _Learn more about supported data formats at <a href="https://docs.qgis.org/2.6/en/docs/user_manual/working_with_vector/supported_data.html" target="_blank">docs.qgis.org</a>._

If you plan to start a project on QGIS from existing data, and then upload it to the Cadasta platform, then follow the following step
### 1. Prep the dat

> Examples of shapefile data; gpx; csv with format

A layer will not properly upload into the Cadasta system unless it has values for four required fields. The purpose of prepping the data is to make sure that it works with some of the necessary fields in Cadasta: 

* Location types
* People / Party types
* People / Party name
* Relationship / Tenure types

Follow these steps to fill in the Cadasta fields and values so that the layer will be properly uploaded:

1. Load the layer in QGIS. You can drag or drop the layer in or you can use the "Layer"< "Add Layer" setting. And then choose the option that relates best to your layer.  For example, 
To add these columns in your attribute table of your layer, you will need to right click on the layer. These fields need to be formatted like this:

> add formatting examples

> Katrina, in the below paragraph, you talk about layers. How do these layers come into play??

You can use the Table Manager plugin or Toggle Edit Tool for editing the layer if need be. You will also need to make sure there a column that can be used for the party name field. 


Please note that creating Cadasta projects using QGIS really only works with location data, with limited capabilities with regards to information about relationships, parties, and resources. If you are starting a project using a lot of that kind of information, Cadasta recommends starting that project on the platform.

### 2. Create Your Project

Once the data is prepped, select `Vector > Cadasta > Create Project`. This will open a popup window like the one shown below:

> add image

Here, fill out the general project information. Note that the only required field is the project name. 

> Katrina, let's talk about the paragraph below: what if the data isn't formatted as a table?

Beware that if the data does not have the proper required fields or has null values in some of those columns then the project information will be saved without the data. You may need to use a different project name if there are data issues)

![image of step 1]

3. Match up the Cadasta required fields with your layer's column headers.

4. Submit the data

### Part III. Troubleshooting

At the moment there is no easy way to upload party and relationship field data. It is also a little bit trickier to set up select one or select multiple fields. We recommend that you create a questionnaire on the web, download the project with the QGIS project and use the "Update Project" option for being able to upload location layers with party and relationship data.

You can use the "Advanced" settings for adjusting the questionnaire json. (will write up more later)

Notes for more info:
- format of CSVs-- WKT? 
- need to check what happens if you edit the field type in the advanced settings
- need to check about how to upload party and relationship fields via advanced settings














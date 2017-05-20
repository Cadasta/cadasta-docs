
## Creating Projects {#creating}

_Please note that this feature is in development. At the moment, you can only upload the required Cadasta fields, geometries and location attributes (no party or relationship attributes)._

In addition to downloading an existing project from the Cadasta platform, you can create new Cadasta projects using QGIS as well. 

Creating a project with QGIS allows quite a bit of flexibility when it comes to using different data formats. You can upload common layer types, such as: 

* Shapefiles, 
* Geojson, 
* KML,
* GPX, 
* CSV (geometry must be in WKT),
* Database layers, like SpatialLite, postGres

And any other layer that is supported by QGIS. _Learn more about supported data formats at <a href="https://docs.qgis.org/2.6/en/docs/user_manual/working_with_vector/supported_data.html" target="_blank">docs.qgis.org</a>._

### 1. Prep the data file

> Examples of shapefile data; gpx; csv with format

A layer will not properly upload into the Cadasta system unless it has values for four required fields. You will likely need to add three columns to your The purpose of prepping the data is to make sure that it works with some of the necessary fields in Cadasta: 

* Location types
* People / Party types
* People / Party name
* Relationship / Tenure types

Follow these steps to fill in the Cadasta fields and values so that the layer will be properly uploaded:

1. Load the layer in QGIS. You can drag or drop the layer in or you can use the "Layer"> "Add Layer" setting. And then choose the option that relates best to your layer.  For example, if you are loading up a CSV file then you can use the "Add Delimited Text File" option. 
2. Once the layer is loaded, right click on the layer and click "Properties".
3. Click the "Fields" tab on the left (fourth down).
4. Click the pencil icon, which will enable you to edit your layer. Then click the first icon that has a pencil and table. That will birng up a window where you can create a column name and choose what type of column it will be. You can label the column anything you would like-- just make sure the type is a text field.
5. Add columns for location type, party type, tenure type and party name (if you don't already have a column that you can use for a party name).
6. If you would like a quick way to populate the values of those columns, you can click "Text Edit" button on the new columns and fill out a default value.  In the default value text box, you can type in the value you would like to use (make sure to wrap the text with quotations). If you have no clue as to what to type to use then we recommend:
  * location type ==> 'PA'
  * party type ==> 'IN'
  * tenure type ==> 'FH'
7. Once the values are set, you can click "Ok" and review your work in the attribute table. Right click on the layer and select "Open Attribute Table".

If you need to do additional data clean-up, you can use the "pencil" icon, known as the Toggle Edit tool, in the attribute table to fix spelling errors or inconsistancies. You can also use a plugin called "Table Manager" if you require more aggressive editing. 

Please note that creating Cadasta projects using QGIS really only works with location data, with limited capabilities with regards to information about relationships, parties, and resources. If you are starting a project using a lot of that kind of information, Cadasta recommends starting that project on the platform.

Lastly, if you have multiple files that you would like to upload, we recommend that you merge and/or join those layers before uplaoding to Cadasta. The "Create Project" window is best used with one layer.


### 2. Create Your Project

Once the data is prepped, select `Vector > Cadasta > Create Project`. This will open a popup window like the one shown below:

> add image

Step 1: Here, fill out the general project information. Note that the only required field is the project name. 

Beware that if the data does not have the proper required fields or has null values in some of those columns then the project information will be saved without the data. You may need to use a different project name if there are data issues)

> ![image of step 1]

Step 2: Match up the Cadasta required fields with your layer's column headers.

Step 3: Submit the data

### Part III. Troubleshooting

At the moment there is no easy way to upload party and relationship field data. It is also a little bit trickier to set up select one or select multiple fields. We recommend that you create a questionnaire on the web, download the project with the QGIS project and use the "Update Project" option for being able to upload location layers with party and relationship data.

#### Advanced Questionnaire Adjustments

You can use the "Advanced" settings for adjusting the questionnaire json. The json that you see when

> Notes for more info:
> - format of CSVs-- WKT? 
> - need to check what happens if you edit the field type in the advanced settings
> - need to check about how to upload party and relationship fields via advanced settings

# Cadasta QGIS Plugin

_8 September 2017: Please note that this page is in-progress; refresh to view any changes._


* [Overview](#overview})
* [Setting up the QGIS Plugin](#setup)
* [Recommended Map Making/Printing Workflows](#map-making)
* [Recommended Uploading Workflows](#uploading)
* [Other Tips and Tricks](#other)


## Overview {#overview}

[Quantum GIS (QGIS)](http://www.qgis.org/en/site/) is a free and open source geographic information system. It's a powerful tool that's used by organizations all over the world to work with geographic data, without any cost. Now it can be used to analyze and update the data you've collected using the Cadasta platfom through a custom plugin.

Please note that this section assumes that you have already created a Cadasta account and have an active project. If you need help getting those set up, visit the first three sections of this documentation: [Getting Started](01-gettingstarted.md), [Organizations](02-organizations.md) and [Projects](03-projects.md).

This section also assumes some knowledge of QGIS and how it works. If you are unfamiliar with the platform, please visit <a href="http://www.qgis.org/en/docs/index.html">documentation.qgis.org</a>.


## Setting up the QGIS Plugin {#setup}

### 1. Download and install QGIS

Before getting started with the plugin, you will need to install QGIS. Find the version you need on the <a href="http://www.qgis.org/en/site/forusers/download.html" target="_blank">QGIS download page</a> and then follow their instructions for installation. 

If you are wondering whether you should install the 32-bit or 64-bit version, you can read more about the difference [here](https://www.digitaltrends.com/computing/32-bit-64-bit-operating-systems/).

### 2. Install & Activate the Cadasta Plugin for QGIS

Next, install and activate the Cadasta Plugin. Head to `Plugins` and click the first option `Manage and Install Plugins`. 

![install cadasta plugin](/assets/qgis-plugin-install-01.png)

A window will open up and you will have access to the list of plugins, or specialized libraries, that are available with QGIS. Scroll down until you see the "Cadasta" plugin. Click on that option to download the plugin.

![install cadasta plugin](/assets/qgis-plugin-install-02.png)

### 3. Connect to your Cadasta Account

![connect to user account](/assets/qgis-plugin-install-03.png)

Now, select `Vector > Cadasta > User Settings`. This is the window where you can switch accounts or platforms (demo vs platform).

![User settings](/assets/qgis-plugin-install-04.png)

Enter the platform you are working on (either `https://demo.cadasta.org/` or `https://platform.cadasta.org/`) and your username and password. 

Then, hit **Connect** in the lower left. Hitting "Connect" talks to the Cadasta server to make sure that If all has been done correctly, you'll get a `Success`message. 

Finally, hit **Save** so that your login credentials are saved for future use.

Once the Cadasta QGIS plugin is installed and you have connected it to your Cadasta account, you can use it to download your project data, analyze it, make maps for print and/or upload some missing data. Now you're ready to get to work! 

*Tip:* If you want to switch platforms or usernames, you must hit **Clear** on right before editing the fields. 

#### Download a Public Project to Test

Using the `demo` username and `password` password in `https://demo.cadasta.org/`, you can test out the plugin. To download the project, select `Vector > Cadasta > Download Project`. On the popup that follows, you can select any of the projects associated with your account. 

![](/assets/qgis-image-01.png)

If you're looking for a public project to download, select `Include all Cadasta public projects` from below the dropdown.

![](/assets/qgis-image-02.png)

Once you have selected your project, click **Next** to start downloading. The window will auto-close once the layers have completed downloading.

Now you should be able to see your map data in the main QGIS screen, with layers on the left.

![](/assets/qgis-image-03.png)

If you do not see your map layer, right click on the polygon/point/line layer and click "Zoom to Layer". That setting is useful for being able to track down where your spatial layer is. 

![](/assets/qgis-image-04.png)

**Note**: For some layers that have parcels spread out, the "Zoom to Layer" may not work well and you may have to select a row in the Attribute Table and zoom to that selected parcel to see the geometries. 

#### File Layers Overview

<!-- Digital maps are made using a series of geometry layers (points, lines, polygons) – for example, roads may all be on one layer, while parcel polygons are on another. The basemap, providing background and context for this data, could be on its own layer at the very bottom. Organizing data this way makes it much easier to analyze and style. 

QGIS uses this layering convention as part of its interface. You can see the layers in your project listed one the left of the platform (like in the above image). 
 -->
Each Cadasta project comes with three different layers: one for parties data, one for relationship data, and one for each type of geographic data (the points, lines, and polygons you have stored on the Cadasta platform). 

The parties and relationships layers are CSV files and do not have a visibility on the map; however, they have id fields that can be used to _join_ with the geometry layers. The relationship table can be unioned with the geometry layer and the party layer can be joined with the relationship layer. In other words, the  point, line, and polygon layers can access the party and relationship fields through a table join. _To learn more about joining data layers together, see [Joining Relationships and Parties to Location Geometry](#joining) below._

You can change the order of these layers by dragging and dropping them on top of one another.

### Joining Relationships and Parties to Location Geometry {#joining}

One of the more powerful features of QGIS is its capacity for geographic analysis. For example, for a customary rights Cadasta project, you can use QGIS to see which groups of people are using what piece of land. 

To do this, the parties and relationship data needs to be **joined** to each layer of geographic data. 

To link these layers, right click one of your map data layers and then select **Properties**. In the popup that appears, select Joins on the left, and the the green plus sign at the bottom. 

![](/assets/qgis-join-01.png)

This will take you to a new popup window where you can join the layers. 

First, join your relationships to the geometry by creating the following settings:

* Join layer: use the option ending in `/relationships`, such as `cadasta-foundation/concessions-in-liberia/relationships`
* Join field: `spatial_id`
* Target field: `id`

*Tip*: We recommend renaming your layer names if they are too long.  Also, in the join process you are able to edit the field names by clicking the bottom checkbox "Custom field name prefix". In checking that checkbox, you are able to delete all of the layer name information that you do not need. 

The settings should look something like this:

![](/assets/qgis-join-03.png)

Next, join your parties to the relationships using the following settings:

* Join layer: use the option ending in `/parties`, such as `cadasta-foundation/concessions-in-liberia/parties`
* Join field: `id`
* Target field: use the option ending in `/relationships_party_id`, such as `cadasta-foundation/concessions-in-liberia/relationships_party_id`

These settings should look something like this:

![](/assets/qgis-join-05.png)

Repeat these steps for each map layer. Now, you can run analysis to see how these fields are joined together. 

**Troubleshooting**: Sometimes, the party table does not join correctly and you see `NULL` values in all of the party fields. I have found that by removing the "Memory cache" on the file, the fields join properly. To do so, go back into the Join settings and click on the pen icon to edit the party join. Uncheck the box for "Cache join layer in virtual memory".  Then hit "Apply" and view the layer's Attribute table.

### 4. Recommended Map Making/Printing Workflows {#map-making}

Once your data is collected and stored in Cadasta, you may want to be able to print out a summary map of all of the work that you have done or be able to print out individual reports on each parcel that you have collected information on. The Cadasta plugin allows you to do this using the power of QGIS' styling and print composer. In this section, we will walk through two ways of styling and prepping the data you collected for publishing: map summary and individual parcel reports.


### Adding a Basemap

If you would like to add a background map, such as satellite imagery or OpenStreetMap, as a reference layer you can add a basemap layer using the OpenLayers plugin.

You can install the plugin from `Plugins > Manage & Install Plugins`.

Once installed, go to `Web > OpenLayers`, and then select the basemap you'd like to use. Below you can see Stamen's OSM watercolor map being used.

![](/assets/qgis-plugin-04.png)

It is not uncommon for the OpenLayer to appear above your map layer data, making it seem like your data has disappeared. To fix, drag your basemap layer to the bottom of your layers. 


#### Styling Boundary Lines

You can learn basic styling skills through various other [guides](https://www.ordnancesurvey.co.uk/docs/user-guides/cartographic-stylesheet-user-guide.pdf). We will focus on the best way to style polygons so that you can print map summaries and/or individual boundary reports:


##### (1) Map Summary

QGIS offers the ability to print overview maps for land use status and planning purposes. The steps you will need to follow for printing out a map overview are:

1. Using the layer's "properties" setting: Style the layer in a way that is visible with the basemap (if you are using one)
2. Using the layer's "properties" setting: Add labels in a neat manner (if you need access to the party's fields then you will need to [join](#joining) the layers)
3. Head to the Print Composer. And under the "Composition" settings on the right, change the document to the correct position and size you require.
4. Add the necessary scales, arrows and datum that you require (through drag and dropping the elements on the left of the document)
5. Print!

##### (2) Individual Reports

You can create dyanmic reports on individual parcels in QGIS through the Print Composer's "atlas composer" option. A great example of when you would want to do this is issuing land titles or documentations to individual land holders. 

The best way to set up the individual resports is to get a png or svg copy of an empty report and to past that in the body of the Print Composer template. Once you have the image sized correctly in the Print Composer document then you can drag text fields to where the values will be answered.

###### 1. Open up the Print Composer.

After installing the Cadasta plugin and downloading the Cadasta data collected into QGIS, open up the QGIS’ “Print Composer”. The Print Composer is a different environment than the regular QGIS view: 

![](/assets/qgis-print-00.png)

Change the “Composition” of the page with the settings on the right. For this example, change the “Orientation” to “Portrait”.

![](/assets/qgis-print-00.png)

###### 2. Set up the layer that you will want to pull data from

After setting up the document to have the paper size and orientation you require, click on the “Atlas Generation” tab on the right. This setting is where you can choose which layer of data you would like to bring in. 

Cadasta divides all of the data collected into three files (location, party and relationship). If you want to create a report that accesses data from multiple files, it is recommended that you join the cadasta files (see more on how to do this here). 

If you are only using location data or if you have joined the party and relationship columns to the location layer, then you can choose that layer as the “coverage layer” for the reports. You can also choose a field to act as the page name for when you are looping through all of the rows in your data-- an “id” or “name” field will work. 

![](/assets/qgis-print-00.png)

###### 3.  Create the Report

Using the “Print Composer” tools on the left, you can drag and drop text fields, images and map screenshots to the page.  

For values that need to be brought in dynamically, you will need to create a text box and in the “Main properties” section under the “items properties” tab, you will want to “Insert an expression…”. 

![](/assets/qgis-print-00.png)

This action opens up the “field calculator”, which lets you conduct math equations, write custom code and pull in values from your data. To pull in your data, you will want to open the “Fields and Values” then double click the field you would like to pull in and click “Save”. Alternatively, you could also write in the name of the value you wanted to pull in with this format “[% “name” %]”.

![](/assets/qgis-print-field-calc.png)

Once you have completed the three steps you should have a report template that looks like this:

![](/assets/qgis-print-00.png)

###### 4. Turn on the Atlas Preview

We have one more step to wrap up everything: turning on the “Atlas Preview” settings. 

Once we have the “Atlas Preview” settings turned on, we can click through all the different land titles that will print.  We are able to loop through each parcel/land.

Using the toggles on the top right, you can dynamically preview what each print off will look like (notice how the name of the party is what each page is named):

![](/assets/qgis-print-00.png)


### 5. Recommended Uploading Workflows

At the moment, the best way to upload data to Cadasta is through converting the data into a csv or XLS file and uploading it on the web. The QGIS plugin only supports uploading location attributes consistently. 


#### (1) Data Prep

If you would like to try uploading data via the plugin, we recommend that you only use a couple of rows of data for those trials. If the data upload ends up erroring out then you only have a couple of errors on the server with a smaller upload. 

There are a number of rules that layers must follow to upload in Cadasta: 

	#1. The layer must have a `location_type` field
	#2. The layer must have a geometry in a supported projection (CRS EPSG: 3857)
	#3. Data formats must be precise. If you are uploading a data, make sure that the field is a date field. 
	#4. There must not be any white space in integer or date fields. 


### Other Tips and Tricks {#other}

##### Recommended Plugins

You can do most of your map making and data prep with the built-in tools that QGIS offers. However, if you would like to try a few more tools the Cadasta team has had good experience with these following plugins: 

* **OpenLayers** provides a selection of basemaps - including OpenStreetMap and satellite imagery - so that you can see your map data in context of the area around it. 

* **TableManager** makes it easier to edit the attribute tables associated with your spatial data. 

* **mmqgis** is a set of Python plugins for manipulating vector map layers in Quantum GIS. 

All of these plugins can be found by selecting `Plugins > Manage & Install Plugins`. Select the plugin on the left, and then click the **Install plugin** button on the bottom right.


_The following sections are in development:_

##### Editing the Questionnaire JSON in the "Create Project" step

The Cadasta plugin permits users to upload a project from scratch. If there are additional fields, select one and/or select multiple choices that you would like to add to the project you can do so using the "Advanced" setting in the "Create Project" window.

Here is a reference table for the type of fields in the project:

`type` | XLSform | Answer Input
---|---|---
`IN` | `integer` |	Integer (i.e., whole number) input.
`DE` | `decimal` |	Decimal input.
`TX` | `text` |	Free text response.
`S1` | `select_one` | Multiple choice question; only one answer can be selected.
`SM` | `select_multiple` | Multiple choice question; multiple answers can be selected.
`NO` | `note` |	Display a note on the screen, takes no input.
`GP` | `geopoint` |	Collect a single GPS coordinates.
`GT` | `geotrace` |	Record a line of two or more GPS coordinates.
`GS` | `geoshape` |	Record a polygon of multiple GPS coordinates; the last point is the same as the first point.
`DA` | `date` |	Date input.
`TI` | `time` |	Time input.
`DT` | `dateTime` |	Accepts a date and a time input.
`PH` | `image` / `photo`| Take a picture.
`AU` | `audio` | Take an audio recording.
`VI` | `video` | Take a video recording.
`BC` | `barcode` | Scan a barcode, requires the barcode scanner app to be installed.
`CA` | `calculate` | Perform a calculation; see the Calculation section below.
`AC` | `acknowledge` | Acknowledge prompt that sets value to “OK” if selected.

To add choices to `select_one` and/or `select_multiple` fields, you will need to add an `options` property like so:

```
"options": [
        {
          "label": "Farm",
          "name": "farm"
        },{
          "label": "Building",
          "name": "building"
        },{
          "label": "Park",
          "name": "park"
        }
      ],


```

Note: At the moment, updating and creating projects in QGIS does not support custom location type and tenure type values.  This is not the case when using the platform-- you are able to use custom values if you build a questionnaire with XLS.
##### Troubleshooting

Sometimes the best steps to figure out an issue are to start with small data sets. 

Restart QGIS. 

Make sure you are in the correct projection. (Click on the projection button on the bottom right, reproject the layer and save the layer as a new layer with the new projection)

QGIS and the plugin are both finicky. If you get stuck on anything please do not hesitate to email katrina@cadasta.org. She is here to help!





# Cadasta QGIS Plugin

_12 May 2017: please note that this page is in-progress; refresh to view any changes._


* [Overview](#overview})
* [Setting up the QGIS Plugin](#setup)
* [Downloading Projects to QGIS](#downloading)
* [Creating Projects](#creating)
* [Updating Projects](#updating)
* [Advanced](#advanced)


## Overview {#overview}

[Quantum GIS (QGIS)](http://www.qgis.org/en/site/) is a free and open source geographic information system. It's a powerful tool that's used by organizations all over the world to work with geographic data, without any cost. Now it can be used to analyze and update the data you've collected using the Cadasta platfom through a custom plugin. 

This section covers how to [set up the plugin](#setup), and then use it to [download](downloading), [create](#creating), and [update](#updating) your Cadasta project using the tool.

Please note that this section assumes that you have already created a Cadasta account and have an active project. If you need help getting those set up, visit the first three sections of this documentation: [Getting Started](01-gettingstarted.md), [Organizations](02-organizations.md) and [Projects](03-projects.md).

This section also assumes some knowledge of QGIS and how it works. If you are unfamiliar with the platform, please visit <a href="http://www.qgis.org/en/docs/index.html">documentation.qgis.org</a>.


## Setting up the QGIS Plugin {#setup}

### 1. Download and install QGIS

Before getting started with the plugin, you'll need to install QGIS. Find the version you need on the <a href="http://www.qgis.org/en/site/forusers/download.html" target="_blank">QGIS download page</a> and then follow their instructions for installation. 


### 2. Install & Activate the Cadasta Plugin for QGIS

Next, install and activate the Cadasta Plugin. 

At this time, the first part of this process must be completed on the command line. 

On a Mac, open Terminal and then navigate to the QGIS `plugins` folder by using the following command:

```
.qgis2/python/plugins
```

Then, install the plugin directly from the repo using this command:

```
git clone https://github.com/Cadasta/cadasta-qgis-plugin.git
```

Once your installation is complete, start or restart QGIS.

Inside the application, navigate to `Plugins > Manage & Install Plugins`. In the popup that appears, select Cadasta. Be sure that the checkbox to the right of the name is ticked (it's a little hard to see).

> add image

Then, you can close the popup window. 

### 3. Connect to your Cadasta Account

Now, select `Vector > Cadsta > User Settings`. Before proceeding, hit **Clear** on the bottom right. 

> add image

Here, enter the platform you're working on (either `https://demo.cadasta.org/` or `https://platform.cadasta.org/`), as well as your username and password. 

Then, hit **Test Connection** in the lower left. If all has been done correctly, you'll get a `Success`message. 

Finally, hit **Save**.

Now you're ready to get to work!

### Additional Recommended Plugins

To make your experience using QGIS the best it can be, Cadasta recommends activating a few more plugins:

* **OpenLayers** provides a selection of basemaps - including OpenStreetMap and satellite imagery - so that you can see your map data in context of the area around it. 

* **TableManager** makes it easier to edit the attribute tables associated with your spatial data. 

* **mmqgis** is a set of Python plugins for manipulating vector map layers in Quantum GIS. 

All of these plugins can be found by selecting `Plugins > Manage & Install Plugins`. Select the plugin on the left, and then click the **Install plugin** button on the bottom right.














## Downloading Projects to QGIS {#downloading}

Once the Cadasta QGIS plugin is installed and you've connected it to your Cadasta account, you can use it to download your project data, analyze it, and make maps for print or web.

### Steps to Download

To download the project, select `Vector > Cadasta > Download Project`. On the popup that follows, you can select any of the projects associated with your account. 

> Add image

If you're looking for a public project to download, select `Include all Cadasta public projects`.

Once you've selected your project, click **Next** to start downloading. 

When you get a message that `Your data has been downloaded`, click **Close**.

Now you should be able to see your map data in the main QGIS screen, with layers on the left.

> Add image


### Adding a Basemap

If you'd like to add a little bit of background imagery, then you can add a basemap layer using the OpenLayers plugin, which you can install from `Plugins > Manage & Install Plugins`.

Once installed, go to `Web > OpenLayers`, and then select the basemap you'd like to use. Below you can see Stamen's OSM watercolor map being used.

> Add image

It's not uncommon for the OpenLayer to appear above your map layer data, making it seem like your data has disappeared. 

To fix, drag your basemap layer to the bottom of your layers. 

> Add image

### Layout of Files

> Katrina, what does this mean?




















## Creating Projects {#creating}

_Please note that this feature is in development._

In addition to downloading an existing project from the Cadasta platform, you can create new Cadasta projects using QGIS as well. 

Creating a project with QGIS allows quite a bit of flexibility when it comes to using different data formats. You can upload data as: 

* shapefiles, 
* geojson, 
* .kml,
* .gpx, 
* .csv,

And any other layer that's supported by QGIS. 
You can upload any layer, such as a s etc, that is supported by QGIS. _Learn more about supported data formats at <a href="https://docs.qgis.org/2.6/en/docs/user_manual/working_with_vector/supported_data.html" target="_blank">docs.qgis.org</a>._

Please note that creating Cadasta projects using QGIS really only works with location data, with limited capabilities with regards to information about relationships, parties, and resources. If you are starting a project using a lot of that kind of information, Cadasta recommends starting that project on the platform.

If you plan to start a project on QGIS from existing data, and then upload it to the Cadasta platform, then follow the following steps. 

### 1. Prep the data

> Katrina, I feel like we need examples of this. What do these fields look like in GeoJSON? As a shapefile? How does that even work? Or does this only work with certain data types?

The purpose of prepping the data is to make sure that it works with some of the necessary fields in Cadasta: 

* Location types
* People / Party types
* People / Party name
* Relationship / Tenure types

These fields need to be formatted like this:

> add formatting examples

> Katrina, in the below paragraph, you talk about layers. How do these layers come into play??

You can use the Table Manager plugin or Toggle Edit Tool for editing the layer if need be. You will also need to make sure there a column that can be used for the party name field. 

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


























## Updating Projects {#updating}

* Editing Fields
* Adding Fields
* Details on Version Control


## Advanced {#advanced}

* Joining CSV files
* Uploading project
* Advanced json
* Troublshooting


## Troubleshooting


# Cadasta QGIS Plugin

_16 May 2017: please note that this page is in-progress; refresh to view any changes._


* [Overview](#overview})
* [Setting up the QGIS Plugin](#setup)
* [Recommended Printing Workflows](#printing)
* [Recommended Uploading Workflows](#uploading)
* [Advanced](#advanced)


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

![install cadasta plugin](/assets/qgis-plugin-install.png)

A window will open up and you will have access to the list of plugins, or specialized libraries, that are available with QGIS. Scroll down until you see the "Cadasta" plugin. Click on that option and 

![install cadasta plugin](/assets/qgis-plugin-install-02.png)

### 3. Connect to your Cadasta Account

Now, select `Vector > Cadasta > User Settings`. This is the window where you can switch accounts or platforms (demo vs platform).

![User settings](/assets/qgis-plugin-01.png)

Enter the platform you are working on (either `https://demo.cadasta.org/` or `https://platform.cadasta.org/`) and your username and password. 

Then, hit **Connect** in the lower left. Hitting "Connect" talks to the Cadasta server to make sure that If all has been done correctly, you'll get a `Success`message. 

Finally, hit **Save** so that your login credentials are saved for future use.

Now you're ready to get to work!

Tip: If you want to switch platforms or usernames, you must hit **Clear** on the bottom right. 

### 4. Style and Adjust your Cadasta Data

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

![](/assets/qgis-plugin-02.png)

If you're looking for a public project to download, select `Include all Cadasta public projects` from below the dropdown.

Once you've selected your project, click **Next** to start downloading. 

When you get a message that `Your data has been downloaded`, click **Close**.

Now you should be able to see your map data in the main QGIS screen, with layers on the left.

![](/assets/qgis-plugin-03.png)


### File Layers Overview

Digital maps are made using a series of layers – for example, roads may all be on one layer, while parcel polygons are on another. The basemap, providing background and context for this data, could be on its own layer at the very bottom. Organizing data this way makes it much easier to analyze and style. 

QGIS uses this layering convention as part of its interface. You can see the layers in your project listed one the left of the platform (like in the above image). 

Any basic Cadasta project comes with three different layers: one for parties data, one for relationship data, and one for each type of geographic data: the points, lines, and polygons you have stored on the Cadasta platform. 

The parties and relationships layers do not have a visibility on the map; however they can be joined with your points, lines, and polygons so that you can see which geographic data relates to what party or relationship. _To learn more about joining data layers together, see [Joining Relationships and Parties to Location Geometry](#joining) below._

You can change the order of these layers by dragging and dropping them on top of one another.


### Adding a Basemap

If you'd like to add a little bit of background imagery to you newly-imported map data, then you can add a basemap layer using the OpenLayers plugin.

You can install the plugin from `Plugins > Manage & Install Plugins`.

Once installed, go to `Web > OpenLayers`, and then select the basemap you'd like to use. Below you can see Stamen's OSM watercolor map being used.

![](/assets/qgis-plugin-04.png)

It's not uncommon for the OpenLayer to appear above your map layer data, making it seem like your data has disappeared. 

To fix, drag your basemap layer to the bottom of your layers. 


## Advanced {#advanced}

### Joining Relationships and Parties to Location Geometry {#joining}

One of the more powerful features of QGIS is its capacity for geographic analysis. For example, for a customary rights Cadasta project, you can use QGIS to see which groups of people are using what piece of land. 

To do this, the parties and relationship data needs to be **joined** to each layer of geographic data. 

To link these layers, right click one of your map data layers and then select **Properties**.

![](/assets/qgis-plugin-05.png)

In the popup that appears, select Joins on the left, and the the green plus sign at the bottom. 

![](/assets/qgis-plugin-06.png)

This will take you to a new popup window where you can join the layers. 

First, join your relationships to the geometry by creating the following settings:

* Join layer: use the option ending in `/relationships`, such as `cadasta-foundation/concessions-in-liberia/relationships`
* Join field: `spatial_id`
* Target field: `id`

The settings should look something like this:

![](/assets/qgis-plugin-07.png)

Next, join your parties to the relationships using the following settings:

* Join layer: use the option ending in `/parties`, such as `cadasta-foundation/concessions-in-liberia/parties`
* Join field: `id`
* Target field: use the option ending in `/relationships_party_id`, such as `cadasta-foundation/concessions-in-liberia/relationships_party_id`

These settings should look something like this:

![](/assets/qgis-plugin-08.png)

Repeat these steps for each map layer. Now, you can run analysis to see how these fields are joined together. 


connects parties and relationships to geometry

use a different project

used for one to one
used for one to many

download project
get relationship csv
get party csv
gqis - right click layers - join 


_The following sections are in development:_

* Advanced JSON
* Troubleshooting


# Cadasta QGIS Plugin

* [Overview](#overview})
* [Setting up the QGIS Plugin](#setup)
* [Plugin Overview](#plugin-overview)
* [Downloading Projects to QGIS](#downloading)
* [Creating Projects](#creating)
* [Updating Projects](#updating)


## Overview {#overview}

[QGIS](http://www.qgis.org/en/site/) is a free and open source geographic information system. It's a powerful tool that's used by organizations all over the world to work with geographic data, without any cost. Now it can be used to analyze and update the data you've collected using the Cadasta platfom through a custom plugin. 

This section covers how to [set up the plugin](#setup), and then use it to [download](downloading), [create](#creating), and [update](#updating) your Cadasta project using the tool.

Please note that this section assumes that you have already created a Cadasta account and have an active project. If you need help getting those set up, visit the first three sections of this documentation: [Getting Started](01-gettingstarted.md), [Organizations](02-organizations.md) and [Projects](03-projects.md).


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

Now, select `Vector > Settings`. Before proceeding, hit **Clear** on the bottom right. 

> add image

Here, enter the platform you're working on (either `https://demo.cadasta.org/` or `https://platform.cadasta.org/`), as well as your username and password. 

Then, hit **Test Connection** in the lower left. If all has been done correctly, you'll get a `Success`message. 

Finally, hit **Save**.

Now you're ready to get to work!

### Additional Recommended Plugins

To make your experience using QGIS the best it can be, Cadasta recommends activating a couple more plugins:

* **OpenLayers** provides a satellite imagery basemap, so that you can see your map data in context of the area around it. 

* **TableManager** makes it easier to edit the attribute tables associated with your spatial data. 

Both of these plugins can be found by selecting `Plugins > Manage & Install Plugins`.


## Plugin Overview {#plugin-overview}
* Overview of Plugin
* Setting up "User Settings"


## Downloading Projects to QGIS {#downloading}

* Steps for downloading project
* Layout of Files
* Join Tables
* Analysis Options, such as styling, printing, and statistical analysis



## Creating Projects {#creating}

// only for location

* Prep for shapefile and GPX files
* Joining CSV files
* Uploading project
* Advanced json
* Troublshooting

## Updating Projects {#updating}

* Editing Fields
* Adding Fields
* Details on Version Control
* Troubleshooting

* Recommended plugins
	* MMqgis // geoprocessing
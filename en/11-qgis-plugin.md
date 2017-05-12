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


### 2. Install the Cadasta Plugin for QGIS

Next, install the Cadasta Plugin. At this time, the installation must be completed on the command line. 

First, navigate to the folder where QGIS is installed. The command will 



To do this, you need to open Terminal on your computer and enter the following command:

cd ~.qgis/python/plugins
git clone https://github.com/Cadasta/cadasta-qgis-plugin.git
```

* Installing the Plugin


## Plugin Overview {#plugin-overview}
* Overview of Plugin
* Setting up "User Settings"


## Downloading Projects to QGIS {#downloading}

* Steps for downloading project
* Layout of Files
* Join Tables
* Analysis Options, such as styling, printing, and statistical analysis

* Recommended plugins
	* OpenLayers // basemap, get data in context
	* TableManager // more aggressively edit the attribute tables


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
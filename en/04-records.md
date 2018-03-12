# Project Records: Locations, People (Parties), Relationships, and Resources

* [Overview](#overview)
* [Project Locations, Location Types, and Location Acquisition](#project-locations)    
* [People (a.k.a Parties) and Their Relationship to a Location](#location-relationships)
* [Resources](#project-resources)
* [Searching Through Records](#search)
* [Editing Records and its Polygons, Polylines and Points](#editing)

## Overview {#overview}

Within any given project, you may be working with lots of different [locations](#project-locations). For example, within a forested area, there may be a national park boundary as well as a building that you'll need to track.

Each of these locations may have a [relationship](#relationships) with one or more [people (or parties)](#parties). For example, a park may be owned by the government, but a community group may have special access to it. Each of these has their own relationship to that bit of land. That relationship is known as their tenure. There are often many [resources](#project-resources) to track this, like photos, letters, and deeds. 

The Cadasta Platform is designed to deal with this complexity. This section outlines how the Platform handles tracking locations, people, their relationship(s) to the land, and all of the documentation and resources.. 

## Project Locations, Location Types, & Location Aquisition {#project-locations}

### Adding a Location {#adding-a-location}

From the main project page, select either **Add location** or **Add a location**: 

![](/assets/add-location-0724.png)

On the next page, you'll be asked to draw your location on the map as a point, line, polygon, or rectangle.

![](/assets/records-02-polygon.png)

Here, you'll also be asked to provide some information about your location (shown on the right).  

This might be information like:

* [Location type](#location-types)
* Name of Location
* [How Location was Acquired](#location-acquisition), 
* When the location was acquired, and
* Location Notes.

When you're done, save your location. 

To access this location, click on it from the main project page. 

#### Adding a Location from a GPX File {#gpx-location}

If you've been collecting location using a GPS device, you can upload GPX files and use them to create a new location. 

To do this, first upload your GPX file as a [Project Resource](#project-resources). 

![](/assets/gpx-00-project-resource.png)

Then, go to the Project Overview page and select **Add Location**.

From this screen, click the Map Layers icon at the top right of the map. There, you'll see your GPX file as a layer option. Select it.

![](/assets/gpx-01-select-waypoints.png)

Now you can use those points to trace your new location. 

![](/assets/gpx-02-trace.png)

### Location Types {#location-types}

Location types define the type of location you are collecting.  Here is a _suggested_ list of location types that you could use:

* **Parcel** - a plot of land.
* **Community Boundary** - a formal or informal boundary between two groups of people.
* **Building** - any kind of structure.
* **Apartment** - an apartment or apartment building.
* **Right-of-Way** - an easement that allows a person or group of people to pass throuh another's land.
* **Utility Corridor** - a passage, either overground or underground, meant to carry utility lines like electricity and water. 
* **National Park Boundary** - the boundary between a national park and another kind of land. 
* **Miscellaneous** - another kind of location that doesn't fit into any of your categories.

You can come up with your own list of location types in your custom form. To change the location types that you are using, [edit your Cadasta XLSForm](09-XLSForms.md). 

### Location Acquisition {#location-acquisition}

Another suggested field is the land acquisition. It is useful to collect the history of how the land was acquired. Here are some recommended options: 

```
* share_crop - Contractual Share Crop
* cust_arg - Customary Arrangement
* gift - Gift
* homestead - Homestead
* inf_occ - Informal Occupant
* inherit - Inheritance
* leasehold - Leasehold 
* pur_freehold - Purchased Freehold
* rental - Rental
* other - Other
```

## People (a.k.a. Parties) and Their Relationship to a Location{#location-relationships}

### People (a.k.a Parties) {#Parties}

People are the individuals, groups or corporations who have a relationship to one or more of the locations in your project.

* **Individuals** are single people, like a landowner or lessee.

* **Groups** are collections of people who may not have an officially documented organization, such as a tribe, community group or family.

* **Corporations** are organizations like companies, NGOs, or government bodies.

### Viewing People / Parties

To view all of the people / parties who have a relationship with a project or location, click the **Parties** button on the left:

![](/assets/parties-0724.png)

This will take you to a new page listing all of the parties related to the project:

![](/assets/parties-01-page.png)

If you click on a name, it will take you to a detail page where you can see an overview of information about that party, the relationships they have to one or more locations, and any resources associated with them.


![](/assets/parties-02-party-detail.png)


### Relationships {#relationships}

Any given location has a relationship to a number of parties. For example, a municipality may own a utility corridor, which a local community may use as a right-of-way. 


### Adding a New Relationship {#adding-a-new-relationship}

To add a new relationship for a project location, click on the Relationships tab. Then, click on **Add relationship**. 

![](/assets/add-relationship-01-0724.png)

In the pop-up that follows, you'll be first asked to either choose from an existing party or add a new one. 

![](/assets/add-relationship-02-0724.png)

If you're adding a new one, you'll need to provide:

* Name, 
* Type (individual, group, or corporation), and
* Any other information you might have. 

Next, you'll be asked to add relationship details: including the [tenure type](#tenure-type) and notes about the tenure. 

When you're done adding notes about the relationship, click save. 

### Relationship Type {#tenure-type}

**Relationship type** refers to the type of ownership or right that people may have to a location. In the Cadasta Platform, you can define tenure type in a variety of ways. 

* CU    Customary Rights
* EA    Easement
* ES    Equitable Servitude
* FH    Freehold
* JT    Joint Tenancy
* LH    Leasehold
* LL    Longterm leasehold
* OC    Occupancy (No Documented Rights)
* TN    Tenancy (Documented Sub-lease)
* TC    Tenancy in Common
* UC    Undivided Co-ownership
* WR    Water Rights


To learn more about many of these terms, see the glossary from [Focus on Land in Africa](http://www.focusonland.com/resources/glossary/#e). 

## Resources {#project-resources}

Land rights projects can come with all kinds of documentation - like legal documents, letters, pictures and more. Some of that documentation may relate to multiple locations within a project, or to one location, or it may just relate to the project in general.

The Cadasta Platform is set up to handle this kind of complexity, organizing resources into four different types:

* Resources pertaining a specific location,
* Resources pertaining to a person or party, 
* Resources partaining to a relationship, and
* Resources pertaining to the project generally.


### Adding a New Resource {#adding-new-resource}

There are a few ways to add a new resource, depending on what it pertains to.

If you're adding a **project location resource**, select the **Resources tab** from the location overview page, and then **Attach.**

![](/assets/attach-resource-0724.png)

To add a **resource that pertains to a certain person or party**, go to the **Parties page** from the location overview page. 

![](/assets/parties-0724.png)

Then, select the party you'd like to add a resource for.

![](/assets/parties-01-page.png)

Then click on the Resources tab. There, select the **Attach** button and upload your resource.

![](/assets/parties-02-party-detail.png)

To add a **resource that pertains to the overall project**, go to the project's overview page by clicking **Overview**. Then, click **Resources.** 

Clicking on resources from the project overview page will take you to your project library, which will have all of the resources related to your project.

![](/assets/add-resource-02.png)

To add a resource while you're in the the library, click **Attach** on the upper right.

From any of these starting points, you'll be led to a pop-up window. Here, you'll be asked to upload a file, and give it a name and description. 

![](/assets/add-resource-03.png)

Acceptable file types are:

```
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
* .xml 
* .gpx
```

#### .gpx Files as Project Resources

![](/assets/gpx.png)

If you've been collecting data in .gpx format (which is the filetype created by most GPS devices) you can store it as a resource in the Cadasta system. [You can use these files to create new project locations](#gpx-location). 

## Searching Through Records {#search}

If you need to find a record in the data you've collected, you can search for it using the search bar at the top of the Project Overview page. 

![](/assets/search-01-0724.png)

This will produce a search result with the record you're looking for. 

![](/assets/search-02-0724.png)

At this time, you cannot use Search to look through geographic records (a.k.a. the points, lines, and polygons you see on the map); however, you can use it to search for people and parties. 

## Editing Records and its Polygons, Polylines and Points {#edit}

Sometimes you will find that you need to edit information from the record. Editing location information comes in two parts: (1) changing the geometry (2) changing the questions and answers.

To edit a polygon on the web...

1. Click on a location "Open Location".
2. You will need to click the "edit" icon on the top right of the location view. 
3. That should change the polygon outline to pink and dotted.
4. Click on a white triangle and move it.  Continue editing the polygon until the layer is fixed.
5. IMPORTANT: Click "Save" on the LEFT next to the polygon icon. 
6. Click "Save" on the right. The large, green "Save" button.

![](https://cloud.githubusercontent.com/assets/25337622/25371067/005b8b2e-294c-11e7-9b16-f34edc9f3103.gif)

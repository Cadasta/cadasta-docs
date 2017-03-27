# Projects

* [Overview](#overview)
* [Setting Up a New Project](#setting-up-new-project)
* [Editing a Project](#editing-a-project)
* [Project Members & Member Permissions](#project-members-member-permissions)

## Overview {#overview}

Within any organization, there may be any number of projects: initiatives to collect information about a series of locations in a given area. This section goes over how to [create a new project](#setting-up-a-new-project) in the Cadasta Platform, as well as how to [edit it](#editing-a-project) and [assign member permissions](#assign-member-permissions) for different projects. 

### Setting Up a New Project {#setting-up-new-project}

Once your organization exists, administrators can start to add projects to it. 

#### 1. Navigate to the "Add project" button.

You can find the **Add project** button in one of two ways. The first way is from your Organization Overview page:

![](/assets/add-project-1.png)

And the second way is by clicking the **Projects** button at the top of the page, and then clicking **Add**.

![](/assets/add-project-2.png)

#### 2. Navigate to your project area

Your project area is the geographic area where field data collection activities take place. You can find your area on the map using a couple different approaches.

##### a. Zooming from the map

![](/assets/Cadasta-Map-Overview.png)

From the map view, use the `+` and `-` signs on the upper left to zoom in and out.

In the upper right, you can choose from a couple of different layers depending on what kind of map you need.

The default layer is the graphic OpenStreetMap (OSM) layer, shown above. You can also select from a few other layers, including the Vivid Satellite layer:

![](/assets/layers-02-vivid.png)

And a combination of Vivid Satellite and OSM:

![](/assets/layers-04-vivid-osm.png)


##### b. Search by a geographic Place Name

Click on the magnifying glass in the upper left to search for your location by name.

![](/assets/cadasta-map-search.png)

#### 3. Create your project boundary.

The next thing you need to do is create your project boundary by drawing either a rectangle or polygon on the map. 

Note that your project boundary does not need to be exact. To ensure full coverage, add a little bit of space outside the area where you'll be working.

**To draw a polygon**, click the polygon button. Then, start clicking points on the map to draw your shape.

![](/assets/cadasta-map-polygon.png)

You can edit your polygon by clicking the Edit Location button.

From there, you can click to add each point of your polygon and move it to its intended location. To close the polygon, click on the first point that you added.

**To draw a rectangle**, select the rectangle icon. Then, click and drag over your project area on the map.

![](/assets/cadasta-map-rectangle.png)

**To edit your project area**, select the edit icon. Then, click and drag the points on your polygon or rectangle to their correct location. When you're done, click the gray Save button on the left

Once you've drawn your project area to your satisfaction, click the green **Next** button on the right.

_Note that if your project is a global one, simply click the green **Next** button without drawing any polygons or rectangles._


#### 4. Provide some general information about the project.

At this stage, you will be asked to fill out some General Information regarding the project, including:

* **Project name**

* **Project privacy preference**, or whether the project will be Public or Private. Public projects are viewable by anyone, whereas private projects are only available to members of your organization.

* **Project description**

* **Project URL**, which must start with _http://_ or _https://_

* **Cadasta XLSForm** (previously called a Questionnaire), a spreadsheet that serves as the basis for your data collection. It should not be heavily changed once your project is created. To learn more about how they work and get sample forms, read the section on [custom data collection](09-XLSForms.md)

* **Project contacts**, if any. These contacts do not have to be project members, but may be people who are important to the project. For example, you may be working with an administrator or communications specialist who is not involved with data collection, but who may have integral roles in what you're doing. 

If you're adding a project by navigating from the Project page, you'll also be asked to select the project's organization from a dropdown menu at the top.

#### 5. Assign Project Member Permissions {#assign-member-permissions}

When you're done adding your general information, you can assign member permissions. Project members are members of your organization, and their permissions reflect their role in any given project. 

To learn more about member permissions, see the  [Project Members & Member Permissions](#project-members-member-permissions) section below.

![](/assets/project-member-permissions.png)

When you're done, **congratulations!** You've created your very first project. 

Your next steps are to start collecting records for your project, including:
* **project locations** - all the parcels, buildings, boundaries and other locations relevant to your project;
* **location relationships** to **parties** that have some right or access to one or more of your locations, and 
* **resources** like photos, deeds, and other documentation related to your project, or an associated location or party. 

Read more about these records in the next section: [Project Records: Locations, Parties, Relationships, and Resources](04-records.md). 

## Editing a Project {#editing-a-project}

Once you've created a project, you may find that you need to make some changes. There are three aspects of a project that you can change:

* Project Boundary (the area of the project)

* Project Details, and

* Member Permissions. 

To change any of these aspects of your project, navigate to your project page, and then click **More actions** button in on the upper right of your screen. 

![](/assets/edit-project-info.png)

From there, select the item that needs to be edited. 

### Editing a Project Boundary

Once you've navigated to the Edit Project Boundary page, you have a few options for making edits.  

One is simply to drag the points already drawn on the map. 

![](/assets/edit-project-boundary-easy.png)

Alternatively, you can select the polygon or rectangle tools to draw completely new boundaries. 

When you're done, click the **gray Save button** on the left to save your shape, and the **green Save button** on the right to save your project location. 

###Editing Project Details

Once you've navigated to the Project Details page, you can edit information like the name, description, or privacy settings. When you're done, save your changes by clicking the **Save** button at the bottom of the page. 

###Editing Member Permissions

Once you've navigated to the Edit Member Permissions page, you can change your member permissions by using the drop-down menu for each member. 

To learn more about member permissions and what they mean, read on to the next section.

###Archiving a Project

When it's time for your project to come to a close, you can easily archive it. Archiving allows you to keep all of your data in the Cadasta platform, while keeping it out of the way of current projects. 

To archive a project, go to the project's Overview page. From there, click the **More actions** button in the upper right, then select **Archive Project**. 

![](/assets/archive-project-01.png)

You'll be asked to confirm that you want to archive the project:

![](/assets/archive-project-02.png)

If you'd like to unarchive the project, first navigate to the Organization Overview page. Then, select Archive from the dropdown menu at the top of the list of projects:

![](/assets/archive-project-03.png)

Then, on the archived project's page, select the **More actions** button in the upper right, then **Unarchive Project**. 

![](/assets/archive-project-04.png)

Now the project is active again.

## Project Members & Member Permissions {#project-members-member-permissions}

When you create members of your project, you must assign them permissions. These permissions will define user accesses and privileges for that project. Currently, there are five user roles, each with their own set of privileges:

* **Administrator**. The Administrator can create new projects within an organization and manage user roles and access. This role has full permissions regarding accessing and editing data in the project.

* **Project Manager**. The Project Manager works within an organization on a specific project. This role can also access and edit all data within the project, including adding new users and setting access rights.

* **Data Collector**. The Data Collector primarily works in the field with communities to collect data using Field Papers, Mobile Applications, or by directly entering data into the platform. The Data Collector can add data to a project, but cannot edit existing data.

* **Project User**. The Project User can view all data within the project, even if it is set to private. The Project User does not have the ability to add or edit data.

* **Public User**. A Public User can only view data that is publicly available.



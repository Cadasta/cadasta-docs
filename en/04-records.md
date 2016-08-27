# Organizing Project Members, Locations, Relationships, and Resources

* [Overview](#overview)
* [Project Members & Member Permissions](#project-members-member-permissions)
* [Project Locations & Location Types](#project-locations)
* [Location Relationships & Tenure Types](#location-relationships)
* [Project Resources](#project-resources)


## Overview {#overview}

Once you've set up your organization and project, you can start gathering the information you need to organize your project. 

To do this effectively, it's important to understand the structure of a Cadasta project and how everything works together. 

* A **project** coveres a specific geographic area. Within that area, there can be numerous project **locations**. A project may also have multiple **members**, all of whom need to have an account in the Cadasta system. 

* The structure of the data you're collecting for your project depends on how you've structured your **questionnaire**, which is required to set up your project. To learn more about how questionnaires work, [read this section](08-XLSForms.md).

* Each project also tracks the **relationships** that a party may have to one of it's locations. In addition, each location may also need to track specific **resources** - like deeds or images of the location - that can help with land rights documentation. All of the location resources are stored in the project **library**. 

If you were to view all these parts as an outline, it would look something like this:

* Organization
    * Organization Members
    * Project
        * Project Members
        * Project Locations
            * Overview (determined by the structure of the questionnaire)
            * Relationships
            * Resources

Typically data for each project is collected in the field using mobile devices. The Cadasta Platform supports two mobile data collection platforms:

* **Open Data Kit (ODK)**, and
* **Geo Open Data Kit (GeoOKD)**.

Both of these platforms integrate with your questionnaire, ensuring that the data you're collecting is in your desired format.

Whenever you need your data, all you have to do is organize it. 



The first step is defining the spatial details of a location for which a relationship is to be assigned.  Defining the location can be done in a number of ways - currently we allow for direct data collection from OpenDataKit \(ODK Collect\) or GeoODK \(Described in a subsequent section\), or digitizing from imagery.  In the coming months we will be adding functionality to allow for entering GPS coordinates and utilizing the Field Papers application.

Let's begin by looking at digitizing from the imagery provided by the Cadasta platform.

## Digitizing from Imagery

### Location Information

1. After logging into the Platform and navigating to your project, click **Add a location** to begin data entry.
  ![](/assets/addlocation.png)
2. You can then use the drawing tools \(see label A in the image below\) to draw the location on the map as a point, line, or polygon, and if imagery is needed, remember that you can change the background by switching the map layers \(see B below\). Also note the boundary of the project area shaded in a dotted line as defined during the creation of the project \(see C below\).

3. Now fill out all property details as defined in the Excel Form \(see [Custom Data Collection Section](http://docs.cadasta.org/en/XLSForms.html) for details\) submitted during project setup \(see D below\).

4. Click **Save** and your first location has been recorded.


![](/assets/records_digitizing.png)

### Relationship Information

Now that the spatial details have been recorded, its now necessary to establish a relationship between the person or party, and the location.

1. From the Project Overview page, select **Relationships** and then **Add Relationship**.
  ![](/assets/records_relationships.png)
2. You will be prompted to define the relationship, or tenure, type \(see A below\) as defined by the Excel form, and then prompted to add a party with which the relationship will be established \(see B below\). 

![](/assets/records_relationship_type_and_party.png)

### Associating Resource Files

Now that we have added locations and established relationships with a party, it may be useful to provide evidence of the rights.  This might vary to include pictures of properties, right holders or documentation attesting to rights \(transfer documents, tax payments receipts, etc\), or video or audio files detailing agreements on rights and\/or boundaries.

1. Select **Resources** from the overview page. 
  ![](/assets/records_resourcefiles.png)
2. Now you can either upload resources directly, or add them from the resource library if you have already saved to the project. The Resource File will be associated with the location in question.

![](/assets/records_resource_files_addition.png)

***

### Project Members & Member Permissions {#project-members-member-permissions}



When you create members of your project, you must assign them permissions. These permissions will define user accesses and privileges for using the platform. Currently, there are five user roles, defined below with details regarding access rights:



* **Administrator**. The Administrator can create new projects within an organization, manages user roles and access, and has full permissions regarding accessing and editing data.



* **Project Manager**. The Project Manager works within an organization on a specific project, and with regard to that project can access and edit all data within the project, including adding new users to the project and setting access rights.



* **Data Collector**. The Data Collector works in the field with the communities to collect data using Field Papers, Mobile Applications, or by directly entering data into the platform. The Data Collector can add data in a project, but cannot edit existing data.



* **Project User**. The Project User can view all data within the project, even if it is set to private. The Project User does not have the ability to add or edit data.



* **Public User**. A Public User can view only data that is publicly available.





### Project Locations & Location Types {#project-locations}





### Location Relationships & Tenure Types {#location-relationships}





### Project Resources {#project-resources}











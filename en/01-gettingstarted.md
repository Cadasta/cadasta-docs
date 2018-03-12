# Getting Started

* [How Cadasta is Structured](#how-cadasta-is-organized)
* [Quick Guide to Getting Started](#quick-guide-to-getting-started)
* [Creating a New Account](#createnewaccount)

_Looking for API documentation? <a href="https://cadasta.github.io/api-docs/#cadasta-api-documentation" target="_blank">Click here</a>._

## How Cadasta is Structured {#how-cadasta-is-organized}

While anyone can use the Cadasta Platform, it's designed primarily for organizations working to document land and resource rights of individuals and communities. The structure of the Platform matches this design.

Before jumping in, it's important to understand this structure and how everything works together.

![](/assets/diagram-organizations-projects-members-orig.png)

* At the core of the Cadasta platform are a series of **[projects](03-projects.md)**. A project covers a specific geographic area, from a small parcel of land to the entire globe. Within the specified project area, there can be numerous project **locations**. A project may also have multiple **project members**, each of whom will have permissions specific to the project.

* Each project must belong to an **[organization](02-organizations.md)**. An organization represents an organized body of people with a particular purpose. In most cases, organizations are NGOs helping communities to document their land rights. In the Cadasta system, people who belong to an organization are called **organization members**. 

* The structure of the data you're collecting for your project depends on how you've structured your **[Cadasta XLSForm](09-XLSForms.md)**, which is required to set up your project.

![](/assets/diagram-resources.png)

* In addition to storing geographic data, each project is also meant to store a series of **[records](04-records.md)**. These records may include **resources** about the location, such as scanned documents, images, video, audio testimonials or anything else that can help with land rights documentation. All of the location resources are stored in the project **library**. In addition, each project can also track **relationships** that a various **people (or parties)** may have to one or more of its locations.

If you were to view all these parts as an outline, it would look something like this:

* Organization
  * Organization Members
  * Project
    * Project Members
    * Cadasta XLSForm (which determines the structure of your data collection)
    * Project Locations
      * Relationships (to People or Parties)
      * Resources


Typically data for each project is collected in the field. This might be done using mobile applications or paper questionnaires. The Cadasta Platform currently supports two mobile data collection platforms, which are both available for use on Android devices:

* **[Open Data Kit \(ODK Collect\)](05-odkcollect.md)**, and
* **[Geographical Open Data Kit \(GeoODK Collect\)](06-geoodkcollect.md)**.

Both of these applications integrate with the Cadasta XLSForm you're using to collect your data and allow it all to be stored on the Cadasta Platform.

Whenever you need to get your data and resources out of the Platform, all you have to do is **[download it](07-download.md)**.

## Quick Guide to Getting Started {#quick-guide-to-getting-started}

To get started, follow the steps below! For more information and images, follow the links on each step.* 

1. **[Create your new account](#createnewaccount)** by clicking **register** and entering your name, email, and a few other key pieces of information. _Note that you have up to 48 hours to verify your account using the verification link sent to your registered email address._

2. Next, you need to be added to an organization. To do this, contact your organization's administrator to add you as an organization member. Note that you can be added to multiple organizations in the Cadasta sytem.  

    * If you're going to be the administrator of a new organization in Cadasta, you can **[create your organization](02-organizations.md)** by selecting the **Organizations** button and then **Add**. You'll be asked to enter some basic information about your organization and save it. The person who creates an organization becomes the organization's administrator by default. Note that most users will not create their own organizations; instead they will be added to one. 

3. Next, you need to be added to a project by your organization or project administrator. Administrators can also **[create new projects](03-projects.md)** and add members to it. As part of the project creation process, you'll be asked to upload a [Cadasta XLSForm](09-XLSForms.md), which creates the structure for your data collection.You'll also need to add project members, project locations, and project resources as needed. 

4. Once you have an account, organization, and project, it's time to start gathering data! If you need to collect data in the field, you can use either [ODK Collect](/en/05-odkcollect.md) or [GeoODK Collect](/en/06-geoodkcollect.md), which are both applications for Android. If you don't need to be in the field, you can use the Cadasta Platform directly.

_* For printed versions, go to the associated section in the document._

## **Creating a New Account** {#createnewaccount}

![](/assets/sign-in-register-arrow.png)

To get started with Cadasta, the first thing you need to do to is create a user account.

1. If you're just trying out the Platform, navigate to [demo.cadasta.org](https://demo.cadasta.org). Partners with live projects should create accounts at [platform.cadasta.org](https://platform.cadasta.org).
2. Select **Register** from the upper right of the screen. 
3. Input a username, valid email address, password and your full name.
4. Select **Register**.

From here, check your inbox for a verification email. You'll have 48 hours to verify account creation, or else your account will be deleted.

Next, log into Cadasta, where you'll return to the home screen, where you can view public projects and organizations.


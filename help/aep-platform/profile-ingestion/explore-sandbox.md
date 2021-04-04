---
title: Access and Explore the AEP Sandbox
description: Access and Explore the AEP Sandbox
exl-id: 62c21615-4b03-4900-a1ad-8f809c836491
---
# Access and Explore the AEP Sandbox


## Overview

This article will cover the following:

* The differences between an existing Adobe Exchange Partner sandbox Organization and the shared AEP sandbox.
* Requesting access to the AEP shared sandbox.
* Receiving an email invitation to the AEP shared sandbox.
* Inviting new users in the adminconsole.
* Navigating the AEP UI.

For a general overview of the Sandbox technology in AEP, see this [article](https://docs.adobe.com/content/help/en/experience-platform/sandbox/home.html).

## The Shared AEP Sandbox


Exchange partners are given access to various Adobe Experience Cloud products (non-AEP products like Analytics, Target, Launch, etc) via their own Adobe Experience Cloud Org (non-shared). Partners are given system administrator access rights to their own Org to manage users and other permissions. Adobe Experience Platform (AEP) is treated differently than other Adobe sandboxes. Here are the key differences:

* Access to AEP will NOT be through the partners main Adobe Experience Cloud sandbox Org.
* Access to AEP will be through a shared Adobe Exchange Org.
* Many other Adobe Exchange partner companies will be accessing AEP using the same Org
  * Through the AEP Sandbox feature, data and activities within this shared Org can not be seen or modified by the other partners; each partner will have access to a different Sandbox within the shared Org.
* Administration rights within this shared Org are very limited.
* After being given access to a Sandbox on AEP, partners will see two Orgs on the Org switcher in the top right of the UI while in the Admin Console or main Experience Cloud home page. However, when signed into AEP, only the shared Org should be visible.

## How to Request Access to the Shared AEP Sandbox

Submit a [support request](https://adobeexchangeec.zendesk.com/hc/en-us/requests/new) with the following information:

* Email Address
* Subject:  AEP Sandbox Request
* Product: General Provisioning / Sandbox
* Ticket Type:  Program Support - Exchange Program / Provisioning Request Questions
* Description: Provide a brief description of the integration use case(s) that require the use of an AEP sandbox
* Be sure to also provide all of the user names and emails that should be added to the AEP sandbox. It is possible for additional users to be added after the request is made but the users will need to be added by Adobe via an additional ticket (see below).

## Receiving the Email Invitation 


The primary contact that requested the AEP sandbox will receive an automated email inviting them to "get started" with the Adobe Experience Platform. The primary contact will also have some administration privileges which will be covered in the next section.

Instead of selecting the "get started" button in the email, navigate directly to `https://platform.adobe.com.` Sign in with the Adobe ID that is associated with the email address in the invite or create one if it is not associated with an Adobe ID.


## Inviting Additional Users


Submit a [support request](https://adobeexchangeec.zendesk.com/hc/en-us/requests/new) with the following information:

* Requestor Email Address
* Subject:  AEP Sandbox - Add Admin/User
* Product: General Provisioning / Sandbox
* Ticket Type:  Program Support - Exchange Program / Provisioning Request Questions
* Description: List of users to be added (names and emails)

## Navigating the AEP UI


Watch the AEP UI [introduction video](https://docs.adobe.com/content/help/en/platform-learn/tutorials/intro-to-platform/interface-tour.html)


There are 12 primary areas within the AEP UI that can be navigated via the left-hand panel. However, the most important sections for this type of integration are Schemas, Datasets, and Profiles.

* Home - the landing screen

  * Suggests some getting started activities
  * Provides some links to learning content
  * Gives a dashboard view for some of the main AEP objects, such as Schemas, DataSets and Profiles

* Workflows - launch into common workflows for bringing data into AEP
* Connections / Sources - manage sources of data coming into AEP
* Connections / Destinations - manage the connections to send data to external systems
* Profiles - view and manage individual customer profiles
* Segments - browse, create and modify customer segments
* Identities - browse, create and modify identity namespaces; these are the types of primary IDs used to uniquely identify a customer
* Models (Data Science) - engage in Data Science activities, including the use of an embedded Jupyter Notebooks environment
* Services (Data Science) - publish data science recipes as services
* Schemas - browse, create and modify schemas; these are the detailed data definitions used to keep data organized
* DataSets - browse, create and manage DataSets; a DataSet is defined by a Schema and is where data resides within AEP
* Queries - browse, create, modify and use a repository of queries for gaining insights from the data within DataSets
* Monitoring - view the status of all of the data moving in and out of AEP for both Batch and Streaming

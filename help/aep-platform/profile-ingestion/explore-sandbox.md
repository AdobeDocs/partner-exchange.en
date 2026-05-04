---
title: Access and explore the AEP sandbox
description: Learn how to access and explore the Experience Platform sandbox.
exl-id: 62c21615-4b03-4900-a1ad-8f809c836491
TQID: https://experienceleague.adobe.com/A5sl-xNZBPjIKn6HO1iwM78IaQWQs4yBgbw9wwpMrGw
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
    internal-label: Getting started
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
    internal-label: Customer profiles
---
# Access and explore the AEP sandbox

This article covers the following:

* The differences between an existing Adobe Exchange Partner sandbox Organization and the shared AEP sandbox.
* Requesting access to the AEP shared sandbox.
* Receiving an email invitation to the AEP shared sandbox.
* Inviting new users in the [!DNL Admin Console].
* Navigating the AEP UI.

For a general overview of the Sandbox technology in AEP, see this [article](https://docs.adobe.com/content/help/en/experience-platform/sandbox/home.html).

## The shared AEP sandbox

Exchange partners are given access to various Adobe [!DNL Experience Cloud] products (non-AEP products like [!DNL Analytics], [!DNL Target], Platform tags, and so on) via their own Adobe [!DNL Experience Cloud] Org (non-shared). Partners are given system administrator access rights to their own Org to manage users and other permissions. Adobe [!DNL Experience Platform] (AEP) is treated differently than other Adobe sandboxes. Here are the key differences:

* Access to AEP will NOT be through the partners main Adobe [!DNL Experience Cloud] sandbox Org.
* Access to AEP is through a shared Adobe Exchange Org.
* Many other Adobe Exchange partner companies is accessing AEP using the same Org
  * Through the AEP Sandbox feature, data and activities within this shared Org can not be seen or modified by the other partners; each partner will have access to a different Sandbox within the shared Org.
* Administration rights within this shared Org are very limited.
* After being given access to a Sandbox on AEP, partners will see two Orgs on the Org switcher in the top right of the UI while in the Admin Console or main Experience Cloud home page. However, when signed into AEP, only the shared Org should be visible.

## Request access to the shared AEP sandbox

Submit a [support request](https://adobeexchangeec.zendesk.com/hc/en-us/requests/new) with the following information:

* Email Address
* Subject: AEP Sandbox Request
* Product: General Provisioning / Sandbox
* Ticket Type: Program Support - Exchange Program / Provisioning Request Questions
* Description: Provide a brief description of the integration use case(s) that require the use of an AEP sandbox
* Be sure to also provide all of the user names and emails that should be added to the AEP sandbox. It is possible for additional users to be added after the request is made but the users will need to be added by Adobe via an additional ticket (see below).

## Receive the email invitation 

The primary contact that requested the AEP sandbox will receive an automated email inviting them to "get started" with the Adobe [!DNL Experience Platform]. The primary contact will also have some administration privileges which are covered in the next section.

Instead of selecting the "get started" button in the email, navigate directly to `https://platform.adobe.com.` Sign in with the Adobe ID that is associated with the email address in the invite or create one if it is not associated with an Adobe ID.

## Invite additional users

Submit a [support request](https://adobeexchangeec.zendesk.com/hc/en-us/requests/new) with the following information:

* Requestor Email Address
* Subject: AEP Sandbox - Add Admin/User
* Product: General Provisioning / Sandbox
* Ticket Type: Program Support - Exchange Program / Provisioning Request Questions
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

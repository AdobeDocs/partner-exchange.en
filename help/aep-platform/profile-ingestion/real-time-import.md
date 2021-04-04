---
title: Real-time Import
description: Import data to AEP in real-time
exl-id: 0b6215a9-1160-49ae-8aa5-302b47357200
---
# Streaming Data to AEP

## Overview

Adobe Experience Platform allows for both profile and experience events to be streamed and available in near real-time. All data sent to AEP via streaming is persisted in the data lake. Data can be streamed to existing data sets or to entirely new data sets via APIs or using Adobe Launch. 

This article will cover the following:

* Streaming to the XDM Individual Profile
* Streaming to the XDM ExperienceEvent
* Using AEP the Launch extension to stream

The [Postman collection](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman) will be referenced throughout the article using the associated calls by number. More details on installing and using the Postman collection are available on the Github [README](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman/blob/master/README.md) page. There are also sample datasets of [loyalty](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman/blob/master/AEP%20loyalty%20events.json) and [profile](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman/blob/master/AEP%20loyalty%20profiles.json) data.

## Prerequisites

* [Authenticate to the platform](https://docs.adobe.com/content/help/en/experience-platform/tutorials/authentication.html).
* Gather the values for required headers from the authentication tutorial linked above.

## Create a Streaming Connection

In order to stream to AEP you must first create a streaming connection. Streaming connections will contain attributes such as the source of streaming data and whether or not you are sending in records that belong to the Experience Data Model (XDM) schemas. After creating a streaming connection you will be given a unique URL which will be used to stream data into AEP.

Go [here](https://docs.adobe.com/content/help/en/experience-platform/ingestion/tutorials/create-streaming-connection.html) for instructions on how to create a streaming connection via API or [here](https://docs.adobe.com/content/help/en/experience-platform/ingestion/tutorials/create-streaming-connection-ui.html) for instructions on how to create a streaming connection via the UI.

```json
curl -X POST https://platform.adobe.io/data/foundation/flowservice/connections \
 -H 'Authorization: Bearer {ACCESS_TOKEN}' \
 -H 'Content-Type: application/json' \
 -H 'x-gw-ims-org-id: {IMS_ORG}' \
 -H 'x-api-key: {API_KEY}' \
 -H 'x-sandbox-name: {SANDBOX_NAME}' \
 -d '{
     "name": "Sample name",
     "providerId": "521eee4d-8cbe-4906-bb48-fb6bd4450033",
     "description": "Sample description",
     "connectionSpec": {
         "id": "bc7b00d6-623a-4dfc-9fdb-f1240aeadaeb",
         "version": "1.0"
     },
     "auth": {
         "specName": "Streaming Connection",
         "params": {
             "sourceId": "Sample connection",
             "dataType": "xdm",
             "name": "Sample connection"
         }
     }
 }
```

Response:

```json
 {
    "id": "77a05521-91d6-451c-a055-2191d6851c34",
    "etag": "\"a500e689-0000-0200-0000-5e31df730000\""
}
```

Be sure to save the ID provided in the response above for future streaming ingestion calls (the Postman collection will save this for you in the CONNECTION_ID environment variable).

## Stream Profile Data to AEP

For this section, use Postman call folders: 3: Real-time import, 3a: Real-time import for PROFILE data.

Detailed JSON requests with responses for streaming profile data are documented [here](https://docs.adobe.com/content/help/en/experience-platform/ingestion/tutorials/streaming-record-data.html).

Steps:

1. Create an XDM Individual Profile Schema
1. Set the Primary Identity Descriptor for XDM Individual Profile (primary key)
1. Create a dataset for XDM Individual Profile Records
1. Call the Streaming Ingestion APIs to create an XDM Individual Profile Record
1. Retrieve the newly created profile

## Stream Experience Events to AEP

For this section, use Postman call folders: 3: Real-time import, 3b: Real-time import for PROFILE data.

Detailed JSON requests with responses for streaming experience data are documented [here](https://docs.adobe.com/content/help/en/experience-platform/ingestion/tutorials/streaming-time-series-data.html).

Steps:

1. Create an XDM ExperienceEvent Schema
1. Set the Primary Identity Descriptor for XDM ExperienceEvent (primary key)
1. Create a dataset for XDM ExperienceEvents
1. Call the Streaming Ingestion APIs to create an XDM ExperienceEvent
1. Retrieve the newly created event

## Using Adobe Launch to Stream to AEP

The Adobe Experience Platform Launch extension provides a way to stream to AEP via Launch. To learn more, see [this guide](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html).

## Reference Articles

* [Data Ingestion APIs](https://www.adobe.io/apis/experienceplatform/home/api-reference.html#/acpdr/swagger-specs)
* [Streaming Ingestion Overview](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/streaming_ingest_overview.md)
* [Streaming Ingestion Developer Guide](https://www.adobe.io/apis/experienceplatform/home/data-ingestion/data-ingestion-services.html#!api-specification/markdown/narrative/technical_overview/streaming_ingest/getting_started_with_platform_streaming_ingestion.md)
* [Using the AEP Launch Extension](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/aep-extension/overview.html)

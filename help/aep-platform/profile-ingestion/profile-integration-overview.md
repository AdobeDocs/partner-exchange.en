---
title: Platform Profile Ingestion and Access Integration Guide Overview
description: Overview for the Platform Profile Ingestion and Access Integration Guide
exl-id: a593511c-dd4c-4437-af73-f44d795cacb8
---
# Integration Guide: Adobe Experience Platform (AEP) Profile Ingestion and Access

## Overview

Partners should use this integration guide to assist them in building out ingress and egress functionality with the Adobe Experience Platform (AEP). There are APIs for batch ingestion, streaming ingestion, and Unified Profile access (egress). 

To assist in development, a [Postman collection](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman) has been created by the Adobe Exchange team. This Postman collection will be referenced throughout the integration guide.

More details on installing and using the Postman collection are available on the Github [README](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman/blob/master/README.md) page. There are also sample datasets of [loyalty](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman/blob/master/AEP%20loyalty%20events.json) and [profile](https://github.com/Adobe-Marketing-Cloud/exchange-aep-profile-integration-postman/blob/master/AEP%20loyalty%20profiles.json) data.

## Integration Use-Case Example: Interactive Voice Response System

For integrators, the Experience Platform APIs provide all capabilities of the platform that are offered throughout the user interface, but now with the ability to create customer workflows and automated data flows. As an integrator, you periodically check the status of datasets, set up new data ingestion procedures, and integrate your own audience activation solution with the Unified Profile.

Consider the world of Interactive Voice Response (IVR) systems and Call Center management software. The supplier can use the Experience Platform APIs to ingest historical information of the customer’s call center activity in the Experience Data Lake. If the data is ingested in the XDM ExperienceEvent Schema (a schema that expresses customer interactions), these interactions can be ingested with no friction directly into the Unified Profile Service. In this case, the “callerId” will be used as the customer’s identifier. The Identity service will take care of identity resolution and assist the Unified Profile Service to add any data points from recent interactions with the Call Center to the customer’s profile.

The next time a customer calls into the Call Center, they will first be answered by the IVR. To personalize the message and deliver an offer tailored to the caller, the IVR system needs to understand more about the caller. This is where API integration with the Unified Profile comes in. The IVR backend can contact the Unified Profile Service for a point lookup. Then, consult either the profile attributes that apply to just the call-center interactions or the full customer profile, which also has attributes for interactions on other touchpoints. By combining data from multiple data sources, using identity resolution, and the Unified Profile, the call center and IVR provider can deliver a tailored customer experience, supported by Adobe Experience Platform."

## General Resources

* AEP [Product Documentation](https://docs.adobe.com/content/help/en/experience-platform/landing/documentation/overview.html).
* AEP [Extensibility](https://www.adobe.com/insights/experience-platform-api-extensibility.html).

## Questions or Feedback?

Please submit all questions and feedback via the [support channel](https://adobeexchangeec.zendesk.com/hc/en-us/requests/new)

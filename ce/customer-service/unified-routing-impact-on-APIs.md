---
title: "Impact of unified routing on queue items and the corresponding APIs| MicrosoftDocs"
description: "How unified routing affects queue items and the corresponding APIs"
ms.date: 04/15/2021
ms.topic: article
author: mh-jaya
ms.author: v-jmh
manager: shujoshi
search.audienceType: 
  - developer
  - customizer
search.app: 
  - D365CE
  - D365CS
ms.custom: 
  - dyn365-customerservice
ms.reviewer: nenellim
---
# How unified routing affects queue items and the corresponding APIs

When you change the status of a queue item that has been routed using unified routing, the queue item is affected in the following ways:

- When you change a queue item from a basic queue to an advanced queue&mdash;or from one advanced queue to another&mdash;by selecting  **Add to Queue** on the record (via the [AddToQueue Action](/dynamics365/customer-engagement/web-api/addtoqueue?view=dynamics-ce-odata-9&preserve-view=true)) or by selecting **Route To** on the queue item (via the [**RouteTo Action**](/dynamics365/customer-engagement/web-api/routeto?view=dynamics-ce-odata-9&preserve-view=true)), the associated queue for the live work item ([msdyn_ocliveworkitem](/dynamics365/customer-service/developer/reference/entities/msdyn_ocliveworkitem)) also gets updated to the same destination queue. This action then updates the unified routing services that maintain agent presence and capacity with the corresponding changes.

- When you update the **Worked By** field of queue items by selecting **Route To** on the queue items list (via the **RouteTo Action**), the live work item (msdyn_ocliveworkitem) also gets assigned to the same agent.

- When you update a queue item using unified routing, you can't remove it from the queue by selecting **Pick** ([**PickFromQueue Action**](/dynamics365/customer-engagement/web-api/pickfromqueue?view=dynamics-ce-odata-9&preserve-view=true)) or **RouteTo Action** on the queue item.

- When you resolve a routed record, the corresponding queue item that gets deactivated can't be activated again.

- When you delete a queue item by selecting **Remove** (via the [**RemoveFromQueue Action**](/dynamics365/customer-engagement/web-api/removefromqueue?view=dynamics-ce-odata-9&preserve-view=true)) or by deleting or canceling the underlying record, the associated live work item (msdyn_ocliveworkitem) is also closed. This action then updates the unified routing services that maintain agent presence and capacity with the corresponding changes.

### See also

[Overview of unified routing](overview-unified-routing.md)   
[Set up record routing](set-up-record-routing.md)   
[Set up unified routing](set-up-routing-process.md)   


[!INCLUDE[footer-include](../includes/footer-banner.md)]

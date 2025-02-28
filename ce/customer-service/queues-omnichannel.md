---
title: Create and manage queues for unified routing | MicrosoftDocs
description: "Use this article to understand how to create and manage queues for unified routing in Customer Service and Omnichannel for Customer Service apps."
author: neeranelli
ms.author: nenellim
manager: shujoshi
ms.topic: article
ms.date: 04/04/2022
ms.custom: intro-internal
searchScope:
- D365-App-customerservice
- D365-Entity-queueitem
- D365-UI-*
- Customer Engagement
- Dynamics 365
- Customer Service
---

# Create and manage queues for unified routing

[!INCLUDE[cc-use-with-omnichannel](../includes/cc-use-with-omnichannel.md)]

In Customer Service, queues are used to collect and distribute workload among agents. Workload includes records such as cases, and conversations such as chat or SMS. Agents are added as members to the queues and the workload is distributed among the agents based on assignment methods.

## How work items are routed to queues

You can create separate queues for each line of business such as billing, investment, and products. When a customer query is raised for any of the areas, it is routed to the corresponding designated queue based on how you define route to queues in the classification. You can also set up a customer support availability matrix by using a combination of queues, operating hour schedules, and routing rules.

In an enterprise scenario, you can have various supervisors handling different issues, and therefore, different types of queues are required to handle the various scenarios. Accordingly, routing rules are set up based on the complexity of issues that need to be handled.

To simplify the routing experience for administrators and supervisors, queues are categorized based on the channel types as follows:

- **Messaging**: To route all messaging conversations pertaining to the live chat, SMS, and social channels.
- **Records**: To route work items pertaining to records, such as cases and emails.
- **Voice**: To route calls made to the support numbers listed on the customer portal.

The queue types allow issues to be routed correctly and help avoid cross-queue assignments. When you configure workstreams and routing rule items, the queues that'll be available for selection will be based on the channel type for the workstream. For example, for routing rules for a live chat workstream, only messaging type queues will be shown for selection. Similarly, in a conversation transfer scenario, you can transfer a chat conversation only to a messaging queue, and a case only to an entity queue.

Assign a group number that helps you organize your queues in the list view. The group number won't affect the priority of the queue or incoming conversations.

## Create a queue for unified routing

1. In Dynamics 365, go to one of the apps, and perform the following steps:
   
   ### [Customer Service admin center](#tab/customerserviceadmincenter)
   
    1. In the site map, select **Queues** in **Customer support**.
    
    2. On the **Queues** page, select **Manage** for **Advanced queues**.
    
   
   ### [Omnichannel admin center](#tab/omnichanneladmincenter)

    - In the site map, select **Queues** in **General settings**.
    
   ### [Customer Service Hub](#tab/customerservicehub)

    - Go to the **Service Management** site map, and select **Advanced queues** in **Unified routing**.

2. On the **Queues** page, do the following:

    1. Select **New**.
    2. In the **Create a queue** dialog, enter the following:
       - **Name**: A name for the queue.
       - **Type**: Select **Messaging**, **Record**, or **Voice**.
       - **Group number**: A number to organize the queue.
    3. Select **Create**. The queue that you created is displayed.

       > [!div class=mx-imgBorder]
       > ![Queue in Omnichannel admin center.](../customer-service/media/queue-summary-ur.png "Queue in Omnichannel admin center")

3. Select **Add users**, and in the flyout menu, select the users who should be part of the queue, and then select **Add**. The users are added to the queue.

4. In **Assignment method**, do one of the following:
   - **Highest capacity**: Assigns work item to the agent with the highest capacity, among those who have the skills identified during the classification stage, and have the presence as specified in the allowed presence option of the workstream; selected by default.
   - **Round robin**: Assigns work item to the agent in the list order who matches the criteria for skills and presence.
   - **Create new**: Lets you create a custom assignment method. The custom assignment method lets you use your own rulesets and rules to configure priority, severity, and capacity for choosing the queues to which work items need to be routed by setting up the rulesets for Prioritization and assignment. For more information about the custom assignment method, see [Create custom assignment method](assignment-methods.md).

5. To set operation hours, in the **Operation hours** area, select **Set operation hours**. If you don't set operation hours, the queue is considered to be available round the clock. You must configure the operating hour record before you can set it for the queue. More information: [Configure operating hour record](create-operating-hours.md)

6. On the **Set operation hours** dialog that appears, select an operating hour record in the **Name** list.

7. Select **Save and close**. The operating hour record that you selected is configured for the queue.

### Manage queues for unified routing

You can manage queues on the **Queues** page, and perform operations such as search, edit, copy, and delete the queues.

- Select a queue to edit the users, assignment methods, or operating hour record.

- Select a queue on the **Queues** page, select **Copy** on the command menu, and then select **Copy** in the *<queue_name>* dialog. The queue is copied and inherits the settings of the queue you copied from, including its name, prefixed with **Copy of**.

### Fallback queues

To efficiently manage the work items, you can configure a fallback queue per workstream. You can set an existing queue as the fallback queue or create a fallback queue with the required settings when you are creating a workstream. For existing workstreams, you can configure the fallback queue on the workstream page. If you choose to create a queue, you'll need to add users. By default, the assignment method for the fallback queue is highest capacity.

Out of the box, the following queues are available. You can add and remove users from these queues.

- **Default entity queue** for routing entity records.
- **Default messaging queue** for routing all messaging conversations pertaining to live chat, SMS, Microsoft Teams, and social channels.
- **Default voice queue** for routing all voice calls.

Work is routed to these queues that act as a safety net in the following scenarios:

- Work item encounters an error during classification.
- Work item encounters an error when running a route-to-queue rule.
- Work item does not match any route-to-queue rules.

### See also

[Create and manage workstreams](create-workstreams.md)  
[Create and manage assignment methods](configure-assignment-rules.md#create-an-assignment-method-and-configure-rules)  
[Create and manage operating hours](create-operating-hours.md)  
[Configure the voice queues](voice-channel-route-queues.md)  


[!INCLUDE[footer-include](../includes/footer-banner.md)]

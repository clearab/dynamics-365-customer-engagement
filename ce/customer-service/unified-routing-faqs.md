---
title: "Frequently asked questions about unified routing | MicrosoftDocs"
description: "Learn about the frequently asked questions (FAQs) for unified routing in Customer Service and Omnichannel for Customer Service."
ms.date: 02/07/2022
ms.topic: article
author: neeranelli
ms.author: nenellim
manager: shujoshi
---

# FAQ about unified routing in Customer Service, Omnichannel for Customer Service

[!INCLUDE[cc-omnichannel-administration-deprecation-note.md](../includes/cc-omnichannel-administration-deprecation-note.md)]

## Overview

This topic contains the FAQs that you as an administrator, supervisor, or agent might have about unified routing.

### What SKUs must I have to get unified routing?

Customers will get unified routing for entities, such as Cases, Leads, and custom entities as a part of the Customer Service Enterprise license. When you purchase channels (Chat and Digital messaging), you'll get unified routing for chat and messaging channels automatically.

### What will happen to my current workstreams after unified routing is installed?

For messaging channels, use the migration utility to migrate the workstream and associated routing rules. For entity routing, you'll configure new workstreams and rules in unified routing. More information: [Migrate workstreams created in Omnichannel Administration](migrate-workstreams.md). 

### What are the implications when migration is in progress?

There is no downtime involved when you are migrating the workstreams, but it's recommended that you perform the migration during low load or off hours.

### Why do I see workstreams that I didn't create in Omnichannel Administration?

These workstreams were created either in the Omnichannel admin center or Customer Service Hub app. In the Omnichannel Administration app, you'll see all the workstreams irrespective of the app that has been used to create them. We recommend that you manage the workstreams in the same app that you've used to create them.

### Will unified routing support activity routing?

Yes, unified routing supports routing activities, including email.

### What happens to my existing queues after I migrate to unified routing?

The existing queues will be automatically migrated to unified routing.

### Will intelligent skill finder be available in all geographical regions?

Intelligent skill finder requires AI Builder to create and train the machine learning (ML) model. If AI Builder is not available in the customer region where unified routing is, the customer will get a generic error when trying to setup the model.

### Can I use intelligent skill finder with email activities?

Yes, intelligent skill finder can be enabled for any entity that is enabled for routing by using any text-based field. For email body skill finder, an additional step is required because email body (description) includes HTML tags that can impact the ML model. You'll extract the text from HTML, copy it into another text field, then configure the ML model against the new field.

### How do I make sure that the right skills are attached to the work items when machine learning-based model is in use?

- Ensure that agents are trained to attach correct skills, review, and correct any incorrectly attached skills.
- Review the skill finder model to make sure that the training data is correct and retrain the model periodically to improve it.

### How do I migrate my configurations from the Omnichannel Administration app to the Omnichannel admin center app?

To migrate the messaging workstreams, you can use the Unified Routing Migration Application. For information on the migration tool and instructions, see [Migrate workstreams created in Omnichannel Administration](migrate-workstreams.md).

> [!Note]
> After you migrate the workstreams, you'll be able to manage them only in the Omnichannel admin center app. We recommend that you familiarize yourself with the new app before migrating. More information: [Get started with Omnichannel admin center](oc-admin-center.md).

### Can I manage my workstreams in the Omnichannel Administration app post migration?

No. Although you will see the migrated workstreams in the old admin app as well, we recommend that you manage the migrated workstreams in the new Omnichannel admin center app.

### What are the implications when I start the migration process for the workstreams?

There is no downtime when you are migrating the workstreams, but we recommend that you perform the migration during low load or off work hours.

### Is it possible to rollback the migration?

To rollback the migration, you will need to contact [Microsoft Support](https://dynamics.microsoft.com/support/).

### How can I migrate the entity routing workstreams?

Entity routing workstreams must be recreated in the new Omnichannel admin center or Customer Service Hub app and the rules must be manually recreated in the new workstream.

If you need further help, contact Microsoft Support.

### Can I create workstreams for routing records in the Omnichannel Administration app after upgrading Omnichannel for Customer Service to 2021 release wave 1?

No. After upgrade, you'll no longer be able to create workstreams for routing records because they will not work as expected. We recommend that you start using the new Omnichannel admin center app to create and manage routing of records.

### Can I route any record type by using basic routing?

No. Basic routing can be used only for cases. To route any record type, use unified routing.

### Is there a priority among queues? Can we use the field **Group Number** or **Priority**? Does it affect the order of the case assignment?

No. There is no priority amongst queues. However, you can prioritize records within a queue.

### Can I pause the assignment of a case?

No. It's not possible to pause the assignment of a case.

### Can I export a Unified Routing configuration and sign in to another environment?

No, a configuration can't be exported.

### I have two workstreams (W1, W2) and four queues (Q1, Q2, Q3, Q4) and a case (C1) is assigned to Q2. Is is possible to now reassign C1 to Q3?

Yes. It's possible to reassign a case to another queue. On the case form, select **Save and route** to reassign the work item from one queue to another queue.

### Why am I not able to see the **Keep same agent for entire conversation** toggle in my **Work distribution settings** for a workstream related to cases?

A case remains with the agent that it was initially assigned to and therefore the corresponding workstream for cases does not have the agent affinity toggle.

### Can I access Omnichannel Ongoing Conversations Dashboard and Omnichannel Intraday Insights in Customer Service workspace?

Yes, you can access Omnichannel Ongoing Conversations Dashboard and Omnichannel Intraday Insights in Customer Service workspace if you have the Chat for Dynamics 365 Customer Service or Digital Messaging for Dynamics 365 Customer Service license.

### See also

[Overview of unified routing](overview-unified-routing.md)  
[System requirements for Omnichannel for Customer Service](system-requirements-omnichannel.md)  
[Set up unified routing for records](set-up-record-routing.md)  

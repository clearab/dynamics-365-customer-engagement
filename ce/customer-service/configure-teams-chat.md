---
title: "Configure Microsoft Teams chats in Customer Service | Microsoft Docs"
description: "Learn how to configure Microsoft Teams chat functionality in Dynamics 365 Customer Service and Dynamics 365 Customer Service workspace."
ms.date: 04/21/2022
ms.topic: article
author: lalexms
ms.author: laalexan
manager: shujoshi
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365CS
ms.custom: 
  - dyn365-customerservice
  - intro-internal
---

# Configure Microsoft Teams chat in Customer Service (Preview)

> [!IMPORTANT]
>
> [!INCLUDE[cc-preview-features-definition](../includes/cc-preview-features-definition.md)]
>
> [!INCLUDE[cc-preview-features-expect-changes](../includes/cc-preview-features-expect-changes.md)]
>
> [!INCLUDE[cc-preview-features-no-ms-support](../includes/cc-preview-features-no-ms-support.md)]


## Introduction

You can configure the ability for agents to chat in Microsoft Teams from within Customer Service Hub, Customer Service workspace, and your custom apps. Teams chat is also available in other customer engagement apps such as Dynamics 365 Field Service and Dynamics 365 Sales.

> [!NOTE]
> Teams settings apply across all supported customer engagement apps. Whether you enable the feature from Customer Service Hub or a custom app, it'll be enabled for all supported customer engagement apps.

When the feature is enabled, while working on customer records, agents can start a new chat or link an existing chat to a record, and thus collaborate efficiently without switching context or leaving the application. Linking all the associated chats to a record can help agents maintain all the chats related to the record in one place. You can also configure an optional introduction message that agents can use to provide further context when collaborating on Teams.

## Enable or disable Teams chat

The Teams chat feature must be enabled in customer engagement apps and custom apps. It requires certain permissions to access Teams data. Review the following permissions required section to learn more.

### Permissions required

As a tenant administrator, when you enable the Teams chat feature, the app has the following permissions:

|Permission | What the app does with the permission |
|-------------|-----------------------|
|Chat.ReadWrite.All |Reads user’s chats and recent messages to display in chat list. |
|Directory.Read.All	|Reads user’s teams and channels display name. |
|Presence.Read.All	|Reads presence information of all users to be displayed on the user avatars in chat list. |
|User.Read.All	|Reads users’ display name and licenses to validate if the suggested participants have a Teams license assigned. This is used by the suggested section in the chat list.|
|User.ReadBasic.All	|Reads users’ photos. |

### Data security and privacy

The following data security and privacy considerations apply for Teams chat functionality in Dynamics 365:

- Dynamics 365 doesn't store any Teams data except for the mapping between the record ID and the linked chat ID. No data from Teams is duplicated in Dynamics 365 unless the user manually adds it to the record notes or tasks.

- The communication between the applications is secured through TLS.

- Policies that apply both to Teams and Dynamics 365 are honored by the integration. For example, confidential files shared in a linked chat can only be accessed by permitted users. Similarly, a record shared in a Teams chat in Dynamics 365 can only be accessed if the user has permission to view it.

- The app requires certain permissions to start a chat, display suggested contacts, show presence, and so on. For more information, review [Permissions required](#permissions-required).


### Add the Teams collaboration and chat settings page to the sitemap of your app

1. Sign in to [Power Apps](https://make.powerapps.com/).

1. Select the environment, and then select **Apps**.

1. Select your custom app, and then select **Edit**.

1. In the **App Designer**, edit the **Sitemap**.

1. To add the Teams **Chat and collaborate** settings page, add a subarea component, and then for the **Type**, select **URL**.

1. Copy the following value and paste it into URL field: <br>
    ```/main.aspx?pagetype=control&controlName=MscrmControls.TeamsCollaborationAdmin.TeamsCollaborationAdmin```

1. Save and publish the changes.

### Access the Teams settings

 

1. In Customer Service Hub, go to **Service Management**, and in the site map, select **Service Management**.
1. In **Collaboration**, select **Embedded chat using Teams**.
1. On the **Microsoft Teams collaboration and chat** page, turn on the toggle for the following settings:

   - **Turn on Microsoft Teams chats inside Dynamics 365 (preview)** 
   - **Use record title as the default chat name for linked chats**.

      > [!div class="mx-imgBorder"] 
      > ![Enable the Microsoft Teams chat experience in Dynamics 365 Customer Service.](media/teams-chat-enable-cs.png "Enable the Microsoft Teams chat experience")
    
1. Save the changes.<br>
   The preview is now enabled for the Dynamics 365 Customer Service Hub, Customer Service workspace, and your custom apps (and also Field Service and Sales customer engagement apps, if you're using them). You can open a record and verify if you’re able to view the chats and channels related to the record.
    

### Add the Teams chat settings page for specific multisession users

If you're using the default profile, once you complete the steps in [Add the Teams chat settings page to the sitemap of your app](#add-the-teams-collaboration-and-chat-settings-page-to-the-sitemap-of-your-app), Teams chat is enabled.

If you want Teams chat to work for specific users, you must enable the feature for your custom profile. For more information about creating custom profiles in App profile manager, see [Overview of App profile manager](/dynamics365/app-profile-manager/overview).

To enable Teams chat settings for a custom multisession user, complete the following steps:

1. Create the custom profile from the default profile in App profile manager. More info: [Create an app profile](/dynamics365/app-profile-manager/app-profile-manager#create-an-app-profile)

1. Go to [Power Apps](https://make.powerapps.com/), and then under **Environments**, select your environment.

1. In the left-side pane, select **Apps**, and then next to the custom app, select the **More Commands** ellipsis.

   > [!div class="mx-imgBorder"] 
   > ![Configure Teams chat settings for specific multisession users.](media/teams-chat-more-commands.png "Configure Teams chat settings for custom profiles")

1. From the dropdown menu, select **App profile manager**, select the custom profile, and then select **Edit**.

1. Select the **Productivity pane** tab, and then toggle **Turn on productivity pane** to **On**.

1. Under **Productivity tools**, toggle **Microsoft Teams collaboration** to **On**.

   > [!div class="mx-imgBorder"] 
   > ![Set Teams collaboration to On.](media/teams-chat-custom-profile.png "Turn on Teams collaboration")

1. Select the **General** tab to assign users. More information: [Assign profiles to users](/dynamics365/app-profile-manager/app-profile-manager#assign-profiles-to-users)

## Configure the ability to link chats to Dynamics 365 records

Once you’ve enabled Teams chats, you can link the chats to different record types. Standard record types, including case, account, contacts, knowledge article, and email, are available out-of-the-box, or you can add your desired record type.

**To configure the ability to link a chat to a record type:**

1. In Customer Service Hub, open the **Microsoft Teams collaboration and chat settings** page.

1. Under **Link chats to Dynamics 365 records**, select the record type you want to configure.<br>
   If you want to add a record type, see Add record types in the section below.
    
1. Select **Save**.

**To add a record type to link chats to in Dynamics 365 records**

1.	In Customer Service Hub, open the **Microsoft Teams collaboration and chat settings** page.
	
1. Under **Link chats to Dynamics 365 records**, select **Add record types**.
	
1. In the **Link chat to record type** pane, in **Choose record type**, type the name of the record type you want to use.
	
1. (Optional): If you want to display content for new linked chats, toggle **Introduction message** to **Yes**, and then use the existing views functionality to define the fields that will represent context card or [create a custom view in Power Apps](/powerapps/maker/model-driven-apps/create-edit-views). You can choose up to five fields you want to include as a context card. 
            
1. Select **Save**.

For any view that's selected, keep in mind the following details:

 - The first five fields of any view are used as the context card details (in addition to a link to the record).
 - If a field isn't supported, it's skipped and the display will include the first four fields that are supported. You'll be able to see from the configuration experience that the specific field isn't supported.
 
   > [!div class="mx-imgBorder"] 
   > ![View for supported fields and message for an unsupported field.](media/teams-chat-unsupported-field-type.png "View for supported fields and message for unsupported field")
    
 - Because the data fields are static, field-level permissions aren't checked for collaborators. This means if the agent has the field-level permissions to view data fields, collaborators will also be able to see those fields.
- if you don't select a view for the Case record type, agents will see the default, out-of-box **Case introduction message** view.

   > [!div class="mx-imgBorder"] 
   > ![Default case introduction message view.](media/teams-chat-case-intro-message-view.png "Default case introduction message view")
 
- For other out-of-box standard record types, including account, contacts, knowledge article, and email, the default view is the **Quick find** view.


## Assign permissions to unlink chats for specific user and user roles

Agents can create Teams chats directly from Dynamics 365 apps and then link them to records. They can also link existing chats to Dynamics 365 records from the Teams embedded chat experience.

> [!NOTE]
> The retroactive link chat experience can only be set up in Dynamics 365 apps.

As an admin, you can control which user or role can unlink chats that are linked. These user permissions help give you the flexibility to adapt the Teams embedded chat experience to match your business processes.

You can choose from the following options for assigning permissions to agents:

- [Assign unlink chat rights to specific users](#assign-unlink-chat-rights-to-specific-users)
- [Assign unlink chat rights for security roles](#assign-unlink-chat-rights-for-security-roles)

### Assign unlink chat rights to specific users

You can assign the ability to unlink chats to record owners or users who linked a chat to a record.
   - **Record owner**: When enabled, record owners can unlink any chats that are linked to a record. As an admin, you can assign this permission at a record-type level (for example, a case, contact, and so forth).
   - **Chat linker**: When enabled, users who linked a chat to the Dynamics 365 record can unlink that linked chat. This permission can also be assigned at the record level.

**To enable or disable user-specific rights to unlink chats:**

1. In Customer Service Hub, go to **Collaboration settings**.
1. Select the record type (for example, **Case**), and then from the linked chat settings pane, toggle on or off **Record owner can unlink** and/or **Chat linker can unlink**, depending on your preferences.

    > [!div class="mx-imgBorder"] 
    > ![Toggles for unlinking chats in Collaboration settings.](media/unlink-chat-rights-toggles.png "Toggles for unlinking chats on the Collaboration settings page")
    
1. Select **Save**.

### Assign unlink chat rights for security roles

When you assign unlink chat rights to a security role, all users with that role can unlink chats that are linked to any record type. Certain role types have unlink chats rights by default.

The following table details the apps and security roles where the unlink chats feature is configured:

|App   |Security role |
|---------|-----------|
|Admin    |System admin  |
|Customer Service apps | CSR manager<br>Customer Service Representative |
|Omnichannel for Customer Service | OC admin<br>OC supervisor<br>OC agent |
|||

**To edit unlink chat rights to security roles:**

1. In Customer Service Hub, go to the **Embedded chat admin settings** page, and then scroll down to **Linked chat settings**.
1. In **Security role settings**, select **Edit**. The Power Platform admin center app is opened.
1. In **Security roles**, select the role that you want to assign the rights to, and then select **Edit**.

    > [!div class="mx-imgBorder"] 
    > ![Select role you want to assign unlink chat rights to.](media/unlink-teams-chat-security-roles.png "Select the role you want to assign unlink chat rights to")
    
1. For the specific security role, go to **Business management** > **Miscellaneous privileges** > **Unlink Teams chat from Dynamics 365 record**.

    > [!div class="mx-imgBorder"] 
    > ![Unlink Teams chat from Dynamics 365 record.](media/unlink-teams-chat-record.png "Security role setting for unlinking Teams chats")


### How user rights work together for unlinking chats

The following table summarizes whether a user can unlink a linked chat based on the rights assigned to them. You can use the table as a guide for how to use these chat rights to help you configure a secure and effective collaboration experience for your business and users.

| Scenario | Scenario | Scenario | Scenario | Scenario | Result |
|----|----|----|----|----|----|
| Record is user/team-owned and current user is owner | Current user was most recent to link chat | "Record owner can unlink" toggle is on | "Chat creator can unlink" toggle is on | Global Unlink Chat permissions are assigned to user | User can unlink? |
|Y |Y/N |N |N |N |N |
|Y |Y/N |Y |Y/N |Y/N |Y |
|Y/N |Y |N |N |N |N |
|Y/N |Y |Y/N |Y |Y/N |Y |
|Y/N |Y/N |Y/N |Y/N |Y |Y |
|N |N |Y |N |N |N |
|N |Y |N |N |N |N |
|N |N |N |N |N |N |


## Configure the ability for users to join chats

As an admin, you can enable users to view and easily join chats that are linked to records they have write access to, even if they weren't orginally part of those chats. You can configure the ability for users to join linked chats at a record-type level. This functionality can help you tailor the user experience for your business processes.

> [!NOTE]
> The join chat feature only works for linked chats and is on by default for the case record type.

The ability for users to join existing chats related to cases is especially useful for the following scenarios:

- **Case transfers**: If an agent has onboarded to a case that wwas previously handled by another agent, they can join existing linked chats to better understand the context of the case and what steps the previous agent had taken, and then continue to collaborate with their relevant colleagues.
- **Case escalations**: If a case needs attention from someone with specific knowledge, the subject-matter expert who reviews it can participate in the relevant conversations.

**To turn on or off the join chat capability for a record type**:

1. In Customer Service Hub, select **Change area** in the lower-left corner, and then select **Service Management**.
1. Under **Microsoft Teams Integration**, select **Collaboration**.
1. Select the specific record type (for example, Case), and then in the settings pane, toggle **Join chat** on or off.

   > [!div class="mx-imgBorder"] 
   > ![Settings page to turn on or off the join chat feature.](media/teams-configure-join-chat.png "Settings page for turning the join chat feature on or off")

1. Select **Save**.


### See also

[Use Teams chat](use-teams-chat.md)  
[Install and set up Microsoft Teams integration](/dynamics365/teams-integration/teams-install-app)  
[Microsoft Teams integration FAQ](/dynamics365/teams-integration/teams-in-dynamics-faq)  
[Configure AI suggestions for contacts in Microsoft Teams](configure-teams-collaboration.md)  
[Collaborate with AI-suggested agents in Microsoft Teams](use-ai-suggested-contacts-teams.md)  

[!INCLUDE[footer-include](../includes/footer-banner.md)]

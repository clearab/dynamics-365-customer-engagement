---
title: "Create rich messages | MicrosoftDocs"
description: "This article provides steps to help you create rich messages in Omnichannel for Customer Service."
ms.date: 07/18/2022
ms.topic: article
author: lalexms
ms.author: laalexan
manager: shujoshi
---


# Create rich messages

Some channel apps such as Apple Messages for Business support a set of channel-specific rich messages. Rich messages contain information that is used to generate interactive content and experiences that all take place within the messages application.

By creating and publishing rich messages, your organization's customer support team can send them to customers, and their contents can be used when designing automated experiences. For information about using rich messages in Omnichannel for Customer service, see [Rich messages in conversation control]().

## Manage rich messages for Apple Messages for Business

### Rich messages designer

1. In **Omnichannel admin center**, navigate to **Agent experience** under the **Advanced Settings**.

1. Under agent experiences, locate **Rich messages**, and select **Manage**.

1. Select **New**, and then enter the following information:
    - **Name**: A descriptive name that will be used by agents when searching for rich messages.
    - **Locale**: The language of the rich message. Rich messages are filtered by locale within agent sessions.
    - **Type**:
      - Apple Pay
      - Authentication
      - Custom JSON
      -	Forms
      -	List Picker
      -	Suggested Reply
      -	Time Picker
      -	Video Rich Link
      -	Website Rich Link
   - **Tags**: A message type tag is automatically added to each rich message. In addition to the type tag, any relevant search tags can be added to the rich message. This will help agents identify the correct rich message when searching.
   - **Allow agents to configure**: Some rich message types allow agents to update the contents before sending to customers. By enabling configurations, agents can make single-use customizations, which don't affect the original rich message made here. Agent editing can be enabled for the following rich message types:
      - List picker
      - Suggested reply
      - Time picker
      - Video rich link
      - Website rich link

1. Select **Create**.

1. Begin building your rich message within the rich message designer. You may save your work at any time by selecting **Save** at the top of the designer. For additional information on building each rich message type, select the type to learn more:
   - Apple Pay
   - Authentication
   - Custom JSON
   - List Picker
   - Suggested Reply
   - Time Picker
   - Video Rich Link
   - Website Rich Link

## Publish rich messages

For agents to send a rich message in conversations, the message must first be published.

1. Complete the steps for building your rich message, as defined above. 

1. At the top of the designer page, select **Publish**. If there are any missing fields, the designer will highlight them in red, and won’t allow the rich message to be published.

1. You can confirm that your rich message was successfully published in two ways:
    
    - The **Publish Save** button will no longer appear above the designer. 
    - The status will show as **Active** within the designer and the rich messages settings page.

### Update a published rich message

After a rich message is published and active, it can still be updated. To update a rich message, select it and open the designer. Unlike inactive rich messages, you must fill in all required fields before pressing **Publish**. This ensures that no rich messages that are missing required fields can become active.

## Workstream association

Workstream association for rich messages behaves similarly to quick replies today. By default, an active rich message will be available to use across all Apple Messages for Business workstreams.

After a rich message has been associated with one or more specific workstreams, it will no longer be available to use in all other workstreams.

To associate rich messages with a workstream, complete the following steps: 

1. Within a workstream, expand the **Advanced settings** panel by selecting **Show advanced settings**. 

1. Within the advanced settings, navigate to **Rich messages**. 

1. Select **Add rich messages**. All existing rich messages are displayed. 

1. Select one or more rich messages from the list, then select **Add**. Any associated rich messages will appear within the **Rich messages** table in **Advanced settings**. 

1. To edit a workstream's rich messages, select **Edit**, and then add or remove rich messages as required. 

1. To add more rich messages, select **Add**. Select additional rich messages, and then select **Add**. They should now appear in the list of rich messages.

1. To remove rich messages, select one or more within the table, and then select **Remove**. The removed rich message will no longer appear in the list.

#### Apple Pay 

##### Properties

**messageTitle**

Text displayed in the message bubble.

Type: ```string``` - Required: Yes


**imageURL**

URL linking to the image displayed in the message bubble.

Type: ```string``` - Required: No


**currencyCode**

The three-letter ISO 4217 currency code for the currency used in the payment request.

Type: ```string``` - Required: Yes


**requiredBillingContactFields**

The customer's billing contact fields that are needed to process the transaction.

Type: ```requiredBillingContactFields[]``` - Required: Yes - Allowed values: - "email" - "name" - "phone" - "phoneticName" - "post"


**requiredShippingContactFields**

The customer's shipping address information. Only include this if the purchase must be shipped.


Type: ```requiredShippingContactFields[]``` - Required: No - Allowed values: - "email" - "name" - "phone" - "phoneticName" - "post"


**shippingMethods**

An array of shippingMethods. Omnichannel currently supports only one shipping method per payment request. If more than one shipping methods are included, only the first will be used.

Type: ```shippingMethods[]``` - Required: No - Allowed values: - "shippingMethod"

**shippingMethod**

Describes the shipping method, which contains the amount, detail, label, and identifier properties.

**amount**

A non-negative value associated with this shipping method.

Type: ```string``` - Required: Yes

**identifier**

Internally defined, unique value used to identify this shipping method.

Type: ```string``` - Required: Yes


**label**

Description of the shipping method.

Type: ```string``` - Required: Yes


**type**

Property to represent whether the line item amount is final or pending.

Type: ```string``` - Required: Yes - Allowed values: - "final" - "pending"


**total**

Describes the final amount of the Apple Pay request. It contains the amount, label, and type properties.


**amount**

The monetary amount of the Apple Pay request. This must be greater than zero.

Type: ```string``` - Required: Yes


**label**

The friendly business name customers will see when the charge appears on statements. For example, "Contoso Coffee".

Type: ```string``` - Required: Yes


**type**

Property to represent whether the Apple Pay request's total amount is final or pending.

Type: ```string``` - Required: Yes - Allowed values: - "final" - "pending"

**Example**

```
{
    "messageTitle" : "Purchase your Contoso Barista Home",
    
    "imageUrl" : "https://images-us-prod.cms.commerce.dynamics.com/cms/api/qbvttlwqcm/imageFileData/search?fileName=/Products%2FSP-DCM1008_000_001.png&w=315&h=315&q=80&m=6&f=jpg&cropfocalregion=true",
    
    "imageStyle" : "large",
    
    "currencyCode" :"USD",
    
    //Billing contact information requested during purchase
    "requiredBillingContactFields" : [
        "post",
        "email",
        "phone",
        "name",
        "phoneticname"
    ],
    //Only required when customer's purchase must be shipped
    "requiredShippingContactFields" : [
        "post",
        "email",
        "phone",
        "name",
        "phoneticname"
    ],
    "shippingMethods" : [
        {
            "amount" : "0.00",
            "detail" :"Available within an Hour",
            "label" : "In-Store pickup",
            "identifier" : "in_store_pickup"
        }         
    ],

    "lineItems" : [
        {
            "label" : "Barista Home Espresso Maker",
            "amount" : "899.00",
            "type" : "Final"
        },
        {
            "label" : "Contoso Customer Discount",
            "amount" : "-898.99",
            "type" : "Final"
        }
    ],

    "total" : {
        "label" : "Label",
        "amount" : "0.01",
        "type" : "Final"
    }
}
```

##### Limitations

|Description | Limitation |
|------------|--------------|
| Merchant country | Payment processing for merchants in China and Saudi Arabia, country codes CN and SA, respectively, is not supported in Omnichannel.|
| Merchant capabilities | EMV – Omnichannel does not currently support China Union Pay transactions. |
| Supported networks | The list of supported networks is limited to:<br><br> - American Express <br> - Discover <br> - Mastercard <br> - Visa |


#### Authentication

##### Properties

**receivedmessage**

Text displayed in the message alongside the “sign in” button.

Type: ```string``` - Required: Yes

**replymessage**

Text displayed to the customer once they have successfully authenticated.

Type: ```string``` - Required: Yes

**Example**

```
{
    "receivedmessage":"Please sign-in",
    "replymessage":"You're signed in"
}
```


##### Limitations

|Description | Limitation |
|------------|--------------|
|Message contents | Images aren't currently supported for authentication.|
|Agent | Authentication request-type rich messages don't currently support agent configuration.|


#### Custom JSON

##### Properties

**bid**

A string identifying the iMessage extension that the user interacts with while using Messages. The bid value format is `com.apple.messages.MSMessageExtensionBalloonPlugin:team-id:extension-id`. Replace `team-id` and `extension-id` with your Apple Developer team and extension IDs. 

Type: ```string``` - Required: Yes


**URL**

A URL string containing data that the Messages app sends to the iMessage app.

Type: ```string``` - Required: Yes

**Example**

```
{   "bid":"com.apple.messages.MSMessageExtensionBalloonPlugin:{team-id}:{ext-bundle-id}",
"URL":"?name=WWDC%20Goodies&deliveryDate=09-06-2017&destinationName=Contoso%20Coffee%20Redmond&street=1%20Microsoft%20Way&state=WA&city=Seattle&country=USA&postalCode=98052&latitude=47%2E6395&longitude=%2D122%2E1281&extraCharge=15%2E00"
}
```


## Forms

Survey-level properties

1. When a form rich message is created, you'll see the form level properties panel and builder. First, provide a title by selecting **Form Title** in the builder, or **Title** in the properties panel. You can also provide information for the following optional fields, which appear as part of the form's opening page:
   - **Header** (Optional): A large central header with a short text greeting or call to action.
   - **Image URL** (Optional) The image displayed to customers within the list picker's message and customer response message. Image URLs must be a valid image type. Videos and GIFs aren't supported.
   - **Start button**: You can change the label from the default string, but it can't be left blank.

1. The following form behaviors may be configured by navigating to the **Behavior** section in the property panel:<br>
     a.	By default, form responses are shown to the customer before they submit responses. This summary can be removed by deselecting **Show summary page**.<br>
     b.	Form responses can be hidden from live agents, which may be helpful when designing automated processes to handle sensitive information. When **Hide customer responses in chat** is toggled on, agents will be unable to see any customer responses within the form. Privacy cannot be toggled per question.

1. The **Outbound message** properties determine the appearance of the message bubble containing the form. The outbound message may contain the following elements:<br>
     a.	**Message title**: The main text that informs the customer of what type of content the message contains. This could be the full or shortened title of your form.<br>
     b.	**Message description** (Optional): This text appears below the message title. It can be used as a call-to-action or to provide additional context not included in the message title.<br>
     c.	**Image URL** (Optional): The image displayed to customers within the list picker's message and customer's response message. Image URLs must be a valid image type, and do not support videos or GIFs.<br>

1. To begin adding questions select one of the question types from the **toolbox** located between the properties panel and builder. Each question will contain required **Title** and optional **Header** fields, in addition to type-specific configurations. Apple Messages for Business forms support the following question types: Single input, multiline input, single-select, multi-select, dropdown picker, and date picker. 

1. A form can contain no more than 10 questions, and should be completable without needing to leave the messages application. While building a form, select **Save** to keep your changes. An unpublished form can be saved with missing fields. Changes made to a published form may only be saved if rich message has all required fields filled. 

1. New forms will be available for agents to use once they are published. To publish a new form, select **Publish** at the top of the page. To confirm that the form is published, confirm that its status displays as **Active**.

### Single input question

Single input questions are a short-answer free response style question. This question type is good for collecting information like name, contact information, and numbers. These questions are limited to a maximum of 30 characters. For longer responses see the multiline input question type.

1. Provide a **Question title**, optional **Header** text, and use the **Required** toggle to control whether the question may be left unanswered.

1. The **Input** type may be changed from the default **Text** type. Changing the input type will change the input keyboard on iOS devices. The type options and their impact on input are as follows:
   - **Text** (Default): Default keyboard
   - **Name**: Default keyboard and name autofill suggestion
   - **Url**: URL keyboard and URL autofill suggestion
   - **Phone**: Phone pad keyboard and phone number autofill suggestion
   - **Email**: Email keyboard and email address autofill suggestion
   - **Number**: Numbers and punctuation keyboard 
	
     > [!Note]
     >  Autofill suggestions are generated by Apple from the customer’s Apple ID contact information, which isn't shared in forms responses.  

1. The **Input place holder** value appears in the empty textbox to provide example data or relevant information. If no place holder value is provided the form will automatically set the place holder value to “Required” or “Optional” based on your selection in step 1. 

1. The **Label** is an optional value that appears beside the text field and can serve as an additional prompt. For a question titled “What is your name?” the label might be set to “Name”. 

1. A single input can have a **Maximum length** between 1 and 30 characters. By default, the maximum length is 30. 

1. The **Prefix** value can be used to automatically add the first characters in an answer. For example, when asking for a LinkedIn profile link, the prefix might be set to “https://www.linkedin.com/in/”, so that the person completing the form would only need to type their specific information. 

1. The **Regular expression** is a Regex expression used to validate the customer response. The regex is used to validate customer responses on their device to ensure they are providing correctly formatted information. For example, regex can be used when asking for an email address. 

### Multiline input question

Multiline input questions are a long-answer, free-response style question. This question type is good for collecting customer feedback, explanations, and responses that need line breaks. These questions are limited to a maximum of 300 characters. For shorter responses that support different iOS keyboards see the single input question type.

1. Provide a **Question title**, optional **HeaderI** text, and use the **Required** toggle to control whether the question may be left unanswered.

1. The **Input place holder** value appears in the empty textbox to provide example data or relevant information. If no place holder value is provided, the form will automatically set the place holder value to “Required” or “Optional” based on your selection in Step 1. 

1. The **Regular expression** is a regex expression used to validate the customer response. The regex is used to validate customer responses on their device to ensure they are providing correctly formatted information. For example, regex can be used when asking for an email address. 

1. A single input may have a **Maximum length** between 1 and 300 characters. By default, the maximum length is 300. 


### Single-select question

Single-select questions can be used to quickly select a single option from a set of two or more choices. Each choice can additionally support an image. This question type is good for choosing between products and choices, simple triage questions, and any single-select question with a limited number of choices. For multi-select questions that support images, see the multi-select question type, or for single selection questions with ten or more choices, see the dropdown picker question type.

1. Provide a **Question title** and an optional **Header** text.

1. Under **Choices**, you can add each of your options. We recommend that the number of choices is between two and 10 or fewer. Each choice has the following fields:

   a. **Value**: The true identifier for a choice. This is what appears in the conversation control when a customer selects a choice. By default, the value is also used as the text that is shown to customers. However, when working in multiple languages or listing products, you might prefer to show an agent the product reference number and product name.<br>
   
   b. **Text** (Optional): The text is what the customer will see when viewing the question. By default, this will match the Value. Changing the **Text** content can allow you to localize selection questions without changing what the agent sees in the response.<br>
   
   c. **Image link** (Optional): The image displayed to customers within the list picker's message and customer's response message. Image URLs must be a valid image type, and do not support videos or GIFs.<br>

      For example, let's say we want to ask a Contoso customer to select the model of expresso maker that they own. The agent will need the model number, but a customer might only know the model by its name or image. In this instance, we would provide the following content:<br>
      
      |Type | Description | Notes |
      |--------|-----------|-------------|
      |Value | #11235813 Cafe A-100 | The agent will see this text.|
      |Text | Cafe A-100 Automatic | The customer will see this text. |
      |Image link | https://contoso.com/[image].jpg | The customer will see this image.|
          
    > [!div class=mx-imgBorder]
    > ![Apple Messages for Business single-select question example.](media/single-select-question-example.png "Apple Messages for Business single-select question example")
 
1. To add additional choices, select the + icon within the properties panel or builder. You can rearrange the choices by dragging them up or down while selecting the handle button to the left of each choice. You can remove a choice by selecting the delete button. To remove all choices, select the erase icon next to the + icon at the top of the list.

### Multi-select question

Multi-select questions can be used to quickly select one or more options from a set of two or more choices. Each choice can additionally support an image. This question type is good for selecting from a subset of choices, simple triage questions, and any multi-select other multi-select question types. For single selection questions that support images, see the single-select question type, or the dropdown picker question type for single-select questions with a large set of choices.

1. Provide a **Question title** you may also include an optional **Header** text.

1. Under **Choices**, you can add each of your options. We recommended that the number of choices is between two and 10 or fewer. Each choice has the following fields:<br>

   a. **Value**: The true identifier for a choice. This is what appears in the conversation control when a customer selects a choice. By default, the value is also used as the text that is shown to customers. However, when working in multiple languages or listing products, you might prefer to show an agent the product reference number and product name.<br>
   
   b. **Text** (Optional): What the customer will see when viewing the question. By default, this will match the Value. Changing the Text content can allow you to localize selection questions without changing what the agent sees in the response.<br>
   
   c. **Image link** (Optional): The image that is displayed to customers within the list picker's message and customer's response message. Image URLs must be a valid image type, and do not support videos or GIFs.<br>
   
      For an example of the difference between **Value** and **Text**, see the section on single-select question types.<br>

1. To add additional choices, select the + icon within the properties panel or builder. You can rearrange the choices by dragging them up or down while selecting the handle button to the left of each choice. A choice may be removed by selecting the delete icon. To remove all choices, press the erase icon that is located beside the + icon at the top of the list.


### Dropdown picker question

Dropdown picker questions are used to quickly select a single option from a list of choices. These questions use a wheel-like scrolling interaction which only shows a small set of the options at a time. This question type is good for alphabetically sorted single-select questions like country, colors, brands, or categories. For single select questions that support images but fewer choices, see the single-select question type. 

1. Provide a **Question title**. You can also include an optional **Header** text.

1. Under **Choices**, you can add each of your options. As these questions can support a large number of options, it is recommended that you add choices in a logical ordering such as alphabetical. Each choice has the following fields:

   a. **Value**: The true identifier for a choice. This is what appears in the conversation control when a customer selects a choice. By default, the value is also used as the text that is shown to customers. However, when working in multiple languages or listing products, you might prefer to show an agent the product reference number and product name.<br>
   
   b. **Text** (Optional): What the customer will see when viewing the question. By default, the text will match the value. Changing the text content can allow you to localize selection questions without changing what the agent sees in the response.<br>
   
1. To add additional choices, select the + icon within the properties panel or builder. Choices can be rearranged by dragging them up or down while selecting the handle button to the left of each choice. You can remove a choice by selecting the delete button. To remove all choices, select the erase icon located beside the + icon at the top of the list.

1. Once you’ve listed all your choices, you can choose a default answer by selecting **Set default value** and choosing an item from the dropdown. If you choose not to select one, the default is automatically set to the first item in your choices. For a large, sorted set of choices, setting the default value to an item in the middle or the most common answer might reduce the amount of scrolling needed.

### Date picker question

Date picker questions are used to quickly select a date using a wheel-like scrolling interaction. Date picker can be configured to only allow dates within a pre-defined timespan. This question type is good for inputting birthdates, purchase dates, or future events. Date pickers don't support times, which would need to be provided in a single or multi-line input question type. 

1. Provide a **Question title**. You can also include an optional **Header** text. 

1. **Label** is an optional value that appears beside the text field and can serve as an additional prompt. For a question titled “When were you born”, the label might be set to “Birthday”. 

1. To limit the time-range that customers can input, there are two optional rage values:<br>

   a. **Min**: This value represents the furthest back date that can be selected. When this is set, no dates earlier than this date can be selected.<br>
   
   b. **Max**: The value represents the furthest-forward date that can be selected. If this value isn't set, the maximum date will be the date that the customer responds. When asking a question about a future date, this value must be set.<br>
   
1. The **Start date** value is the preset value that appears when the question opens. If this value isn't set, the start date will be the date when the customer is completing the form.

### List Picker

Within the designer, the first fields are related to the message that appears within the messages application.

1. First, provide a message title, which will serve as the title for both the message and list picker.

1. The following fields are optional:

   a. **Message subtitle**: This text appears below the message title. It can be used as a call-to-action or to provide additional context not included in the header.<br>
   
   b. **Image URL**: The image displayed to customers within the list picker's message and customer's response message. Image URLs must be a valid image type, and videos and GIFs aren't supported.<br>
   
1. A list picker is composed of one or more sections containing at least one item. The following fields are part of each section:<br>

   a. **Section title**: A title for each section that can provide context and instructions for customer responses. <br>
   
   b. **Allow multi-select**: Determines whether the customer can select one or more items within the section. By default, sections will be single-select.<br>
   
   c. **List items**: Each section must include at least one option. Options can be added by selecting **Add option**, or removed by selecting **Remove**. Each option has the following fields:<br>
   
      i. **Option title**: The title field is required and will be what appears as the customer's response in the messages app and in conversation control. Titles should be simple and straightforward, using the subtitle field for additional details.<br>
      
      ii. **Option subtitle**: Subtitles are an optional field that can be used to provide details about an option, such as add-on costs, item descriptions, and other secondary information. <br>
      
      iii. **Image URL**: A valid image URL for adding an image beside a list option. Images are optional and shouldn't be used in place of the title or subtitle text.<br>
      
1. To add additional sections, select **Add section**. When there are two or more sections, a section can be deleted by selecting **Remove**.

1. An optional response message can be added to the list picker rich message. This text will appear in the customer's response, below selection choices.

### Suggested reply

1. The **Summary text** field contains helper text for the customer to see after they've responded to a suggested reply message. This field shouldn't be used as the question, as customers won't see it until after they select a choice.

1. Suggested reply messages can have between two and five options that should be kept concise.

1. To add additional options, select **Add option**. When there are more than two options, an option can be removed by selecting the option's corresponding **Remove** icon.

### Time picker

1. Within the designer, the first fields are related to the message that appears within the messages application. First provide a message title, which will serve as the title for the message.

1. The following fields are optional:

   a. **Message subtitle**: This text appears below the message title. It can be used as a call-to-action or to provide additional context not included in the header.<br>
   
   b. **Image URL**: The image displayed to customers within the list picker's message and customer's response message. Image URLs must be a valid image type, and videos and GIFs aren't supported.<br>
   
1. Under **Event information**, you can configure the details and time-slots as follows:<br>
    
   a. **Event title**: The event title will appear within the customer's calendar application if they choose to add the event to their calendar.<br>
   
   b. **Location name**: The location name will appear within the customer's calendar application if they choose to add the event to their calendar.<br>
   
   c. **Event time zone**: This is the time zone where the event will take place.<br>
   
   d. **Adjust for daylight saving time**: By default, time zones are listed by their standard offset from GMT. However, if the event takes place in a region that uses daylight savings, this can result in timeslots being incorrectly converted. By toggling this setting to **Yes**, the daylight saving offset will be automatically applied for each timeslot listed.<br>
   
   e. **Customer display option**: By default, each time slot's start times will be converted to the customer's local time zone. To cause events to display in the event time zone regardless of the customer's current time zone, select **match event time**. Matching the event time can be helpful when customers may be travelling across time zones for the event, and need to more clearly understand the start time.<br>
   
   f. **Duration**: The duration of an event is not visible during time slot selection. It's automatically added to the calendar event and used to calculate the end time of an event. Events can range from zero minutes to multiple days long. Duration can be defined in the following units:<br>
      - Minutes
      - Hours
      - Days
     
   g. **Time slot**: The set of choices a customer can select from. To create times slots, select **Add date**, then add the following fields:<br>
   
      - **Date**: The date used for each associated start time.
       
      - **Start time**: Define each time slot that a customer can select. These will all be grouped under the selected date.
       
      - To add additional start times for a specific date, select the Add time slot button below existing start time.
       
   h. To add additional dates, select **Add date**, and then complete the steps above for adding time slots.
  
     > [!Note]
     > Past time slots won’t display on the customer's device.
     
1. An optional response message can be added to the time picker rich message. This text will appear in the customer's response, below their time slot selection.

   - Recommendation: Use the response message as a call to action, encouraging customers to click the message for additional details. The additional details will include an **Add to Calendar** option that will display information such as event title and duration.
   
   
### Video rich link

1. Provide a **Title** for the website rich link, which will be displayed alongside the image within the messages application.

1. Provide the **Video URL**, which is the plain text URL that links directly to a video file.

   > [!Note]
   > Embedded videos and video streaming websites won't work correctly. The video URL must link directly to a video's source. If a video streaming website's URL is used, the rich link won't work. To link to video streaming sites, instead use the **Website rich link** style rich message. Supported format types include .mp4, .mkv, .wmv, .m4v, .mov, .avi, .flv, .webm, .flac, .mka, .m4a, .aac, and .ogg
   
1. Provide the **Image URL**, which is used to display a relevant image alongside the rich link title. The image URL must be a valid, still image in order to display correctly.

   While an image URL is not required for video rich link messages, it's highly recommended. Video rich links that are sent without an image preview will appear as blank previews. Adding a keyframe or relevant image will improve the customer experience.

### Website rich link

1. Provide a **Title** for the website rich link, which will be displayed alongside the image within the messages application.

1. The **Website URL** is the plain text URL that the rich link will launch when the customer selects or long-presses on the message.

1. The **Image URL** is used to display a relevant image alongside the rich link title. The image URL must be a valid, still image in order for it to display correctly.



### See also

[Configure Apple Messages for Business](configure-apple-messages-for-business-channel.md)  
[Understand and create workstreams](work-streams-introduction.md)  
[Create and manage routing rules](routing-rules.md)  
[Configure automated messages](configure-automated-message.md)  
[Configure a post-conversation survey](configure-post-conversation-survey.md)  
[Skill-based routing](overview-skill-work-distribution.md)  
[Create message templates](create-message-templates.md)  
[Templates](/dynamics365/app-profile-manager/templates-overview)  
[Delete a configured channel](delete-channel.md)  
[Support for live chat and asynchronous channels](card-support-in-channels.md)  

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: "QueueItem entity reference (Dynamics 365 Customer Engagement) | Microsoft Docs"
description: "Includes schema information and supported messages for the QueueItem entity."
ms.date: 08/30/2022
ms.topic: "reference"
ms.assetid: 3948cc48-07c8-7f60-0608-71c37158ad7c
author: "KumarVivek"
ms.author: "kvivek"
manager: "margoc"
search.audienceType: 
  - developer
search.app: 
  - D365CE
---

# QueueItem entity reference

A specific item in a queue, such as a case record or an activity record.


## Messages

|Message|SDK class or method|
|-|-|
|AddToQueue|<xref:Microsoft.Crm.Sdk.Messages.AddToQueueRequest>|
|Create|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>|
|Delete|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>|
|PickFromQueue|<xref:Microsoft.Crm.Sdk.Messages.PickFromQueueRequest>|
|ReleaseToQueue|<xref:Microsoft.Crm.Sdk.Messages.ReleaseToQueueRequest>|
|RemoveFromQueue|<xref:Microsoft.Crm.Sdk.Messages.RemoveFromQueueRequest>|
|Retrieve|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>|
|RetrieveMultiple|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>|
|RouteTo|<xref:Microsoft.Crm.Sdk.Messages.RouteToRequest>|
|SetState|<xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>|
|Update|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>|

## Properties

|Property|Value|
|--------|-----|
|CollectionSchemaName|QueueItems|
|DisplayCollectionName|Queue Items|
|DisplayName|Queue Item|
|EntitySetName|queueitems|
|IsBPFEntity|False|
|LogicalCollectionName|queueitems|
|LogicalName|queueitem|
|OwnershipType|None|
|PrimaryIdAttribute|queueitemid|
|PrimaryNameAttribute|title|
|SchemaName|QueueItem|

<a name="writable-attributes"></a>

## Writable attributes

These attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [ImportSequenceNumber](#BKMK_ImportSequenceNumber)
- [ObjectId](#BKMK_ObjectId)
- [ObjectIdTypeCode](#BKMK_ObjectIdTypeCode)
- [OverriddenCreatedOn](#BKMK_OverriddenCreatedOn)
- [Priority](#BKMK_Priority)
- [QueueId](#BKMK_QueueId)
- [QueueItemId](#BKMK_QueueItemId)
- [Sender](#BKMK_Sender)
- [State](#BKMK_State)
- [StateCode](#BKMK_StateCode)
- [Status](#BKMK_Status)
- [StatusCode](#BKMK_StatusCode)
- [TimeZoneRuleVersionNumber](#BKMK_TimeZoneRuleVersionNumber)
- [ToRecipients](#BKMK_ToRecipients)
- [TransactionCurrencyId](#BKMK_TransactionCurrencyId)
- [UTCConversionTimeZoneCode](#BKMK_UTCConversionTimeZoneCode)
- [WorkerId](#BKMK_WorkerId)
- [WorkerIdType](#BKMK_WorkerIdType)


### <a name="BKMK_ImportSequenceNumber"></a> ImportSequenceNumber

|Property|Value|
|--------|-----|
|Description|Unique identifier of the data import or data migration that created this record.|
|DisplayName|Import Sequence Number|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|importsequencenumber|
|MaxValue|2147483647|
|MinValue|-2147483648|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_ObjectId"></a> ObjectId

|Property|Value|
|--------|-----|
|Description|Choose the activity, case, or article assigned to the queue.|
|DisplayName|Object|
|IsValidForForm|True|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|objectid|
|RequiredLevel|ApplicationRequired|
|Targets|activitypointer,appointment,bulkoperation,campaignactivity,campaignresponse,email,fax,incident,knowledgearticle,letter,phonecall,recurringappointmentmaster,serviceappointment,socialactivity,task|
|Type|Lookup|


### <a name="BKMK_ObjectIdTypeCode"></a> ObjectIdTypeCode

|Property|Value|
|--------|-----|
|Description||
|DisplayName|Regarding Object Type|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|objectidtypecode|
|RequiredLevel|None|
|Type|EntityName|


### <a name="BKMK_OverriddenCreatedOn"></a> OverriddenCreatedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Date and time that the record was migrated.|
|DisplayName|Record Created On|
|Format|DateOnly|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|overriddencreatedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_Priority"></a> Priority

|Property|Value|
|--------|-----|
|Description|Priority of the queue item.|
|DisplayName|Priority|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|priority|
|MaxValue|1000000000|
|MinValue|0|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_QueueId"></a> QueueId

|Property|Value|
|--------|-----|
|Description|Choose the queue that the item is assigned to.|
|DisplayName|Queue|
|IsValidForForm|True|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|queueid|
|RequiredLevel|ApplicationRequired|
|Targets|queue|
|Type|Lookup|


### <a name="BKMK_QueueItemId"></a> QueueItemId

|Property|Value|
|--------|-----|
|Description|Unique identifier of the queue item.|
|DisplayName|Queue Item|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|queueitemid|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|


### <a name="BKMK_Sender"></a> Sender

|Property|Value|
|--------|-----|
|Description|Sender who created the queue item.|
|DisplayName|From|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|sender|
|MaxLength|250|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_State"></a> State

|Property|Value|
|--------|-----|
|Description|Status of the queue item.|
|DisplayName|Status (deprecated)|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|state|
|MaxValue|1000000000|
|MinValue|0|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_StateCode"></a> StateCode

|Property|Value|
|--------|-----|
|Description|Shows whether the queue record is active or inactive. Inactive queue records are read-only and can't be edited unless they are reactivated.|
|DisplayName|Status|
|IsValidForCreate|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|statecode|
|RequiredLevel|SystemRequired|
|Type|State|

#### StateCode Choices/Options

|Value|Label|DefaultStatus|InvariantName|
|-----|-----|-------------|-------------|
|0|Active|1|Active|
|1|Inactive|2|Inactive|



### <a name="BKMK_Status"></a> Status

|Property|Value|
|--------|-----|
|Description|Reason for the status of the queue item.|
|DisplayName|Status Reason (deprecated)|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|status|
|MaxValue|1000000000|
|MinValue|0|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_StatusCode"></a> StatusCode

|Property|Value|
|--------|-----|
|Description|Select the item's status.|
|DisplayName|Status Reason|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|statuscode|
|RequiredLevel|SystemRequired|
|Type|Status|

#### StatusCode Choices/Options

|Value|Label|State|
|-----|-----|-----|
|1|Active|0|
|2|Inactive|1|



### <a name="BKMK_TimeZoneRuleVersionNumber"></a> TimeZoneRuleVersionNumber

|Property|Value|
|--------|-----|
|Description|For internal use only.|
|DisplayName|Time Zone Rule Version Number|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|timezoneruleversionnumber|
|MaxValue|2147483647|
|MinValue|-1|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_ToRecipients"></a> ToRecipients

|Property|Value|
|--------|-----|
|Description|Recipients listed on the To line of the message for email queue items.|
|DisplayName|To|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|torecipients|
|MaxLength|500|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_TransactionCurrencyId"></a> TransactionCurrencyId

|Property|Value|
|--------|-----|
|Description|Choose the local currency for the record to make sure budgets are reported in the correct currency.|
|DisplayName|Currency|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|transactioncurrencyid|
|RequiredLevel|None|
|Targets|transactioncurrency|
|Type|Lookup|


### <a name="BKMK_UTCConversionTimeZoneCode"></a> UTCConversionTimeZoneCode

|Property|Value|
|--------|-----|
|Description|Time zone code that was in use when the record was created.|
|DisplayName|UTC Conversion Time Zone Code|
|Format|None|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|utcconversiontimezonecode|
|MaxValue|2147483647|
|MinValue|-1|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_WorkerId"></a> WorkerId

|Property|Value|
|--------|-----|
|Description|Shows who is working on the queue item.|
|DisplayName|Worked By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|workerid|
|RequiredLevel|None|
|Targets|systemuser,team|
|Type|Lookup|


### <a name="BKMK_WorkerIdType"></a> WorkerIdType

|Property|Value|
|--------|-----|
|Description||
|DisplayName|Worker Type|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|workeridtype|
|RequiredLevel|ApplicationRequired|
|Type|EntityName|

<a name="read-only-attributes"></a>

## Read-only attributes

These attributes return false for both **IsValidForCreate** or **IsValidForUpdate**. Listed by **SchemaName**.

- [CreatedBy](#BKMK_CreatedBy)
- [CreatedByName](#BKMK_CreatedByName)
- [CreatedByYomiName](#BKMK_CreatedByYomiName)
- [CreatedOn](#BKMK_CreatedOn)
- [CreatedOnBehalfBy](#BKMK_CreatedOnBehalfBy)
- [CreatedOnBehalfByName](#BKMK_CreatedOnBehalfByName)
- [CreatedOnBehalfByYomiName](#BKMK_CreatedOnBehalfByYomiName)
- [EnteredOn](#BKMK_EnteredOn)
- [ExchangeRate](#BKMK_ExchangeRate)
- [ModifiedBy](#BKMK_ModifiedBy)
- [ModifiedByName](#BKMK_ModifiedByName)
- [ModifiedByYomiName](#BKMK_ModifiedByYomiName)
- [ModifiedOn](#BKMK_ModifiedOn)
- [ModifiedOnBehalfBy](#BKMK_ModifiedOnBehalfBy)
- [ModifiedOnBehalfByName](#BKMK_ModifiedOnBehalfByName)
- [ModifiedOnBehalfByYomiName](#BKMK_ModifiedOnBehalfByYomiName)
- [ObjectIdName](#BKMK_ObjectIdName)
- [ObjectTypeCode](#BKMK_ObjectTypeCode)
- [OrganizationId](#BKMK_OrganizationId)
- [OrganizationIdName](#BKMK_OrganizationIdName)
- [OwnerId](#BKMK_OwnerId)
- [OwnerIdType](#BKMK_OwnerIdType)
- [OwningBusinessUnit](#BKMK_OwningBusinessUnit)
- [OwningUser](#BKMK_OwningUser)
- [QueueIdName](#BKMK_QueueIdName)
- [Title](#BKMK_Title)
- [TransactionCurrencyIdName](#BKMK_TransactionCurrencyIdName)
- [VersionNumber](#BKMK_VersionNumber)
- [WorkerIdModifiedOn](#BKMK_WorkerIdModifiedOn)
- [WorkerIdName](#BKMK_WorkerIdName)
- [WorkerIdYomiName](#BKMK_WorkerIdYomiName)


### <a name="BKMK_CreatedBy"></a> CreatedBy

|Property|Value|
|--------|-----|
|Description|Shows who created the record.|
|DisplayName|Created By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedByName"></a> CreatedByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_CreatedByYomiName"></a> CreatedByYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdbyyominame|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_CreatedOn"></a> CreatedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date and time when the record was created. The date and time are displayed in the time zone selected in Microsoft Dynamics 365 options.|
|DisplayName|Created On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_CreatedOnBehalfBy"></a> CreatedOnBehalfBy

|Property|Value|
|--------|-----|
|Description|Shows who created the record on behalf of another user.|
|DisplayName|Created By (Delegate)|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedOnBehalfByName"></a> CreatedOnBehalfByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdonbehalfbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_CreatedOnBehalfByYomiName"></a> CreatedOnBehalfByYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|createdonbehalfbyyominame|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_EnteredOn"></a> EnteredOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date the record was assigned to the queue.|
|DisplayName|Entered Queue|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|enteredon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_ExchangeRate"></a> ExchangeRate

|Property|Value|
|--------|-----|
|Description|Shows the conversion rate of the record's currency. The exchange rate is used to convert all money fields in the record from the local currency to the system's default currency.|
|DisplayName|Exchange Rate|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|exchangerate|
|MaxValue|100000000000|
|MinValue|0.0000000001|
|Precision|10|
|RequiredLevel|None|
|Type|Decimal|


### <a name="BKMK_ModifiedBy"></a> ModifiedBy

|Property|Value|
|--------|-----|
|Description|Shows who last updated the record.|
|DisplayName|Modified By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedByName"></a> ModifiedByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ModifiedByYomiName"></a> ModifiedByYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedbyyominame|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ModifiedOn"></a> ModifiedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date and time when the record was last updated. The date and time are displayed in the time zone selected in Microsoft Dynamics 365 options.|
|DisplayName|Modified On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_ModifiedOnBehalfBy"></a> ModifiedOnBehalfBy

|Property|Value|
|--------|-----|
|Description|Unique identifier of the delegate user who last modified the queueitem.|
|DisplayName|Modified By (Delegate)|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedOnBehalfByName"></a> ModifiedOnBehalfByName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfbyname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ModifiedOnBehalfByYomiName"></a> ModifiedOnBehalfByYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfbyyominame|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ObjectIdName"></a> ObjectIdName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|objectidname|
|MaxLength|300|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_ObjectTypeCode"></a> ObjectTypeCode

|Property|Value|
|--------|-----|
|Description|Select the type of the queue item, such as activity, case, or appointment.|
|DisplayName|Type|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|objecttypecode|
|RequiredLevel|None|
|Type|Picklist|

#### ObjectTypeCode Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|112|Case|Service request case associated with a contract.|
|4200|Activity|Task performed, or to be performed, by a user. An activity is any action for which an entry can be made on a calendar.|
|4201|Appointment|Commitment representing a time interval with start/end times and duration.|
|4202|Email|Activity that is delivered using email protocols.|
|4204|Fax|Activity that tracks call outcome and number of pages for a fax and optionally stores an electronic copy of the document.|
|4207|Letter|Activity that tracks the delivery of a letter. The activity can contain the electronic copy of the letter.|
|4210|Phone Call|Activity to track a telephone call.|
|4212|Task|Generic activity representing work needed to be done.|
|4214|Service Activity|Activity offered by the organization to satisfy its customer's needs. Each service activity includes date, time, duration, and required resources.|
|4216|Social Activity|For internal use only.|
|4251|Recurring Appointment|The Master appointment of a recurring appointment series.|
|4401|Campaign Response|Response from an existing or a potential new customer for a campaign.|
|4402|Campaign Activity|Task performed, or to be performed, by a user for planning or running a campaign.|
|4406|Quick Campaign|System operation used to perform lengthy and asynchronous operations on large data sets, such as distributing a campaign activity or quick campaign.|
|9953|Knowledge Article|Organizational knowledge for internal and external use.|



### <a name="BKMK_OrganizationId"></a> OrganizationId

|Property|Value|
|--------|-----|
|Description|Unique identifier of the organization with which the queue item is associated.|
|DisplayName|Organization|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|organizationid|
|RequiredLevel|SystemRequired|
|Targets|organization|
|Type|Lookup|


### <a name="BKMK_OrganizationIdName"></a> OrganizationIdName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|organizationidname|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwnerId"></a> OwnerId

|Property|Value|
|--------|-----|
|Description|Unique identifier of the user or team who owns the queue item.|
|DisplayName|Owner|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|ownerid|
|RequiredLevel|ApplicationRequired|
|Targets|systemuser,team|
|Type|Owner|


### <a name="BKMK_OwnerIdType"></a> OwnerIdType

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridtype|
|RequiredLevel|SystemRequired|
|Type|EntityName|


### <a name="BKMK_OwningBusinessUnit"></a> OwningBusinessUnit

|Property|Value|
|--------|-----|
|Description|Unique identifier of the business unit that owns the queue item.|
|DisplayName|Owning Business Unit|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningbusinessunit|
|RequiredLevel|ApplicationRequired|
|Targets|businessunit|
|Type|Lookup|


### <a name="BKMK_OwningUser"></a> OwningUser

|Property|Value|
|--------|-----|
|Description|Unique identifier of the user who owns the queue item.|
|DisplayName|Owning User|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owninguser|
|RequiredLevel|ApplicationRequired|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_QueueIdName"></a> QueueIdName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|queueidname|
|MaxLength|400|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_Title"></a> Title

|Property|Value|
|--------|-----|
|Description|Shows the title or name that describes the queue record. This value is copied from the record that was assigned to the queue.|
|DisplayName|Title|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|title|
|MaxLength|300|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_TransactionCurrencyIdName"></a> TransactionCurrencyIdName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|transactioncurrencyidname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_VersionNumber"></a> VersionNumber

|Property|Value|
|--------|-----|
|Description|Version number of the queue item.|
|DisplayName|Version Number|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|versionnumber|
|MaxValue|9223372036854775807|
|MinValue|-9223372036854775808|
|RequiredLevel|None|
|Type|BigInt|


### <a name="BKMK_WorkerIdModifiedOn"></a> WorkerIdModifiedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date and time when the queue item was last assigned to a user.|
|DisplayName|Worked On|
|Format|DateOnly|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|workeridmodifiedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_WorkerIdName"></a> WorkerIdName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|workeridname|
|MaxLength|160|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_WorkerIdYomiName"></a> WorkerIdYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|workeridyominame|
|MaxLength|160|
|RequiredLevel|None|
|Type|String|

<a name="onetomany"></a>

## One-To-Many Relationships

Listed by **SchemaName**.

- [QueueItem_AsyncOperations](#BKMK_QueueItem_AsyncOperations)
- [QueueItem_SyncErrors](#BKMK_QueueItem_SyncErrors)
- [QueueItem_BulkDeleteFailures](#BKMK_QueueItem_BulkDeleteFailures)
- [queueitem_principalobjectattributeaccess](#BKMK_queueitem_principalobjectattributeaccess)
- [QueueItem_ProcessSessions](#BKMK_QueueItem_ProcessSessions)


### <a name="BKMK_QueueItem_AsyncOperations"></a> QueueItem_AsyncOperations

Same as the [QueueItem_AsyncOperations](asyncoperation.md#BKMK_QueueItem_AsyncOperations) many-to-one relationship for the [asyncoperation](asyncoperation.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|asyncoperation|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|False|
|ReferencedEntityNavigationPropertyName|QueueItem_AsyncOperations|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: NoCascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_QueueItem_SyncErrors"></a> QueueItem_SyncErrors

Same as the [QueueItem_SyncErrors](syncerror.md#BKMK_QueueItem_SyncErrors) many-to-one relationship for the [syncerror](syncerror.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|syncerror|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|QueueItem_SyncErrors|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: Cascade<br />Delete: Cascade<br />Merge: Cascade<br />Reparent: Cascade<br />Share: Cascade<br />Unshare: Cascade|


### <a name="BKMK_QueueItem_BulkDeleteFailures"></a> QueueItem_BulkDeleteFailures

Same as the [QueueItem_BulkDeleteFailures](bulkdeletefailure.md#BKMK_QueueItem_BulkDeleteFailures) many-to-one relationship for the [bulkdeletefailure](bulkdeletefailure.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|bulkdeletefailure|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|False|
|ReferencedEntityNavigationPropertyName|QueueItem_BulkDeleteFailures|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_queueitem_principalobjectattributeaccess"></a> queueitem_principalobjectattributeaccess

Same as the [queueitem_principalobjectattributeaccess](principalobjectattributeaccess.md#BKMK_queueitem_principalobjectattributeaccess) many-to-one relationship for the [principalobjectattributeaccess](principalobjectattributeaccess.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|principalobjectattributeaccess|
|ReferencingAttribute|objectid|
|IsHierarchical|False|
|IsCustomizable|False|
|ReferencedEntityNavigationPropertyName|queueitem_principalobjectattributeaccess|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_QueueItem_ProcessSessions"></a> QueueItem_ProcessSessions

Same as the [QueueItem_ProcessSessions](processsession.md#BKMK_QueueItem_ProcessSessions) many-to-one relationship for the [processsession](processsession.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|processsession|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|False|
|ReferencedEntityNavigationPropertyName|QueueItem_ProcessSessions|
|AssociatedMenuConfiguration|Behavior: UseCollectionName<br />Group: Details<br />Label: <br />Order: 110|
|CascadeConfiguration|Assign: NoCascade<br />Delete: NoCascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|

<a name="manytoone"></a>

## Many-To-One Relationships

Each Many-To-One relationship is defined by a corresponding One-To-Many relationship with the related entity. Listed by **SchemaName**.

- [knowledgearticle_QueueItems](#BKMK_knowledgearticle_QueueItems)
- [CampaignActivity_QueueItem](#BKMK_CampaignActivity_QueueItem)
- [CampaignResponse_QueueItem](#BKMK_CampaignResponse_QueueItem)
- [BulkOperation_QueueItem](#BKMK_BulkOperation_QueueItem)
- [Incident_QueueItem](#BKMK_Incident_QueueItem)
- [ServiceAppointment_QueueItem](#BKMK_ServiceAppointment_QueueItem)
- [lk_queueitem_createdonbehalfby](#BKMK_lk_queueitem_createdonbehalfby)
- [lk_queueitembase_workerid](#BKMK_lk_queueitembase_workerid)
- [ActivityPointer_QueueItem](#BKMK_ActivityPointer_QueueItem)
- [queue_entries](#BKMK_queue_entries)
- [lk_queueitembase_createdby](#BKMK_lk_queueitembase_createdby)
- [organization_queueitems](#BKMK_organization_queueitems)
- [TransactionCurrency_QueueItem](#BKMK_TransactionCurrency_QueueItem)
- [Appointment_QueueItem](#BKMK_Appointment_QueueItem)
- [Fax_QueueItem](#BKMK_Fax_QueueItem)
- [team_queueitembase_workerid](#BKMK_team_queueitembase_workerid)
- [Email_QueueItem](#BKMK_Email_QueueItem)
- [SocialActivity_QueueItem](#BKMK_SocialActivity_QueueItem)
- [lk_queueitem_modifiedonbehalfby](#BKMK_lk_queueitem_modifiedonbehalfby)
- [PhoneCall_QueueItem](#BKMK_PhoneCall_QueueItem)
- [Task_QueueItem](#BKMK_Task_QueueItem)
- [RecurringAppointmentMaster_QueueItem](#BKMK_RecurringAppointmentMaster_QueueItem)
- [Letter_QueueItem](#BKMK_Letter_QueueItem)
- [lk_queueitembase_modifiedby](#BKMK_lk_queueitembase_modifiedby)


### <a name="BKMK_knowledgearticle_QueueItems"></a> knowledgearticle_QueueItems

See the [knowledgearticle_QueueItems](knowledgearticle.md#BKMK_knowledgearticle_QueueItems) one-to-many relationship for the [knowledgearticle](knowledgearticle.md) entity.

### <a name="BKMK_CampaignActivity_QueueItem"></a> CampaignActivity_QueueItem

**Added by**: Marketing Solution

See the [CampaignActivity_QueueItem](campaignactivity.md#BKMK_CampaignActivity_QueueItem) one-to-many relationship for the [campaignactivity](campaignactivity.md) entity.

### <a name="BKMK_CampaignResponse_QueueItem"></a> CampaignResponse_QueueItem

**Added by**: Marketing Solution

See the [CampaignResponse_QueueItem](campaignresponse.md#BKMK_CampaignResponse_QueueItem) one-to-many relationship for the [campaignresponse](campaignresponse.md) entity.

### <a name="BKMK_BulkOperation_QueueItem"></a> BulkOperation_QueueItem

**Added by**: Marketing Solution

See the [BulkOperation_QueueItem](bulkoperation.md#BKMK_BulkOperation_QueueItem) one-to-many relationship for the [bulkoperation](bulkoperation.md) entity.

### <a name="BKMK_Incident_QueueItem"></a> Incident_QueueItem

**Added by**: Service Solution

See the [Incident_QueueItem](incident.md#BKMK_Incident_QueueItem) one-to-many relationship for the [incident](incident.md) entity.

### <a name="BKMK_ServiceAppointment_QueueItem"></a> ServiceAppointment_QueueItem

**Added by**: Service Solution

See the [ServiceAppointment_QueueItem](serviceappointment.md#BKMK_ServiceAppointment_QueueItem) one-to-many relationship for the [serviceappointment](serviceappointment.md) entity.

### <a name="BKMK_lk_queueitem_createdonbehalfby"></a> lk_queueitem_createdonbehalfby

See the [lk_queueitem_createdonbehalfby](systemuser.md#BKMK_lk_queueitem_createdonbehalfby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_lk_queueitembase_workerid"></a> lk_queueitembase_workerid

See the [lk_queueitembase_workerid](systemuser.md#BKMK_lk_queueitembase_workerid) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_ActivityPointer_QueueItem"></a> ActivityPointer_QueueItem

See the [ActivityPointer_QueueItem](activitypointer.md#BKMK_ActivityPointer_QueueItem) one-to-many relationship for the [activitypointer](activitypointer.md) entity.

### <a name="BKMK_queue_entries"></a> queue_entries

See the [queue_entries](queue.md#BKMK_queue_entries) one-to-many relationship for the [queue](queue.md) entity.

### <a name="BKMK_lk_queueitembase_createdby"></a> lk_queueitembase_createdby

See the [lk_queueitembase_createdby](systemuser.md#BKMK_lk_queueitembase_createdby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_organization_queueitems"></a> organization_queueitems

See the [organization_queueitems](organization.md#BKMK_organization_queueitems) one-to-many relationship for the [organization](organization.md) entity.

### <a name="BKMK_TransactionCurrency_QueueItem"></a> TransactionCurrency_QueueItem

See the [TransactionCurrency_QueueItem](transactioncurrency.md#BKMK_TransactionCurrency_QueueItem) one-to-many relationship for the [transactioncurrency](transactioncurrency.md) entity.

### <a name="BKMK_Appointment_QueueItem"></a> Appointment_QueueItem

See the [Appointment_QueueItem](appointment.md#BKMK_Appointment_QueueItem) one-to-many relationship for the [appointment](appointment.md) entity.

### <a name="BKMK_Fax_QueueItem"></a> Fax_QueueItem

See the [Fax_QueueItem](fax.md#BKMK_Fax_QueueItem) one-to-many relationship for the [fax](fax.md) entity.

### <a name="BKMK_team_queueitembase_workerid"></a> team_queueitembase_workerid

See the [team_queueitembase_workerid](team.md#BKMK_team_queueitembase_workerid) one-to-many relationship for the [team](team.md) entity.

### <a name="BKMK_Email_QueueItem"></a> Email_QueueItem

See the [Email_QueueItem](email.md#BKMK_Email_QueueItem) one-to-many relationship for the [email](email.md) entity.

### <a name="BKMK_SocialActivity_QueueItem"></a> SocialActivity_QueueItem

See the [SocialActivity_QueueItem](socialactivity.md#BKMK_SocialActivity_QueueItem) one-to-many relationship for the [socialactivity](socialactivity.md) entity.

### <a name="BKMK_lk_queueitem_modifiedonbehalfby"></a> lk_queueitem_modifiedonbehalfby

See the [lk_queueitem_modifiedonbehalfby](systemuser.md#BKMK_lk_queueitem_modifiedonbehalfby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_PhoneCall_QueueItem"></a> PhoneCall_QueueItem

See the [PhoneCall_QueueItem](phonecall.md#BKMK_PhoneCall_QueueItem) one-to-many relationship for the [phonecall](phonecall.md) entity.

### <a name="BKMK_Task_QueueItem"></a> Task_QueueItem

See the [Task_QueueItem](task.md#BKMK_Task_QueueItem) one-to-many relationship for the [task](task.md) entity.

### <a name="BKMK_RecurringAppointmentMaster_QueueItem"></a> RecurringAppointmentMaster_QueueItem

See the [RecurringAppointmentMaster_QueueItem](recurringappointmentmaster.md#BKMK_RecurringAppointmentMaster_QueueItem) one-to-many relationship for the [recurringappointmentmaster](recurringappointmentmaster.md) entity.

### <a name="BKMK_Letter_QueueItem"></a> Letter_QueueItem

See the [Letter_QueueItem](letter.md#BKMK_Letter_QueueItem) one-to-many relationship for the [letter](letter.md) entity.

### <a name="BKMK_lk_queueitembase_modifiedby"></a> lk_queueitembase_modifiedby

See the [lk_queueitembase_modifiedby](systemuser.md#BKMK_lk_queueitembase_modifiedby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### See also

[About the Entity Reference](../about-entity-reference.md)<br />
[Web API EntityType Reference](/power-apps/developer/data-platform/webapi/reference/entitytypes)
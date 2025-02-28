---
title: "msdyn_wallsavedqueryusersettings entity reference (Dynamics 365 Customer Engagement) | Microsoft Docs"
description: "Includes schema information and supported messages for the msdyn_wallsavedqueryusersettings entity."
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

# msdyn_wallsavedqueryusersettings entity reference

Contains user personalization information regarding which of the administrator’s selected views to display on a user’s personal wall.

**Added by**: Activity Feeds Solution


## Messages

|Message|SDK class or method|
|-|-|
|Assign|<xref:Microsoft.Crm.Sdk.Messages.AssignRequest>|
|Create|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>|
|Delete|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>|
|GrantAccess|<xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>|
|IsValidStateTransition|<xref:Microsoft.Crm.Sdk.Messages.IsValidStateTransitionRequest>|
|ModifyAccess|<xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>|
|Retrieve|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>|
|RetrieveMultiple|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>|
|RetrievePrincipalAccess|<xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest>|
|RetrieveSharedPrincipalsAndAccess|<xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest>|
|RevokeAccess|<xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>|
|SetState|<xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>|
|Update|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>|

## Properties

|Property|Value|
|--------|-----|
|CollectionSchemaName|msdyn_wallsavedqueryusersettingses|
|DisplayCollectionName|Filters|
|DisplayName|Filter|
|EntitySetName|msdyn_wallsavedqueryusersettingses|
|IsBPFEntity|False|
|LogicalCollectionName|msdyn_wallsavedqueryusersettingses|
|LogicalName|msdyn_wallsavedqueryusersettings|
|OwnershipType|UserOwned|
|PrimaryIdAttribute|msdyn_wallsavedqueryusersettingsid|
|PrimaryNameAttribute|msdyn_entityname|
|SchemaName|msdyn_wallsavedqueryusersettings|

<a name="writable-attributes"></a>

## Writable attributes

These attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [ImportSequenceNumber](#BKMK_ImportSequenceNumber)
- [msdyn_data](#BKMK_msdyn_data)
- [msdyn_default](#BKMK_msdyn_default)
- [msdyn_entitydisplayname](#BKMK_msdyn_entitydisplayname)
- [msdyn_entityname](#BKMK_msdyn_entityname)
- [msdyn_includewallinresponse](#BKMK_msdyn_includewallinresponse)
- [msdyn_isfollowing](#BKMK_msdyn_isfollowing)
- [msdyn_IsVirtual](#BKMK_msdyn_IsVirtual)
- [msdyn_isvisible](#BKMK_msdyn_isvisible)
- [msdyn_isvisiblebit](#BKMK_msdyn_isvisiblebit)
- [msdyn_otc](#BKMK_msdyn_otc)
- [msdyn_savedqueryname](#BKMK_msdyn_savedqueryname)
- [msdyn_sortorder](#BKMK_msdyn_sortorder)
- [msdyn_type](#BKMK_msdyn_type)
- [msdyn_userid](#BKMK_msdyn_userid)
- [msdyn_wallsavedqueryid](#BKMK_msdyn_wallsavedqueryid)
- [msdyn_wallsavedqueryusersettingsId](#BKMK_msdyn_wallsavedqueryusersettingsId)
- [OverriddenCreatedOn](#BKMK_OverriddenCreatedOn)
- [OwnerId](#BKMK_OwnerId)
- [OwnerIdType](#BKMK_OwnerIdType)
- [statecode](#BKMK_statecode)
- [statuscode](#BKMK_statuscode)
- [TimeZoneRuleVersionNumber](#BKMK_TimeZoneRuleVersionNumber)
- [UTCConversionTimeZoneCode](#BKMK_UTCConversionTimeZoneCode)


### <a name="BKMK_ImportSequenceNumber"></a> ImportSequenceNumber

|Property|Value|
|--------|-----|
|Description|Sequence number of the import that created this record.|
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


### <a name="BKMK_msdyn_data"></a> msdyn_data

|Property|Value|
|--------|-----|
|Description|XML blob that stores personalization data for the user.|
|DisplayName|Data|
|Format|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_data|
|MaxLength|10000|
|RequiredLevel|Recommended|
|Type|Memo|


### <a name="BKMK_msdyn_default"></a> msdyn_default

|Property|Value|
|--------|-----|
|Description|Indicates that view is selected by default if value is greater than 0. Also contains information which specific filter is applied.|
|DisplayName|Default|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_default|
|MaxValue|2147483647|
|MinValue|0|
|RequiredLevel|ApplicationRequired|
|Type|Integer|


### <a name="BKMK_msdyn_entitydisplayname"></a> msdyn_entitydisplayname

|Property|Value|
|--------|-----|
|Description|Display name of the entity to which the corresponding views belong.|
|DisplayName|Entity Display Name|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_entitydisplayname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_msdyn_entityname"></a> msdyn_entityname

|Property|Value|
|--------|-----|
|Description|Name of the entity to which the corresponding views belong.|
|DisplayName|Entity Name|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_entityname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_msdyn_includewallinresponse"></a> msdyn_includewallinresponse

|Property|Value|
|--------|-----|
|Description|Indicates that wall should be included in response to avoid roundtrips to server|
|DisplayName|Include Wall in response|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_includewallinresponse|
|RequiredLevel|None|
|Type|Boolean|

#### msdyn_includewallinresponse Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|1|Yes||
|0|No||

**DefaultValue**: 0



### <a name="BKMK_msdyn_isfollowing"></a> msdyn_isfollowing

|Property|Value|
|--------|-----|
|Description|Indicates that corresponding view is following view|
|DisplayName|Is Following|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_isfollowing|
|RequiredLevel|None|
|Type|Boolean|

#### msdyn_isfollowing Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|1|Yes||
|0|No||

**DefaultValue**: 0



### <a name="BKMK_msdyn_IsVirtual"></a> msdyn_IsVirtual

|Property|Value|
|--------|-----|
|Description|Indicates that the record is virtual|
|DisplayName|Is Virtual|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_isvirtual|
|RequiredLevel|None|
|Type|Boolean|

#### msdyn_IsVirtual Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|1|Yes||
|0|No||

**DefaultValue**: 0



### <a name="BKMK_msdyn_isvisible"></a> msdyn_isvisible

|Property|Value|
|--------|-----|
|Description|Information that indicates whether the corresponding view should be displayed on the personal wall for this user.|
|DisplayName|Display on the wall|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_isvisible|
|RequiredLevel|Recommended|
|Type|Boolean|

#### msdyn_isvisible Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|1|Shown||
|0|Hidden||

**DefaultValue**: 1



### <a name="BKMK_msdyn_isvisiblebit"></a> msdyn_isvisiblebit

|Property|Value|
|--------|-----|
|Description|For internal use only.|
|DisplayName|Is Visible bit|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_isvisiblebit|
|MaxValue|2147483647|
|MinValue|-2147483648|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_msdyn_otc"></a> msdyn_otc

|Property|Value|
|--------|-----|
|Description|Virtual column which contains entity type code for the entities returned by corresponding savedquery|
|DisplayName|Entity Type|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_otc|
|MaxValue|2147483647|
|MinValue|0|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_msdyn_savedqueryname"></a> msdyn_savedqueryname

|Property|Value|
|--------|-----|
|Description|Name of the corresponding view.|
|DisplayName|View Name|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_savedqueryname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_msdyn_sortorder"></a> msdyn_sortorder

|Property|Value|
|--------|-----|
|Description|Sort order to be used when displaying the filter on the user’s personal wall.|
|DisplayName|Sort Order|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_sortorder|
|MaxValue|2147483647|
|MinValue|0|
|RequiredLevel|Recommended|
|Type|Integer|


### <a name="BKMK_msdyn_type"></a> msdyn_type

|Property|Value|
|--------|-----|
|Description|Reserved to support different view types. Currently not used.|
|DisplayName|Type|
|Format|None|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_type|
|MaxValue|2147483647|
|MinValue|0|
|RequiredLevel|None|
|Type|Integer|


### <a name="BKMK_msdyn_userid"></a> msdyn_userid

|Property|Value|
|--------|-----|
|Description|Unique identifier for User associated with Wall View User Setting.|
|DisplayName|User Id|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_userid|
|RequiredLevel|ApplicationRequired|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_msdyn_wallsavedqueryid"></a> msdyn_wallsavedqueryid

|Property|Value|
|--------|-----|
|Description|Unique identifier for Wall View associated with Wall View User Setting.|
|DisplayName|Wall View Id|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|msdyn_wallsavedqueryid|
|RequiredLevel|ApplicationRequired|
|Targets|msdyn_wallsavedquery|
|Type|Lookup|


### <a name="BKMK_msdyn_wallsavedqueryusersettingsId"></a> msdyn_wallsavedqueryusersettingsId

|Property|Value|
|--------|-----|
|Description|Unique identifier for entity instances|
|DisplayName|Filter|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|msdyn_wallsavedqueryusersettingsid|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|


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


### <a name="BKMK_OwnerId"></a> OwnerId

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Owner Id|
|DisplayName|Owner|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|ownerid|
|RequiredLevel|SystemRequired|
|Targets|systemuser,team|
|Type|Owner|


### <a name="BKMK_OwnerIdType"></a> OwnerIdType

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Owner Id Type|
|DisplayName||
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridtype|
|RequiredLevel|SystemRequired|
|Type|EntityName|


### <a name="BKMK_statecode"></a> statecode

|Property|Value|
|--------|-----|
|Description|Status of the Wall View User Setting|
|DisplayName|Status|
|IsValidForCreate|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|statecode|
|RequiredLevel|SystemRequired|
|Type|State|

#### statecode Choices/Options

|Value|Label|DefaultStatus|InvariantName|
|-----|-----|-------------|-------------|
|0|Active|1|Active|
|1|Inactive|2|Inactive|



### <a name="BKMK_statuscode"></a> statuscode

|Property|Value|
|--------|-----|
|Description|Reason for the status of the Wall View User Setting|
|DisplayName|Status Reason|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|statuscode|
|RequiredLevel|None|
|Type|Status|

#### statuscode Choices/Options

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
- [ModifiedBy](#BKMK_ModifiedBy)
- [ModifiedByName](#BKMK_ModifiedByName)
- [ModifiedByYomiName](#BKMK_ModifiedByYomiName)
- [ModifiedOn](#BKMK_ModifiedOn)
- [ModifiedOnBehalfBy](#BKMK_ModifiedOnBehalfBy)
- [ModifiedOnBehalfByName](#BKMK_ModifiedOnBehalfByName)
- [ModifiedOnBehalfByYomiName](#BKMK_ModifiedOnBehalfByYomiName)
- [msdyn_useridName](#BKMK_msdyn_useridName)
- [msdyn_useridYomiName](#BKMK_msdyn_useridYomiName)
- [msdyn_wallsavedqueryidName](#BKMK_msdyn_wallsavedqueryidName)
- [OwnerIdName](#BKMK_OwnerIdName)
- [OwnerIdYomiName](#BKMK_OwnerIdYomiName)
- [OwningBusinessUnit](#BKMK_OwningBusinessUnit)
- [OwningTeam](#BKMK_OwningTeam)
- [OwningUser](#BKMK_OwningUser)
- [VersionNumber](#BKMK_VersionNumber)


### <a name="BKMK_CreatedBy"></a> CreatedBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the user who created the record.|
|DisplayName|Created By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedByName"></a> CreatedByName

**Added by**: Active Solution Solution

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

**Added by**: Active Solution Solution

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
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_CreatedOn"></a> CreatedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Date and time when the record was created.|
|DisplayName|Created On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_CreatedOnBehalfBy"></a> CreatedOnBehalfBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the delegate user who created the record.|
|DisplayName|Created By (Delegate)|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|createdonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_CreatedOnBehalfByName"></a> CreatedOnBehalfByName

**Added by**: Active Solution Solution

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

**Added by**: Active Solution Solution

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
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_ModifiedBy"></a> ModifiedBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the user who modified the record.|
|DisplayName|Modified By|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedByName"></a> ModifiedByName

**Added by**: Active Solution Solution

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

**Added by**: Active Solution Solution

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
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_ModifiedOn"></a> ModifiedOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Date and time when the record was modified.|
|DisplayName|Modified On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedon|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_ModifiedOnBehalfBy"></a> ModifiedOnBehalfBy

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier of the delegate user who modified the record.|
|DisplayName|Modified By (Delegate)|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|modifiedonbehalfby|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_ModifiedOnBehalfByName"></a> ModifiedOnBehalfByName

**Added by**: Active Solution Solution

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

**Added by**: Active Solution Solution

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
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_msdyn_useridName"></a> msdyn_useridName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|msdyn_useridname|
|MaxLength|200|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_msdyn_useridYomiName"></a> msdyn_useridYomiName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|msdyn_useridyominame|
|MaxLength|200|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_msdyn_wallsavedqueryidName"></a> msdyn_wallsavedqueryidName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|msdyn_wallsavedqueryidname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_OwnerIdName"></a> OwnerIdName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Name of the owner|
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridname|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwnerIdYomiName"></a> OwnerIdYomiName

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Yomi name of the owner|
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridyominame|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwningBusinessUnit"></a> OwningBusinessUnit

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier for the business unit that owns the record|
|DisplayName|Owning Business Unit|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningbusinessunit|
|RequiredLevel|None|
|Targets|businessunit|
|Type|Lookup|


### <a name="BKMK_OwningTeam"></a> OwningTeam

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier for the team that owns the record.|
|DisplayName|Owning Team|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningteam|
|RequiredLevel|None|
|Targets|team|
|Type|Lookup|


### <a name="BKMK_OwningUser"></a> OwningUser

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Unique identifier for the user that owns the record.|
|DisplayName|Owning User|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owninguser|
|RequiredLevel|None|
|Targets|systemuser|
|Type|Lookup|


### <a name="BKMK_VersionNumber"></a> VersionNumber

**Added by**: Active Solution Solution

|Property|Value|
|--------|-----|
|Description|Version Number|
|DisplayName|Version Number|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|versionnumber|
|MaxValue|9223372036854775807|
|MinValue|-9223372036854775808|
|RequiredLevel|None|
|Type|BigInt|

<a name="onetomany"></a>

## One-To-Many Relationships

Listed by **SchemaName**.

- [msdyn_wallsavedqueryusersettings_SyncErrors](#BKMK_msdyn_wallsavedqueryusersettings_SyncErrors)
- [msdyn_wallsavedqueryusersettings_AsyncOperations](#BKMK_msdyn_wallsavedqueryusersettings_AsyncOperations)
- [msdyn_wallsavedqueryusersettings_MailboxTrackingFolders](#BKMK_msdyn_wallsavedqueryusersettings_MailboxTrackingFolders)
- [msdyn_wallsavedqueryusersettings_ProcessSession](#BKMK_msdyn_wallsavedqueryusersettings_ProcessSession)
- [msdyn_wallsavedqueryusersettings_BulkDeleteFailures](#BKMK_msdyn_wallsavedqueryusersettings_BulkDeleteFailures)
- [msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses](#BKMK_msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses)


### <a name="BKMK_msdyn_wallsavedqueryusersettings_SyncErrors"></a> msdyn_wallsavedqueryusersettings_SyncErrors

**Added by**: System Solution Solution

Same as the [msdyn_wallsavedqueryusersettings_SyncErrors](syncerror.md#BKMK_msdyn_wallsavedqueryusersettings_SyncErrors) many-to-one relationship for the [syncerror](syncerror.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|syncerror|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|msdyn_wallsavedqueryusersettings_SyncErrors|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_msdyn_wallsavedqueryusersettings_AsyncOperations"></a> msdyn_wallsavedqueryusersettings_AsyncOperations

**Added by**: System Solution Solution

Same as the [msdyn_wallsavedqueryusersettings_AsyncOperations](asyncoperation.md#BKMK_msdyn_wallsavedqueryusersettings_AsyncOperations) many-to-one relationship for the [asyncoperation](asyncoperation.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|asyncoperation|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|msdyn_wallsavedqueryusersettings_AsyncOperations|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: NoCascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_msdyn_wallsavedqueryusersettings_MailboxTrackingFolders"></a> msdyn_wallsavedqueryusersettings_MailboxTrackingFolders

**Added by**: System Solution Solution

Same as the [msdyn_wallsavedqueryusersettings_MailboxTrackingFolders](mailboxtrackingfolder.md#BKMK_msdyn_wallsavedqueryusersettings_MailboxTrackingFolders) many-to-one relationship for the [mailboxtrackingfolder](mailboxtrackingfolder.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|mailboxtrackingfolder|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|msdyn_wallsavedqueryusersettings_MailboxTrackingFolders|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_msdyn_wallsavedqueryusersettings_ProcessSession"></a> msdyn_wallsavedqueryusersettings_ProcessSession

**Added by**: System Solution Solution

Same as the [msdyn_wallsavedqueryusersettings_ProcessSession](processsession.md#BKMK_msdyn_wallsavedqueryusersettings_ProcessSession) many-to-one relationship for the [processsession](processsession.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|processsession|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|msdyn_wallsavedqueryusersettings_ProcessSession|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: NoCascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_msdyn_wallsavedqueryusersettings_BulkDeleteFailures"></a> msdyn_wallsavedqueryusersettings_BulkDeleteFailures

**Added by**: System Solution Solution

Same as the [msdyn_wallsavedqueryusersettings_BulkDeleteFailures](bulkdeletefailure.md#BKMK_msdyn_wallsavedqueryusersettings_BulkDeleteFailures) many-to-one relationship for the [bulkdeletefailure](bulkdeletefailure.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|bulkdeletefailure|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|msdyn_wallsavedqueryusersettings_BulkDeleteFailures|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses"></a> msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses

**Added by**: System Solution Solution

Same as the [msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses](principalobjectattributeaccess.md#BKMK_msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses) many-to-one relationship for the [principalobjectattributeaccess](principalobjectattributeaccess.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|principalobjectattributeaccess|
|ReferencingAttribute|objectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|msdyn_wallsavedqueryusersettings_PrincipalObjectAttributeAccesses|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: Cascade<br />Merge: NoCascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|

<a name="manytoone"></a>

## Many-To-One Relationships

Each Many-To-One relationship is defined by a corresponding One-To-Many relationship with the related entity. Listed by **SchemaName**.

- [lk_msdyn_wallsavedqueryusersettings_createdby](#BKMK_lk_msdyn_wallsavedqueryusersettings_createdby)
- [lk_msdyn_wallsavedqueryusersettings_createdonbehalfby](#BKMK_lk_msdyn_wallsavedqueryusersettings_createdonbehalfby)
- [lk_msdyn_wallsavedqueryusersettings_modifiedby](#BKMK_lk_msdyn_wallsavedqueryusersettings_modifiedby)
- [lk_msdyn_wallsavedqueryusersettings_modifiedonbehalfby](#BKMK_lk_msdyn_wallsavedqueryusersettings_modifiedonbehalfby)
- [user_msdyn_wallsavedqueryusersettings](#BKMK_user_msdyn_wallsavedqueryusersettings)
- [team_msdyn_wallsavedqueryusersettings](#BKMK_team_msdyn_wallsavedqueryusersettings)
- [business_unit_msdyn_wallsavedqueryusersettings](#BKMK_business_unit_msdyn_wallsavedqueryusersettings)
- [msdyn_systemuser_wallsavedqueryusersettings_userid](#BKMK_msdyn_systemuser_wallsavedqueryusersettings_userid)
- [msdyn_wallsavedquery_wallsavedqueryusersettings](#BKMK_msdyn_wallsavedquery_wallsavedqueryusersettings)


### <a name="BKMK_lk_msdyn_wallsavedqueryusersettings_createdby"></a> lk_msdyn_wallsavedqueryusersettings_createdby

**Added by**: System Solution Solution

See the [lk_msdyn_wallsavedqueryusersettings_createdby](systemuser.md#BKMK_lk_msdyn_wallsavedqueryusersettings_createdby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_lk_msdyn_wallsavedqueryusersettings_createdonbehalfby"></a> lk_msdyn_wallsavedqueryusersettings_createdonbehalfby

**Added by**: System Solution Solution

See the [lk_msdyn_wallsavedqueryusersettings_createdonbehalfby](systemuser.md#BKMK_lk_msdyn_wallsavedqueryusersettings_createdonbehalfby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_lk_msdyn_wallsavedqueryusersettings_modifiedby"></a> lk_msdyn_wallsavedqueryusersettings_modifiedby

**Added by**: System Solution Solution

See the [lk_msdyn_wallsavedqueryusersettings_modifiedby](systemuser.md#BKMK_lk_msdyn_wallsavedqueryusersettings_modifiedby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_lk_msdyn_wallsavedqueryusersettings_modifiedonbehalfby"></a> lk_msdyn_wallsavedqueryusersettings_modifiedonbehalfby

**Added by**: System Solution Solution

See the [lk_msdyn_wallsavedqueryusersettings_modifiedonbehalfby](systemuser.md#BKMK_lk_msdyn_wallsavedqueryusersettings_modifiedonbehalfby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_user_msdyn_wallsavedqueryusersettings"></a> user_msdyn_wallsavedqueryusersettings

**Added by**: System Solution Solution

See the [user_msdyn_wallsavedqueryusersettings](systemuser.md#BKMK_user_msdyn_wallsavedqueryusersettings) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_team_msdyn_wallsavedqueryusersettings"></a> team_msdyn_wallsavedqueryusersettings

**Added by**: System Solution Solution

See the [team_msdyn_wallsavedqueryusersettings](team.md#BKMK_team_msdyn_wallsavedqueryusersettings) one-to-many relationship for the [team](team.md) entity.

### <a name="BKMK_business_unit_msdyn_wallsavedqueryusersettings"></a> business_unit_msdyn_wallsavedqueryusersettings

**Added by**: System Solution Solution

See the [business_unit_msdyn_wallsavedqueryusersettings](businessunit.md#BKMK_business_unit_msdyn_wallsavedqueryusersettings) one-to-many relationship for the [businessunit](businessunit.md) entity.

### <a name="BKMK_msdyn_systemuser_wallsavedqueryusersettings_userid"></a> msdyn_systemuser_wallsavedqueryusersettings_userid

**Added by**: System Solution Solution

See the [msdyn_systemuser_wallsavedqueryusersettings_userid](systemuser.md#BKMK_msdyn_systemuser_wallsavedqueryusersettings_userid) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_msdyn_wallsavedquery_wallsavedqueryusersettings"></a> msdyn_wallsavedquery_wallsavedqueryusersettings

See the [msdyn_wallsavedquery_wallsavedqueryusersettings](msdyn_wallsavedquery.md#BKMK_msdyn_wallsavedquery_wallsavedqueryusersettings) one-to-many relationship for the [msdyn_wallsavedquery](msdyn_wallsavedquery.md) entity.

### See also

[About the Entity Reference](../about-entity-reference.md)<br />
[Web API EntityType Reference](/power-apps/developer/data-platform/webapi/reference/entitytypes)
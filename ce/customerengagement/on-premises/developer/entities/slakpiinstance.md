---
title: "SLAKPIInstance entity reference (Dynamics 365 Customer Engagement) | Microsoft Docs"
description: "Includes schema information and supported messages for the SLAKPIInstance entity."
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

# SLAKPIInstance entity reference

Service level agreement (SLA) key performance indicator (KPI) instance that is tracked for an individual case


## Messages

|Message|SDK class or method|
|-|-|
|Assign|<xref:Microsoft.Crm.Sdk.Messages.AssignRequest>|
|Create|<xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>|
|Delete|<xref:Microsoft.Xrm.Sdk.Messages.DeleteRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>|
|GrantAccess|<xref:Microsoft.Crm.Sdk.Messages.GrantAccessRequest>|
|ModifyAccess|<xref:Microsoft.Crm.Sdk.Messages.ModifyAccessRequest>|
|Retrieve|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>|
|RetrieveMultiple|<xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>|
|RetrievePrincipalAccess|<xref:Microsoft.Crm.Sdk.Messages.RetrievePrincipalAccessRequest>|
|RetrieveSharedPrincipalsAndAccess|<xref:Microsoft.Crm.Sdk.Messages.RetrieveSharedPrincipalsAndAccessRequest>|
|RevokeAccess|<xref:Microsoft.Crm.Sdk.Messages.RevokeAccessRequest>|
|Update|<xref:Microsoft.Xrm.Sdk.Messages.UpdateRequest> or <br /><xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>|

## Properties

|Property|Value|
|--------|-----|
|CollectionSchemaName|SLAKPIInstances|
|DisplayCollectionName|SLA KPI Instances|
|DisplayName|SLA KPI Instance|
|EntitySetName|slakpiinstances|
|IsBPFEntity|False|
|LogicalCollectionName|slakpiinstances|
|LogicalName|slakpiinstance|
|OwnershipType|UserOwned|
|PrimaryIdAttribute|slakpiinstanceid|
|PrimaryNameAttribute|name|
|SchemaName|SLAKPIInstance|

<a name="writable-attributes"></a>

## Writable attributes

These attributes return true for either **IsValidForCreate** or **IsValidForUpdate** (usually both). Listed by **SchemaName**.

- [ComputedFailureTime](#BKMK_ComputedFailureTime)
- [ComputedWarningTime](#BKMK_ComputedWarningTime)
- [Description](#BKMK_Description)
- [FailureTime](#BKMK_FailureTime)
- [Name](#BKMK_Name)
- [OwnerId](#BKMK_OwnerId)
- [OwnerIdType](#BKMK_OwnerIdType)
- [OwningBusinessUnit](#BKMK_OwningBusinessUnit)
- [OwningTeam](#BKMK_OwningTeam)
- [OwningUser](#BKMK_OwningUser)
- [Regarding](#BKMK_Regarding)
- [RegardingObjectTypeCode](#BKMK_RegardingObjectTypeCode)
- [SLAKPIInstanceId](#BKMK_SLAKPIInstanceId)
- [Status](#BKMK_Status)
- [SucceededOn](#BKMK_SucceededOn)
- [TransactionCurrencyId](#BKMK_TransactionCurrencyId)
- [WarningTime](#BKMK_WarningTime)
- [WarningTimeReached](#BKMK_WarningTimeReached)


### <a name="BKMK_ComputedFailureTime"></a> ComputedFailureTime

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Computed Failure Date and time|
|DisplayName|Computed Failure Time|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|computedfailuretime|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_ComputedWarningTime"></a> ComputedWarningTime

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Computed Warning Date and time|
|DisplayName|Computed Warning Time|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|computedwarningtime|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_Description"></a> Description

|Property|Value|
|--------|-----|
|Description|For internal use only.|
|DisplayName|Description|
|FormatName|TextArea|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|description|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_FailureTime"></a> FailureTime

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Enter the date and time when the service level agreement (SLA) key performance indicator (KPI) will expire.|
|DisplayName|Failure Time|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|failuretime|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_Name"></a> Name

|Property|Value|
|--------|-----|
|Description|Type a descriptive name for the service level agreement (SLA) key performance indicator (KPI) instance.|
|DisplayName|Name|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|name|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_OwnerId"></a> OwnerId

|Property|Value|
|--------|-----|
|Description|Enter the user or team who is assigned to manage the record. This field is updated every time the record is assigned to a different user or team.|
|DisplayName|Owner|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|ownerid|
|RequiredLevel|SystemRequired|
|Targets|systemuser|
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
|Description|Owning Business Unit.|
|DisplayName|Owning Business Unit|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningbusinessunit|
|RequiredLevel|None|
|Targets|businessunit|
|Type|Lookup|


### <a name="BKMK_OwningTeam"></a> OwningTeam

|Property|Value|
|--------|-----|
|Description|OwningTeam.|
|DisplayName|Owning Team|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owningteam|
|RequiredLevel|None|
|Targets||
|Type|Lookup|


### <a name="BKMK_OwningUser"></a> OwningUser

|Property|Value|
|--------|-----|
|Description|Owning User.|
|DisplayName|Owning User|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owninguser|
|RequiredLevel|None|
|Targets||
|Type|Lookup|


### <a name="BKMK_Regarding"></a> Regarding

|Property|Value|
|--------|-----|
|Description|Unique identifier of the record that this service level agreement (SLA) key performance indicator (KPI) instance is associated with.|
|DisplayName|Regarding|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|regarding|
|RequiredLevel|None|
|Targets|incident|
|Type|Lookup|


### <a name="BKMK_RegardingObjectTypeCode"></a> RegardingObjectTypeCode

|Property|Value|
|--------|-----|
|Description|RegardingObjectTypeCode|
|DisplayName|RegardingObjectTypeCode|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|regardingobjecttypecode|
|RequiredLevel|None|
|Type|EntityName|


### <a name="BKMK_SLAKPIInstanceId"></a> SLAKPIInstanceId

|Property|Value|
|--------|-----|
|Description|Unique identifier of the SLA KPI Instance.|
|DisplayName|SLA KPI InstanceId|
|IsValidForForm|False|
|IsValidForRead|True|
|IsValidForUpdate|False|
|LogicalName|slakpiinstanceid|
|RequiredLevel|SystemRequired|
|Type|Uniqueidentifier|


### <a name="BKMK_Status"></a> Status

|Property|Value|
|--------|-----|
|Description|Reason for the status of the service level agreement (SLA) key performance indicator (KPI) instance. For example, the SLA KPI could be Noncompliant or Succeeded.|
|DisplayName|Status|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|status|
|RequiredLevel|None|
|Type|Picklist|

#### Status Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|0|In Progress||
|1|Noncompliant||
|2|Nearing Noncompliance||
|3|Paused||
|4|Succeeded||
|5|Canceled||



### <a name="BKMK_SucceededOn"></a> SucceededOn

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Shows the date and time when the service level agreement (SLA) key performance indicator (KPI) success criteria was met.|
|DisplayName|Succeeded On|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|succeededon|
|RequiredLevel|None|
|Type|DateTime|


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


### <a name="BKMK_WarningTime"></a> WarningTime

|Property|Value|
|--------|-----|
|DateTimeBehavior|UserLocal|
|Description|Enter the date and time when the service level agreement (SLA) key performance indicator (KPI)will go to a warning state.|
|DisplayName|Warning Time|
|Format|DateAndTime|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|warningtime|
|RequiredLevel|None|
|Type|DateTime|


### <a name="BKMK_WarningTimeReached"></a> WarningTimeReached

|Property|Value|
|--------|-----|
|Description|Shows information about whether the case has reached its warning time.|
|DisplayName|Warning Time Reached|
|IsValidForForm|True|
|IsValidForRead|True|
|LogicalName|warningtimereached|
|RequiredLevel|None|
|Type|Picklist|

#### WarningTimeReached Choices/Options

|Value|Label|Description|
|-----|-----|--------|
|0|No||
|1|Yes||


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
- [ExchangeRate](#BKMK_ExchangeRate)
- [ModifiedBy](#BKMK_ModifiedBy)
- [ModifiedByName](#BKMK_ModifiedByName)
- [ModifiedByYomiName](#BKMK_ModifiedByYomiName)
- [ModifiedOn](#BKMK_ModifiedOn)
- [ModifiedOnBehalfBy](#BKMK_ModifiedOnBehalfBy)
- [ModifiedOnBehalfByName](#BKMK_ModifiedOnBehalfByName)
- [ModifiedOnBehalfByYomiName](#BKMK_ModifiedOnBehalfByYomiName)
- [OwnerIdName](#BKMK_OwnerIdName)
- [OwnerIdYomiName](#BKMK_OwnerIdYomiName)
- [RegardingIdName](#BKMK_RegardingIdName)
- [RegardingName](#BKMK_RegardingName)
- [RegardingYomiName](#BKMK_RegardingYomiName)
- [TransactionCurrencyIdName](#BKMK_TransactionCurrencyIdName)
- [VersionNumber](#BKMK_VersionNumber)


### <a name="BKMK_CreatedBy"></a> CreatedBy

|Property|Value|
|--------|-----|
|Description|For internal use only.|
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
|Description|For internal use only.|
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
|Description|For internal use only.|
|DisplayName|Created By (Delegate)|
|IsValidForForm|True|
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


### <a name="BKMK_ExchangeRate"></a> ExchangeRate

|Property|Value|
|--------|-----|
|Description|For internal use only.|
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
|Description|For internal use only.|
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
|Description|For internal use only.|
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
|Description|For internal use only.|
|DisplayName|Modified By (Delegate)|
|IsValidForForm|True|
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


### <a name="BKMK_OwnerIdName"></a> OwnerIdName

|Property|Value|
|--------|-----|
|Description||
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

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|owneridyominame|
|MaxLength|100|
|RequiredLevel|SystemRequired|
|Type|String|


### <a name="BKMK_RegardingIdName"></a> RegardingIdName

|Property|Value|
|--------|-----|
|Description|RegardingName|
|DisplayName|RegardingName|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|regardingidname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_RegardingName"></a> RegardingName

|Property|Value|
|--------|-----|
|Description||
|DisplayName||
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|regardingname|
|MaxLength|100|
|RequiredLevel|None|
|Type|String|


### <a name="BKMK_RegardingYomiName"></a> RegardingYomiName

|Property|Value|
|--------|-----|
|Description|RegardingYomiName|
|DisplayName|RegardingYomiName|
|FormatName|Text|
|IsLocalizable|False|
|IsValidForForm|False|
|IsValidForRead|True|
|LogicalName|regardingyominame|
|MaxLength|400|
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
|Description|For internal use only.|
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

- [slakpiinstance_incident_firstresponsebykpi](#BKMK_slakpiinstance_incident_firstresponsebykpi)
- [slakpiinstance_incident_resolvebykpi](#BKMK_slakpiinstance_incident_resolvebykpi)
- [SLAKPIInstance_SyncErrors](#BKMK_SLAKPIInstance_SyncErrors)


### <a name="BKMK_slakpiinstance_incident_firstresponsebykpi"></a> slakpiinstance_incident_firstresponsebykpi

**Added by**: Service Solution

Same as the [slakpiinstance_incident_firstresponsebykpi](incident.md#BKMK_slakpiinstance_incident_firstresponsebykpi) many-to-one relationship for the [incident](incident.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|incident|
|ReferencingAttribute|firstresponsebykpiid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|slakpiinstance_incident_firstresponsebykpi|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: RemoveLink<br />Merge: Cascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_slakpiinstance_incident_resolvebykpi"></a> slakpiinstance_incident_resolvebykpi

**Added by**: Service Solution

Same as the [slakpiinstance_incident_resolvebykpi](incident.md#BKMK_slakpiinstance_incident_resolvebykpi) many-to-one relationship for the [incident](incident.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|incident|
|ReferencingAttribute|resolvebykpiid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|slakpiinstance_incident_resolvebykpi|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: NoCascade<br />Delete: RemoveLink<br />Merge: Cascade<br />Reparent: NoCascade<br />Share: NoCascade<br />Unshare: NoCascade|


### <a name="BKMK_SLAKPIInstance_SyncErrors"></a> SLAKPIInstance_SyncErrors

Same as the [SLAKPIInstance_SyncErrors](syncerror.md#BKMK_SLAKPIInstance_SyncErrors) many-to-one relationship for the [syncerror](syncerror.md) entity.

|Property|Value|
|--------|-----|
|ReferencingEntity|syncerror|
|ReferencingAttribute|regardingobjectid|
|IsHierarchical|False|
|IsCustomizable|True|
|ReferencedEntityNavigationPropertyName|SLAKPIInstance_SyncErrors|
|AssociatedMenuConfiguration|Behavior: DoNotDisplay<br />Group: Details<br />Label: <br />Order: |
|CascadeConfiguration|Assign: Cascade<br />Delete: Cascade<br />Merge: Cascade<br />Reparent: Cascade<br />Share: Cascade<br />Unshare: Cascade|

<a name="manytoone"></a>

## Many-To-One Relationships

Each Many-To-One relationship is defined by a corresponding One-To-Many relationship with the related entity. Listed by **SchemaName**.

- [slakpiinstance_lead](#BKMK_slakpiinstance_lead)
- [slakpiinstance_incident](#BKMK_slakpiinstance_incident)
- [slakpiinstance_serviceappointment](#BKMK_slakpiinstance_serviceappointment)
- [slakpiinstance_invoice](#BKMK_slakpiinstance_invoice)
- [slakpiinstance_opportunity](#BKMK_slakpiinstance_opportunity)
- [slakpiinstance_quote](#BKMK_slakpiinstance_quote)
- [slakpiinstance_salesorder](#BKMK_slakpiinstance_salesorder)
- [slakpiinstance_activitypointer](#BKMK_slakpiinstance_activitypointer)
- [slakpiinstance_email](#BKMK_slakpiinstance_email)
- [slakpiinstance_fax](#BKMK_slakpiinstance_fax)
- [lk_slakpiinstancebase_createdonbehalfby](#BKMK_lk_slakpiinstancebase_createdonbehalfby)
- [lk_slakpiinstancebase_modifiedonbehalfby](#BKMK_lk_slakpiinstancebase_modifiedonbehalfby)
- [slakpiinstance_account](#BKMK_slakpiinstance_account)
- [slakpiinstance_letter](#BKMK_slakpiinstance_letter)
- [slakpiinstance_phonecall](#BKMK_slakpiinstance_phonecall)
- [business_unit_slakpiinstance](#BKMK_business_unit_slakpiinstance)
- [slakpiinstance_socialactivity](#BKMK_slakpiinstance_socialactivity)
- [slakpiinstance_task](#BKMK_slakpiinstance_task)
- [lk_slakpiinstancebase_modifiedby](#BKMK_lk_slakpiinstancebase_modifiedby)
- [TransactionCurrency_slakpiinstance](#BKMK_TransactionCurrency_slakpiinstance)
- [slakpiinstance_contact](#BKMK_slakpiinstance_contact)
- [lk_slakpiinstancebase_createdby](#BKMK_lk_slakpiinstancebase_createdby)
- [slakpiinstance_appointment](#BKMK_slakpiinstance_appointment)


### <a name="BKMK_slakpiinstance_lead"></a> slakpiinstance_lead

**Added by**: Lead Management Solution

See the [slakpiinstance_lead](lead.md#BKMK_slakpiinstance_lead) one-to-many relationship for the [lead](lead.md) entity.

### <a name="BKMK_slakpiinstance_incident"></a> slakpiinstance_incident

**Added by**: Service Solution

See the [slakpiinstance_incident](incident.md#BKMK_slakpiinstance_incident) one-to-many relationship for the [incident](incident.md) entity.

### <a name="BKMK_slakpiinstance_serviceappointment"></a> slakpiinstance_serviceappointment

**Added by**: Service Solution

See the [slakpiinstance_serviceappointment](serviceappointment.md#BKMK_slakpiinstance_serviceappointment) one-to-many relationship for the [serviceappointment](serviceappointment.md) entity.

### <a name="BKMK_slakpiinstance_invoice"></a> slakpiinstance_invoice

**Added by**: Sales Solution

See the [slakpiinstance_invoice](invoice.md#BKMK_slakpiinstance_invoice) one-to-many relationship for the [invoice](invoice.md) entity.

### <a name="BKMK_slakpiinstance_opportunity"></a> slakpiinstance_opportunity

**Added by**: Sales Solution

See the [slakpiinstance_opportunity](opportunity.md#BKMK_slakpiinstance_opportunity) one-to-many relationship for the [opportunity](opportunity.md) entity.

### <a name="BKMK_slakpiinstance_quote"></a> slakpiinstance_quote

**Added by**: Sales Solution

See the [slakpiinstance_quote](quote.md#BKMK_slakpiinstance_quote) one-to-many relationship for the [quote](quote.md) entity.

### <a name="BKMK_slakpiinstance_salesorder"></a> slakpiinstance_salesorder

**Added by**: Sales Solution

See the [slakpiinstance_salesorder](salesorder.md#BKMK_slakpiinstance_salesorder) one-to-many relationship for the [salesorder](salesorder.md) entity.

### <a name="BKMK_slakpiinstance_activitypointer"></a> slakpiinstance_activitypointer

See the [slakpiinstance_activitypointer](activitypointer.md#BKMK_slakpiinstance_activitypointer) one-to-many relationship for the [activitypointer](activitypointer.md) entity.

### <a name="BKMK_slakpiinstance_email"></a> slakpiinstance_email

See the [slakpiinstance_email](email.md#BKMK_slakpiinstance_email) one-to-many relationship for the [email](email.md) entity.

### <a name="BKMK_slakpiinstance_fax"></a> slakpiinstance_fax

See the [slakpiinstance_fax](fax.md#BKMK_slakpiinstance_fax) one-to-many relationship for the [fax](fax.md) entity.

### <a name="BKMK_lk_slakpiinstancebase_createdonbehalfby"></a> lk_slakpiinstancebase_createdonbehalfby

See the [lk_slakpiinstancebase_createdonbehalfby](systemuser.md#BKMK_lk_slakpiinstancebase_createdonbehalfby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_lk_slakpiinstancebase_modifiedonbehalfby"></a> lk_slakpiinstancebase_modifiedonbehalfby

See the [lk_slakpiinstancebase_modifiedonbehalfby](systemuser.md#BKMK_lk_slakpiinstancebase_modifiedonbehalfby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_slakpiinstance_account"></a> slakpiinstance_account

See the [slakpiinstance_account](account.md#BKMK_slakpiinstance_account) one-to-many relationship for the [account](account.md) entity.

### <a name="BKMK_slakpiinstance_letter"></a> slakpiinstance_letter

See the [slakpiinstance_letter](letter.md#BKMK_slakpiinstance_letter) one-to-many relationship for the [letter](letter.md) entity.

### <a name="BKMK_slakpiinstance_phonecall"></a> slakpiinstance_phonecall

See the [slakpiinstance_phonecall](phonecall.md#BKMK_slakpiinstance_phonecall) one-to-many relationship for the [phonecall](phonecall.md) entity.

### <a name="BKMK_business_unit_slakpiinstance"></a> business_unit_slakpiinstance

See the [business_unit_slakpiinstance](businessunit.md#BKMK_business_unit_slakpiinstance) one-to-many relationship for the [businessunit](businessunit.md) entity.

### <a name="BKMK_slakpiinstance_socialactivity"></a> slakpiinstance_socialactivity

See the [slakpiinstance_socialactivity](socialactivity.md#BKMK_slakpiinstance_socialactivity) one-to-many relationship for the [socialactivity](socialactivity.md) entity.

### <a name="BKMK_slakpiinstance_task"></a> slakpiinstance_task

See the [slakpiinstance_task](task.md#BKMK_slakpiinstance_task) one-to-many relationship for the [task](task.md) entity.

### <a name="BKMK_lk_slakpiinstancebase_modifiedby"></a> lk_slakpiinstancebase_modifiedby

See the [lk_slakpiinstancebase_modifiedby](systemuser.md#BKMK_lk_slakpiinstancebase_modifiedby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_TransactionCurrency_slakpiinstance"></a> TransactionCurrency_slakpiinstance

See the [TransactionCurrency_slakpiinstance](transactioncurrency.md#BKMK_TransactionCurrency_slakpiinstance) one-to-many relationship for the [transactioncurrency](transactioncurrency.md) entity.

### <a name="BKMK_slakpiinstance_contact"></a> slakpiinstance_contact

See the [slakpiinstance_contact](contact.md#BKMK_slakpiinstance_contact) one-to-many relationship for the [contact](contact.md) entity.

### <a name="BKMK_lk_slakpiinstancebase_createdby"></a> lk_slakpiinstancebase_createdby

See the [lk_slakpiinstancebase_createdby](systemuser.md#BKMK_lk_slakpiinstancebase_createdby) one-to-many relationship for the [systemuser](systemuser.md) entity.

### <a name="BKMK_slakpiinstance_appointment"></a> slakpiinstance_appointment

See the [slakpiinstance_appointment](appointment.md#BKMK_slakpiinstance_appointment) one-to-many relationship for the [appointment](appointment.md) entity.

### See also

[About the Entity Reference](../about-entity-reference.md)<br />
[Web API EntityType Reference](/power-apps/developer/data-platform/webapi/reference/entitytypes)
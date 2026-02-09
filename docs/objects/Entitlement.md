---
hide:
  - path
---

<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->


## Schema

```mermaid
graph TD
Entitlement["Entitlement"]:::mainObject
click Entitlement "/objects/Entitlement/"
EGH_Matrix_Assigning_Entitlement__c["EGH Matrix Assigning Entitlement"]:::customObject
click EGH_Matrix_Assigning_Entitlement__c "/objects/EGH_Matrix_Assigning_Entitlement__c/"

EGH_Matrix_Assigning_Entitlement__c -->|EGH_EntitlementProcessLookup__c| Entitlement

classDef object fill:#D6E9FF,stroke:#0070D2,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObject fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObjectManaged fill:#FFD8B2,stroke:#CC5500,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainObject fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;
linkStyle 0 stroke:#A6A6A6,stroke-width:2px;

```


<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| AccountId |  | MasterDetail | undefined |
| AssetId |  | Lookup | undefined |
| BusinessHoursId |  | Lookup | undefined |
| CasesPerEntitlement |  |  | undefined |
| ContractLineItemId |  | Lookup | undefined |
| EndDate |  |  | undefined |
| IsPerIncident |  |  | undefined |
| LocationId |  | Lookup | undefined |
| Name |  |  | undefined |
| RemainingCases |  |  | undefined |
| RemainingWorkOrders |  |  | undefined |
| ServiceContractId |  | Lookup | undefined |
| SlaProcessId |  | Lookup | undefined |
| StartDate |  |  | undefined |
| Status |  |  | undefined |
| StatusIndicator |  |  | undefined |
| SvcApptBookingWindowsId |  | Lookup | undefined |
| Type |  | Picklist | undefined |
| WorkOrdersPerEntitlement |  |  | undefined |








## Related Profiles

| Profile | User License |
| :----      | :--: | 
| [Admin](../profiles/Admin.md) |  Salesforce |
| [EGH Minimum Access Profile](../profiles/EGH%20Minimum%20Access%20Profile.md) |  Salesforce |
| [EGH Sales Profile](../profiles/EGH%20Sales%20Profile.md) |  Salesforce |
| [EGH Service Profile](../profiles/EGH%20Service%20Profile.md) |  Salesforce |


## Related Permission Sets

| Permission Set | User License |
| :----      | :--: | 
| [EGH_Contact_Center_PS](../permissionsets/EGH_Contact_Center_PS.md) | None |
| [EGH_Digital_Sales_Consultant_Omni_Channel](../permissionsets/EGH_Digital_Sales_Consultant_Omni_Channel.md) | None |
| [EGH_Fleet_Consultant](../permissionsets/EGH_Fleet_Consultant.md) | None |
| [EGH_Lease_Consultant](../permissionsets/EGH_Lease_Consultant.md) | None |
| [EGH_Meet_and_Greet_Application](../permissionsets/EGH_Meet_and_Greet_Application.md) | None |
| [EGH_Product_Genius](../permissionsets/EGH_Product_Genius.md) | None |
| [EGH_Sales_Consultant_Omni_Channel](../permissionsets/EGH_Sales_Consultant_Omni_Channel.md) | None |
| [EGH_Service_Consultants_PS](../permissionsets/EGH_Service_Consultants_PS.md) | None |
| [EGH_SystemAdminPermissionSet](../permissionsets/EGH_SystemAdminPermissionSet.md) | None |
| [EGH_Test_Drive_Team](../permissionsets/EGH_Test_Drive_Team.md) | None |


_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_

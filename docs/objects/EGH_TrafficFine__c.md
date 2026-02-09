---
hide:
  - path
---

<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->


## Schema

```mermaid
graph TD
ServiceAppointment["ServiceAppointment"]:::object
click ServiceAppointment "/objects/ServiceAppointment/"
Lead["Lead"]:::object
click Lead "/objects/Lead/"
EGH_TrafficFine__c["Traffic Fine"]:::mainObject
click EGH_TrafficFine__c "/objects/EGH_TrafficFine__c/"
Contact["Contact"]:::object
click Contact "/objects/Contact/"
Asset["Asset"]:::object
click Asset "/objects/Asset/"

EGH_TrafficFine__c -->|EGH_TestDriveVehicleLookup__c| Asset
EGH_TrafficFine__c -->|EGH_TestDriveAppointmentLookup__c| ServiceAppointment
EGH_TrafficFine__c -->|EGH_LeadDriver__c| Lead
EGH_TrafficFine__c -->|EGH_CustomerDriverLookup__c| Contact

classDef object fill:#D6E9FF,stroke:#0070D2,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObject fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObjectManaged fill:#FFD8B2,stroke:#CC5500,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainObject fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;
linkStyle 0,1,2,3 stroke:#A6A6A6,stroke-width:2px;

```


<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| EGH_CustomerDriverLookup__c | Customer Driver | Lookup | Driver of the vehicle in the moment the traffic fine was created (Customer). There will be other field to indicate the driver if a lead was driving. |
| EGH_DateOfInfractionDateTime__c | Date/Time Of Infraction | DateTime | Date and Time of the infraction related with the traffic fine |
| EGH_DescriptionLongText__c | Description | LongTextArea | Description of the infraction |
| EGH_FineAmountCurrency__c | Fine Amount | Currency | Amount of the traffic fine |
| EGH_FineNumberText__c | Fine Number | Text | Traffic Fine number |
| EGH_IncidentLocationLongText__c | Incident Location | LongTextArea | Where the infraction occurred |
| EGH_LeadDriver__c | Lead Driver | Lookup | Driver of the vehicle in the moment the traffic fine was created (Lead). There will be other field to indicate the driver if a customer was driving. |
| EGH_PaymentDate__c | Payment Date | Date | Date when the fine was paid |
| EGH_PaymentStatusPicklist__c | Payment Status | Picklist | Payment status of the traffic fine |
| EGH_TestDriveAppointmentLookup__c | Test Drive Appointment | Lookup | Test Drive appointment in which the infraction occurred |
| EGH_TestDriveVehicleLookup__c | Test Drive Vehicle | Lookup | Test Drive Vehicle the Traffic Fine is related to |






## Related Lightning Pages

| Lightning Page | Type |
| :----      | :--: | 
| [EGH_Traffic_Fine_Lightning_Page](../pages/EGH_Traffic_Fine_Lightning_Page.md) |  Record Page |


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
| [EGH_Core_Integration_Permission_Set](../permissionsets/EGH_Core_Integration_Permission_Set.md) | None |
| [EGH_Core_Permission](../permissionsets/EGH_Core_Permission.md) | None |
| [EGH_QA_and_Data_Analyst_PS](../permissionsets/EGH_QA_and_Data_Analyst_PS.md) | None |
| [EGH_SystemAdminPermissionSet](../permissionsets/EGH_SystemAdminPermissionSet.md) | None |
| [EGH_Test_Drive_Team](../permissionsets/EGH_Test_Drive_Team.md) | None |


_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_

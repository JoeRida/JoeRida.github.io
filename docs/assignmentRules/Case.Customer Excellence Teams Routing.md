---
hide:
  - path
---

<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->

<!-- Assignment Rule description -->
## Assignment Rules list
## Customer Excellence Teams Routing Rules
| Order |  Criteria | Assigned To | Assigned To Type | Email |
| :--: | :------------- | :--: | :--: | :--: |
| 1 | (**Case**: RecordTypeId _equals_ Complaint)<br> AND (**Case**: EGH_Source__c _equals_ Consumer Rights)<br> AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Consumer_Rights_Complaint | Queue | false |
| 2 | (**Case**: RecordTypeId _equals_ Complaint)<br> AND (**Case**: EGH_Category__c _equals_ Sales)<br> AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Sales_Complaints_Queue | Queue | false |
| 3 | (**Case**: RecordTypeId _equals_ Complaint)<br> AND (**Case**: EGH_Category__c _equals_ Service)<br> AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Service_Complaints_Queue | Queue | false |
| 4 | (**Case**: RecordTypeId _equals_ Complaint)<br> AND (**Case**: EGH_Category__c _equals_ Reception)<br> AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Reception_Complaints | Queue | false |
| 5 | (**Case**: RecordTypeId _equals_ Complaint)<br> AND (**Case**: EGH_Category__c _equals_ Contact Center)<br> AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Contact_Center_Complaints_Queue | Queue | false |
| 6 | (**Case**: RecordTypeId _equals_ Complaint)<br> AND ((**Case**: EGH_Category__c _equals_ Other)<br> OR (**Case**: EGH_Category__c _equals_ ' ')<br>) AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Generic_Complaints | Queue | false |
| 7 | (**Case**: RecordTypeId _equals_ Feedback)<br> AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_CSI_Queue | Queue | false |
| 8 | ((**Case**: RecordTypeId _equals_ General Enquiry, Follow-Up)<br> OR (**Case**: EGH_Category__c _equals_ ' ')<br>) AND (**Case**: EGH_Case_SLACategory__c _notContain_ Internal)<br> |  EGH_Contact_Center_Queue | Queue | false |


_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_

---
hide:
  - path
---

<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->

<!-- Assignment Rule description -->
## Assignment Rules list
## EGH Lead Queue Assignment Rules
| Order |  Criteria | Assigned To | Assigned To Type | Email |
| :--: | :------------- | :--: | :--: | :--: |
| 1 | "EGH_AssignToPG__c = false && ISCHANGED(LeadSource) && ISPICKVAL(LeadSource, \"Walk-in\")" |  EGH_WalkInLeadsQueue | Queue | false |
| 2 | "EGH_AssignToPG__c = false && ISCHANGED(LeadSource) &&  RecordType.DeveloperName  <> \"EGH_Service_RecordType\" && RecordType.DeveloperName <> \"EGH_Spares_RecordType\" && (      CONTAINS($UserRole.Name, \"Product Genius\") ||    ISPICKVAL(LeadSource, \"Contact Centre\") ||     ISPICKVAL(LeadSource, \"Event\") ||     ISPICKVAL(LeadSource, \"Other\") ||     ISPICKVAL(LeadSource, \"Digital Sales Consultant\") ||     ISPICKVAL(LeadSource, \"TikTok\") ||     ISPICKVAL(LeadSource, \"Instagram\") ||     ISPICKVAL(LeadSource, \"Facebook\") ||     ISPICKVAL(LeadSource, \"WhatsApp Bot\") )" |  EGH_Digital_Sales_Consultant_Queue | Queue | false |
| 3 | "EGH_AssignToPG__c = false && ISNEW() &&  (   ISPICKVAL(LeadSource, \"Website\") ||    ISPICKVAL(LeadSource, \"WebBot\") ||    ISPICKVAL(LeadSource, \"Campaign\") )" |  EGH_WhatsAppBotQueue | Queue | false |
| 4 | "EGH_AssignToPG__c = false && (RecordType.DeveloperName  = \"EGH_Service_RecordType\" || RecordType.DeveloperName = \"EGH_Spares_RecordType\")" |  EGH_Contact_Center_Queue | Queue | false |


_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_

---
hide:
  - path
---

# EGH_OpportunityScoringController Class

## Class Diagram

```mermaid
graph TD
  EGH_OpportunityScoringController["EGH_OpportunityScoringController"]:::mainApexClass
  click EGH_OpportunityScoringController "/objects/EGH_OpportunityScoringController/"
  EGH_OpportunityScoringControllerTest["EGH_OpportunityScoringControllerTest"]:::apexTestClass
  click EGH_OpportunityScoringControllerTest "/apex/EGH_OpportunityScoringControllerTest/"


  EGH_OpportunityScoringControllerTest --> EGH_OpportunityScoringController


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public with sharing class EGH_OpportunityScoringController {
    @AuraEnabled(cacheable=true)
    public static Map<String, Integer> getAccountScoringData(String accountId) {
        Map<String, Integer> result = new Map<String, Integer>();
        
        // Showroom visits count
        result.put('showroomCount', [SELECT COUNT() FROM EGH_ShowroomVisit__c 
                                     WHERE EGH_AccountLookup__c = :accountId]);
        
        // Service appointment counts
        result.put('totalServiceCount', [SELECT COUNT() FROM ServiceAppointment 
                                        WHERE AccountId = :accountId]);
        
        result.put('completedServiceCount', [SELECT COUNT() FROM ServiceAppointment 
                                            WHERE AccountId = :accountId 
                                            AND Status = 'Completed']);
        
        return result;
    }
}
```

## Methods
### `getAccountScoringData(accountId)`

`AURAENABLED`

#### Signature
```apex
public static Map<String,Integer> getAccountScoringData(String accountId)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| accountId | String |  |

#### Return Type
**Map<String,Integer>**
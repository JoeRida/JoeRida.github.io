---
hide:
  - path
---

# EGH_UpdateVisitTimeAndStatus Class

## Class Diagram

```mermaid
graph TD
  EGH_UpdateVisitTimeAndStatus["EGH_UpdateVisitTimeAndStatus"]:::mainApexClass
  click EGH_UpdateVisitTimeAndStatus "/objects/EGH_UpdateVisitTimeAndStatus/"
  EGH_getPresenceStatusIdClass["EGH_getPresenceStatusIdClass"]:::apexClass
  click EGH_getPresenceStatusIdClass "/apex/EGH_getPresenceStatusIdClass/"
  EGH_UpdateVisitStartEndTime_Test["EGH_UpdateVisitStartEndTime_Test"]:::apexTestClass
  click EGH_UpdateVisitStartEndTime_Test "/apex/EGH_UpdateVisitStartEndTime_Test/"


  EGH_getPresenceStatusIdClass --> EGH_UpdateVisitTimeAndStatus
  EGH_UpdateVisitStartEndTime_Test --> EGH_UpdateVisitTimeAndStatus


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0,1 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public class EGH_UpdateVisitTimeAndStatus {

    @AuraEnabled
    public static void updateVisitStartTime(Id recordId) {
      
        EGH_ShowroomVisit__c sv = [SELECT Id, EGH_StartDateTime__c
                                   FROM EGH_ShowroomVisit__c   
                                   WHERE Id = :recordId WITH SYSTEM_MODE 
                                   LIMIT 1];
        sv.EGH_StartDateTime__c = System.now();
        sv.EGH_Status__c = 'Assigned';
        sv.EGH_Visit_Started__c = True;
        Database.update(sv, AccessLevel.USER_MODE);
      }

    
    
       @AuraEnabled
    public static void updateVisitEndTime(Id recordId) {
         EGH_ShowroomVisit__c sv = [SELECT Id, EGH_StartDateTime__c 
                                    FROM EGH_ShowroomVisit__c 
                                    WHERE Id = :recordId WITH SYSTEM_MODE 
                                    LIMIT 1];
        sv.EGH_EndDateTime__c = System.now();
        sv.EGH_Status__c = 'Ended';
        sv.EGH_Visit_Completed__c =TRUE;
        Database.update(sv,AccessLevel.SYSTEM_MODE);
    }


}
```

## Methods
### `updateVisitStartTime(recordId)`

`AURAENABLED`

#### Signature
```apex
public static void updateVisitStartTime(Id recordId)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| recordId | Id |  |

#### Return Type
**void**

---

### `updateVisitEndTime(recordId)`

`AURAENABLED`

#### Signature
```apex
public static void updateVisitEndTime(Id recordId)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| recordId | Id |  |

#### Return Type
**void**
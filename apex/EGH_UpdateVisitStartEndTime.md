---
hide:
  - path
---

# EGH_UpdateVisitStartEndTime Class

## Class Diagram

```mermaid
graph TD
  EGH_UpdateVisitStartEndTime["EGH_UpdateVisitStartEndTime"]:::mainApexClass
  click EGH_UpdateVisitStartEndTime "/objects/EGH_UpdateVisitStartEndTime/"
  EGH_UpdateVisitStartEndTime_Test["EGH_UpdateVisitStartEndTime_Test"]:::apexTestClass
  click EGH_UpdateVisitStartEndTime_Test "/apex/EGH_UpdateVisitStartEndTime_Test/"


  EGH_UpdateVisitStartEndTime_Test --> EGH_UpdateVisitStartEndTime


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public class EGH_UpdateVisitStartEndTime {

    @AuraEnabled
    public static void updateVisitStartTime(Id recordId) {
        // Replace Case with your specific object if needed
        EGH_ShowroomVisit__c svs = [SELECT Id, EGH_StartDateTime__c FROM EGH_ShowroomVisit__c WHERE Id = :recordId LIMIT 1];
        svs.EGH_StartDateTime__c = System.now();
        svs.EGH_Status__c = 'Assigned';
        update svs;
    }
    
    
       @AuraEnabled
    public static void updateVisitEndTime(Id recordId) {
        // Replace Case with your specific object if needed
       EGH_ShowroomVisit__c sve = [SELECT Id, EGH_StartDateTime__c FROM EGH_ShowroomVisit__c WHERE Id = :recordId LIMIT 1];
       sve.EGH_EndDateTime__c = System.now();
      sve.EGH_Status__c = 'Ended';
       update sve;
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
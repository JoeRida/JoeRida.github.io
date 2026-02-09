---
hide:
  - path
---

# EGH_getPresenceStatusIdClass Class

## Class Diagram

```mermaid
graph TD
  EGH_getPresenceStatusIdClass["EGH_getPresenceStatusIdClass"]:::mainApexClass
  click EGH_getPresenceStatusIdClass "/objects/EGH_getPresenceStatusIdClass/"
  EGH_UpdateVisitTimeAndStatus["EGH_UpdateVisitTimeAndStatus"]:::apexClass
  click EGH_UpdateVisitTimeAndStatus "/apex/EGH_UpdateVisitTimeAndStatus/"
  EGH_getPresenceStatusIdClassTest["EGH_getPresenceStatusIdClassTest"]:::apexTestClass
  click EGH_getPresenceStatusIdClassTest "/apex/EGH_getPresenceStatusIdClassTest/"

  EGH_getPresenceStatusIdClass --> EGH_UpdateVisitTimeAndStatus

  EGH_getPresenceStatusIdClassTest --> EGH_getPresenceStatusIdClass


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
linkStyle 1 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public with sharing class EGH_getPresenceStatusIdClass {
    
    @AuraEnabled(cacheable=true)
    public static string getPresenceStatusID(string presenceStatusDeveloperName)
        
    {
        String id=[select id from ServicePresenceStatus  where developername=:presenceStatusDeveloperName  WITH SYSTEM_MODE Limit 1].id;
        system.debug(Id.substring(0, 15));
        return id.substring(0, 15);
        
    }
    
    @AuraEnabled
    public static void updateVisitStartTime(Id recordId) {
        
       EGH_UpdateVisitTimeAndStatus.updateVisitStartTime(recordId);
        
    }
    
    
    @AuraEnabled
    public static void updateVisitEndTime(Id recordId) {
        
       EGH_UpdateVisitTimeAndStatus.updateVisitEndTime(recordId);
    }
      
}
```

## Methods
### `getPresenceStatusID(presenceStatusDeveloperName)`

`AURAENABLED`

#### Signature
```apex
public static string getPresenceStatusID(string presenceStatusDeveloperName)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| presenceStatusDeveloperName | string |  |

#### Return Type
**string**

---

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
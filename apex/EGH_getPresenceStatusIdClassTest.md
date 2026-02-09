---
hide:
  - path
---

# EGH_getPresenceStatusIdClassTest Class

`ISTEST`

## Class Diagram

```mermaid
graph TD
  EGH_getPresenceStatusIdClassTest["EGH_getPresenceStatusIdClassTest"]:::mainApexClass
  click EGH_getPresenceStatusIdClassTest "/objects/EGH_getPresenceStatusIdClassTest/"
  EGH_getPresenceStatusIdClass["EGH_getPresenceStatusIdClass"]:::apexClass
  click EGH_getPresenceStatusIdClass "/apex/EGH_getPresenceStatusIdClass/"

  EGH_getPresenceStatusIdClassTest --> EGH_getPresenceStatusIdClass



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
@isTest(SeeAllData=True)
public class EGH_getPresenceStatusIdClassTest {
    
    @isTest
    static void testGetPresenceStatusID() {
       
        
           String MasterLabel = 'Available';
      
       
        
        Test.startTest();
        // Call the method with the DeveloperName we just inserted
        String returnedId = EGH_getPresenceStatusIdClass.getPresenceStatusID(MasterLabel);
        Test.stopTest();
        
        // Assert that the returned Id matches the inserted record's Id (15-character version)
        System.assertEquals(returnedId, returnedId);
    }
    
    
    @isTest
    static void testUpdateServiceStatus()
    {
        
        String showroomVisitIdPrefix=[SELECT Label, KeyPrefix FROM EntityDefinition where label ='Showroom Visit' limit 1].KeyPrefix;
        EGH_ShowroomVisit__c sv=new EGH_ShowroomVisit__c();
        insert sv;
        
        
        
        EGH_getPresenceStatusIdClass.updateVisitStartTime(sv.id);
        EGH_getPresenceStatusIdClass.updateVisitEndTime(sv.id);
        system.assertEquals([select EGH_StartDateTime__c from EGH_ShowroomVisit__c where id=:sv.id limit 1].EGH_StartDateTime__c,System.now());
        
    }
}
```

## Methods
### `testGetPresenceStatusID()`

`ISTEST`

#### Signature
```apex
private static void testGetPresenceStatusID()
```

#### Return Type
**void**

---

### `testUpdateServiceStatus()`

`ISTEST`

#### Signature
```apex
private static void testUpdateServiceStatus()
```

#### Return Type
**void**
---
hide:
  - path
---

# EGH_OpportunityScoringControllerTest Class

`ISTEST`

## Class Diagram

```mermaid
graph TD
  EGH_OpportunityScoringControllerTest["EGH_OpportunityScoringControllerTest"]:::mainApexClass
  click EGH_OpportunityScoringControllerTest "/objects/EGH_OpportunityScoringControllerTest/"
  EGH_OpportunityScoringController["EGH_OpportunityScoringController"]:::apexClass
  click EGH_OpportunityScoringController "/apex/EGH_OpportunityScoringController/"

  EGH_OpportunityScoringControllerTest --> EGH_OpportunityScoringController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
@isTest
public class EGH_OpportunityScoringControllerTest {
    
    @isTest
    static void testGetAccountScoringData() {
        // Create test Account
        Account testAccount = new Account(Name = 'Test Account');
        insert testAccount;
        
        Test.startTest();
        Map<String, Integer> result = EGH_OpportunityScoringController.getAccountScoringData(testAccount.Id);
        Test.stopTest();
        
        // Basic assertions
        System.assertNotEquals(null, result);
        System.assert(result.containsKey('showroomCount'));
        System.assert(result.containsKey('totalServiceCount'));
        System.assert(result.containsKey('completedServiceCount'));
    }
}
```

## Methods
### `testGetAccountScoringData()`

`ISTEST`

#### Signature
```apex
private static void testGetAccountScoringData()
```

#### Return Type
**void**
---
hide:
  - path
---

# MicrobatchSelfRegControllerTest Class

`ISTEST`

## Class Diagram

```mermaid
graph TD
  MicrobatchSelfRegControllerTest["MicrobatchSelfRegControllerTest"]:::mainApexClass
  click MicrobatchSelfRegControllerTest "/objects/MicrobatchSelfRegControllerTest/"
  MicrobatchSelfRegController["MicrobatchSelfRegController"]:::apexClass
  click MicrobatchSelfRegController "/apex/MicrobatchSelfRegController/"

  MicrobatchSelfRegControllerTest --> MicrobatchSelfRegController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
@IsTest
 public with sharing class MicrobatchSelfRegControllerTest {
      @IsTest(SeeAllData=true)
     public static void testMicrobatchSelfRegController() {
         MicrobatchSelfRegController controller = new MicrobatchSelfRegController();
         controller.firstName = 'FirstName';
         controller.lastName = 'LastName';
         controller.email = 'test@force.com';
         controller.communityNickname = 'test';

         // registerUser will always return null when the page isn't accessed as a guest user
         System.assert(controller.registerUser() == null);
     }
 }
```

## Methods
### `testMicrobatchSelfRegController()`

`ISTEST`

#### Signature
```apex
public static void testMicrobatchSelfRegController()
```

#### Return Type
**void**
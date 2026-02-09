---
hide:
  - path
---

# CommunitiesSelfRegConfirmControllerTest Class

`ISTEST`

An apex page controller that takes the user to the right start page based on credentials or lack thereof

## Class Diagram

```mermaid
graph TD
  CommunitiesSelfRegConfirmControllerTest["CommunitiesSelfRegConfirmControllerTest"]:::mainApexClass
  click CommunitiesSelfRegConfirmControllerTest "/objects/CommunitiesSelfRegConfirmControllerTest/"
  CommunitiesSelfRegConfirmController["CommunitiesSelfRegConfirmController"]:::apexClass
  click CommunitiesSelfRegConfirmController "/apex/CommunitiesSelfRegConfirmController/"

  CommunitiesSelfRegConfirmControllerTest --> CommunitiesSelfRegConfirmController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that takes the user to the right start page based on credentials or lack thereof
 */
@IsTest public with sharing class CommunitiesSelfRegConfirmControllerTest {
    @IsTest(SeeAllData=true) public static void testCommunitiesSelfRegConfirmController() {
        // Instantiate a new controller with all parameters in the page
        CommunitiesSelfRegConfirmController controller = new CommunitiesSelfRegConfirmController();
      }    
}
```

## Methods
### `testCommunitiesSelfRegConfirmController()`

`ISTEST`

#### Signature
```apex
public static void testCommunitiesSelfRegConfirmController()
```

#### Return Type
**void**
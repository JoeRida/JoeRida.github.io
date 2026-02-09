---
hide:
  - path
---

# CommunitiesSelfRegConfirmController Class

An apex page controller that takes the user to the right start page based on credentials or lack thereof

## Class Diagram

```mermaid
graph TD
  CommunitiesSelfRegConfirmController["CommunitiesSelfRegConfirmController"]:::mainApexClass
  click CommunitiesSelfRegConfirmController "/objects/CommunitiesSelfRegConfirmController/"
  CommunitiesSelfRegConfirmControllerTest["CommunitiesSelfRegConfirmControllerTest"]:::apexTestClass
  click CommunitiesSelfRegConfirmControllerTest "/apex/CommunitiesSelfRegConfirmControllerTest/"


  CommunitiesSelfRegConfirmControllerTest --> CommunitiesSelfRegConfirmController


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that takes the user to the right start page based on credentials or lack thereof
 */
public with sharing class CommunitiesSelfRegConfirmController {
    
    public CommunitiesSelfRegConfirmController() {}
}
```

## Constructors
### `CommunitiesSelfRegConfirmController()`

#### Signature
```apex
public CommunitiesSelfRegConfirmController()
```
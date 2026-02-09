---
hide:
  - path
---

# CommunitiesLandingController Class

An apex page controller that takes the user to the right start page based on credentials or lack thereof

## Class Diagram

```mermaid
graph TD
  CommunitiesLandingController["CommunitiesLandingController"]:::mainApexClass
  click CommunitiesLandingController "/objects/CommunitiesLandingController/"
  CommunitiesLandingControllerTest["CommunitiesLandingControllerTest"]:::apexTestClass
  click CommunitiesLandingControllerTest "/apex/CommunitiesLandingControllerTest/"


  CommunitiesLandingControllerTest --> CommunitiesLandingController


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
public with sharing class CommunitiesLandingController {
    
    // Code we will invoke on page load.
    public PageReference forwardToStartPage() {
        return Network.communitiesLanding();
    }
    
    public CommunitiesLandingController() {}
}
```

## Constructors
### `CommunitiesLandingController()`

#### Signature
```apex
public CommunitiesLandingController()
```

## Methods
### `forwardToStartPage()`

#### Signature
```apex
public PageReference forwardToStartPage()
```

#### Return Type
**PageReference**
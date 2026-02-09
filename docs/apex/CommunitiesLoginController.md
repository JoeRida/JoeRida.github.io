---
hide:
  - path
---

# CommunitiesLoginController Class

An apex page controller that exposes the site login functionality

## Class Diagram

```mermaid
graph TD
  CommunitiesLoginController["CommunitiesLoginController"]:::mainApexClass
  click CommunitiesLoginController "/objects/CommunitiesLoginController/"
  CommunitiesLoginControllerTest["CommunitiesLoginControllerTest"]:::apexTestClass
  click CommunitiesLoginControllerTest "/apex/CommunitiesLoginControllerTest/"


  CommunitiesLoginControllerTest --> CommunitiesLoginController


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that exposes the site login functionality
 */
global with sharing class CommunitiesLoginController {

    global CommunitiesLoginController () {}
    
    // Code we will invoke on page load.
    global PageReference forwardToAuthPage() {
    	String startUrl = System.currentPageReference().getParameters().get('startURL');
    	String displayType = System.currentPageReference().getParameters().get('display');
        return Network.forwardToAuthPage(startUrl, displayType);
    }
}
```

## Constructors
### `CommunitiesLoginController()`

#### Signature
```apex
global CommunitiesLoginController()
```

## Methods
### `forwardToAuthPage()`

#### Signature
```apex
global PageReference forwardToAuthPage()
```

#### Return Type
**PageReference**
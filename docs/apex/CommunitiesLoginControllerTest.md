---
hide:
  - path
---

# CommunitiesLoginControllerTest Class

`ISTEST`

An apex page controller that exposes the site login functionality

## Class Diagram

```mermaid
graph TD
  CommunitiesLoginControllerTest["CommunitiesLoginControllerTest"]:::mainApexClass
  click CommunitiesLoginControllerTest "/objects/CommunitiesLoginControllerTest/"
  CommunitiesLoginController["CommunitiesLoginController"]:::apexClass
  click CommunitiesLoginController "/apex/CommunitiesLoginController/"

  CommunitiesLoginControllerTest --> CommunitiesLoginController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that exposes the site login functionality
 */
@IsTest global with sharing class CommunitiesLoginControllerTest {
    @IsTest(SeeAllData=true) 
    global static void testCommunitiesLoginController () {
     	CommunitiesLoginController controller = new CommunitiesLoginController();
     	System.assertEquals(null, controller.forwardToAuthPage());       
    }    
}
```

## Methods
### `testCommunitiesLoginController()`

`ISTEST`

#### Signature
```apex
global static void testCommunitiesLoginController()
```

#### Return Type
**void**
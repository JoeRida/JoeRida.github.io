---
hide:
  - path
---

# SiteLoginControllerTest Class

`ISTEST`

An apex page controller that exposes the site login functionality

## Class Diagram

```mermaid
graph TD
  SiteLoginControllerTest["SiteLoginControllerTest"]:::mainApexClass
  click SiteLoginControllerTest "/objects/SiteLoginControllerTest/"
  SiteLoginController["SiteLoginController"]:::apexClass
  click SiteLoginController "/apex/SiteLoginController/"

  SiteLoginControllerTest --> SiteLoginController



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
@IsTest global with sharing class SiteLoginControllerTest {
    @IsTest(SeeAllData=true) global static void testSiteLoginController () {
        // Instantiate a new controller with all parameters in the page
        SiteLoginController controller = new SiteLoginController ();
        controller.username = 'test@salesforce.com';
        controller.password = '123456'; 
                
        System.assertEquals(controller.login(),null);                           
    }    
}
```

## Methods
### `testSiteLoginController()`

`ISTEST`

#### Signature
```apex
global static void testSiteLoginController()
```

#### Return Type
**void**
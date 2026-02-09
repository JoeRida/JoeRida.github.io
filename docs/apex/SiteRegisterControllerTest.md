---
hide:
  - path
---

# SiteRegisterControllerTest Class

`ISTEST`

Class containing tests for SiteRegisterController

## Class Diagram

```mermaid
graph TD
  SiteRegisterControllerTest["SiteRegisterControllerTest"]:::mainApexClass
  click SiteRegisterControllerTest "/objects/SiteRegisterControllerTest/"
  SiteRegisterController["SiteRegisterController"]:::apexClass
  click SiteRegisterController "/apex/SiteRegisterController/"

  SiteRegisterControllerTest --> SiteRegisterController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * Class containing tests for SiteRegisterController
 */
@IsTest public with sharing class SiteRegisterControllerTest {
    @IsTest(SeeAllData=true) static void testRegistration() {
        SiteRegisterController controller = new SiteRegisterController();
        controller.username = 'test@force.com';
        controller.email = 'test@force.com';
        controller.communityNickname = 'test';
        // registerUser will always return null when the page isn't accessed as a guest user
        System.assert(controller.registerUser() == null);    
        
        controller.password = 'abcd1234';
        controller.confirmPassword = 'abcd123';
        System.assert(controller.registerUser() == null);  
    }
}
```

## Methods
### `testRegistration()`

`ISTEST`

#### Signature
```apex
private static void testRegistration()
```

#### Return Type
**void**
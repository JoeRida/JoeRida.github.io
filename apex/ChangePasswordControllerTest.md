---
hide:
  - path
---

# ChangePasswordControllerTest Class

`ISTEST`

An apex page controller that exposes the change password functionality

## Class Diagram

```mermaid
graph TD
  ChangePasswordControllerTest["ChangePasswordControllerTest"]:::mainApexClass
  click ChangePasswordControllerTest "/objects/ChangePasswordControllerTest/"
  ChangePasswordController["ChangePasswordController"]:::apexClass
  click ChangePasswordController "/apex/ChangePasswordController/"

  ChangePasswordControllerTest --> ChangePasswordController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that exposes the change password functionality
 */
@IsTest public with sharing class ChangePasswordControllerTest {
   	@IsTest(SeeAllData=true) public static void testChangePasswordController() {
        // Instantiate a new controller with all parameters in the page
        ChangePasswordController controller = new ChangePasswordController();
        controller.oldPassword = '123456';
        controller.newPassword = 'qwerty1'; 
        controller.verifyNewPassword = 'qwerty1';                
        
        System.assertEquals(controller.changePassword(),null);                           
    }    
}
```

## Methods
### `testChangePasswordController()`

`ISTEST`

#### Signature
```apex
public static void testChangePasswordController()
```

#### Return Type
**void**
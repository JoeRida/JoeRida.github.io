---
hide:
  - path
---

# ForgotPasswordControllerTest Class

`ISTEST`

An apex page controller that exposes the site forgot password functionality

## Class Diagram

```mermaid
graph TD
  ForgotPasswordControllerTest["ForgotPasswordControllerTest"]:::mainApexClass
  click ForgotPasswordControllerTest "/objects/ForgotPasswordControllerTest/"
  ForgotPasswordController["ForgotPasswordController"]:::apexClass
  click ForgotPasswordController "/apex/ForgotPasswordController/"

  ForgotPasswordControllerTest --> ForgotPasswordController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that exposes the site forgot password functionality
 */
@IsTest public with sharing class ForgotPasswordControllerTest {
  	 @IsTest(SeeAllData=true) public static void testForgotPasswordController() {
    	// Instantiate a new controller with all parameters in the page
    	ForgotPasswordController controller = new ForgotPasswordController();
    	controller.username = 'test@salesforce.com';     	
    
    	System.assertEquals(controller.forgotPassword(),null); 
    }
}
```

## Methods
### `testForgotPasswordController()`

`ISTEST`

#### Signature
```apex
public static void testForgotPasswordController()
```

#### Return Type
**void**
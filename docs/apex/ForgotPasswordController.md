---
hide:
  - path
---

# ForgotPasswordController Class

An apex page controller that exposes the site forgot password functionality

## Class Diagram

```mermaid
graph TD
  ForgotPasswordController["ForgotPasswordController"]:::mainApexClass
  click ForgotPasswordController "/objects/ForgotPasswordController/"
  ForgotPasswordControllerTest["ForgotPasswordControllerTest"]:::apexTestClass
  click ForgotPasswordControllerTest "/apex/ForgotPasswordControllerTest/"


  ForgotPasswordControllerTest --> ForgotPasswordController


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that exposes the site forgot password functionality
 */
public with sharing class ForgotPasswordController {
    public String username {get; set;}   
       
    public ForgotPasswordController() {}
	
  	public PageReference forgotPassword() {
  		boolean success = Site.forgotPassword(username);
  		PageReference pr = Page.ForgotPasswordConfirm;
  		pr.setRedirect(true);
  		
  		if (success) {  			
  			return pr;
  		}
  		return null;
  	}
}
```

## Properties
### `username`

#### Signature
```apex
public username
```

#### Type
String

## Constructors
### `ForgotPasswordController()`

#### Signature
```apex
public ForgotPasswordController()
```

## Methods
### `forgotPassword()`

#### Signature
```apex
public PageReference forgotPassword()
```

#### Return Type
**PageReference**
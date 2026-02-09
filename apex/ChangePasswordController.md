---
hide:
  - path
---

# ChangePasswordController Class

An apex page controller that exposes the change password functionality

## Class Diagram

```mermaid
graph TD
  ChangePasswordController["ChangePasswordController"]:::mainApexClass
  click ChangePasswordController "/objects/ChangePasswordController/"
  ChangePasswordControllerTest["ChangePasswordControllerTest"]:::apexTestClass
  click ChangePasswordControllerTest "/apex/ChangePasswordControllerTest/"


  ChangePasswordControllerTest --> ChangePasswordController


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that exposes the change password functionality
 */
public with sharing class ChangePasswordController {
    public String oldPassword {get; set;}
    public String newPassword {get; set;}
    public String verifyNewPassword {get; set;}        
    
    public PageReference changePassword() {
        return Site.changePassword(newPassword, verifyNewPassword, oldpassword);    
    }     
    
   	public ChangePasswordController() {}
}
```

## Properties
### `oldPassword`

#### Signature
```apex
public oldPassword
```

#### Type
String

---

### `newPassword`

#### Signature
```apex
public newPassword
```

#### Type
String

---

### `verifyNewPassword`

#### Signature
```apex
public verifyNewPassword
```

#### Type
String

## Constructors
### `ChangePasswordController()`

#### Signature
```apex
public ChangePasswordController()
```

## Methods
### `changePassword()`

#### Signature
```apex
public PageReference changePassword()
```

#### Return Type
**PageReference**
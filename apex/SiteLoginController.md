---
hide:
  - path
---

# SiteLoginController Class

An apex page controller that exposes the site login functionality

## Class Diagram

```mermaid
graph TD
  SiteLoginController["SiteLoginController"]:::mainApexClass
  click SiteLoginController "/objects/SiteLoginController/"
  SiteLoginControllerTest["SiteLoginControllerTest"]:::apexTestClass
  click SiteLoginControllerTest "/apex/SiteLoginControllerTest/"


  SiteLoginControllerTest --> SiteLoginController


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
global with sharing class SiteLoginController {
    global String username {get; set;}
    global String password {get; set;}

    global PageReference login() {
        String startUrl = System.currentPageReference().getParameters().get('startURL');
        return Site.login(username, password, startUrl);
    }
    
   	global SiteLoginController () {}
}
```

## Properties
### `username`

#### Signature
```apex
global username
```

#### Type
String

---

### `password`

#### Signature
```apex
global password
```

#### Type
String

## Constructors
### `SiteLoginController()`

#### Signature
```apex
global SiteLoginController()
```

## Methods
### `login()`

#### Signature
```apex
global PageReference login()
```

#### Return Type
**PageReference**
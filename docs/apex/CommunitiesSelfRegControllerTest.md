---
hide:
  - path
---

# CommunitiesSelfRegControllerTest Class

`ISTEST`

An apex page controller that supports self registration of users in communities that allow self registration

## Class Diagram

```mermaid
graph TD
  CommunitiesSelfRegControllerTest["CommunitiesSelfRegControllerTest"]:::mainApexClass
  click CommunitiesSelfRegControllerTest "/objects/CommunitiesSelfRegControllerTest/"
  CommunitiesSelfRegController["CommunitiesSelfRegController"]:::apexClass
  click CommunitiesSelfRegController "/apex/CommunitiesSelfRegController/"

  CommunitiesSelfRegControllerTest --> CommunitiesSelfRegController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that supports self registration of users in communities that allow self registration
 */
@IsTest public with sharing class CommunitiesSelfRegControllerTest {
    @IsTest(SeeAllData=true) 
    public static void testCommunitiesSelfRegController() {
        CommunitiesSelfRegController controller = new CommunitiesSelfRegController();
        controller.firstName = 'FirstName';
        controller.lastName = 'LastName';
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
### `testCommunitiesSelfRegController()`

`ISTEST`

#### Signature
```apex
public static void testCommunitiesSelfRegController()
```

#### Return Type
**void**
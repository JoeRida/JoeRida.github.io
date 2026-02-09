---
hide:
  - path
---

# CommunitiesLandingControllerTest Class

`ISTEST`

An apex page controller that takes the user to the right start page based on credentials or lack thereof

## Class Diagram

```mermaid
graph TD
  CommunitiesLandingControllerTest["CommunitiesLandingControllerTest"]:::mainApexClass
  click CommunitiesLandingControllerTest "/objects/CommunitiesLandingControllerTest/"
  CommunitiesLandingController["CommunitiesLandingController"]:::apexClass
  click CommunitiesLandingController "/apex/CommunitiesLandingController/"

  CommunitiesLandingControllerTest --> CommunitiesLandingController



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
/**
 * An apex page controller that takes the user to the right start page based on credentials or lack thereof
 */
@IsTest public with sharing class CommunitiesLandingControllerTest {
    @IsTest(SeeAllData=true) public static void testCommunitiesLandingController() {
        // Instantiate a new controller with all parameters in the page
        CommunitiesLandingController controller = new CommunitiesLandingController();
        PageReference pageRef = controller.forwardToStartPage();
        //PageRef is either null or an empty object in test context
        if(pageRef != null){
            String url = pageRef.getUrl();
            if(url != null){
                System.assertEquals(true, String.isEmpty(url));
                //show up in perforce
            }
        }
    }
}
```

## Methods
### `testCommunitiesLandingController()`

`ISTEST`

#### Signature
```apex
public static void testCommunitiesLandingController()
```

#### Return Type
**void**
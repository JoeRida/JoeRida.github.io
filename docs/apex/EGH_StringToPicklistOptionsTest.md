---
hide:
  - path
---

# EGH_StringToPicklistOptionsTest Class

`ISTEST`

## Class Diagram

```mermaid
graph TD
  EGH_StringToPicklistOptionsTest["EGH_StringToPicklistOptionsTest"]:::mainApexClass
  click EGH_StringToPicklistOptionsTest "/objects/EGH_StringToPicklistOptionsTest/"
  EGH_StringToPicklistOptions["EGH_StringToPicklistOptions"]:::apexClass
  click EGH_StringToPicklistOptions "/apex/EGH_StringToPicklistOptions/"
  PicklistOption["PicklistOption"]:::apexClass
  click PicklistOption "/apex/PicklistOption/"

  EGH_StringToPicklistOptionsTest --> EGH_StringToPicklistOptions
  EGH_StringToPicklistOptionsTest --> PicklistOption


  EGH_StringToPicklistOptions --> PicklistOption

classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0,1 stroke:#4C9F70,stroke-width:4px;
linkStyle 2 stroke:#A6A6A6,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
@IsTest
private class EGH_StringToPicklistOptionsTest {

    @IsTest
    static void testTransformToOptions_Success() {
        EGH_StringToPicklistOptions.FlowInput input = new EGH_StringToPicklistOptions.FlowInput();
        input.semicolonSeparatedString = 'val1;val2;val3';
        
        List<EGH_StringToPicklistOptions.FlowInput> inputs = new List<EGH_StringToPicklistOptions.FlowInput>{input};

        Test.startTest();
        List<List<PicklistOption>> results = EGH_StringToPicklistOptions.transformToOptions(inputs);
        Test.stopTest();

        System.assertEquals(1, results.size(), 'Should return one list of results for one input');
        List<PicklistOption> firstResultList = results[0];
        
        System.assertEquals(3, firstResultList.size(), 'Should have split the string into 3 options');
        System.assertEquals('val1', firstResultList[0].label, 'First label should be val1');
        System.assertEquals('val2', firstResultList[1].value, 'Second value should be val2');
        System.assertEquals('val3', firstResultList[2].value, 'Second value should be val3');
    }
}
```

## Methods
### `testTransformToOptions_Success()`

`ISTEST`

#### Signature
```apex
private static void testTransformToOptions_Success()
```

#### Return Type
**void**
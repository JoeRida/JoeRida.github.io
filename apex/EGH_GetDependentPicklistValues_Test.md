---
hide:
  - path
---

# EGH_GetDependentPicklistValues_Test Class

`ISTEST`

## Class Diagram

```mermaid
graph TD
  EGH_GetDependentPicklistValues_Test["EGH_GetDependentPicklistValues_Test"]:::mainApexClass
  click EGH_GetDependentPicklistValues_Test "/objects/EGH_GetDependentPicklistValues_Test/"
  EGH_GetDependentPicklistValues["EGH_GetDependentPicklistValues"]:::apexClass
  click EGH_GetDependentPicklistValues "/apex/EGH_GetDependentPicklistValues/"
  PicklistOption["PicklistOption"]:::apexClass
  click PicklistOption "/apex/PicklistOption/"

  EGH_GetDependentPicklistValues_Test --> EGH_GetDependentPicklistValues
  EGH_GetDependentPicklistValues_Test --> PicklistOption


  EGH_GetDependentPicklistValues --> PicklistOption

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
public class EGH_GetDependentPicklistValues_Test {

    @IsTest
    static void testGetDependentValuesSuccess() {
        
        EGH_GetDependentPicklistValues.FlowInput input = new EGH_GetDependentPicklistValues.FlowInput();
        input.objectAPIName = 'Lead';
        input.dependentFieldAPIName = 'EGH_Model_of_Interest__c';
        input.controllingValue = 'Jetour'; // Example value

        List<EGH_GetDependentPicklistValues.FlowInput> inputs = new List<EGH_GetDependentPicklistValues.FlowInput>{input};

        Test.startTest();
        List<List<PicklistOption>> results = EGH_GetDependentPicklistValues.getDependentValuesFlow(inputs);
        Test.stopTest();

        // Assertions
        System.assertNotEquals(null, results, 'The result list should not be null');
        System.assertEquals(1, results.size(), 'There should be one result list for the one input provided');
        
        // Since we can't guarantee a dependency exists in every scratch org/sandbox for standard fields,
        // we check that the code didn't crash and returned a valid list (even if empty).
        List<PicklistOption> options = results[0];
        System.assertNotEquals(null, options, 'The options list should be initialized');
    }

    @IsTest
    static void testInvalidObjectOrField() {
        EGH_GetDependentPicklistValues.FlowInput input = new EGH_GetDependentPicklistValues.FlowInput();
        input.objectAPIName = 'Invalid_Object_Name__c';
        input.dependentFieldAPIName = 'No_Field__c';
        input.controllingValue = 'SomeValue';

        List<EGH_GetDependentPicklistValues.FlowInput> inputs = new List<EGH_GetDependentPicklistValues.FlowInput>{input};

        Test.startTest();
        List<List<PicklistOption>> results = EGH_GetDependentPicklistValues.getDependentValuesFlow(inputs);
        Test.stopTest();

        System.assertEquals(1, results.size());
        System.assertEquals(0, results[0].size(), 'Should return an empty list for invalid metadata names');
    }
}
```

## Methods
### `testGetDependentValuesSuccess()`

`ISTEST`

#### Signature
```apex
private static void testGetDependentValuesSuccess()
```

#### Return Type
**void**

---

### `testInvalidObjectOrField()`

`ISTEST`

#### Signature
```apex
private static void testInvalidObjectOrField()
```

#### Return Type
**void**
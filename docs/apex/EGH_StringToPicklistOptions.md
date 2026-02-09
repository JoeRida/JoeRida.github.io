---
hide:
  - path
---

# EGH_StringToPicklistOptions Class

## Class Diagram

```mermaid
graph TD
  EGH_StringToPicklistOptions["EGH_StringToPicklistOptions"]:::mainApexClass
  click EGH_StringToPicklistOptions "/objects/EGH_StringToPicklistOptions/"
  PicklistOption["PicklistOption"]:::apexClass
  click PicklistOption "/apex/PicklistOption/"
  EGH_StringToPicklistOptionsTest["EGH_StringToPicklistOptionsTest"]:::apexTestClass
  click EGH_StringToPicklistOptionsTest "/apex/EGH_StringToPicklistOptionsTest/"

  EGH_StringToPicklistOptions --> PicklistOption

  EGH_StringToPicklistOptionsTest --> EGH_StringToPicklistOptions

  EGH_StringToPicklistOptionsTest --> PicklistOption

classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
linkStyle 1 stroke:#FF8C00,stroke-width:2px;
linkStyle 2 stroke:#A6A6A6,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public with sharing class EGH_StringToPicklistOptions {

    public class FlowInput {
        @InvocableVariable(label='Semicolon separated String' required=true)
        public String semicolonSeparatedString;
    }

    @InvocableMethod(label='Transform semicolon-separated string values to Picklist Options' description='Splits a semicolon-separated string into a list of PicklistOption objects')
    public static List<List<PicklistOption>> transformToOptions(List<FlowInput> inputs) {
        List<List<PicklistOption>> results = new List<List<PicklistOption>>();

        for (FlowInput input : inputs) {
            List<PicklistOption> picklistOptionsList = new List<PicklistOption>();

            if (String.isNotBlank(input.semicolonSeparatedString)) {                
                for (String val : input.semicolonSeparatedString.split(';')) {
                    picklistOptionsList.add(new PicklistOption(val, val));
                }
            }
            results.add(picklistOptionsList);
        }

        return results;
    }
}
```

## Methods
### `transformToOptions(inputs)`

`INVOCABLEMETHOD`

#### Signature
```apex
public static List<List<PicklistOption>> transformToOptions(List<FlowInput> inputs)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| inputs | List<FlowInput> |  |

#### Return Type
**List<List<PicklistOption>>**

## Classes
### FlowInput Class

#### Fields
##### `semicolonSeparatedString`

`INVOCABLEVARIABLE`

###### Signature
```apex
public semicolonSeparatedString
```

###### Type
String
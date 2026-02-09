---
hide:
  - path
---

# PicklistOption Class

## Class Diagram

```mermaid
graph TD
  PicklistOption["PicklistOption"]:::mainApexClass
  click PicklistOption "/objects/PicklistOption/"
  EGH_GetDependentPicklistValues["EGH_GetDependentPicklistValues"]:::apexClass
  click EGH_GetDependentPicklistValues "/apex/EGH_GetDependentPicklistValues/"
  EGH_GetDependentPicklistValues_Test["EGH_GetDependentPicklistValues_Test"]:::apexTestClass
  click EGH_GetDependentPicklistValues_Test "/apex/EGH_GetDependentPicklistValues_Test/"
  EGH_StringToPicklistOptions["EGH_StringToPicklistOptions"]:::apexClass
  click EGH_StringToPicklistOptions "/apex/EGH_StringToPicklistOptions/"
  EGH_StringToPicklistOptionsTest["EGH_StringToPicklistOptionsTest"]:::apexTestClass
  click EGH_StringToPicklistOptionsTest "/apex/EGH_StringToPicklistOptionsTest/"


  EGH_GetDependentPicklistValues --> PicklistOption
  EGH_GetDependentPicklistValues_Test --> PicklistOption
  EGH_StringToPicklistOptions --> PicklistOption
  EGH_StringToPicklistOptionsTest --> PicklistOption

  EGH_GetDependentPicklistValues_Test --> EGH_GetDependentPicklistValues
  EGH_StringToPicklistOptionsTest --> EGH_StringToPicklistOptions

classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0,1,2,3 stroke:#FF8C00,stroke-width:2px;
linkStyle 4,5 stroke:#A6A6A6,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public with sharing class PicklistOption {
        @AuraEnabled
        @InvocableVariable
        public String label;
        @AuraEnabled
        @InvocableVariable
        public String value;

        public PicklistOption(String label, String value) {
            this.label = label;
            this.value = value;
        }
}
```

## Fields
### `label`

`AURAENABLED`
`INVOCABLEVARIABLE`

#### Signature
```apex
public label
```

#### Type
String

---

### `value`

`AURAENABLED`
`INVOCABLEVARIABLE`

#### Signature
```apex
public value
```

#### Type
String

## Constructors
### `PicklistOption(label, value)`

#### Signature
```apex
public PicklistOption(String label, String value)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| label | String |  |
| value | String |  |
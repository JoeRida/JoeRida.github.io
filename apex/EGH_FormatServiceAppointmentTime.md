---
hide:
  - path
---

# EGH_FormatServiceAppointmentTime Class

## Class Diagram

```mermaid
graph TD
  EGH_FormatServiceAppointmentTime["EGH_FormatServiceAppointmentTime"]:::mainApexClass
  click EGH_FormatServiceAppointmentTime "/objects/EGH_FormatServiceAppointmentTime/"
  EGH_FormatServiceAppointmentTime_Test["EGH_FormatServiceAppointmentTime_Test"]:::apexTestClass
  click EGH_FormatServiceAppointmentTime_Test "/apex/EGH_FormatServiceAppointmentTime_Test/"


  EGH_FormatServiceAppointmentTime_Test --> EGH_FormatServiceAppointmentTime


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public class EGH_FormatServiceAppointmentTime {

    public class Input {
        @InvocableVariable(required=true)
        public Datetime startTime;

        @InvocableVariable(required=true)
        public Datetime endTime;

        @InvocableVariable(required=true)
        public String userTimeZone;
    }

    public class Output {
        @InvocableVariable
        public String formattedDate;

        @InvocableVariable
        public String formattedStartTime;

        @InvocableVariable
        public String formattedEndTime;
    }

    @InvocableMethod(label='Format Date & Time in User Time Zone')
    public static List<Output> format(List<Input> inputs) {
        List<Output> results = new List<Output>();

        for (Input i : inputs) {
            Output o = new Output();
            o.formattedDate      = i.startTime.format('EEEE, MMMM d, yyyy', i.userTimeZone);
            o.formattedStartTime = i.startTime.format('h:mm a', i.userTimeZone);
            o.formattedEndTime   = i.endTime.format('h:mm a', i.userTimeZone);
            results.add(o);
        }
        return results;
    }
}
```

## Methods
### `format(inputs)`

`INVOCABLEMETHOD`

#### Signature
```apex
public static List<Output> format(List<Input> inputs)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| inputs | List<Input> |  |

#### Return Type
**List<Output>**

## Classes
### Input Class

#### Fields
##### `startTime`

`INVOCABLEVARIABLE`

###### Signature
```apex
public startTime
```

###### Type
Datetime

---

##### `endTime`

`INVOCABLEVARIABLE`

###### Signature
```apex
public endTime
```

###### Type
Datetime

---

##### `userTimeZone`

`INVOCABLEVARIABLE`

###### Signature
```apex
public userTimeZone
```

###### Type
String

### Output Class

#### Fields
##### `formattedDate`

`INVOCABLEVARIABLE`

###### Signature
```apex
public formattedDate
```

###### Type
String

---

##### `formattedStartTime`

`INVOCABLEVARIABLE`

###### Signature
```apex
public formattedStartTime
```

###### Type
String

---

##### `formattedEndTime`

`INVOCABLEVARIABLE`

###### Signature
```apex
public formattedEndTime
```

###### Type
String
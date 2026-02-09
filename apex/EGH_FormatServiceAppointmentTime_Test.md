---
hide:
  - path
---

# EGH_FormatServiceAppointmentTime_Test Class

`ISTEST`

## Class Diagram

```mermaid
graph TD
  EGH_FormatServiceAppointmentTime_Test["EGH_FormatServiceAppointmentTime_Test"]:::mainApexClass
  click EGH_FormatServiceAppointmentTime_Test "/objects/EGH_FormatServiceAppointmentTime_Test/"
  EGH_FormatServiceAppointmentTime["EGH_FormatServiceAppointmentTime"]:::apexClass
  click EGH_FormatServiceAppointmentTime "/apex/EGH_FormatServiceAppointmentTime/"

  EGH_FormatServiceAppointmentTime_Test --> EGH_FormatServiceAppointmentTime



classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
```

<!-- Apex description -->

## Apex Code

```java
@IsTest
public class EGH_FormatServiceAppointmentTime_Test {

    @IsTest
    static void testFormatDateAndTimeInUserTimeZone() {

        // Arrange
        Datetime startDt = Datetime.newInstanceGmt(2026, 1, 27, 6, 15, 0); // 10:15 AM Dubai
        Datetime endDt   = Datetime.newInstanceGmt(2026, 1, 27, 6, 45, 0); // 10:45 AM Dubai
        String timeZone  = 'Asia/Dubai';

        EGH_FormatServiceAppointmentTime.Input input = 
            new EGH_FormatServiceAppointmentTime.Input();
        input.startTime = startDt;
        input.endTime   = endDt;
        input.userTimeZone = timeZone;

        List<EGH_FormatServiceAppointmentTime.Input> inputs =
            new List<EGH_FormatServiceAppointmentTime.Input>{ input };

        // Act
        Test.startTest();
        List<EGH_FormatServiceAppointmentTime.Output> results =
            EGH_FormatServiceAppointmentTime.format(inputs);
        Test.stopTest();

        // Assert
        System.assertEquals(1, results.size());

        EGH_FormatServiceAppointmentTime.Output output = results[0];

        System.assertEquals(
            'Tuesday, January 27, 2026',
            output.formattedDate,
            'Date should be formatted in user timezone'
        );

        System.assertEquals(
            '10:15 AM',
            output.formattedStartTime,
            'Start time should be formatted in user timezone'
        );

        System.assertEquals(
            '10:45 AM',
            output.formattedEndTime,
            'End time should be formatted in user timezone'
        );
    }
}
```

## Methods
### `testFormatDateAndTimeInUserTimeZone()`

`ISTEST`

#### Signature
```apex
private static void testFormatDateAndTimeInUserTimeZone()
```

#### Return Type
**void**
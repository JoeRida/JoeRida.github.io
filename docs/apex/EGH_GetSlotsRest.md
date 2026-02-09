---
hide:
  - path
---

# EGH_GetSlotsRest Class

`RESTRESOURCE`

## Class Diagram

```mermaid
graph TD
  EGH_GetSlotsRest["EGH_GetSlotsRest"]:::mainApexClass
  click EGH_GetSlotsRest "/objects/EGH_GetSlotsRest/"
  EGH_TestDriveSlotFinder["EGH_TestDriveSlotFinder"]:::apexClass
  click EGH_TestDriveSlotFinder "/apex/EGH_TestDriveSlotFinder/"
  EGH_RestTests["EGH_RestTests"]:::apexTestClass
  click EGH_RestTests "/apex/EGH_RestTests/"

  EGH_GetSlotsRest --> EGH_TestDriveSlotFinder

  EGH_RestTests --> EGH_GetSlotsRest


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#4C9F70,stroke-width:4px;
linkStyle 1 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
@RestResource(urlMapping='/testdrive/slots')
global with sharing class EGH_GetSlotsRest {

    global class SlotsRequest {
        public Id territoryId;
        public Id vehicleResourceId;
        public Id workTypeId;
        public Datetime startTime;
        public Datetime endTime;
    }

    global class SlotsResponse {
        public Boolean success;
        public String message;
        public List<EGH_TestDriveSlotFinder.TimeSlotWrapper> slots;
    }

    @HttpPost
    global static void doPost() {
        RestRequest req = RestContext.request;
        RestResponse res = RestContext.response;
        res.addHeader('Content-Type', 'application/json');

        SlotsResponse out = new SlotsResponse();
        out.success = false;
        out.message = '';
        out.slots = new List<EGH_TestDriveSlotFinder.TimeSlotWrapper>();

        try {
            if (req == null || String.isBlank(req.requestBody.toString())) {
                out.message = 'Empty request body';
                writeResponse(res, out, 400);
                return;
            }

            SlotsRequest body = (SlotsRequest) JSON.deserialize(req.requestBody.toString(), SlotsRequest.class);

            // Basic validation
            List<String> missing = new List<String>();
            if (body.territoryId == null) missing.add('territoryId');
            if (body.vehicleResourceId == null) missing.add('vehicleResourceId');
            if (body.workTypeId == null) missing.add('workTypeId');
            if (body.startTime == null) missing.add('startTime');
            if (body.endTime == null) missing.add('endTime');

            if (!missing.isEmpty()) {
                out.message = 'Missing required fields: ' + String.join(missing, ', ');
                writeResponse(res, out, 400);
                return;
            }

            List<EGH_TestDriveSlotFinder.TimeSlotWrapper> slots =
                EGH_TestDriveSlotFinder.getCombinedSlots(
                    body.territoryId,
                    body.vehicleResourceId,
                    body.workTypeId,
                    body.startTime,
                    body.endTime
                );

            out.success = true;
            out.slots = slots;
            out.message = 'OK';
            writeResponse(res, out, 200);

        } catch (Exception e) {
            // Return a 400 for known/handled functional errors if they bubbled up with a clear message
            // Otherwise default to 500
            String msg = e.getMessage();
            if (msg != null && msg.contains('No ') || msg != null && msg.contains('Failed to')) {
                out.message = msg;
                writeResponse(res, out, 400);
            } else {
                out.message = 'Failed to retrieve slots: ' + msg;
                writeResponse(res, out, 500);
            }
        }
    }

    private static void writeResponse(RestResponse res, Object payload, Integer statusCode) {
        res.statusCode = statusCode;
        res.responseBody = Blob.valueOf(JSON.serialize(payload));
    }
}
```

## Methods
### `doPost()`

`HTTPPOST`

#### Signature
```apex
global static void doPost()
```

#### Return Type
**void**

---

### `writeResponse(res, payload, statusCode)`

#### Signature
```apex
private static void writeResponse(RestResponse res, Object payload, Integer statusCode)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| res | RestResponse |  |
| payload | Object |  |
| statusCode | Integer |  |

#### Return Type
**void**

## Classes
### SlotsRequest Class

#### Fields
##### `territoryId`

###### Signature
```apex
public territoryId
```

###### Type
Id

---

##### `vehicleResourceId`

###### Signature
```apex
public vehicleResourceId
```

###### Type
Id

---

##### `workTypeId`

###### Signature
```apex
public workTypeId
```

###### Type
Id

---

##### `startTime`

###### Signature
```apex
public startTime
```

###### Type
Datetime

---

##### `endTime`

###### Signature
```apex
public endTime
```

###### Type
Datetime

### SlotsResponse Class

#### Fields
##### `success`

###### Signature
```apex
public success
```

###### Type
Boolean

---

##### `message`

###### Signature
```apex
public message
```

###### Type
String

---

##### `slots`

###### Signature
```apex
public slots
```

###### Type
List<EGH_TestDriveSlotFinder.TimeSlotWrapper>
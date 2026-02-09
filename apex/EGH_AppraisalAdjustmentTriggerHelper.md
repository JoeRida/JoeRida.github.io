---
hide:
  - path
---

# EGH_AppraisalAdjustmentTriggerHelper Class

## Class Diagram

```mermaid
graph TD
  EGH_AppraisalAdjustmentTriggerHelper["EGH_AppraisalAdjustmentTriggerHelper"]:::mainApexClass
  click EGH_AppraisalAdjustmentTriggerHelper "/objects/EGH_AppraisalAdjustmentTriggerHelper/"
  EGH_AppraisalAdjustmentTrigger["EGH_AppraisalAdjustmentTrigger"]:::apexClass
  EGH_AppraisalAdjustmentTriggerTest["EGH_AppraisalAdjustmentTriggerTest"]:::apexTestClass
  click EGH_AppraisalAdjustmentTriggerTest "/apex/EGH_AppraisalAdjustmentTriggerTest/"


  EGH_AppraisalAdjustmentTrigger --> EGH_AppraisalAdjustmentTriggerHelper
  EGH_AppraisalAdjustmentTriggerTest --> EGH_AppraisalAdjustmentTriggerHelper


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0,1 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public class EGH_AppraisalAdjustmentTriggerHelper {
    
    // Helper method to update Appraisal records
    public static void updateAppraisalRecords(Set<Id> appraisalIds, Map<Id, Id> appraisalToEvaluatorMap) {
    
    List<Appraisal> appraisalsToUpdate = new List<Appraisal>();
    
    // Query existing Appraisal records
    for (Appraisal appr : [SELECT Id, Status FROM Appraisal WHERE Id IN :appraisalIds]) {
        
        // Create update record
        Appraisal updateAppr = new Appraisal();
        updateAppr.Id = appr.Id;
        updateAppr.Status = 'Evaluated'; // Change status to Evaluated
        
        // Set Last Evaluator (assuming this field exists)
        // Note: You'll need to add this field to the Appraisal object
        // updateAppr.LastEvaluatorId = appraisalToEvaluatorMap.get(appr.Id);
        
        appraisalsToUpdate.add(updateAppr);
    }
    
    // Perform DML operation
    if (!appraisalsToUpdate.isEmpty()) {
        try {
            update appraisalsToUpdate;
        } catch (DmlException e) {
            System.debug('Error updating Appraisal records: ' + e.getMessage());
            // Handle error appropriately
        }
    }
}}
```

## Methods
### `updateAppraisalRecords(appraisalIds, appraisalToEvaluatorMap)`

#### Signature
```apex
public static void updateAppraisalRecords(Set<Id> appraisalIds, Map<Id,Id> appraisalToEvaluatorMap)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| appraisalIds | Set<Id> |  |
| appraisalToEvaluatorMap | Map<Id,Id> |  |

#### Return Type
**void**
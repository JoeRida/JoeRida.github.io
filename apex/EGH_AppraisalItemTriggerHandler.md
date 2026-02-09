---
hide:
  - path
---

# EGH_AppraisalItemTriggerHandler Class

## Class Diagram

```mermaid
graph TD
  EGH_AppraisalItemTriggerHandler["EGH_AppraisalItemTriggerHandler"]:::mainApexClass
  click EGH_AppraisalItemTriggerHandler "/objects/EGH_AppraisalItemTriggerHandler/"
  EGH_AppraisalAdjustmentTriggerTest["EGH_AppraisalAdjustmentTriggerTest"]:::apexTestClass
  click EGH_AppraisalAdjustmentTriggerTest "/apex/EGH_AppraisalAdjustmentTriggerTest/"
  EGH_AppraisalItemTrigger["EGH_AppraisalItemTrigger"]:::apexClass


  EGH_AppraisalAdjustmentTriggerTest --> EGH_AppraisalItemTriggerHandler
  EGH_AppraisalItemTrigger --> EGH_AppraisalItemTriggerHandler


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0,1 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public class EGH_AppraisalItemTriggerHandler {
    
    public static void handleBeforeUpdate(List<AppraisalItem> newItems, Map<Id, AppraisalItem> oldItemMap) {
        validateCustomerAskingValue(newItems, oldItemMap);
    }
    
    private static void validateCustomerAskingValue(List<AppraisalItem> newItems, Map<Id, AppraisalItem> oldItemMap) {
        for (AppraisalItem item : newItems) {
            AppraisalItem oldItem = oldItemMap.get(item.Id);
            
            // Check if CustomerAskingValue is being modified
            if (item.CustomerAskingValue != oldItem.CustomerAskingValue) {
                item.CustomerAskingValue.addError('Price requested by Customer cannot be modified after the record is created.');
            }
        }
    }
}
```

## Methods
### `handleBeforeUpdate(newItems, oldItemMap)`

#### Signature
```apex
public static void handleBeforeUpdate(List<AppraisalItem> newItems, Map<Id,AppraisalItem> oldItemMap)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| newItems | List<AppraisalItem> |  |
| oldItemMap | Map<Id,AppraisalItem> |  |

#### Return Type
**void**

---

### `validateCustomerAskingValue(newItems, oldItemMap)`

#### Signature
```apex
private static void validateCustomerAskingValue(List<AppraisalItem> newItems, Map<Id,AppraisalItem> oldItemMap)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| newItems | List<AppraisalItem> |  |
| oldItemMap | Map<Id,AppraisalItem> |  |

#### Return Type
**void**
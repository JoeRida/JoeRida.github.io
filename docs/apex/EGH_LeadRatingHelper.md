---
hide:
  - path
---

# EGH_LeadRatingHelper Class

## Class Diagram

```mermaid
graph TD
  EGH_LeadRatingHelper["EGH_LeadRatingHelper"]:::mainApexClass
  click EGH_LeadRatingHelper "/objects/EGH_LeadRatingHelper/"
  EGH_LeadRatingTrigger["EGH_LeadRatingTrigger"]:::apexClass


  EGH_LeadRatingTrigger --> EGH_LeadRatingHelper


classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

linkStyle 0 stroke:#FF8C00,stroke-width:2px;
```

<!-- Apex description -->

## Apex Code

```java
public class EGH_LeadRatingHelper {
    // Helper method to determine and set the Rating
    public static void setLeadRating(Lead lead) {
        Decimal score = lead.EGH_Total_Lead_Score__c;
        String rating = determineRating(score);
        lead.Rating = rating;
    }

    // Logic to determine the Rating based on the score
    private static String determineRating(Decimal score) {
        if (score == null) {
            return 'Cold'; // Handle null scores as Cold
        }
        if (score >= 10) {
            return 'Hot';
        } else if (score >= 5) {
            return 'Warm';
        } else {
            return 'Cold';
        }
    }
}
```

## Methods
### `setLeadRating(lead)`

#### Signature
```apex
public static void setLeadRating(Lead lead)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| lead | [Lead](../objects/Lead.md) |  |

#### Return Type
**void**

---

### `determineRating(score)`

#### Signature
```apex
private static String determineRating(Decimal score)
```

#### Parameters
| Name | Type | Description |
|------|------|-------------|
| score | Decimal |  |

#### Return Type
**String**
---
hide:
  - path
---

# RecentAccountsController Class

## Class Diagram

```mermaid
graph TD
  RecentAccountsController["RecentAccountsController"]:::mainApexClass
  click RecentAccountsController "/objects/RecentAccountsController/"




classDef apexClass fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef apexTestClass fill:#F5F5F5,stroke:#999999,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainApexClass fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

```

<!-- Apex description -->

## Apex Code

```java
public with sharing class RecentAccountsController {
    @AuraEnabled(cacheable=true)
    public static List<Account> getRecentAccounts() {
        return [SELECT Id, Name FROM Account ORDER BY CreatedDate DESC LIMIT 10];
    }
}
```

## Methods
### `getRecentAccounts()`

`AURAENABLED`

#### Signature
```apex
public static List<Account> getRecentAccounts()
```

#### Return Type
**List<Account>**
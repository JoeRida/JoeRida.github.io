---
hide:
  - path
---

<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->


## Schema

```mermaid
graph TD
UserServicePresence["UserServicePresence"]:::mainObject
click UserServicePresence "/objects/UserServicePresence/"


classDef object fill:#D6E9FF,stroke:#0070D2,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObject fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObjectManaged fill:#FFD8B2,stroke:#CC5500,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainObject fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

```


<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| AtCapacityDuration |  |  | undefined |
| AtCapacityStartTime |  |  | undefined |
| AverageCapacity |  |  | undefined |
| AverageCapacityStartTime |  |  | undefined |
| Capacity |  |  | undefined |
| ClusterId |  |  | undefined |
| ConfiguredCapacity |  |  | undefined |
| ConfiguredInterruptCapacity |  |  | undefined |
| IdleDuration |  |  | undefined |
| IdleStartTime |  |  | undefined |
| InterruptibleCapacity |  |  | undefined |
| IsAway |  |  | undefined |
| IsCurrentState |  |  | undefined |
| LASessionId |  |  | undefined |
| OwnerId |  | Lookup | undefined |
| PresenceUserConfig |  |  | undefined |
| PreviousCapacity |  |  | undefined |
| PreviousInterruptibleCapacity |  |  | undefined |
| ServicePresenceStatusId |  | Lookup | undefined |
| StatusEndDate |  |  | undefined |
| StatusSequence |  |  | undefined |
| StatusStartDate |  |  | undefined |
| UserId |  | Lookup | undefined |


## Related Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| 💻 | [EGH_Lead_Routing_SubFlow](../flows/EGH_Lead_Routing_SubFlow.md) |  Routing Flow | <!-- --> |


## Related Apex Classes

| Apex Class | Type |
| :----      | :--: | 
| [EGH_CheckCapacityForVisitRouting](../apex/EGH_CheckCapacityForVisitRouting.md) | Invocable |
| [EGH_CheckCapacityForVisitRoutingTest](../apex/EGH_CheckCapacityForVisitRoutingTest.md) | Test (See All Data) |








_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_

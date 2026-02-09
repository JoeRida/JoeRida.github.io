---
hide:
  - path
---

<!-- This file is auto-generated. if you do not want it to be overwritten, set TRUE in the line below -->
<!-- DO_NOT_OVERWRITE_DOC=FALSE -->


## Schema

```mermaid
graph TD
CaseMilestone["CaseMilestone"]:::mainObject
click CaseMilestone "/objects/CaseMilestone/"


classDef object fill:#D6E9FF,stroke:#0070D2,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObject fill:#FFF4C2,stroke:#CCAA00,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef customObjectManaged fill:#FFD8B2,stroke:#CC5500,stroke-width:3px,rx:12px,ry:12px,shadow:drop,color:#333;
classDef mainObject fill:#FFB3B3,stroke:#A94442,stroke-width:4px,rx:14px,ry:14px,shadow:drop,color:#333,font-weight:bold;

```


<!-- Object description -->

## Fields

| Name      | Label | Type | Description |
| :-------- | :---- | :--: | :---------- | 
| ActualElapsedTimeInDays |  |  | undefined |
| ActualElapsedTimeInHrs |  |  | undefined |
| ActualElapsedTimeInMins |  |  | undefined |
| BusinessHoursId |  | Lookup | undefined |
| CaseId |  | Lookup | undefined |
| CompletionDate |  |  | undefined |
| ElapsedTimeInDays |  |  | undefined |
| ElapsedTimeInHrs |  |  | undefined |
| ElapsedTimeInMins |  |  | undefined |
| IsCompleted |  |  | undefined |
| IsViolated |  |  | undefined |
| MilestoneId |  | Lookup | undefined |
| SlaProcessId |  | Lookup | undefined |
| StartDate |  |  | undefined |
| StoppedTimeInDays |  |  | undefined |
| StoppedTimeInHrs |  |  | undefined |
| StoppedTimeInMins |  |  | undefined |
| TargetDate |  |  | undefined |
| TargetResponseInDays |  |  | undefined |
| TargetResponseInHrs |  |  | undefined |
| TargetResponseInMins |  |  | undefined |
| TimeRemainingInDays |  |  | undefined |
| TimeRemainingInHrs |  |  | undefined |
| TimeRemainingInMins |  |  | undefined |
| TimeSinceTargetInDays |  |  | undefined |
| TimeSinceTargetInHrs |  |  | undefined |
| TimeSinceTargetInMins |  |  | undefined |


## Related Flows

| Object | Name      | Type | Description |
| :----  | :-------- | :--: | :---------- | 
| 💻 | [EGH_Auto_Complete_Milestonnes](../flows/EGH_Auto_Complete_Milestonnes.md) |  Auto Launched Flow | <!-- --> |
| 💻 | [EGH_Case_Action_Notification_After_4_Hour](../flows/EGH_Case_Action_Notification_After_4_Hour.md) |  Auto Launched Flow | <!-- --> |
| 💻 | [EGH_Case_Notification_After_5_Hour](../flows/EGH_Case_Notification_After_5_Hour.md) |  Auto Launched Flow | <!-- --> |
| Case | [EGH_Auto_Complete_Case_Milestones](../flows/EGH_Auto_Complete_Case_Milestones.md) |  Record After Save | <!-- --> |










_Documentation generated with [sfdx-hardis](https://sfdx-hardis.cloudity.com), by [Cloudity](https://www.cloudity.com/) & [friends](https://github.com/hardisgroupcom/sfdx-hardis/graphs/contributors)_

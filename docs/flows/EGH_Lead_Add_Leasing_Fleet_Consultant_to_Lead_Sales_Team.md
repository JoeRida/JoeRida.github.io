# EGH Lead - Add Leasing/Fleet Consultant to Lead Sales Team

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
click START "#general-information" "4154479989"

Add_Lead_Owner_to_Lead_Sales_Team[("➕ <em></em><br/>Add Lead Owner to Lead Sales Team")]:::recordCreates
click Add_Lead_Owner_to_Lead_Sales_Team "#add_lead_owner_to_lead_sales_team" "3793164721"

Add_Lead_Owner_to_Lead_Sales_Team --> END_Add_Lead_Owner_to_Lead_Sales_Team
START -->  Add_Lead_Owner_to_Lead_Sales_Team
END_Add_Lead_Owner_to_Lead_Sales_Team(( END )):::endClass


classDef actionCalls fill:#D4E4FC,color:black,text-decoration:none,max-height:100px
classDef assignments fill:#FBEED7,color:black,text-decoration:none,max-height:100px
classDef collectionProcessors fill:#F0E3FA,color:black,text-decoration:none,max-height:100px
classDef customErrors fill:#FFE9E9,color:black,text-decoration:none,max-height:100px
classDef decisions fill:#FDEAF6,color:black,text-decoration:none,max-height:100px
classDef loops fill:#FDEAF6,color:black,text-decoration:none,max-height:100px
classDef recordCreates fill:#FFF8C9,color:black,text-decoration:none,max-height:100px
classDef recordDeletes fill:#FFF8C9,color:black,text-decoration:none,max-height:100px
classDef recordLookups fill:#EDEAFF,color:black,text-decoration:none,max-height:100px
classDef recordUpdates fill:#FFF8C9,color:black,text-decoration:none,max-height:100px
classDef screens fill:#DFF6FF,color:black,text-decoration:none,max-height:100px
classDef subflows fill:#D4E4FC,color:black,text-decoration:none,max-height:100px
classDef startClass fill:#D9F2E6,color:black,text-decoration:none,max-height:100px
classDef endClass fill:#F9BABA,color:black,text-decoration:none,max-height:100px
classDef transforms fill:#FDEAF6,color:black,text-decoration:none,max-height:100px


```

<!-- Flow description -->

## General Information

|<!-- -->|<!-- -->|
|:---|:---|
|Object|Lead|
|Process Type| Auto Launched Flow|
|Trigger Type| Record After Save|
|Record Trigger Type| Create|
|Label|EGH Lead - Add Leasing/Fleet Consultant to Lead Sales Team|
|Status|Active|
|Filter Formula|BEGINS({!$Record.OwnerId},"005") && <br/> ( {!$Record.Owner:User.UserRole.DeveloperName} = "Fleet_Sales_Consultant" || {!$Record.Owner:User.UserRole.DeveloperName} = "Leasing_Sales_Consultant")|
|Environments|Default|
|Interview Label|EGH Lead - Add Leasing/Fleet Consultant to Lead Sales Team {!$Flow.CurrentDateTime}|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Add_Lead_Owner_to_Lead_Sales_Team](#add_lead_owner_to_lead_sales_team)|
|Next Node|[Add_Lead_Owner_to_Lead_Sales_Team](#add_lead_owner_to_lead_sales_team)|


## Flow Nodes Details

### Add_Lead_Owner_to_Lead_Sales_Team

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_LeadSalesTeam__c|
|Label|Add Lead Owner to Lead Sales Team|
|Store Output Automatically|✅|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_LeadLookup__c|$Record.Id|
|EGH_ShowroomLookup__c|$Record.EGH_LeadBranchUnitLookup__c|
|EGH_TeamMemberLookup__c|$Record.OwnerId|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
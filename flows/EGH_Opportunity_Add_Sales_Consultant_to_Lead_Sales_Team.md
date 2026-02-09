# EGH Opportunity Add Sales Consultant to Lead Sales Team

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
click START "#general-information" "377820101"

Lead_Sales_Team_Exist{"🔀 <em></em><br/>Lead Sales Team Exist ?"}:::decisions
click Lead_Sales_Team_Exist "#lead_sales_team_exist" "2193967514"

Add_Sales_Consultant_Owner_to_Lead_Sales_Team[("➕ <em></em><br/>Add Sales Consultant Owner to Lead Sales Team")]:::recordCreates
click Add_Sales_Consultant_Owner_to_Lead_Sales_Team "#add_sales_consultant_owner_to_lead_sales_team" "4218153816"

Get_Existing_Lead_Sales_Team[("🔍 <em></em><br/>Get Existing Lead Sales Team")]:::recordLookups
click Get_Existing_Lead_Sales_Team "#get_existing_lead_sales_team" "3745109255"

Lead_Sales_Team_Exist --> |"No Create One"| Add_Sales_Consultant_Owner_to_Lead_Sales_Team
Lead_Sales_Team_Exist --> |"Exist Already"| END_Lead_Sales_Team_Exist
Add_Sales_Consultant_Owner_to_Lead_Sales_Team --> END_Add_Sales_Consultant_Owner_to_Lead_Sales_Team
Get_Existing_Lead_Sales_Team --> Lead_Sales_Team_Exist
START -->  Get_Existing_Lead_Sales_Team
END_Lead_Sales_Team_Exist(( END )):::endClass
END_Add_Sales_Consultant_Owner_to_Lead_Sales_Team(( END )):::endClass


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
|Object|Opportunity|
|Process Type| Auto Launched Flow|
|Trigger Type| Record After Save|
|Record Trigger Type| Update|
|Label|EGH Opportunity Add Sales Consultant to Lead Sales Team|
|Status|Active|
|Filter Formula|ISCHANGED({!$Record.OwnerId}) && BEGINS({!$Record.OwnerId}, "005") && <br/>{!$Record.Owner.UserRole.DeveloperName} = "EGH_SalesConsultantRole"|
|Environments|Default|
|Interview Label|EGH Opportunity Add Sales Consultant to Lead Sales Team {!$Flow.CurrentDateTime}|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Get_Existing_Lead_Sales_Team](#get_existing_lead_sales_team)|
|Next Node|[Get_Existing_Lead_Sales_Team](#get_existing_lead_sales_team)|


## Flow Nodes Details

### Lead_Sales_Team_Exist

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Lead Sales Team Exist ?|
|Default Connector Label|Exist Already|


#### Rule No_Create_One (No Create One)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Add_Sales_Consultant_Owner_to_Lead_Sales_Team](#add_sales_consultant_owner_to_lead_sales_team)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|[Get_Existing_Lead_Sales_Team](#get_existing_lead_sales_team)| Is Null|✅|




### Add_Sales_Consultant_Owner_to_Lead_Sales_Team

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_LeadSalesTeam__c|
|Label|Add Sales Consultant Owner to Lead Sales Team|
|Store Output Automatically|✅|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_OpportunityLookup__c|$Record.Id|
|EGH_ShowroomLookup__c|$Record.EGH_BranchUnitLookup__c|
|EGH_TeamMemberLookup__c|$Record.OwnerId|




### Get_Existing_Lead_Sales_Team

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|EGH_LeadSalesTeam__c|
|Label|Get Existing Lead Sales Team|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Lead_Sales_Team_Exist](#lead_sales_team_exist)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|EGH_OpportunityLookup__c| Equal To|$Record.Id|
|2|EGH_TeamMemberLookup__c| Equal To|$Record.OwnerId|
|3|EGH_ShowroomLookup__c| Equal To|$Record.EGH_BranchUnitLookup__c|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
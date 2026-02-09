# EGH Lead And Visit Showroom Assignment Flow

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
click START "#general-information" "3179318733"

Find_Team_Leader("⚙️ <em></em><br/>Find Team Leader"):::actionCalls
click Find_Team_Leader "#find_team_leader" "2519409653"

Assign_Account_Language[\"🟰 <em></em><br/>Assign Account Language"/]:::assignments
click Assign_Account_Language "#assign_account_language" "403230875"

Assign_English[\"🟰 <em></em><br/>Assign English"/]:::assignments
click Assign_English "#assign_english" "11724605"

Assign_Lead_Language[\"🟰 <em></em><br/>Assign Lead Language"/]:::assignments
click Assign_Lead_Language "#assign_lead_language" "1038173912"

Assigned_to_PG{"🔀 <em></em><br/>Assigned to PG ?"}:::decisions
click Assigned_to_PG "#assigned_to_pg" "1152957882"

Copy_1_of_Visit_Related_To{"🔀 <em></em><br/>Visit Related To ?"}:::decisions
click Copy_1_of_Visit_Related_To "#copy_1_of_visit_related_to" "815544230"

Is_created_by_Product_Genius_or_purpose_is_Event{"🔀 <em></em><br/>Is created by Product Genius or purpose is Event or purpose is Meet F&I Team"}:::decisions
click Is_created_by_Product_Genius_or_purpose_is_Event "#is_created_by_product_genius_or_purpose_is_event" "528753779"

Is_Person_Account{"🔀 <em></em><br/>Is Person Account ?"}:::decisions
click Is_Person_Account "#is_person_account" "1175635674"

Is_Showroom_Manager_Configured{"🔀 <em></em><br/>Is Showroom Manager Configured"}:::decisions
click Is_Showroom_Manager_Configured "#is_showroom_manager_configured" "908265112"

Is_the_purpose_of_the_visit_Meet_F_I_Team{"🔀 <em></em><br/>Is the purpose of the visit Meet F&I Team?"}:::decisions
click Is_the_purpose_of_the_visit_Meet_F_I_Team "#is_the_purpose_of_the_visit_meet_f_i_team" "1959759571"

To_be_Routed{"🔀 <em></em><br/>To be Routed?"}:::decisions
click To_be_Routed "#to_be_routed" "2253070348"

Visit_Related_To{"🔀 <em></em><br/>Visit Related To ?"}:::decisions
click Visit_Related_To "#visit_related_to" "3238900076"

Get_Branch_Unit[("🔍 <em></em><br/>Get Branch Unit")]:::recordLookups
click Get_Branch_Unit "#get_branch_unit" "2615753059"

Get_Digital_Sales_Consultant_Queue[("🔍 <em></em><br/>Get Digital Sales Consultant Queue")]:::recordLookups
click Get_Digital_Sales_Consultant_Queue "#get_digital_sales_consultant_queue" "2577905927"

Get_F_I_Queue[("🔍 <em></em><br/>Get F & I Queue")]:::recordLookups
click Get_F_I_Queue "#get_f_i_queue" "37077566"

Assign_related_lead_to_team_lead[("🛠️ <em></em><br/>Assign related lead to team lead")]:::recordUpdates
click Assign_related_lead_to_team_lead "#assign_related_lead_to_team_lead" "3105333636"

Update_Digital_Sales_Queue_as_Owner[("🛠️ <em></em><br/>Update Digital Sales Queue as Lead Owner")]:::recordUpdates
click Update_Digital_Sales_Queue_as_Owner "#update_digital_sales_queue_as_owner" "2490531346"

Update_F_I_Queue_as_Owner[("🛠️ <em></em><br/>Update  F & I Queue as Owner")]:::recordUpdates
click Update_F_I_Queue_as_Owner "#update_f_i_queue_as_owner" "3452713529"

Update_Lead_Owner[("🛠️ <em></em><br/>Update Lead Owner")]:::recordUpdates
click Update_Lead_Owner "#update_lead_owner" "1691955810"

Update_Opportunity_Owner_If_Not_Reserved[("🛠️ <em></em><br/>Update Opportunity Owner If Not Reserved")]:::recordUpdates
click Update_Opportunity_Owner_If_Not_Reserved "#update_opportunity_owner_if_not_reserved" "686688770"

Update_Visit_As_Assigned[("🛠️ <em></em><br/>Update Visit As Assigned")]:::recordUpdates
click Update_Visit_As_Assigned "#update_visit_as_assigned" "2176696209"

Routing_Omni_Flow[["🔗 <em>Subflow</em><br/>Routing Omni Flow"]]:::subflows
click Routing_Omni_Flow "#routing_omni_flow" "983148070"

Find_Team_Leader --> Is_Showroom_Manager_Configured
Assign_Account_Language --> Routing_Omni_Flow
Assign_English --> Routing_Omni_Flow
Assign_Lead_Language --> Routing_Omni_Flow
Assigned_to_PG --> |"Yes Skip assigning to Digital Queue"| Update_Lead_Owner
Assigned_to_PG --> |"No"| Is_the_purpose_of_the_visit_Meet_F_I_Team
Copy_1_of_Visit_Related_To --> |"Related to Lead"| Assigned_to_PG
Copy_1_of_Visit_Related_To --> |"Related to Account/Opportunity"| Update_Opportunity_Owner_If_Not_Reserved
Copy_1_of_Visit_Related_To --> |"Default Outcome"| END_Copy_1_of_Visit_Related_To
Is_created_by_Product_Genius_or_purpose_is_Event --> |"Yes"| Copy_1_of_Visit_Related_To
Is_created_by_Product_Genius_or_purpose_is_Event --> |"No"| To_be_Routed
Is_Person_Account --> |"Person Account"| Assign_Account_Language
Is_Person_Account --> |"Default Outcome"| Assign_English
Is_Showroom_Manager_Configured --> |"Yes"| Assign_related_lead_to_team_lead
Is_Showroom_Manager_Configured --> |"Default Outcome"| END_Is_Showroom_Manager_Configured
Is_the_purpose_of_the_visit_Meet_F_I_Team --> |"Meet F&I Team"| Get_F_I_Queue
Is_the_purpose_of_the_visit_Meet_F_I_Team --> |"Not F&I"| Get_Digital_Sales_Consultant_Queue
To_be_Routed --> |"Yes"| Visit_Related_To
To_be_Routed --> |"No"| Get_Branch_Unit
Visit_Related_To --> |"Related to Lead"| Assign_Lead_Language
Visit_Related_To --> |"Related to Account/Opportunity"| Is_Person_Account
Visit_Related_To --> |"Default Outcome"| END_Visit_Related_To
Get_Branch_Unit --> Find_Team_Leader
Get_Digital_Sales_Consultant_Queue --> Update_Digital_Sales_Queue_as_Owner
Get_F_I_Queue --> Update_F_I_Queue_as_Owner
Assign_related_lead_to_team_lead --> END_Assign_related_lead_to_team_lead
Update_Digital_Sales_Queue_as_Owner --> Update_Visit_As_Assigned
Update_F_I_Queue_as_Owner --> Update_Visit_As_Assigned
Update_Lead_Owner --> Update_Visit_As_Assigned
Update_Opportunity_Owner_If_Not_Reserved --> Update_Visit_As_Assigned
Update_Visit_As_Assigned --> END_Update_Visit_As_Assigned
START -->  Is_created_by_Product_Genius_or_purpose_is_Event
Routing_Omni_Flow --> Update_Visit_As_Assigned
END_Copy_1_of_Visit_Related_To(( END )):::endClass
END_Is_Showroom_Manager_Configured(( END )):::endClass
END_Visit_Related_To(( END )):::endClass
END_Assign_related_lead_to_team_lead(( END )):::endClass
END_Update_Visit_As_Assigned(( END )):::endClass


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
|Object|EGH_ShowroomVisit__c|
|Process Type| Auto Launched Flow|
|Trigger Type| Record After Save|
|Record Trigger Type| Create|
|Label|EGH Lead And Visit Showroom Assignment Flow|
|Status|Active|
|Description|Flow to assign a Lead to the appropriate Sales Consultant or the Team Leader based on Skills, Presence Status and previously assign Sales Consultant. Check if the purpose of the visit is Meet F&I Team.|
|Environments|Default|
|Interview Label|Lead And Visit Assignment Flow {!$Flow.CurrentDateTime}|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Is_created_by_Product_Genius_or_purpose_is_Event](#is_created_by_product_genius_or_purpose_is_event)|
|Next Node|[Is_created_by_Product_Genius_or_purpose_is_Event](#is_created_by_product_genius_or_purpose_is_event)|


#### Filters (logic: **or**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|EGH_LeadLookup__c| Is Null|<!-- -->|
|2|EGH_AccountLookup__c| Is Null|<!-- -->|


## Variables

|Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
|:-- |:--:|:--:|:--:|:--:|:--:|:--  |
|recordId|String|⬜|⬜|⬜|<!-- -->|Lead record Id|
|varSkillLanguage|String|⬜|⬜|⬜|<!-- -->|<!-- -->|


## Formulas

|Name|Data Type|Expression|Description|
|:-- |:--:|:-- |:--  |
|varShowroomBackupQueueName|String|'Showroom'+'_'+{!$User.Division}+'_'+'Backup'+'_'+'Queue'|<!-- -->|
|varShowroomQueueName|String|'Showroom'+'_'+{!$User.Division}+'_'+'Lead'+'_'+'Queue'|<!-- -->|


## Flow Nodes Details

### Find_Team_Leader

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Find Team Leader|
|Action Type|Apex|
|Action Name|[EGH_TeamLeaderControllerClass](../apex/EGH_TeamLeaderControllerClass.md)|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_TeamLeaderControllerClass|
|Offset|0|
|Store Output Automatically|✅|
|Record Id (input)|Get_Branch_Unit.Id|
|Connector|[Is_Showroom_Manager_Configured](#is_showroom_manager_configured)|


### Assign_Account_Language

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Account Language|
|Connector|[Routing_Omni_Flow](#routing_omni_flow)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varSkillLanguage| Assign|$Record.EGH_AccountLookup__r.EGH_ContactLanguagePicklist__pc|




### Assign_English

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign English|
|Connector|[Routing_Omni_Flow](#routing_omni_flow)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varSkillLanguage| Assign|English|




### Assign_Lead_Language

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Lead Language|
|Connector|[Routing_Omni_Flow](#routing_omni_flow)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varSkillLanguage| Assign|$Record.EGH_LeadLookup__r.EGH_LeadLanguagePicklist__c|




### Assigned_to_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned to PG ?|
|Default Connector|[Is_the_purpose_of_the_visit_Meet_F_I_Team](#is_the_purpose_of_the_visit_meet_f_i_team)|
|Default Connector Label|No|


#### Rule Yes_Skip_assigning_to_Digital_Queue (Yes Skip assigning to Digital Queue)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Update_Lead_Owner](#update_lead_owner)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$UserRole.Name| Contains|$Label.EGH_Product_Genius_Role|
|2|$Record.EGH_LeadLookup__r.EGH_AssignToPG__c| Equal To|✅|




### Copy_1_of_Visit_Related_To

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Visit Related To ?|
|Default Connector Label|Default Outcome|


#### Rule Copy_1_of_Related_to_Lead (Related to Lead)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assigned_to_PG](#assigned_to_pg)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.EGH_LeadLookup__c| Is Null|⬜|




#### Rule Copy_1_of_Related_to_Account_Opportunity (Related to Account/Opportunity)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Update_Opportunity_Owner_If_Not_Reserved](#update_opportunity_owner_if_not_reserved)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.EGH_SR_Opportunity__c| Is Null|⬜|
|2|$Record.EGH_AccountLookup__c| Is Null|⬜|




### Is_created_by_Product_Genius_or_purpose_is_Event

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Is created by Product Genius or purpose is Event or purpose is Meet F&I Team|
|Description|This check if the purpose of the visit is Event or if the Visit is created by the Product Genius or if the purpose of the visit is Meet F&I Team|
|Default Connector|[To_be_Routed](#to_be_routed)|
|Default Connector Label|No|


#### Rule Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_1_of_Visit_Related_To](#copy_1_of_visit_related_to)|
|Condition Logic|or|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$UserRole.Name| Contains|$Label.EGH_Product_Genius_Role|
|2|$Record.PurposeVisit__c| Equal To|Event|
|3|$Record.PurposeVisit__c| Equal To|Meet F&I Team|




### Is_Person_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Is Person Account ?|
|Default Connector|[Assign_English](#assign_english)|
|Default Connector Label|Default Outcome|


#### Rule Person_Account (Person Account)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Account_Language](#assign_account_language)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.EGH_AccountLookup__r.IsPersonAccount| Equal To|✅|




### Is_Showroom_Manager_Configured

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Is Showroom Manager Configured|
|Default Connector Label|Default Outcome|


#### Rule Yess (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_related_lead_to_team_lead](#assign_related_lead_to_team_lead)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Find_Team_Leader.teamLeaderId| Is Null|⬜|




### Is_the_purpose_of_the_visit_Meet_F_I_Team

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Is the purpose of the visit Meet F&I Team?|
|Description|This decision is taken if the purpose of the visit is Meet F & I team|
|Default Connector|[Get_Digital_Sales_Consultant_Queue](#get_digital_sales_consultant_queue)|
|Default Connector Label|Not F&I|


#### Rule MeetAndI (Meet F&I Team)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_F_I_Queue](#get_f_i_queue)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.PurposeVisit__c| Equal To|Meet F&I Team|




### To_be_Routed

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|To be Routed?|
|Default Connector|[Get_Branch_Unit](#get_branch_unit)|
|Default Connector Label|No|


#### Rule YesRoute (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Visit_Related_To](#visit_related_to)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.Route_to_Sales__c| Equal To|✅|




### Visit_Related_To

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Visit Related To ?|
|Default Connector Label|Default Outcome|


#### Rule Related_to_Lead (Related to Lead)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Lead_Language](#assign_lead_language)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.EGH_LeadLookup__c| Is Null|⬜|




#### Rule Related_to_Account_Opportunity (Related to Account/Opportunity)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Is_Person_Account](#is_person_account)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$Record.EGH_SR_Opportunity__c| Is Null|⬜|
|2|$Record.EGH_AccountLookup__c| Is Null|⬜|




### Get_Branch_Unit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|BranchUnit|
|Label|Get Branch Unit|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Find_Team_Leader](#find_team_leader)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Name| Equal To|$User.Division|




### Get_Digital_Sales_Consultant_Queue

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Group|
|Label|Get Digital Sales Consultant Queue|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Update_Digital_Sales_Queue_as_Owner](#update_digital_sales_queue_as_owner)|


#### Filters (logic: **1 AND 2**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Name| Starts With|Digital Sales|
|2|Type| Equal To|Queue|




### Get_F_I_Queue

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Group|
|Label|Get F & I Queue|
|Description|Get the F&I Queue for the Showroom of the visit|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Update_F_I_Queue_as_Owner](#update_f_i_queue_as_owner)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Type| Equal To|Queue|
|2|Name| Starts With|$Record.EGH_RelatedShowroomBranch__r.Name|
|3|Name| Ends With|F&I|




### Assign_related_lead_to_team_lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Label|Assign related lead to team lead|
|Input Reference|$Record.EGH_LeadLookup__r|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|$Record.EGH_LeadLookup__r.Id|




#### Input Assignments

|Field|Value|
|:-- |:--: |
|OwnerId|Find_Team_Leader.teamLeaderId|




### Update_Digital_Sales_Queue_as_Owner

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Label|Update Digital Sales Queue as Lead Owner|
|Input Reference|$Record.EGH_LeadLookup__r|
|Connector|[Update_Visit_As_Assigned](#update_visit_as_assigned)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_BranchCode__c|$Record.EGH_RelatedShowroomBranch__r.BranchCode|
|EGH_LeadBranchUnitLookup__c|$Record.EGH_RelatedShowroomBranch__c|
|OwnerId|Get_Digital_Sales_Consultant_Queue.Id|




### Update_F_I_Queue_as_Owner

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Label|Update  F & I Queue as Owner|
|Input Reference|$Record|
|Connector|[Update_Visit_As_Assigned](#update_visit_as_assigned)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|OwnerId|Get_F_I_Queue.Id|




### Update_Lead_Owner

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Label|Update Lead Owner|
|Input Reference|$Record.EGH_LeadLookup__r|
|Connector|[Update_Visit_As_Assigned](#update_visit_as_assigned)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_BranchCode__c|$Record.EGH_RelatedShowroomBranch__r.BranchCode|
|EGH_LeadBranchUnitLookup__c|$Record.EGH_RelatedShowroomBranch__c|
|OwnerId|$Record.OwnerId|




### Update_Opportunity_Owner_If_Not_Reserved

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Object|Opportunity|
|Label|Update Opportunity Owner If Not Reserved|
|Connector|[Update_Visit_As_Assigned](#update_visit_as_assigned)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|$Record.EGH_SR_Opportunity__c|
|2|StageName| Not Equal To|Closed Won|
|3|StageName| Not Equal To|Closed Lost|
|4|StageName| Not Equal To|Reserved/Pre Booked|




#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_BranchUnitLookup__c|$Record.EGH_RelatedShowroomBranch__c|
|OwnerId|$Record.OwnerId|




### Update_Visit_As_Assigned

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Label|Update Visit As Assigned|
|Input Reference|$Record|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Is_Assigned__c|✅|




### Routing_Omni_Flow

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Subflow|
|Label|Routing Omni Flow|
|Flow Name|EGH_Lead_Routing_SubFlow|
|Connector|[Update_Visit_As_Assigned](#update_visit_as_assigned)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|<!-- -->|$Record.Id|
|<!-- -->|$Record.EGH_LeadLookup__r.Id|
|<!-- -->|$Record.EGH_RelatedShowroomBranch__r.Id|
|<!-- -->|varSkillLanguage|
|<!-- -->|$Record.EGH_RelatedShowroomBranch__r.Name|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
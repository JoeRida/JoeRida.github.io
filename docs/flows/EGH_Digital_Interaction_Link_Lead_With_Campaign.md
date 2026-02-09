# EGH - Digital Interaction - Link Lead With Campaign

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
click START "#general-information" "4202995914"

Campaign_Exists{"🔀 <em></em><br/>Campaign Exists ?"}:::decisions
click Campaign_Exists "#campaign_exists" "1477365628"

Campaign_Member_Exists{"🔀 <em></em><br/>Campaign Member Exists ?"}:::decisions
click Campaign_Member_Exists "#campaign_member_exists" "3705960361"

Create_Campaign_Member[("➕ <em></em><br/>Create Campaign Member")]:::recordCreates
click Create_Campaign_Member "#create_campaign_member" "2461722598"

Get_Campaign[("🔍 <em></em><br/>Get Campaign")]:::recordLookups
click Get_Campaign "#get_campaign" "1200934449"

Get_Campaign_Member[("🔍 <em></em><br/>Get Campaign Member")]:::recordLookups
click Get_Campaign_Member "#get_campaign_member" "2980257779"

Campaign_Exists --> |"Yes"| Get_Campaign_Member
Campaign_Exists --> |"No"| END_Campaign_Exists
Campaign_Member_Exists --> |"No"| Create_Campaign_Member
Campaign_Member_Exists --> |"Yes"| END_Campaign_Member_Exists
Create_Campaign_Member --> END_Create_Campaign_Member
Get_Campaign --> Campaign_Exists
Get_Campaign_Member --> Campaign_Member_Exists
START -->  Get_Campaign
END_Campaign_Exists(( END )):::endClass
END_Campaign_Member_Exists(( END )):::endClass
END_Create_Campaign_Member(( END )):::endClass


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
|Object|EGH_Interaction__c|
|Process Type| Auto Launched Flow|
|Trigger Type| Record After Save|
|Record Trigger Type| Create|
|Label|EGH - Digital Interaction - Link Lead With Campaign|
|Status|Active|
|Environments|Default|
|Interview Label|EGH {!$Flow.CurrentDateTime}|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Get_Campaign](#get_campaign)|
|Next Node|[Get_Campaign](#get_campaign)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|EGH_UTMMarketingCampaignTextArea__c| Is Null|<!-- -->|


## Flow Nodes Details

### Campaign_Exists

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Campaign Exists ?|
|Default Connector Label|No|


#### Rule Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Campaign_Member](#get_campaign_member)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|[Get_Campaign](#get_campaign)| Is Null|⬜|




### Campaign_Member_Exists

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Campaign Member Exists ?|
|Default Connector Label|Yes|


#### Rule No (No)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_Campaign_Member](#create_campaign_member)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|[Get_Campaign_Member](#get_campaign_member)| Is Null|✅|




### Create_Campaign_Member

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|CampaignMember|
|Label|Create Campaign Member|
|Store Output Automatically|✅|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|CampaignId|Get_Campaign.Id|
|LeadId|$Record.EGH_LeadLookup__c|




### Get_Campaign

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Campaign|
|Label|Get Campaign|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Campaign_Exists](#campaign_exists)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Name| Equal To|$Record.EGH_UTMMarketingCampaignTextArea__c|




### Get_Campaign_Member

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|CampaignMember|
|Label|Get Campaign Member|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Campaign_Member_Exists](#campaign_member_exists)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|CampaignId| Equal To|Get_Campaign.Id|
|2|LeadId| Equal To|$Record.EGH_LeadLookup__c|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
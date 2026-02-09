# EGH Lead Acknowledgement Email

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
click START "#general-information" "2208276495"

Acknowledgement_Email("📧 <em></em><br/>Acknowledgement Email"):::actionCalls
click Acknowledgement_Email "#acknowledgement_email" "2137709918"

Acknowledgement_Email --> END_Acknowledgement_Email
START -->  Acknowledgement_Email
END_Acknowledgement_Email(( END )):::endClass


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
|Label|EGH Lead Acknowledgement Email|
|Status|Active|
|Filter Formula|AND(<br/>{!$Setup.EGH_Automation_Bypass__c.EGH_Bypass_Flows__c}=false,<br/>NOT(ISBLANK({!$Record.Email}))<br/>)|
|Environments|Default|
|Interview Label|EGH Lead Acknowledgement Email {!$Flow.CurrentDateTime}|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Acknowledgement_Email](#acknowledgement_email)|
|Next Node|[Acknowledgement_Email](#acknowledgement_email)|


## Flow Nodes Details

### Acknowledgement_Email

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Acknowledgement Email|
|Action Type|Email Alert|
|Action Name|Lead.EGH_New_Lead_Email_Alert|
|Description|This action would trigger the acknowledgement Email to the Lead|
|Flow Transaction Model|CurrentTransaction|
|Name Segment|Lead.EGH_New_Lead_Email_Alert|
|Offset|0|
| SObject Row Id (input)|$Record.Id|






___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
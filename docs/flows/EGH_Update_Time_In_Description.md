# EGH Update Time In Description

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>AutoLaunched Flow</b></br>Type: <b> Record After Save</b>"]):::startClass
click START "#general-information" "2871756868"

Format_Date_Time_in_User_Time_Zone("⚙️ <em></em><br/>Format Date & Time in User Time Zone"):::actionCalls
click Format_Date_Time_in_User_Time_Zone "#format_date_time_in_user_time_zone" "3304521419"

Assign_Service_Resource_name[\"🟰 <em></em><br/>Assign Service Resource name"/]:::assignments
click Assign_Service_Resource_name "#assign_service_resource_name" "1202067853"

Assign_Service_Resource_Name1[\"🟰 <em></em><br/>Assign Service Resource Name"/]:::assignments
click Assign_Service_Resource_Name1 "#assign_service_resource_name1" "905574530"

Assign_user_Time_zone[\"🟰 <em></em><br/>Assign user Time zone"/]:::assignments
click Assign_user_Time_zone "#assign_user_time_zone" "3880129516"

Check_Resource_Type{"🔀 <em></em><br/>Check Resource Type"}:::decisions
click Check_Resource_Type "#check_resource_type" "3137022615"

Loop_through_related_assigned_resource{{"🔁 <em></em><br/>Loop through related assigned resource"}}:::loops
click Loop_through_related_assigned_resource "#loop_through_related_assigned_resource" "2142454418"

Get_related_Service_Ressource[("🔍 <em></em><br/>Get related Assigned Ressource")]:::recordLookups
click Get_related_Service_Ressource "#get_related_service_ressource" "1679165205"

Get_User_Time_zone[("🔍 <em></em><br/>Get User Time zone")]:::recordLookups
click Get_User_Time_zone "#get_user_time_zone" "4221849451"

Update_Service_appointment_description[("🛠️ <em></em><br/>Update Service appointment description")]:::recordUpdates
click Update_Service_appointment_description "#update_service_appointment_description" "1565528509"

Format_Date_Time_in_User_Time_Zone --> Update_Service_appointment_description
Assign_Service_Resource_name --> Loop_through_related_assigned_resource
Assign_Service_Resource_Name1 --> Loop_through_related_assigned_resource
Assign_user_Time_zone --> Format_Date_Time_in_User_Time_Zone
Check_Resource_Type --> |"Asset"| Assign_Service_Resource_name
Check_Resource_Type --> |"Technicien"| Assign_Service_Resource_Name1
Check_Resource_Type --> |"Default Outcome"| Loop_through_related_assigned_resource
Loop_through_related_assigned_resource --> |"For Each"|Check_Resource_Type
Loop_through_related_assigned_resource ---> |"After Last"|Get_User_Time_zone
Get_related_Service_Ressource --> Loop_through_related_assigned_resource
Get_User_Time_zone --> Assign_user_Time_zone
Update_Service_appointment_description --> END_Update_Service_appointment_description
START -->  Get_related_Service_Ressource
END_Update_Service_appointment_description(( END )):::endClass


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
|Object|ServiceAppointment|
|Process Type| Auto Launched Flow|
|Trigger Type| Record After Save|
|Record Trigger Type| Update|
|Label|EGH Update Time In Description|
|Status|Active|
|Description|This flow is triggered when the Service Appointment’s Arrival Window Start or End time is changed. It uses an Apex action to format the date and time in the user’s timezone, then updates the Description field with the Date, Time, and Timezone in the correct format.|
|Environments|Default|
|Interview Label|EGH Update Time In Description {!$Flow.CurrentDateTime}|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Get_related_Service_Ressource](#get_related_service_ressource)|
|Next Node|[Get_related_Service_Ressource](#get_related_service_ressource)|


#### Filters (logic: **or**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ArrivalWindowStartTime| Is Changed|✅|
|2|ArrivalWindowEndTime| Is Changed|✅|


## Variables

|Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
|:-- |:--:|:--:|:--:|:--:|:--:|:--  |
|assignedResourceIds|String|✅|⬜|⬜|<!-- -->|<!-- -->|
|FormattedDate|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|FormattedEndTime|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|FormattedStartTime|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|ServiceResourceNameAsset|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|ServiceResourceNameTechnicien|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|userTimeZone|String|⬜|⬜|⬜|<!-- -->|<!-- -->|


## Formulas

|Name|Data Type|Expression|Description|
|:-- |:--:|:-- |:--  |
|buildTimeLine|String|"Time: " & {!FormattedStartTime} & " - " & {!FormattedEndTime}|<!-- -->|
|UpdatedDescription|String|"Test Drive Scheduled!" & BR() &<br/>"Vehicle: " & {!ServiceResourceNameAsset} & BR() &<br/>"Driver: " & {!ServiceResourceNameTechnicien} & BR() &<br/>"Date: " & {!FormattedDate} & BR() &<br/>{!buildTimeLine} & BR() & BR() &<br/>"Timezone: " & {!userTimeZone}|<!-- -->|


## Flow Nodes Details

### Format_Date_Time_in_User_Time_Zone

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Format Date & Time in User Time Zone|
|Action Type|Apex|
|Action Name|[EGH_FormatServiceAppointmentTime](../apex/EGH_FormatServiceAppointmentTime.md)|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_FormatServiceAppointmentTime|
|Offset|0|
|Output Parameters|- assignToReference: FormattedDate<br/>&nbsp;&nbsp;name: formattedDate<br/>- assignToReference: FormattedEndTime<br/>&nbsp;&nbsp;name: formattedEndTime<br/>- assignToReference: FormattedStartTime<br/>&nbsp;&nbsp;name: formattedStartTime<br/>|
|End Time (input)|$Record.ArrivalWindowEndTime|
|Start Time (input)|$Record.ArrivalWindowStartTime|
|User Time Zone (input)|userTimeZone|
|Connector|[Update_Service_appointment_description](#update_service_appointment_description)|


### Assign_Service_Resource_name

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Service Resource name|
|Connector|[Loop_through_related_assigned_resource](#loop_through_related_assigned_resource)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|ServiceResourceNameAsset| Assign|Loop_through_related_assigned_resource.ServiceResource.Name|




### Assign_Service_Resource_Name1

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Service Resource Name|
|Connector|[Loop_through_related_assigned_resource](#loop_through_related_assigned_resource)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|ServiceResourceNameTechnicien| Assign|Loop_through_related_assigned_resource.ServiceResource.Name|




### Assign_user_Time_zone

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign user Time zone|
|Connector|[Format_Date_Time_in_User_Time_Zone](#format_date_time_in_user_time_zone)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|userTimeZone| Assign|Get_User_Time_zone.TimeZoneSidKey|




### Check_Resource_Type

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Check Resource Type|
|Default Connector|[Loop_through_related_assigned_resource](#loop_through_related_assigned_resource)|
|Default Connector Label|Default Outcome|


#### Rule Asset (Asset)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Service_Resource_name](#assign_service_resource_name)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Loop_through_related_assigned_resource.ServiceResource.ResourceType| Equal To|S|




#### Rule Technicien (Technicien)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Service_Resource_Name1](#assign_service_resource_name1)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Loop_through_related_assigned_resource.ServiceResource.ResourceType| Equal To|T|




### Loop_through_related_assigned_resource

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Loop|
|Label|Loop through related assigned resource|
|Collection Reference|[Get_related_Service_Ressource](#get_related_service_ressource)|
|Iteration Order|Asc|
|Next Value Connector|[Check_Resource_Type](#check_resource_type)|
|No More Values Connector|[Get_User_Time_zone](#get_user_time_zone)|


### Get_related_Service_Ressource

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|AssignedResource|
|Label|Get related Assigned Ressource|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|⬜|
|Store Output Automatically|✅|
|Connector|[Loop_through_related_assigned_resource](#loop_through_related_assigned_resource)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ServiceAppointmentId| Equal To|$Record.Id|




### Get_User_Time_zone

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|User|
|Label|Get User Time zone|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Assign_user_Time_zone](#assign_user_time_zone)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|$User.Id|




### Update_Service_appointment_description

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Label|Update Service appointment description|
|Input Reference|$Record|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|Description|UpdatedDescription|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
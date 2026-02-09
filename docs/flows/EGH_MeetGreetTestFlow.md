# EGH Meet&Greet Flow

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>Screen Flow</b>"]):::startClass
click START "#general-information" "2541762776"

AL("⚙️ <em></em><br/>AL"):::actionCalls
click AL "#al" "2424686003"

Find_Lead_Duplicates("⚙️ <em></em><br/>Find Lead Duplicates"):::actionCalls
click Find_Lead_Duplicates "#find_lead_duplicates" "3077166001"

Find_Team_Leader("⚙️ <em></em><br/>Find Team Leader"):::actionCalls
click Find_Team_Leader "#find_team_leader" "542212617"

Get_Model_Of_Interests("⚙️ <em></em><br/>Get Model Of Interests"):::actionCalls
click Get_Model_Of_Interests "#get_model_of_interests" "526619731"

Get_Purpose_Of_Visit_Without_Event_Value("⚙️ <em></em><br/>Get Purpose Of Visit Without Event Value"):::actionCalls
click Get_Purpose_Of_Visit_Without_Event_Value "#get_purpose_of_visit_without_event_value" "1518790984"

Assign_Opportunities_Size[\"🟰 <em></em><br/>Assign Opportunities Size"/]:::assignments
click Assign_Opportunities_Size "#assign_opportunities_size" "3543491674"

Assign_Secondary_Branch_Values[\"🟰 <em></em><br/>Assign Secondary Branch Values"/]:::assignments
click Assign_Secondary_Branch_Values "#assign_secondary_branch_values" "152287899"

Assign_Selected_Branch[\"🟰 <em></em><br/>Assign Selected Branch"/]:::assignments
click Assign_Selected_Branch "#assign_selected_branch" "4136919413"

Assign_Selected_Branch_Values[\"🟰 <em></em><br/>Assign Selected Branch Values"/]:::assignments
click Assign_Selected_Branch_Values "#assign_selected_branch_values" "3540077210"

Copy_1_of_Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Copy_1_of_Set_Visit_ID "#copy_1_of_set_visit_id" "72619702"

Copy_1_of_Update_Purpose_of_Visit[\"🟰 <em></em><br/>Update Purpose of Visit"/]:::assignments
click Copy_1_of_Update_Purpose_of_Visit "#copy_1_of_update_purpose_of_visit" "2594928840"

Copy_2_of_Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Copy_2_of_Set_Visit_ID "#copy_2_of_set_visit_id" "1341288034"

Copy_2_of_UpdatePurposeOfVisit[\"🟰 <em></em><br/>UpdatePurposeOfVisit"/]:::assignments
click Copy_2_of_UpdatePurposeOfVisit "#copy_2_of_updatepurposeofvisit" "2746910189"

Copy_3_of_Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Copy_3_of_Set_Visit_ID "#copy_3_of_set_visit_id" "4216512819"

Copy_4_of_Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Copy_4_of_Set_Visit_ID "#copy_4_of_set_visit_id" "1835867404"

Count_Opportunities[\"🟰 <em></em><br/>Count Opportunities"/]:::assignments
click Count_Opportunities "#count_opportunities" "630704927"

Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Set_Visit_ID "#set_visit_id" "83193006"

setLeadIDArtLeasing[\"🟰 <em></em><br/>setLeadIDArtLeasing"/]:::assignments
click setLeadIDArtLeasing "#setleadidartleasing" "3156224869"

setLeadIDEliteCars[\"🟰 <em></em><br/>setLeadIDEliteCars"/]:::assignments
click setLeadIDEliteCars "#setleadidelitecars" "991327211"

setLeadIDJetour[\"🟰 <em></em><br/>setLeadIDJetour"/]:::assignments
click setLeadIDJetour "#setleadidjetour" "2783407187"

setLeadIDSoueast[\"🟰 <em></em><br/>setLeadIDSoueast"/]:::assignments
click setLeadIDSoueast "#setleadidsoueast" "1479417637"

Update_Purpose_of_Visit[\"🟰 <em></em><br/>Update Purpose of Visit"/]:::assignments
click Update_Purpose_of_Visit "#update_purpose_of_visit" "478641246"

UpdatePurposeOfVisit[\"🟰 <em></em><br/>UpdatePurposeOfVisit"/]:::assignments
click UpdatePurposeOfVisit "#updatepurposeofvisit" "4030795603"

varVisitIDSet[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click varVisitIDSet "#varvisitidset" "1102380205"

Branch_Division_Type{"🔀 <em></em><br/>Branch/Division Type"}:::decisions
click Branch_Division_Type "#branch_division_type" "3855161871"

Decision_1{"🔀 <em></em><br/>Exists Lead or Customer?"}:::decisions
click Decision_1 "#decision_1" "1809077523"

Existing_Lead_Found{"🔀 <em></em><br/>Existing Lead Found"}:::decisions
click Existing_Lead_Found "#existing_lead_found" "1235834727"

Is_Showroom_Manager_Configured{"🔀 <em></em><br/>Is Showroom Manager Configured"}:::decisions
click Is_Showroom_Manager_Configured "#is_showroom_manager_configured" "4258896280"

is_Single_Account{"🔀 <em></em><br/>is Single Account?"}:::decisions
click is_Single_Account "#is_single_account" "742991983"

is_SIngle_lead{"🔀 <em></em><br/>is Single lead"}:::decisions
click is_SIngle_lead "#is_single_lead" "939017021"

Multiple_Leads_Accounts_Chosen{"🔀 <em></em><br/>Multiple Leads/Accounts Chosen"}:::decisions
click Multiple_Leads_Accounts_Chosen "#multiple_leads_accounts_chosen" "2135268560"

New_Lead{"🔀 <em></em><br/>New Lead ?"}:::decisions
click New_Lead "#new_lead" "3062088518"

Secondary_Branch_Exist{"🔀 <em></em><br/>Secondary Branch Exist ?"}:::decisions
click Secondary_Branch_Exist "#secondary_branch_exist" "2951631410"

Showroom_Changed{"🔀 <em></em><br/>Showroom Changed ?"}:::decisions
click Showroom_Changed "#showroom_changed" "969937900"

Showroom_Has_Valid_Brand{"🔀 <em></em><br/>Showroom Has Valid Brand ?"}:::decisions
click Showroom_Has_Valid_Brand "#showroom_has_valid_brand" "3168805888"

Showroom_Skill_Found{"🔀 <em></em><br/>Showroom Skill Found"}:::decisions
click Showroom_Skill_Found "#showroom_skill_found" "937543101"

User_has_Branch{"🔀 <em></em><br/>User has Branch?"}:::decisions
click User_has_Branch "#user_has_branch" "3157193172"

Create_Account_Visit[("➕ <em></em><br/>Create Account Visit")]:::recordCreates
click Create_Account_Visit "#create_account_visit" "1889254355"

Create_Lead_Visit[("➕ <em></em><br/>Create Lead Visit")]:::recordCreates
click Create_Lead_Visit "#create_lead_visit" "669349604"

Create_New_Lead_ArtLeasing[("➕ <em></em><br/>Create New Lead ArtLeasing")]:::recordCreates
click Create_New_Lead_ArtLeasing "#create_new_lead_artleasing" "133594639"

Create_New_Lead_EliteCars[("➕ <em></em><br/>Create New Lead EliteCars")]:::recordCreates
click Create_New_Lead_EliteCars "#create_new_lead_elitecars" "4149725081"

Create_New_Lead_Jetour[("➕ <em></em><br/>Create New Lead Jetour")]:::recordCreates
click Create_New_Lead_Jetour "#create_new_lead_jetour" "1139698348"

Create_Note[("➕ <em></em><br/>Create Note")]:::recordCreates
click Create_Note "#create_note" "480042539"

Create_Visit[("➕ <em></em><br/>Create Visit")]:::recordCreates
click Create_Visit "#create_visit" "2945963378"

Create_Visit_for_Existing_Lead[("➕ <em></em><br/>Create Visit for Existing Lead")]:::recordCreates
click Create_Visit_for_Existing_Lead "#create_visit_for_existing_lead" "2123159731"

Create_Visit_for_Selected_Account[("➕ <em></em><br/>Create Visit for Selected Account")]:::recordCreates
click Create_Visit_for_Selected_Account "#create_visit_for_selected_account" "836198103"

Create_Visit_for_Selected_Lead[("➕ <em></em><br/>Create Visit for  Selected Lead")]:::recordCreates
click Create_Visit_for_Selected_Lead "#create_visit_for_selected_lead" "1411076734"

CreateNewLeadSoueast[("➕ <em></em><br/>Create New Lead Soueast")]:::recordCreates
click CreateNewLeadSoueast "#createnewleadsoueast" "1692150740"

Get_Branch_Unit[("🔍 <em></em><br/>Get Branch Unit")]:::recordLookups
click Get_Branch_Unit "#get_branch_unit" "4231862154"

Get_Brand_by_Parent_Branch_Name[("🔍 <em></em><br/>Get Brand by Parent Branch Name")]:::recordLookups
click Get_Brand_by_Parent_Branch_Name "#get_brand_by_parent_branch_name" "3972039604"

Get_Opportunities_Related_to_Account[("🔍 <em></em><br/>Get Opportunities Related to Account")]:::recordLookups
click Get_Opportunities_Related_to_Account "#get_opportunities_related_to_account" "1000324052"

Get_Opportunities_Related_to_Account_Selected[("🔍 <em></em><br/>Get Opportunities Related to Account Selected")]:::recordLookups
click Get_Opportunities_Related_to_Account_Selected "#get_opportunities_related_to_account_selected" "1559738377"

Get_SA_Related_to_Account_Selected[("🔍 <em></em><br/>Get SA Related to Account Selected")]:::recordLookups
click Get_SA_Related_to_Account_Selected "#get_sa_related_to_account_selected" "3166178646"

Get_Selected_Existing_Lead[("🔍 <em></em><br/>Get Selected Existing Lead")]:::recordLookups
click Get_Selected_Existing_Lead "#get_selected_existing_lead" "868706622"

Get_Selected_Showroom[("🔍 <em></em><br/>Get Selected Showroom")]:::recordLookups
click Get_Selected_Showroom "#get_selected_showroom" "929578787"

Get_Service_Appointments_Related_to_Existing_Lead[("🔍 <em></em><br/>Get Service Appointments Related to Existing Lead")]:::recordLookups
click Get_Service_Appointments_Related_to_Existing_Lead "#get_service_appointments_related_to_existing_lead" "3659267378"

Get_Service_Appointments_Related_to_Lead[("🔍 <em></em><br/>Get Service Appointments Related to Lead Selected")]:::recordLookups
click Get_Service_Appointments_Related_to_Lead "#get_service_appointments_related_to_lead" "4232846390"

Get_Service_Appointmets_Related_to_Account[("🔍 <em></em><br/>Get Service Appointmets Related to Account")]:::recordLookups
click Get_Service_Appointmets_Related_to_Account "#get_service_appointmets_related_to_account" "2239743721"

Get_Service_Appointmets_Related_to_Lead[("🔍 <em></em><br/>Get Service Appointmets Related to Lead")]:::recordLookups
click Get_Service_Appointmets_Related_to_Lead "#get_service_appointmets_related_to_lead" "345783594"

Get_Showroom_Skill[("🔍 <em></em><br/>Get Showroom Skill")]:::recordLookups
click Get_Showroom_Skill "#get_showroom_skill" "3023191589"

Get_User_Secondary_Branch[("🔍 <em></em><br/>Get User Secondary Branch")]:::recordLookups
click Get_User_Secondary_Branch "#get_user_secondary_branch" "216333016"

Customer_Information_Capture_Form(["💻 <em></em><br/>Customer Information Capture Form"]):::screens
click Customer_Information_Capture_Form "#customer_information_capture_form" "743379162"

Customer_Search(["💻 <em></em><br/>Customer Search"]):::screens
click Customer_Search "#customer_search" "2390775286"

Error_Message(["💻 <em></em><br/>Error Message"]):::screens
click Error_Message "#error_message" "3717706518"

Existing_Lead_Details(["💻 <em></em><br/>Existing Lead Details"]):::screens
click Existing_Lead_Details "#existing_lead_details" "2948652853"

Existing_Leads_Screen(["💻 <em></em><br/>Existing Leads Screen"]):::screens
click Existing_Leads_Screen "#existing_leads_screen" "936335621"

Invalid_Brand(["💻 <em></em><br/>Invalid Brand"]):::screens
click Invalid_Brand "#invalid_brand" "1412639257"

Invalid_Brand_Screen(["💻 <em></em><br/>Invalid Brand Screen"]):::screens
click Invalid_Brand_Screen "#invalid_brand_screen" "402739403"

List_of_Customers(["💻 <em></em><br/>List of Customers"]):::screens
click List_of_Customers "#list_of_customers" "2019358190"

loader(["💻 <em></em><br/>loader"]):::screens
click loader "#loader" "2582155801"

opportunityListSecondScreen(["💻 <em></em><br/>opportunityListSecondScreen"]):::screens
click opportunityListSecondScreen "#opportunitylistsecondscreen" "3762333576"

Pre_Validations(["💻 <em></em><br/>Pre Validations"]):::screens
click Pre_Validations "#pre_validations" "3655380063"

serviceAppointmentSecondScreen(["💻 <em></em><br/>serviceAppointmentSecondScreen"]):::screens
click serviceAppointmentSecondScreen "#serviceappointmentsecondscreen" "3598016707"

Get_Lead_Ownersubflow[["🔗 <em>Subflow</em><br/>Get Lead Owner"]]:::subflows
click Get_Lead_Ownersubflow "#get_lead_ownersubflow" "3427292352"

AL --> Decision_1
Find_Lead_Duplicates --> Existing_Lead_Found
Find_Team_Leader --> Is_Showroom_Manager_Configured
Get_Model_Of_Interests --> Get_Purpose_Of_Visit_Without_Event_Value
Get_Purpose_Of_Visit_Without_Event_Value --> Customer_Search
Assign_Opportunities_Size --> Get_Service_Appointmets_Related_to_Account
Assign_Secondary_Branch_Values --> Get_Brand_by_Parent_Branch_Name
Assign_Selected_Branch --> Get_User_Secondary_Branch
Assign_Selected_Branch_Values --> Get_Brand_by_Parent_Branch_Name
Copy_1_of_Set_Visit_ID --> loader
Copy_1_of_Update_Purpose_of_Visit --> Create_Visit_for_Existing_Lead
Copy_2_of_Set_Visit_ID --> loader
Copy_2_of_UpdatePurposeOfVisit --> Create_Visit_for_Selected_Account
Copy_3_of_Set_Visit_ID --> loader
Copy_4_of_Set_Visit_ID --> loader
Count_Opportunities --> opportunityListSecondScreen
Set_Visit_ID --> loader
setLeadIDArtLeasing --> Create_Note
setLeadIDEliteCars --> Create_Note
setLeadIDJetour --> Create_Note
setLeadIDSoueast --> Create_Note
Update_Purpose_of_Visit --> Create_Visit_for_Selected_Lead
UpdatePurposeOfVisit --> Multiple_Leads_Accounts_Chosen
varVisitIDSet --> loader
Branch_Division_Type --> |"Brand Jetour"| Create_New_Lead_Jetour
Branch_Division_Type --> |"Brand Soueast"| CreateNewLeadSoueast
Branch_Division_Type --> |"Brand EliteCars"| Create_New_Lead_EliteCars
Branch_Division_Type --> |"Brand ArtLeasing"| Create_New_Lead_ArtLeasing
Branch_Division_Type --> |"Default Outcome"| Invalid_Brand
Decision_1 --> |"Yes"| is_SIngle_lead
Decision_1 --> |"No"| Customer_Information_Capture_Form
Existing_Lead_Found --> |"No"| Branch_Division_Type
Existing_Lead_Found --> |"Default Outcome"| Existing_Leads_Screen
Is_Showroom_Manager_Configured --> |"Yes"| Get_Showroom_Skill
Is_Showroom_Manager_Configured --> |"No Showroom Manager Found"| Pre_Validations
is_Single_Account --> |"yes"| Get_Opportunities_Related_to_Account
is_Single_Account --> |"Default Outcome"| List_of_Customers
is_SIngle_lead --> |"yes"| Get_Service_Appointmets_Related_to_Lead
is_SIngle_lead --> |"Default Outcome"| is_Single_Account
Multiple_Leads_Accounts_Chosen --> |"New Lead Checked"| Customer_Information_Capture_Form
Multiple_Leads_Accounts_Chosen --> |"Lead Selected from Multiple Lead"| Get_Service_Appointments_Related_to_Lead
Multiple_Leads_Accounts_Chosen --> |"Account Selected from Multiple Account"| Get_SA_Related_to_Account_Selected
Multiple_Leads_Accounts_Chosen --> |"Single Lead Selected"| Create_Lead_Visit
Multiple_Leads_Accounts_Chosen --> |"Single Account Selected"| Create_Account_Visit
Multiple_Leads_Accounts_Chosen --> |"Default Outcome"| END_Multiple_Leads_Accounts_Chosen
New_Lead --> |"New Lead Clicked"| Customer_Information_Capture_Form
New_Lead --> |"Default Outcome"| AL
Secondary_Branch_Exist --> |"Secondary Branch Exist"| Assign_Secondary_Branch_Values
Secondary_Branch_Exist --> |"Secondary Branch Does Not Exist"| Get_Brand_by_Parent_Branch_Name
Showroom_Changed --> |"Changed"| Get_Selected_Showroom
Showroom_Changed --> |"Not Changed"| New_Lead
Showroom_Has_Valid_Brand --> |"Valid Brand"| Find_Team_Leader
Showroom_Has_Valid_Brand --> |"Invalid Brand"| Invalid_Brand_Screen
Showroom_Skill_Found --> |"Yes"| Get_Model_Of_Interests
Showroom_Skill_Found --> |"Showroom Skill Not Found"| Pre_Validations
User_has_Branch --> |"Yes"| Assign_Selected_Branch
User_has_Branch --> |"No Branch"| Pre_Validations
Create_Account_Visit --> Copy_2_of_Set_Visit_ID
Create_Lead_Visit --> Copy_1_of_Set_Visit_ID
Create_New_Lead_ArtLeasing --> setLeadIDArtLeasing
Create_New_Lead_ArtLeasing -. Fault .->Error_Message
Create_New_Lead_EliteCars --> setLeadIDEliteCars
Create_New_Lead_EliteCars -. Fault .->Error_Message
Create_New_Lead_Jetour --> setLeadIDJetour
Create_New_Lead_Jetour -. Fault .->Error_Message
Create_Note --> Create_Visit
Create_Note -. Fault .->Error_Message
Create_Visit --> Copy_3_of_Set_Visit_ID
Create_Visit -. Fault .->Error_Message
Create_Visit_for_Existing_Lead --> Copy_4_of_Set_Visit_ID
Create_Visit_for_Selected_Account --> Set_Visit_ID
Create_Visit_for_Selected_Lead --> varVisitIDSet
CreateNewLeadSoueast --> setLeadIDSoueast
CreateNewLeadSoueast -. Fault .->Error_Message
Get_Branch_Unit --> User_has_Branch
Get_Brand_by_Parent_Branch_Name --> Showroom_Has_Valid_Brand
Get_Opportunities_Related_to_Account --> Assign_Opportunities_Size
Get_Opportunities_Related_to_Account_Selected --> Count_Opportunities
Get_SA_Related_to_Account_Selected --> Get_Opportunities_Related_to_Account_Selected
Get_Selected_Existing_Lead --> Existing_Lead_Details
Get_Selected_Showroom --> Assign_Selected_Branch_Values
Get_Service_Appointments_Related_to_Existing_Lead --> Get_Selected_Existing_Lead
Get_Service_Appointments_Related_to_Lead --> serviceAppointmentSecondScreen
Get_Service_Appointmets_Related_to_Account --> List_of_Customers
Get_Service_Appointmets_Related_to_Lead --> is_Single_Account
Get_Showroom_Skill --> Showroom_Skill_Found
Get_User_Secondary_Branch --> Secondary_Branch_Exist
Customer_Information_Capture_Form --> Find_Lead_Duplicates
Customer_Search --> Showroom_Changed
Error_Message --> END_Error_Message
Existing_Lead_Details --> Copy_1_of_Update_Purpose_of_Visit
Existing_Leads_Screen --> Get_Service_Appointments_Related_to_Existing_Lead
Invalid_Brand --> END_Invalid_Brand
Invalid_Brand_Screen --> END_Invalid_Brand_Screen
List_of_Customers --> UpdatePurposeOfVisit
loader --> Get_Lead_Ownersubflow
opportunityListSecondScreen --> Copy_2_of_UpdatePurposeOfVisit
Pre_Validations --> END_Pre_Validations
serviceAppointmentSecondScreen --> Update_Purpose_of_Visit
START -->  Get_Branch_Unit
Get_Lead_Ownersubflow --> END_Get_Lead_Ownersubflow
END_Multiple_Leads_Accounts_Chosen(( END )):::endClass
END_Error_Message(( END )):::endClass
END_Invalid_Brand(( END )):::endClass
END_Invalid_Brand_Screen(( END )):::endClass
END_Pre_Validations(( END )):::endClass
END_Get_Lead_Ownersubflow(( END )):::endClass


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
|Process Type| Flow|
|Label|EGH Meet&Greet Flow|
|Status|Active|
|Description|Test Flow for Meet&Greet Application. To use in discussion with Irshad|
|Environments|Default|
|Interview Label|EGH Meet&GreetTest Flow {!$Flow.CurrentDateTime}|
|Run In Mode| System Mode Without Sharing|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Get_Branch_Unit](#get_branch_unit)|
|Next Node|[Get_Branch_Unit](#get_branch_unit)|


## Variables

|Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
|:-- |:--:|:--:|:--:|:--:|:--:|:--  |
|BranchSpecificOpportunities|SObject|✅|⬜|⬜|Opportunity|<!-- -->|
|BranchSpecificOpportunitiesCount|Number|⬜|⬜|⬜|<!-- -->|<!-- -->|
|brandDependentModels|String|✅|⬜|⬜|<!-- -->|<!-- -->|
|currentItem_Filter_Branch_Specific_Opportunities|SObject|⬜|⬜|⬜|Opportunity|<!-- -->|
|currentItem_Filter_Division_Opportunities|SObject|⬜|⬜|⬜|Opportunity|<!-- -->|
|DependentPicklistValues|Apex|✅|⬜|⬜|<!-- -->|<!-- -->|
|FilteredPicklistValues|Apex|✅|⬜|⬜|<!-- -->|<!-- -->|
|ListLeads|SObject|✅|⬜|⬜|Lead|List of Leads from the search|
|PotentialDuplicateInDifferentBranch|Boolean|⬜|⬜|⬜|<!-- -->|<!-- -->|
|PrimaryBranchId|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|PrimaryBranchName|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|recordId|String|⬜|✅|⬜|<!-- -->|<!-- -->|
|SecondaryBranchID|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|SecondaryBranchName|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|SelectedBranchCode|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|SelectedBranchId|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|SelectedBranchName|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|SelectedBranchParentName|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|selectedBrand|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|test|String|⬜|✅|⬜|<!-- -->|<!-- -->|
|UserShowrooms|String|✅|⬜|⬜|<!-- -->|<!-- -->|
|varExistingLeads|SObject|✅|⬜|⬜|Lead|<!-- -->|
|varNewLeadID|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|varOpportunityListRelatedtoAccount|SObject|✅|⬜|⬜|Opportunity|<!-- -->|
|varOpportunityListRelatedtoAccountSize|Number|⬜|⬜|⬜|<!-- -->|<!-- -->|
|varOpportunityListSecondScreen|SObject|✅|⬜|⬜|Opportunity|<!-- -->|
|varPersonAccount|SObject|⬜|⬜|⬜|Account|<!-- -->|
|varPurposeOfVisit|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|varServiceAppointmentAccountSecondScreen|SObject|✅|⬜|⬜|ServiceAppointment|<!-- -->|
|varServiceAppointmentListSecondscreen|SObject|✅|⬜|⬜|ServiceAppointment|<!-- -->|
|varServiceAppointmentRelatedToAccount|SObject|✅|⬜|⬜|ServiceAppointment|<!-- -->|
|varServiceAppointmentRelatedtoLead|SObject|✅|⬜|⬜|ServiceAppointment|<!-- -->|
|varSingleLead|SObject|⬜|⬜|⬜|Lead|<!-- -->|
|varSingleOpportunity|SObject|⬜|⬜|⬜|Opportunity|<!-- -->|
|varVisitID|String|⬜|⬜|⬜|<!-- -->|<!-- -->|


## Formulas

|Name|Data Type|Expression|Description|
|:-- |:--:|:-- |:--  |
|BrandListFormula|String|CASE({!SelectedBranchParentName}, <br/>    {!$Label.EGH_Jetour} , "Jetour",<br/>    {!$Label.EGH_Soueast2}, "Soueast",<br/>    {!$Label.EGH_Soueast}, "Soueast",<br/>    {!$Label.EGH_EliteCarsAUH}, "Jetour",<br/>    {!$Label.EGH_EliteCarsTEC}, "Elite",<br/>    {!$Label.EGH_Artleasing}, "ArtLeasing",<br/>    "INVALID BRAND"<br/>)|<!-- -->|
|userRole|String|{!$UserRole.DeveloperName}|<!-- -->|
|varEndDateTime|DateTime|NOW() + (30 / 1440)|<!-- -->|
|varExistOpportunity|Boolean|IF({!Get_Opportunities_Related_to_Account}, true, false)|<!-- -->|
|varExistServiceApoointment|Boolean|IF({!Get_Service_Appointmets_Related_to_Lead}, true, false)|<!-- -->|
|varleadSource|String|IF({!$UserRole.Name}=='Product Genius','Event','Walk-In')|<!-- -->|
|varStartDateTime|DateTime|NOW()|<!-- -->|
|varVisitNameAccountSingle|String|"Visit for " + {!AL.accountSingle.Name}+" on " +TEXT(NOW())|<!-- -->|
|varVisitNameExistingLead|String|"Visit for " +{!ExistingLeadsDataTable.firstSelectedRow.Name}+" on " +TEXT(NOW())|<!-- -->|
|varVisitNameLeadSingle|String|"Visit for " + {!AL.leadSingle.Name}+" on " +TEXT(NOW())|<!-- -->|
|varVisitNameMuletipleLead|String|"Visit for " +{!leadCustomTable.outputSelectedRow.Name}+" on " +TEXT(NOW())|<!-- -->|
|varVisitNameMultipleCustomer|String|"Visit for " +{!customerCustomTable.outputSelectedRow.Name}+" on " +TEXT(NOW())|<!-- -->|
|varVisitNameNewCustomer|String|"Visit for " + {!Copy_1_of_First_Name}+" "+{!Copy_1_of_Last_Name}+" on " +TEXT(NOW())|<!-- -->|


## Flow Nodes Details

### AL

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|[AL](#al)|
|Action Type|Apex|
|Action Name|[EGH_MeetGreetSearchControllerClass](../apex/EGH_MeetGreetSearchControllerClass.md)|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_MeetGreetSearchControllerClass|
|Offset|0|
|Store Output Automatically|✅|
|Brand (input)|selectedBrand|
|Search String (input)|Search|
|User Division (input)|$User.Division|
|Connector|[Decision_1](#decision_1)|


### Find_Lead_Duplicates

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Find Lead Duplicates|
|Action Type|Apex|
|Action Name|[EGH_LeadFindDuplicates](../apex/EGH_LeadFindDuplicates.md)|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_LeadFindDuplicates|
|Offset|0|
|Store Output Automatically|✅|
|Brand (input)|BrandList2|
|Email (input)|Copy_1_of_Email.value|
|First Name (input)|Copy_1_of_First_Name|
|Last Name (input)|Copy_1_of_Last_Name|
|Mobile Phone (input)|MobileNumber.value|
|Connector|[Existing_Lead_Found](#existing_lead_found)|


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
|Record Id (input)|SelectedBranchId|
|Connector|[Is_Showroom_Manager_Configured](#is_showroom_manager_configured)|


### Get_Model_Of_Interests

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Get Model Of Interests|
|Action Type|Apex|
|Action Name|[EGH_GetDependentPicklistValues](../apex/EGH_GetDependentPicklistValues.md)|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_GetDependentPicklistValues|
|Offset|0|
|Output Parameters|assignToReference: DependentPicklistValues<br/>name: output<br/>|
|Controlling Value (input)|selectedBrand|
|Dependent Field A P I Name (input)|EGH_Model_of_Interest__c|
|Object A P I Name (input)|Lead|
|Connector|[Get_Purpose_Of_Visit_Without_Event_Value](#get_purpose_of_visit_without_event_value)|


### Get_Purpose_Of_Visit_Without_Event_Value

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Get Purpose Of Visit Without Event Value|
|Action Type|Apex|
|Action Name|EGH_GetFilteredPicklistValues|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_GetFilteredPicklistValues|
|Offset|0|
|Output Parameters|assignToReference: FilteredPicklistValues<br/>name: output<br/>|
|Excluded Values (input)|Event|
|Object A P I Name (input)|EGH_ShowroomVisit__c|
|Picklist A P I Name (input)|PurposeVisit__c|
|Connector|[Customer_Search](#customer_search)|


### Assign_Opportunities_Size

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Opportunities Size|
|Connector|[Get_Service_Appointmets_Related_to_Account](#get_service_appointmets_related_to_account)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varOpportunityListRelatedtoAccountSize| Assign Count|varOpportunityListRelatedtoAccount|




### Assign_Secondary_Branch_Values

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Secondary Branch Values|
|Connector|[Get_Brand_by_Parent_Branch_Name](#get_brand_by_parent_branch_name)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|SecondaryBranchName| Assign|Get_User_Secondary_Branch.BranchUnit.Name|
|SecondaryBranchID| Assign|Get_User_Secondary_Branch.BranchUnitId|
|UserShowrooms| Add|SecondaryBranchName|




### Assign_Selected_Branch

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Selected Branch|
|Connector|[Get_User_Secondary_Branch](#get_user_secondary_branch)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|SelectedBranchName| Assign|Get_Branch_Unit.Name|
|SelectedBranchId| Assign|Get_Branch_Unit.Id|
|SelectedBranchParentName| Assign|Get_Branch_Unit.ParentBranchUnit.Name|
|SelectedBranchCode| Assign|Get_Branch_Unit.BranchCode|
|UserShowrooms| Add|SelectedBranchName|




### Assign_Selected_Branch_Values

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Selected Branch Values|
|Connector|isGoTo: true<br/>targetReference: Get_Brand_by_Parent_Branch_Name<br/>|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|SelectedBranchId| Assign|Get_Selected_Showroom.Id|
|SelectedBranchName| Assign|Get_Selected_Showroom.Name|
|SelectedBranchParentName| Assign|Get_Selected_Showroom.ParentBranchUnit.Name|
|SelectedBranchCode| Assign|Get_Selected_Showroom.BranchCode|




### Copy_1_of_Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[loader](#loader)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Lead_Visit](#create_lead_visit)|




### Copy_1_of_Update_Purpose_of_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Update Purpose of Visit|
|Connector|[Create_Visit_for_Existing_Lead](#create_visit_for_existing_lead)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varPurposeOfVisit| Assign|ExistingLead_Purpose_of_Visit|




### Copy_2_of_Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[loader](#loader)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Account_Visit](#create_account_visit)|




### Copy_2_of_UpdatePurposeOfVisit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[UpdatePurposeOfVisit](#updatepurposeofvisit)|
|Connector|[Create_Visit_for_Selected_Account](#create_visit_for_selected_account)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varPurposeOfVisit| Assign|Purpose_of_Visit_v|




### Copy_3_of_Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[loader](#loader)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Visit](#create_visit)|




### Copy_4_of_Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[loader](#loader)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Visit_for_Existing_Lead](#create_visit_for_existing_lead)|




### Count_Opportunities

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Count Opportunities|
|Connector|[opportunityListSecondScreen](#opportunitylistsecondscreen)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|BranchSpecificOpportunitiesCount| Assign Count|varOpportunityListSecondScreen|




### Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[loader](#loader)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Visit_for_Selected_Account](#create_visit_for_selected_account)|




### setLeadIDArtLeasing

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDArtLeasing](#setleadidartleasing)|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[Create_New_Lead_ArtLeasing](#create_new_lead_artleasing)|




### setLeadIDEliteCars

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDEliteCars](#setleadidelitecars)|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[Create_New_Lead_EliteCars](#create_new_lead_elitecars)|




### setLeadIDJetour

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDJetour](#setleadidjetour)|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[Create_New_Lead_Jetour](#create_new_lead_jetour)|




### setLeadIDSoueast

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDSoueast](#setleadidsoueast)|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[CreateNewLeadSoueast](#createnewleadsoueast)|




### Update_Purpose_of_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Update Purpose of Visit|
|Connector|[Create_Visit_for_Selected_Lead](#create_visit_for_selected_lead)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varPurposeOfVisit| Assign|Purpose_Of_Visit_SecondScreen|




### UpdatePurposeOfVisit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[UpdatePurposeOfVisit](#updatepurposeofvisit)|
|Connector|[Multiple_Leads_Accounts_Chosen](#multiple_leads_accounts_chosen)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varPurposeOfVisit| Assign|Purpose_Of_Visit|




### varVisitIDSet

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[loader](#loader)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Visit_for_Selected_Lead](#create_visit_for_selected_lead)|




### Branch_Division_Type

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Branch/Division Type|
|Default Connector|[Invalid_Brand](#invalid_brand)|
|Default Connector Label|Default Outcome|


#### Rule Brand_Jetour (Brand Jetour)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_New_Lead_Jetour](#create_new_lead_jetour)|
|Condition Logic|or|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|selectedBrand| Equal To|Jetour|




#### Rule Brand_Soueast (Brand Soueast)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[CreateNewLeadSoueast](#createnewleadsoueast)|
|Condition Logic|or|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|selectedBrand| Equal To|Soueast|




#### Rule Brand_EliteCars (Brand EliteCars)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_New_Lead_EliteCars](#create_new_lead_elitecars)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|selectedBrand| Equal To|Elite|




#### Rule Brand_ArtLeasing (Brand ArtLeasing)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_New_Lead_ArtLeasing](#create_new_lead_artleasing)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|selectedBrand| Equal To|ArtLeasing|




### Decision_1

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Exists Lead or Customer?|
|Description|Validate if a Lead or Customer with these data exists|
|Default Connector|[Customer_Information_Capture_Form](#customer_information_capture_form)|
|Default Connector Label|No|


#### Rule Outcome_1_of_Decision_1 (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[is_SIngle_lead](#is_single_lead)|
|Condition Logic|or|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AL.leadSize| Greater Than|numberValue: 0<br/>|
|2|AL.accountSize| Greater Than|numberValue: 0<br/>|




### Existing_Lead_Found

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Existing Lead Found|
|Default Connector|[Existing_Leads_Screen](#existing_leads_screen)|
|Default Connector Label|Default Outcome|


#### Rule No (No)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Branch_Division_Type](#branch_division_type)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Find_Lead_Duplicates.leadMatchRecordSize| Equal To|numberValue: 0<br/>|




### Is_Showroom_Manager_Configured

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Is Showroom Manager Configured|
|Default Connector|[Pre_Validations](#pre_validations)|
|Default Connector Label|No Showroom Manager Found|


#### Rule YesShowroomManager (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Showroom_Skill](#get_showroom_skill)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Find_Team_Leader.teamLeaderId| Is Null|⬜|




### is_Single_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|is Single Account?|
|Default Connector|[List_of_Customers](#list_of_customers)|
|Default Connector Label|Default Outcome|


#### Rule yesSingleAccount (yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Opportunities_Related_to_Account](#get_opportunities_related_to_account)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AL.accountSize| Equal To|1|




### is_SIngle_lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|is Single lead|
|Default Connector|[is_Single_Account](#is_single_account)|
|Default Connector Label|Default Outcome|


#### Rule yesSingleLead (yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Service_Appointmets_Related_to_Lead](#get_service_appointmets_related_to_lead)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AL.leadSize| Equal To|1|




### Multiple_Leads_Accounts_Chosen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Multiple Leads/Accounts Chosen|
|Default Connector Label|Default Outcome|


#### Rule New_Lead_Checked (New Lead Checked)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|isGoTo: true<br/>targetReference: Customer_Information_Capture_Form<br/>|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|NewLeadButton2.wasButtonClicked| Equal To|✅|




#### Rule Lead_Selected_from_Multiple_Lead (Lead Selected from Multiple Lead)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Service_Appointments_Related_to_Lead](#get_service_appointments_related_to_lead)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|leadCustomTable.numberOfRowsSelected| Greater Than|numberValue: 0<br/>|




#### Rule Account_Selected_from_Multiple_Account (Account Selected from Multiple Account)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_SA_Related_to_Account_Selected](#get_sa_related_to_account_selected)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|customerCustomTable.numberOfRowsSelected| Greater Than|numberValue: 0<br/>|




#### Rule Single_Lead_Selected (Single Lead Selected)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_Lead_Visit](#create_lead_visit)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Create_visit_for_this_customer_Lead| Equal To|✅|




#### Rule Single_Account_Selected (Single Account Selected)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_Account_Visit](#create_account_visit)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Create_visit_for_this_customer_account| Equal To|✅|




### New_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|New Lead ?|
|Default Connector|[AL](#al)|
|Default Connector Label|Default Outcome|


#### Rule New_Lead_Clicked (New Lead Clicked)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|isGoTo: true<br/>targetReference: Customer_Information_Capture_Form<br/>|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|NewLeadButton.wasButtonClicked| Equal To|✅|




### Secondary_Branch_Exist

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Secondary Branch Exist ?|
|Default Connector|[Get_Brand_by_Parent_Branch_Name](#get_brand_by_parent_branch_name)|
|Default Connector Label|Secondary Branch Does Not Exist|


#### Rule Secondary_Branch_Exists (Secondary Branch Exist)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Secondary_Branch_Values](#assign_secondary_branch_values)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|[Get_User_Secondary_Branch](#get_user_secondary_branch)| Is Null|⬜|




### Showroom_Changed

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Showroom Changed ?|
|Default Connector|[New_Lead](#new_lead)|
|Default Connector Label|Not Changed|


#### Rule Changed (Changed)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Selected_Showroom](#get_selected_showroom)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|ShowroomsPicker.wasShowroomChanged| Equal To|✅|




### Showroom_Has_Valid_Brand

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Showroom Has Valid Brand ?|
|Default Connector|[Invalid_Brand_Screen](#invalid_brand_screen)|
|Default Connector Label|Invalid Brand|


#### Rule Valid_Brand (Valid Brand)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Find_Team_Leader](#find_team_leader)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|selectedBrand| Is Null|⬜|




### Showroom_Skill_Found

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Showroom Skill Found|
|Default Connector|[Pre_Validations](#pre_validations)|
|Default Connector Label|Showroom Skill Not Found|


#### Rule YesShowrromSkill (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Model_Of_Interests](#get_model_of_interests)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Get_Showroom_Skill.Id| Is Null|⬜|




### User_has_Branch

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|User has Branch?|
|Default Connector|[Pre_Validations](#pre_validations)|
|Default Connector Label|No Branch|


#### Rule branchYes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Selected_Branch](#assign_selected_branch)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|$User.Division| Is Null|⬜|
|2|[Get_Branch_Unit](#get_branch_unit)| Is Null|⬜|




### Create_Account_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Account Visit|
|Store Output Automatically|✅|
|Connector|[Copy_2_of_Set_Visit_ID](#copy_2_of_set_visit_id)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AccountLookup__c|AL.accountSingle.Id|
|EGH_Brand__c|selectedBrand|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_RelatedShowroomBranch__c|SelectedBranchId|
|EGH_SR_Opportunity__c|Opportunities.firstSelectedRow.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|Name|varVisitNameAccountSingle|
|PurposeVisit__c|varPurposeOfVisit|
|Route_to_Sales__c|✅|




### Create_Lead_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Lead Visit|
|Store Output Automatically|✅|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|selectedBrand|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|AL.leadSingle.Id|
|EGH_RelatedShowroomBranch__c|SelectedBranchId|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|AL.leadSingle.EGH_Model_of_Interest__c|
|Name|varVisitNameLeadSingle|
|PurposeVisit__c|varPurposeOfVisit|
|Route_to_Sales__c|✅|




### Create_New_Lead_ArtLeasing

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|Lead|
|Label|Create New Lead ArtLeasing|
|Description|Create a new Lead|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[setLeadIDArtLeasing](#setleadidartleasing)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|Description|Comments|
|EGH_ArtLeasingEmailOptinCheckbox__c|Email|
|EGH_ArtLeasingPhoneOptinCheckbox__c|Phone|
|EGH_ArtLeasingSMSOptinCheckbox__c|SMS|
|EGH_ArtLeasingWhatsAppOptinCheckbox__c|Whatsapp|
|EGH_BranchCode__c|SelectedBranchCode|
|EGH_BrandListPicklist__c|selectedBrand|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|SelectedBranchId|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|ModelOfInterest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|EGH_UTMCampaignSourceText__c|Event|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Walk-in|
|MobilePhone|MobileNumber.value|
|RecordTypeId|Lead_Type|
|Salutation|Salutationpicklist|




### Create_New_Lead_EliteCars

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|Lead|
|Label|Create New Lead EliteCars|
|Description|Create a new Lead|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[setLeadIDEliteCars](#setleadidelitecars)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|Description|Comments|
|EGH_BranchCode__c|SelectedBranchCode|
|EGH_BrandListPicklist__c|selectedBrand|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|SelectedBranchId|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|ModelOfInterest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|EGH_TheEliteCarsEmailOptinCheckbox__c|Email|
|EGH_TheEliteCarsPhoneOptinCheckbox__c|Phone|
|EGH_TheEliteCarsSMSOptinCheckbox__c|SMS|
|EGH_TheEliteCarsWhatsAppOptinCheckbox__c|Whatsapp|
|EGH_UTMCampaignSourceText__c|Event|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Walk-in|
|MobilePhone|MobileNumber.value|
|RecordTypeId|Lead_Type|
|Salutation|Salutationpicklist|




### Create_New_Lead_Jetour

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|Lead|
|Label|Create New Lead Jetour|
|Description|Create a new Lead|
|Fault Connector|[Error_Message](#error_message)|
|Store Output Automatically|✅|
|Connector|[setLeadIDJetour](#setleadidjetour)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|Description|Comments|
|EGH_BranchCode__c|SelectedBranchCode|
|EGH_BrandListPicklist__c|selectedBrand|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_JetourEmailOptinCheckbox__c|Email|
|EGH_JetourPhoneOptinCheckbox__c|Phone|
|EGH_JetourSMSOptinCheckbox__c|SMS|
|EGH_JetourWhatsAppOptinCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|SelectedBranchId|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|ModelOfInterest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|EGH_UTMCampaignSourceText__c|Event|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Walk-in|
|MobilePhone|MobileNumber.value|
|RecordTypeId|Lead_Type|
|Salutation|Salutationpicklist|




### Create_Note

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|Note|
|Label|Create Note|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[Create_Visit](#create_visit)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|Body|Comments|
|ParentId|varNewLeadID|
|Title|New Note|




### Create_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[Copy_3_of_Set_Visit_ID](#copy_3_of_set_visit_id)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|BrandList2|
|EGH_CommentsRichText__c|Comments|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|varNewLeadID|
|EGH_RelatedShowroomBranch__c|SelectedBranchId|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|ModelOfInterest|
|Name|varVisitNameNewCustomer|
|PurposeVisit__c|Showroom Visit|
|Route_to_Sales__c|Connect_With_Sales_Team|




### Create_Visit_for_Existing_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit for Existing Lead|
|Store Output Automatically|✅|
|Connector|[Copy_4_of_Set_Visit_ID](#copy_4_of_set_visit_id)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|selectedBrand|
|EGH_CommentsRichText__c|Get_Selected_Existing_Lead.Description|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|Get_Selected_Existing_Lead.Id|
|EGH_RelatedShowroomBranch__c|SelectedBranchId|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|Get_Selected_Existing_Lead.EGH_Model_of_Interest__c|
|Name|varVisitNameExistingLead|
|PurposeVisit__c|varPurposeOfVisit|
|Route_to_Sales__c|✅|




### Create_Visit_for_Selected_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit for Selected Account|
|Store Output Automatically|✅|
|Connector|[Set_Visit_ID](#set_visit_id)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AccountLookup__c|customerCustomTable.selectedRowKeyValue|
|EGH_Brand__c|selectedBrand|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_RelatedShowroomBranch__c|SelectedBranchId|
|EGH_SR_Opportunity__c|Copy_1_of_serviceAppointmentList.firstSelectedRow.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|Name|varVisitNameMultipleCustomer|
|PurposeVisit__c|varPurposeOfVisit|
|Route_to_Sales__c|✅|




### Create_Visit_for_Selected_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit for  Selected Lead|
|Store Output Automatically|✅|
|Connector|[varVisitIDSet](#varvisitidset)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|selectedBrand|
|EGH_CommentsRichText__c|leadCustomTable.outputSelectedRow.Description|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|leadCustomTable.selectedRowKeyValue|
|EGH_RelatedShowroomBranch__c|SelectedBranchId|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|leadCustomTable.outputSelectedRow.EGH_Model_of_Interest__c|
|Name|varVisitNameMuletipleLead|
|PurposeVisit__c|varPurposeOfVisit|
|Route_to_Sales__c|✅|




### CreateNewLeadSoueast

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|Lead|
|Label|Create New Lead Soueast|
|Description|Create a new Lead|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[setLeadIDSoueast](#setleadidsoueast)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|Description|Comments|
|EGH_BranchCode__c|SelectedBranchCode|
|EGH_BrandListPicklist__c|selectedBrand|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|SelectedBranchId|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|ModelOfInterest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|EGH_SoueastEmailOptinCheckbox__c|Email|
|EGH_SoueastPhoneOptinCheckbox__c|Phone|
|EGH_SoueastSMSOptinCheckbox__c|SMS|
|EGH_SoueastWhatsAppOptinCheckbox__c|Whatsapp|
|EGH_UTMCampaignSourceText__c|Event|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Walk-in|
|MobilePhone|MobileNumber.value|
|RecordTypeId|Lead_Type|
|Salutation|Salutationpicklist|




### Get_Branch_Unit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|BranchUnit|
|Label|Get Branch Unit|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[User_has_Branch](#user_has_branch)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Name| Equal To|$User.Division|




### Get_Brand_by_Parent_Branch_Name

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|EGH_ParentBranchBrandMapping__mdt|
|Label|Get Brand by Parent Branch Name|
|Assign Null Values If No Records Found|⬜|
|Output Assignments|assignToReference: selectedBrand<br/>field: EGH_BrandName__c<br/>|
|Connector|[Showroom_Has_Valid_Brand](#showroom_has_valid_brand)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|EGH_ParentBranchName__c| Equal To|SelectedBranchParentName|




### Get_Opportunities_Related_to_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Opportunity|
|Label|Get Opportunities Related to Account|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varOpportunityListRelatedtoAccount|
|Queried Fields|- Id<br/>- Name<br/>- Amount<br/>- StageName<br/>- AccountId<br/>- OwnerId<br/>- LastModifiedDate<br/>- EGH_Brand__c<br/>- EGH_Branch_Name__c<br/>- Sales_Representative__c<br/>|
|Connector|[Assign_Opportunities_Size](#assign_opportunities_size)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|StageName| Not Equal To|Closed Lost|
|2|StageName| Not Equal To|Closed Won|
|3|AccountId| Equal To|AL.accountSingle.Id|
|4|IsClosed| Equal To|⬜|




### Get_Opportunities_Related_to_Account_Selected

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Opportunity|
|Label|Get Opportunities Related to Account Selected|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varOpportunityListSecondScreen|
|Queried Fields|- Id<br/>- Name<br/>- Amount<br/>- StageName<br/>- AccountId<br/>- CloseDate<br/>- CreatedDate<br/>- Sales_Representative__c<br/>- OwnerId<br/>- LastModifiedDate<br/>- EGH_Brand__c<br/>- EGH_Branch_Name__c<br/>|
|Connector|[Count_Opportunities](#count_opportunities)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|StageName| Not Equal To|Closed Lost|
|2|StageName| Not Equal To|Closed Won|
|3|AccountId| Equal To|customerCustomTable.selectedRowKeyValue|
|4|IsClosed| Equal To|⬜|




### Get_SA_Related_to_Account_Selected

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|ServiceAppointment|
|Label|Get SA Related to Account Selected|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varServiceAppointmentAccountSecondScreen|
|Queried Fields|- Id<br/>- AppointmentNumber<br/>- Status<br/>- AccountId<br/>- Subject<br/>- DueDate<br/>- Service_Territory_Name__c<br/>- Visit_Type_Name__c<br/>|
|Connector|[Get_Opportunities_Related_to_Account_Selected](#get_opportunities_related_to_account_selected)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ParentRecordId| Equal To|customerCustomTable.selectedRowKeyValue|
|2|Status| Not Equal To|Completed|
|3|Status| Not Equal To|Canceled|
|4|DueDate| Greater Than|$Flow.CurrentDateTime|




### Get_Selected_Existing_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Lead|
|Label|Get Selected Existing Lead|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Existing_Lead_Details](#existing_lead_details)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|ExistingLeadsDataTable.firstSelectedRow.Id|




### Get_Selected_Showroom

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|BranchUnit|
|Label|Get Selected Showroom|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Assign_Selected_Branch_Values](#assign_selected_branch_values)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Name| Equal To|ShowroomsPicker.selectedValue|




### Get_Service_Appointments_Related_to_Existing_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|ServiceAppointment|
|Label|Get Service Appointments Related to Existing Lead|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varServiceAppointmentListSecondscreen|
|Queried Fields|- Id<br/>- ActualStartTime<br/>- ActualEndTime<br/>- AppointmentNumber<br/>- Status<br/>- Service_Territory_Name__c<br/>- Visit_Type_Name__c<br/>|
|Connector|[Get_Selected_Existing_Lead](#get_selected_existing_lead)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ParentRecordId| Equal To|ExistingLeadsDataTable.firstSelectedRow.Id|
|2|Status| Not Equal To|Completed|
|3|Status| Not Equal To|Canceled|
|4|DueDate| Greater Than|$Flow.CurrentDateTime|




### Get_Service_Appointments_Related_to_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|ServiceAppointment|
|Label|Get Service Appointments Related to Lead Selected|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varServiceAppointmentListSecondscreen|
|Queried Fields|- Id<br/>- ActualStartTime<br/>- ActualEndTime<br/>- AppointmentNumber<br/>- Status<br/>- Service_Territory_Name__c<br/>- Visit_Type_Name__c<br/>|
|Connector|[serviceAppointmentSecondScreen](#serviceappointmentsecondscreen)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ParentRecordId| Equal To|leadCustomTable.selectedRowKeyValue|
|2|Status| Not Equal To|Completed|
|3|Status| Not Equal To|Canceled|
|4|DueDate| Greater Than|$Flow.CurrentDateTime|




### Get_Service_Appointmets_Related_to_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|ServiceAppointment|
|Label|Get Service Appointmets Related to Account|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varServiceAppointmentRelatedToAccount|
|Queried Fields|- Id<br/>- Status<br/>- AppointmentNumber<br/>- Subject<br/>- DueDate<br/>|
|Connector|[List_of_Customers](#list_of_customers)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ParentRecordId| Equal To|AL.accountSingle.Id|
|2|Status| Not Equal To|Completed|
|3|Status| Not Equal To|Canceled|




### Get_Service_Appointmets_Related_to_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|ServiceAppointment|
|Label|Get Service Appointmets Related to Lead|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varServiceAppointmentRelatedtoLead|
|Queried Fields|- Id<br/>- Status<br/>- AppointmentNumber<br/>- Subject<br/>- DueDate<br/>|
|Connector|[is_Single_Account](#is_single_account)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ParentRecordId| Equal To|AL.leadSingle.Id|
|2|Status| Not Equal To|Completed|
|3|Status| Not Equal To|Canceled|




### Get_Showroom_Skill

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Skill|
|Label|Get Showroom Skill|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Showroom_Skill_Found](#showroom_skill_found)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|MasterLabel| Equal To|SelectedBranchName|




### Get_User_Secondary_Branch

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|BranchUnitBusinessMember|
|Label|Get User Secondary Branch|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Secondary_Branch_Exist](#secondary_branch_exist)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|BusinessUnitMemberId| Equal To|$User.Id|
|2|IsActive| Equal To|✅|
|3|BranchUnitId| Not Equal To|Get_Branch_Unit.Id|




### Customer_Information_Capture_Form

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Customer Information Capture Form|
|Description|Fields to sear Lead or Person Account|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|⬜|
|Back Button Label|Back|
|Next Or Finish Button Label|Next|
|Show Footer|✅|
|Show Header|⬜|
|Connector|[Find_Lead_Duplicates](#find_lead_duplicates)|


#### Branch

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: right;"><strong style="font-size: 18px;">{!SelectedBranchName}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### CustomerInformation

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Customer Information</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Salutationpicklist

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|Salutation|
|Field Text|Salutation|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Copy_1_of_First_Name

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Field Text|First Name|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column1](#customer_information_capture_form_section1_column1)|




#### Copy_1_of_Email

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|flowruntime:email|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Validation Rule|errorMessage: >-<br/>&nbsp;&nbsp;<p><span style=color: rgb(255, 0, 0);>Please enter a valid email<br/>&nbsp;&nbsp;address.</span></p><br/>formulaExpression: >-<br/>&nbsp;&nbsp;OR(<br/>&nbsp;&nbsp;&nbsp;ISBLANK({!Copy_1_of_Email.value}),<br/>&nbsp;&nbsp;&nbsp;REGEX({!Copy_1_of_Email.value},<br/>&nbsp;&nbsp;^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,4}$)<br/>&nbsp;&nbsp;&nbsp;)<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column1](#customer_information_capture_form_section1_column1)|
|Required (input)|⬜|




#### Consent

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Consent</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column1](#customer_information_capture_form_section1_column1)|




#### Email

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|Email|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column1](#customer_information_capture_form_section1_column1)|




#### SMS

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|SMS|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column1](#customer_information_capture_form_section1_column1)|




#### Customer_Information_Capture_Form_Section1_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Customer_Information_Capture_Form_Section1](#customer_information_capture_form_section1)|
|Width (input)|6|




#### Copy_1_of_Last_Name

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Field Text|Last Name|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column2](#customer_information_capture_form_section1_column2)|




#### MobileNumber

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|flowruntime:phone|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Validation Rule|errorMessage: >-<br/>&nbsp;&nbsp;<p><span style=color: rgb(255, 0, 0);>Mobile Number must start with +971 or<br/>&nbsp;&nbsp;00971 followed by 9 digits.</span></p><br/>formulaExpression: |-<br/>&nbsp;&nbsp;REGEX(<br/>&nbsp;&nbsp;{!MobileNumber.value},<br/>&nbsp;&nbsp;^(\\+971[0-9]{9}|00971[0-9]{9})$<br/>&nbsp;&nbsp;)<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column2](#customer_information_capture_form_section1_column2)|
|Required (input)|✅|
|Label (input)|Mobile|




#### blank

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p> </p><p><br></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column2](#customer_information_capture_form_section1_column2)|




#### Whatsapp

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|Whatsapp|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column2](#customer_information_capture_form_section1_column2)|




#### Phone

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|Phone|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Information_Capture_Form_Section1_Column2](#customer_information_capture_form_section1_column2)|




#### Customer_Information_Capture_Form_Section1_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Customer_Information_Capture_Form_Section1](#customer_information_capture_form_section1)|
|Width (input)|6|




#### Customer_Information_Capture_Form_Section1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section Without Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Lead_Type

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|LeadRTChoices|
|Field Text|Lead Type|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### BrandList2

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|BrandListChoice|
|Default Selected Choice Reference|BrandListChoice|
|Field Text|BrandList|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Disabled|true|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Language

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|EGHLeadLanguage|
|Default Value|English|
|Field Text|Language|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Preferred_Contact_Method

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|PreferredContactMethod|
|Field Text|Preferred Contact Method|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### ModelOfInterest

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|ModelOfInterestChoices|
|Field Text|Model of Interest|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Comments

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Field Text|Comments|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Connect_With_Sales_Team

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Default Value|true|
|Field Text|Connect With Sales Team|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Customer_Search

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Customer Search|
|Description|Fields to sear Lead or Person Account|
|Allow Back|⬜|
|Allow Finish|✅|
|Allow Pause|⬜|
|Next Or Finish Button Label|Search|
|Show Footer|✅|
|Show Header|⬜|
|Connector|[Showroom_Changed](#showroom_changed)|


#### ShowroomsPicker

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eghGenericFlowPicklist|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Input Options (input)|UserShowrooms|
|Selected Value (input)|SelectedBranchName|




#### NewLeadButton

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eghGenericFlowButton|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Button Label (input)|New Lead|




#### Search

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Field Text|Search Here|
|Field Type| Input Field|
|Help Text|<p>Please enter First Name,Last Name,Mobile Number or Email of the Customer</p>|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Validation Rule|errorMessage: >-<br/>&nbsp;&nbsp;<p><span style=color: rgb(231, 12, 12); background-color: rgb(255, 255,<br/>&nbsp;&nbsp;255);>No special characters allowed except .,@,+ and minimum length is 3<br/>&nbsp;&nbsp;characters.</span></p><br/>formulaExpression: REGEX({!Search}, ^[a-zA-Z0-9.@+ ]{3,}$)<br/>|




### Error_Message

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Error Message|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|⬜|


#### ErrorMessage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong>{!$Flow.FaultMessage}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Existing_Lead_Details

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Existing Lead Details|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|⬜|
|Show Footer|✅|
|Show Header|⬜|
|Connector|[Copy_1_of_Update_Purpose_of_Visit](#copy_1_of_update_purpose_of_visit)|


#### Copy_1_of_LeadName

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Name : {!Get_Selected_Existing_Lead.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column1](#existingleaddetails_column1)|




#### Copy_1_of_LeadPhone

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Mobile Phone : {!Get_Selected_Existing_Lead.MobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column1](#existingleaddetails_column1)|




#### Copy_1_of_LeadStatus

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Status : {!Get_Selected_Existing_Lead.Status}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column1](#existingleaddetails_column1)|




#### Copy_1_of_LeadLanguage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Language : {!Get_Selected_Existing_Lead.EGH_LeadLanguagePicklist__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column1](#existingleaddetails_column1)|




#### Copy_1_of_LeadModelOfInterest2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Model of Interest: {!Get_Selected_Existing_Lead.EGH_Model_of_Interest__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column1](#existingleaddetails_column1)|




#### Copy_1_of_LeadOwner2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Lead Owner: {!Get_Selected_Existing_Lead.EGH_Lead_Owner__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column1](#existingleaddetails_column1)|




#### ExistingLeadDetails_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[ExistingLeadDetails](#existingleaddetails)|
|Width (input)|6|




#### Copy_1_of_LeadEmail

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Email : {!Get_Selected_Existing_Lead.Email}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column2](#existingleaddetails_column2)|




#### Copy_1_of_LeadSource

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Lead Source : {!Get_Selected_Existing_Lead.LeadSource}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column2](#existingleaddetails_column2)|




#### Copy_1_of_LeadBrandList

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Brand List : {!Get_Selected_Existing_Lead.EGH_BrandListPicklist__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column2](#existingleaddetails_column2)|




#### Copy_1_of_LeadNationality

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Nationality : {!Get_Selected_Existing_Lead.EGH_LeadNationalityPicklist__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[ExistingLeadDetails_Column2](#existingleaddetails_column2)|




#### ExistingLeadDetails_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[ExistingLeadDetails](#existingleaddetails)|
|Width (input)|6|




#### ExistingLeadDetails

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|Lead Details|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section With Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### ExistingLeadServiceAppointmentList

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: ServiceAppointment<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_Service_Appointments_Related_to_Existing_Lead<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|
|Label (input)|Service Appointment List|
|Selection Mode (input)|NO_SELECTION|
|Min Row Selection (input)|numberValue: 0<br/>|
|Table Data (input)|varServiceAppointmentListSecondscreen|
|Should Display Label (input)|✅|
|Max Row Selection (input)|numberValue: 0<br/>|
|Columns (input)|[{"apiName":"AppointmentNumber","guid":"column-257d","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Appointment Number","type":"text"},{"apiName":"Status","guid":"column-2670","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Status","type":"text"},{"apiName":"DueDate","guid":"column-cd86","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Due Date","type":"customDateTime"},{"apiName":"Subject","guid":"column-3e05","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Subject","type":"text"},{"apiName":"Service_Territory_Name__c","guid":"column-cc43","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"label":"Service Territory Name","type":"customRichText"},{"apiName":"Visit_Type_Name__c","guid":"column-8910","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"label":"Visit Type Name","type":"customRichText"}]|




#### Copy_1_of_noOpenServiceAppointmentBanner

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(244, 12, 12);">There are no open service appointments for the Select Lead</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_Service_Appointments_Related_to_Existing_Lead<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### ExistingLead_Purpose_of_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|PurposeOfVisitChoices|
|Field Text|Purpose Of Visit|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Existing_Leads_Screen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Existing Leads Screen|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|⬜|
|Show Footer|✅|
|Show Header|✅|
|Connector|[Get_Service_Appointments_Related_to_Existing_Lead](#get_service_appointments_related_to_existing_lead)|


#### ExistingLeadDispalyText

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>{!$Label.EGH_DuplicateLeadWarning}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Find_Lead_Duplicates.duplicatesFound<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### ExistingLeadsDataTable

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: Lead<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Find_Lead_Duplicates.leadMatchRecordSize<br/>&nbsp;&nbsp;operator: GreaterThan<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>|
|Label (input)|Existing Leads|
|Selection Mode (input)|SINGLE_SELECT|
|Min Row Selection (input)|1|
|Table Data (input)|Find_Lead_Duplicates.leadMatchRecordList|
|Columns (input)|[{"apiName":"Name","guid":"column-b2b7","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Full Name","type":"text"},{"apiName":"Email","guid":"column-e904","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Email","type":"email"},{"apiName":"MobilePhone","guid":"column-19f3","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Mobile Phone","type":"phone"},{"apiName":"Status","guid":"column-cf0f","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"sortable":false,"label":"Status","type":"text"}]|
|Max Row Selection (input)|1|
|Should Display Label (input)|✅|




#### DuplicateError

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><span style="color: rgb(237, 14, 14);">Error trying to find Lead duplicates : {!Find_Lead_Duplicates.findDuplicatesErrorList}</span></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Find_Lead_Duplicates.duplicateErrorFound<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### MatchError

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><span style="background-color: rgb(255, 255, 255); color: rgb(237, 14, 14);">Error trying to match Lead duplicates : {!Find_Lead_Duplicates.matchErrorList}</span></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Find_Lead_Duplicates.matchErrorFound<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




### Invalid_Brand

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Invalid Brand|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|✅|


#### InvalidBrand

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(247, 0, 0); background-color: rgb(255, 255, 255);">Your Showroom must have a valid brand .It must be either Jetour,Soueast,ArtLeasing or Elite.</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Invalid_Brand_Screen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Invalid Brand Screen|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|✅|


#### Copy_1_of_InvalidBrand

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(247, 0, 0); background-color: rgb(255, 255, 255);">Your Showroom must have a valid brand .It must be either Jetour,Soueast,ArtLeasing or Elite.</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### List_of_Customers

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|List of Customers|
|Description|List of Lead & Customer found|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|⬜|
|Show Footer|⬜|
|Show Header|⬜|
|Connector|[UpdatePurposeOfVisit](#updatepurposeofvisit)|


#### NewLeadButton2

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eghGenericFlowButton|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Button Label (input)|New Lead|




#### LeadData

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Name : {!AL.leadSingle.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column1](#leads_column1)|




#### PhoneLead

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Phone: {!AL.leadSingle.MobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column1](#leads_column1)|




#### LeadModelOfInterest

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Model of Interest: {!AL.leadSingle.EGH_Model_of_Interest__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column1](#leads_column1)|




#### Create_visit_for_this_customer_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|Create visit for this customer?|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column1](#leads_column1)|




#### Leads_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Leads](#leads)|
|Width (input)|6|




#### EmailLead

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Email: {!AL.leadSingle.Email}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column2](#leads_column2)|




#### leadBranch

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Branch: {!AL.leadSingle.EGH_LeadBranchUnitLookup__r.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column2](#leads_column2)|




#### LeadOwner

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Lead Owner: {!AL.leadSingle.EGH_Lead_Owner__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Leads_Column2](#leads_column2)|




#### Leads_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Leads](#leads)|
|Width (input)|6|




#### Leads

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|Leads|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section With Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>|




#### CustomerName

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Name: {!AL.accountSingle.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customers_Column1](#customers_column1)|




#### CustomerMobile

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Phone: {!AL.accountSingle.PersonMobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customers_Column1](#customers_column1)|




#### Create_visit_for_this_customer_account

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|Create visit for this customer?|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customers_Column1](#customers_column1)|




#### Customers_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Customers](#customers)|
|Width (input)|6|




#### CustomerEmail

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Email: {!AL.accountSingle.PersonEmail}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customers_Column2](#customers_column2)|




#### Customers_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Customers](#customers)|
|Width (input)|6|




#### Customers

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|Customers|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section With Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: AL.accountSize<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>|




#### Opportunities

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: Opportunity<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: varOpportunityListRelatedtoAccountSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: GreaterThan<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_account<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|
|Label (input)|Opportunities|
|Selection Mode (input)|SINGLE_SELECT|
|Min Row Selection (input)|1|
|Table Data (input)|varOpportunityListRelatedtoAccount|
|Should Display Label (input)|✅|
|Columns (input)|[{"apiName":"Name","guid":"column-b611","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Name","type":"text"},{"apiName":"Sales_Representative__c","guid":"column-ee8f","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Sales Representative","type":"customRichText"},{"apiName":"StageName","guid":"column-4e59","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Stage","type":"text"},{"apiName":"EGH_Brand__c","guid":"column-0e17","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Brand","type":"text"},{"apiName":"EGH_Branch_Name__c","guid":"column-ddee","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"sortable":false,"label":"Branch Name","type":"customRichText"},{"apiName":"LastModifiedDate","guid":"column-1e2f","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"label":"Last Modified Date","type":"customDateTime"}]|
|Max Row Selection (input)|1|




#### ServiceAppointmentV2

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: ServiceAppointment<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_Service_Appointmets_Related_to_Account<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|
|Label (input)|Service Appointment|
|Selection Mode (input)|MULTI_SELECT|
|Min Row Selection (input)|numberValue: 0<br/>|
|Table Data (input)|varServiceAppointmentRelatedToAccount|
|Columns (input)|[{"apiName":"AppointmentNumber","guid":"column-d745","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Appointment Number","type":"text"},{"apiName":"Status","guid":"column-57d5","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Status","type":"text"},{"apiName":"DueDate","guid":"column-eb9e","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Due Date","type":"customDateTime"},{"apiName":"Subject","guid":"column-3e44","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Subject","type":"text"}]|
|Should Display Label (input)|✅|




#### ServiceAppointment

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: ServiceAppointment<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: varExistServiceApoointment<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>&nbsp;&nbsp;- leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>|
|Label (input)|Service Appointment|
|Selection Mode (input)|NO_SELECTION|
|Min Row Selection (input)|numberValue: 0<br/>|
|Should Display Label (input)|✅|
|Table Data (input)|varServiceAppointmentRelatedtoLead|
|Columns (input)|[{"apiName":"AppointmentNumber","guid":"column-aaa8","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Appointment Number","type":"text"},{"apiName":"Status","guid":"column-45b6","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Status","type":"text"},{"apiName":"DueDate","guid":"column-9f32","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Due Date","type":"customDateTime"},{"apiName":"Subject","guid":"column-6bb8","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Subject","type":"text"}]|
|Max Row Selection (input)|numberValue: 0<br/>|




#### leadCustomTable

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: Lead<br/>|
|Extension Name|c:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;operator: GreaterThan<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>|
|Object Name (input)|Lead|
|Cb_suppress Bottom Bar (input)|CB_FALSE|
|Cb_navigate Next On Save (input)|CB_FALSE|
|Column Fields (input)|Name,Email,MobilePhone,EGH_BrandListPicklist__c,LeadSource,Status,EGH_Model_of_Interest__c,CreatedDate|
|Cb_match Case On Filters (input)|CB_FALSE|
|Column Widths (input)|Name:0, Email:0, MobilePhone:0, EGH_BrandListPicklist__c:0, LeadSource:0, Status:0, EGH_Model_of_Interest__c:0, CreatedDate:0|
|Cb_single Row Selection (input)|CB_TRUE|
|Single Row Selection (input)|✅|
|Column Flexes (input)|All|
|Cb_is Display Header (input)|CB_TRUE|
|Cb_is Show Search Bar (input)|CB_FALSE|
|Is Display Header (input)|✅|
|Table Label (input)|[Leads](#leads)|
|Table Icon (input)|standard:lead|
|Show Selected Count (input)|✅|
|Cb_show Selected Count (input)|CB_TRUE|
|Show Record Count (input)|✅|
|Cb_show Record Count (input)|CB_TRUE|
|Cb_not_suppress Name Field Link (input)|CB_FALSE|
|Cb_is Required (input)|CB_FALSE|
|Cb_hide Checkbox Column (input)|CB_FALSE|
|Table Data (input)|AL.leadList|




#### breakbar

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### linebreak2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### customerCustomTable

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: Account<br/>|
|Extension Name|c:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: AL.accountSize<br/>&nbsp;&nbsp;operator: GreaterThan<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>|
|Object Name (input)|Account|
|Cb_suppress Bottom Bar (input)|CB_FALSE|
|Cb_navigate Next On Save (input)|CB_FALSE|
|Column Fields (input)|Name,PersonEmail,Phone,PersonMobilePhone|
|Cb_match Case On Filters (input)|CB_FALSE|
|Column Flexes (input)|All|
|Column Widths (input)|Name:0, PersonEmail:0, Phone:0, PersonMobilePhone:0|
|Single Row Selection (input)|✅|
|Cb_single Row Selection (input)|CB_TRUE|
|Is Display Header (input)|✅|
|Cb_is Display Header (input)|CB_TRUE|
|Table Label (input)|Accounts|
|Table Icon (input)|standard:account|
|Show Selected Count (input)|✅|
|Cb_show Selected Count (input)|CB_TRUE|
|Show Record Count (input)|✅|
|Cb_show Record Count (input)|CB_TRUE|
|Cb_not_suppress Name Field Link (input)|CB_FALSE|
|Cb_is Remove Row Action (input)|CB_FALSE|
|Cb_is Required (input)|CB_FALSE|
|Cb_hide Checkbox Column (input)|CB_FALSE|
|Table Data (input)|AL.accountList|




#### Purpose_Of_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|PurposeOfVisitChoices|
|Default Value|Showroom First Visit|
|Field Text|Purpose Of Visit|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: (1 AND 2) OR (1 AND 4) OR (2 AND 3)<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: AL.accountSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: AL.accountSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>|




#### linebreak4

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### selectionWarning

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(228, 14, 14);">Please select at least 1 Lead or at least 1 Customer Record.Do not select both. </strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: (1 AND 4) OR (2 AND 3) OR (5 AND 6) OR (7 AND 8)<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: customerCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: customerCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: leadCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: leadCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_account<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_Lead<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_account<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_Lead<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|




#### lineBreak5

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### FLowPrevousComponent

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:egh_customFooterPreviousComponent|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: (1 AND 2) OR ( 3 AND 4)<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: leadCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: customerCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: leadCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: customerCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>|




#### customFooter

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eGH_customFooter|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: >-<br/>&nbsp;&nbsp;(1 AND 3) OR (2 AND 4) OR (1 AND 5) OR (2 AND 6) OR 7 OR 8 OR (9 AND NOT(10))<br/>&nbsp;&nbsp;OR (10 AND NOT(9))<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: customerCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: leadCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: leadCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: customerCustomTable.numberOfRowsSelected<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: AL.accountSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>&nbsp;&nbsp;- leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: AL.accountSize<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 1<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_account<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>&nbsp;&nbsp;- leftValueReference: Create_visit_for_this_customer_Lead<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|
|Auto Navigate To Next (input)|⬜|
|Show Footer Markup (input)|✅|




### loader

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|[loader](#loader)|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|⬜|
|Show Header|⬜|
|Connector|[Get_Lead_Ownersubflow](#get_lead_ownersubflow)|


#### Copy_2_of_loaderText

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><img src="{!$Resource.EGH_Spinner}" alt=""></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### Copy_1_of_autoNavifateFirst

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eGH_AutoNavigate|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Defualt Time Out (input)|6000|




### opportunityListSecondScreen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|[opportunityListSecondScreen](#opportunitylistsecondscreen)|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|⬜|
|Show Footer|✅|
|Show Header|⬜|
|Connector|[Copy_2_of_UpdatePurposeOfVisit](#copy_2_of_updatepurposeofvisit)|


#### AccountName

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Name : {!customerCustomTable.outputSelectedRow.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column1](#customer_details_column1)|




#### AccountPhone

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Phone : {!customerCustomTable.outputSelectedRow.PersonMobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column1](#customer_details_column1)|




#### AccountLanguage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Language : {!customerCustomTable.outputSelectedRow.EGH_ContactLanguagePicklist__pc}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column1](#customer_details_column1)|




#### Customer_Details_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Customer_Details](#customer_details)|
|Width (input)|6|




#### AccountEmail

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Email : {!customerCustomTable.outputSelectedRow.PersonEmail}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column2](#customer_details_column2)|




#### AccountNationality

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Nationality : {!customerCustomTable.outputSelectedRow.EGH_ContactNationalityPicklist__pc}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column2](#customer_details_column2)|




#### Customer_Details_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Customer_Details](#customer_details)|
|Width (input)|6|




#### Customer_Details

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|Customer Details|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section With Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### ServiceAppointmentV

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: ServiceAppointment<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_SA_Related_to_Account_Selected<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|
|Label (input)|Service Appointment|
|Selection Mode (input)|NO_SELECTION|
|Min Row Selection (input)|numberValue: 0<br/>|
|Table Data (input)|varServiceAppointmentAccountSecondScreen|
|Max Row Selection (input)|numberValue: 0<br/>|
|Columns (input)|[{"apiName":"AppointmentNumber","guid":"column-9549","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Appointment Number","type":"text"},{"apiName":"Status","guid":"column-582f","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Status","type":"text"},{"apiName":"DueDate","guid":"column-c3bd","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Due Date","type":"customDateTime"},{"apiName":"Subject","guid":"column-65d7","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Subject","type":"text"},{"apiName":"Service_Territory_Name__c","guid":"column-4591","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"label":"Service Territory Name","type":"customRichText"},{"apiName":"Visit_Type_Name__c","guid":"column-bc91","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"label":"Visit Type Name","type":"customRichText"}]|
|Should Display Label (input)|✅|




#### Copy_1_of_serviceAppointmentList

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: Opportunity<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: BranchSpecificOpportunitiesCount<br/>&nbsp;&nbsp;operator: GreaterThan<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>|
|Label (input)|Opportunity List|
|Selection Mode (input)|SINGLE_SELECT|
|Min Row Selection (input)|1|
|Table Data (input)|varOpportunityListSecondScreen|
|Should Display Label (input)|✅|
|Max Row Selection (input)|1|
|Columns (input)|[{"apiName":"Name","guid":"column-2e42","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Name","type":"text"},{"apiName":"Sales_Representative__c","guid":"column-a5fe","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Sales Representative","type":"customRichText"},{"apiName":"StageName","guid":"column-01db","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Stage","type":"text"},{"apiName":"EGH_Brand__c","guid":"column-234b","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"sortable":false,"label":"Brand","type":"text"},{"apiName":"EGH_Branch_Name__c","guid":"column-3053","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"sortable":false,"label":"Branch Name","type":"customRichText"},{"apiName":"LastModifiedDate","guid":"column-c29e","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"sortable":false,"label":"Last Modified Date","type":"customDateTime"}]|




#### noOpportunitiesScreen

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(228, 8, 8);">There are no  opportunities which are in  open stage for the selected Account</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: BranchSpecificOpportunitiesCount<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>|




#### NoSAforAccount

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(244, 12, 12); background-color: rgb(255, 255, 255);">There are no open service appointments for the Select Account</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_SA_Related_to_Account_Selected<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### Purpose_of_Visit_v

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|PurposeOfVisitChoices|
|Field Text|Purpose of Visit|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Pre_Validations

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Pre Validations|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|⬜|


#### NoBranchMessage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(244, 5, 5); font-size: 18px; background-color: rgb(255, 255, 255);">Your User must have a valid </strong><strong style="color: rgb(244, 5, 5); font-size: 22px; background-color: rgb(255, 255, 255);">BRANCH</strong><strong style="color: rgb(244, 5, 5); font-size: 18px; background-color: rgb(255, 255, 255);"> configured. Please check with your System Administrator</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: SelectedBranchId<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### NoShowroomSkillMessage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="background-color: rgb(255, 255, 255); font-size: 18px; color: rgb(244, 5, 5);">A </strong><strong style="background-color: rgb(255, 255, 255); font-size: 22px; color: rgb(244, 5, 5);">SKILL is not</strong><strong style="background-color: rgb(255, 255, 255); font-size: 18px; color: rgb(244, 5, 5);"> configured for the {!SelectedBranchName}  Showroom. Please check with your System Administrator</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: YesShowrromSkill<br/>&nbsp;&nbsp;operator: NotEqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### NoShowroomManagerMessage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(244, 5, 5); font-size: 18px; background-color: rgb(255, 255, 255);">Your  Showroom {!SelectedBranchName} must have a </strong><strong style="color: rgb(244, 5, 5); font-size: 20px; background-color: rgb(255, 255, 255);">MANAGER</strong><strong style="color: rgb(244, 5, 5); font-size: 18px; background-color: rgb(255, 255, 255);"> Configured in the Branch Unit Record. Please check with your System Administrator</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;- leftValueReference: Find_Team_Leader.teamLeaderId<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>&nbsp;&nbsp;- leftValueReference: SelectedBranchId<br/>&nbsp;&nbsp;&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|




### serviceAppointmentSecondScreen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|[serviceAppointmentSecondScreen](#serviceappointmentsecondscreen)|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|⬜|
|Show Footer|✅|
|Show Header|⬜|
|Connector|[Update_Purpose_of_Visit](#update_purpose_of_visit)|


#### LeadName

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Name : {!leadCustomTable.outputSelectedRow.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column1](#lead_details_column1)|




#### LeadPhone

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Mobile Phone : {!leadCustomTable.outputSelectedRow.MobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column1](#lead_details_column1)|




#### LeadStatus

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Status : {!leadCustomTable.outputSelectedRow.Status}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column1](#lead_details_column1)|




#### LeadLanguage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Language : {!leadCustomTable.outputSelectedRow.EGH_LeadLanguagePicklist__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column1](#lead_details_column1)|




#### LeadModelOfInterest2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Model of Interest: {!leadCustomTable.outputSelectedRow.EGH_Model_of_Interest__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column1](#lead_details_column1)|




#### LeadOwner2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Lead Owner: </strong><strong style="background-color: rgb(255, 255, 255);">{!leadCustomTable.outputSelectedRow.EGH_Lead_Owner__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column1](#lead_details_column1)|




#### Lead_Details_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Lead_Details](#lead_details)|
|Width (input)|6|




#### LeadEmail

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Email : {!leadCustomTable.outputSelectedRow.Email}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column2](#lead_details_column2)|




#### LeadSource

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Lead Source : {!leadCustomTable.outputSelectedRow.LeadSource}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column2](#lead_details_column2)|




#### LeadBrandList

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Brand List : {!leadCustomTable.outputSelectedRow.EGH_BrandListPicklist__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column2](#lead_details_column2)|




#### LeadNationality

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Nationality : {!leadCustomTable.outputSelectedRow.EGH_LeadNationalityPicklist__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Lead_Details_Column2](#lead_details_column2)|




#### Lead_Details_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Lead_Details](#lead_details)|
|Width (input)|6|




#### Lead_Details

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|Lead Details|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section With Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### serviceAppointmentList

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: ServiceAppointment<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_Service_Appointments_Related_to_Lead<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|
|Label (input)|Service Appointment List|
|Selection Mode (input)|NO_SELECTION|
|Min Row Selection (input)|numberValue: 0<br/>|
|Table Data (input)|varServiceAppointmentListSecondscreen|
|Should Display Label (input)|✅|
|Max Row Selection (input)|numberValue: 0<br/>|
|Columns (input)|[{"apiName":"AppointmentNumber","guid":"column-257d","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Appointment Number","type":"text"},{"apiName":"Status","guid":"column-2670","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Status","type":"text"},{"apiName":"DueDate","guid":"column-cd86","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Due Date","type":"customDateTime"},{"apiName":"Subject","guid":"column-3e05","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Subject","type":"text"},{"apiName":"Service_Territory_Name__c","guid":"column-cc43","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"label":"Service Territory Name","type":"customRichText"},{"apiName":"Visit_Type_Name__c","guid":"column-8910","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"label":"Visit Type Name","type":"customRichText"}]|




#### noOpenServiceAppointmentBanner

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(244, 12, 12);">There are no open service appointments for the Select Lead</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_Service_Appointments_Related_to_Lead<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### Purpose_Of_Visit_SecondScreen

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|PurposeOfVisitChoices|
|Field Text|Purpose Of Visit|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Get_Lead_Ownersubflow

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Subflow|
|Label|Get Lead Owner|
|Flow Name|EGH_Lead_Owner_information|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|<!-- -->|varVisitID|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
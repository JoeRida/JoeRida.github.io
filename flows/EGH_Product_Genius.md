# EGH Product Genius Flow

## Flow Diagram

```mermaid
%% If you read this, your Markdown visualizer does not handle MermaidJS syntax.
%% - If you are in VS Code, install extension `Markdown Preview Mermaid Support` at https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid
%% - If you are using sfdx-hardis, try to define env variable `MERMAID_MODES=cli,docker` ,then run again the command to regenerate markdown with SVG images.
%% - If you are within mkdocs-material, define mermaid plugin in `mkdocs.yml` as described in https://squidfunk.github.io/mkdocs-material/extensions/mermaid/
%% - As a last resort, you can copy-paste this MermaidJS code into https://mermaid.live/ to see the flow diagram

flowchart TB
START(["START<br/><b>Screen Flow</b>"]):::startClass
click START "#general-information" "1227078015"

AL("⚙️ <em></em><br/>AL"):::actionCalls
click AL "#al" "1275392956"

Find_Lead_Duplicates("⚙️ <em></em><br/>Find Lead Duplicates"):::actionCalls
click Find_Lead_Duplicates "#find_lead_duplicates" "2338173511"

Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1("⚙️ <em></em><br/>Transform semicolon-separated string values to Picklist Options Action 1"):::actionCalls
click Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1 "#transform_semicolon_separated_string_values_to_picklist_options_action_1" "1545042711"

Assign_Division_Opportunities_Size[\"🟰 <em></em><br/>Assign Division Opportunities Size"/]:::assignments
click Assign_Division_Opportunities_Size "#assign_division_opportunities_size" "129474990"

Assign_Filtered_Opportunities[\"🟰 <em></em><br/>Assign Filtered Opportunities"/]:::assignments
click Assign_Filtered_Opportunities "#assign_filtered_opportunities" "3084110582"

Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Assign_Transferred_Lead_ID "#assign_transferred_lead_id" "583300526"

Assign_Transferred_Opportunity_ID[\"🟰 <em></em><br/>Assign Transferred Opportunity ID"/]:::assignments
click Assign_Transferred_Opportunity_ID "#assign_transferred_opportunity_id" "203875044"

Assign_Transferred_Opportunity_ID_2[\"🟰 <em></em><br/>Assign Transferred Opportunity ID"/]:::assignments
click Assign_Transferred_Opportunity_ID_2 "#assign_transferred_opportunity_id_2" "1083138143"

Copy_1_of_Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Copy_1_of_Assign_Transferred_Lead_ID "#copy_1_of_assign_transferred_lead_id" "4292760909"

Copy_1_of_Flag_Selected_Opportunity_Reserved[\"🟰 <em></em><br/>Flag Selected Opportunity Reserved"/]:::assignments
click Copy_1_of_Flag_Selected_Opportunity_Reserved "#copy_1_of_flag_selected_opportunity_reserved" "1963220564"

Copy_1_of_Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Copy_1_of_Set_Visit_ID "#copy_1_of_set_visit_id" "230595826"

Copy_2_of_Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Copy_2_of_Assign_Transferred_Lead_ID "#copy_2_of_assign_transferred_lead_id" "3307688535"

Copy_2_of_Set_Visit_ID[\"🟰 <em></em><br/>Set Visit ID"/]:::assignments
click Copy_2_of_Set_Visit_ID "#copy_2_of_set_visit_id" "3291623736"

Copy_3_of_Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Copy_3_of_Assign_Transferred_Lead_ID "#copy_3_of_assign_transferred_lead_id" "3485171925"

Copy_4_of_Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Copy_4_of_Assign_Transferred_Lead_ID "#copy_4_of_assign_transferred_lead_id" "3257333321"

Copy_5_of_Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Copy_5_of_Assign_Transferred_Lead_ID "#copy_5_of_assign_transferred_lead_id" "801001249"

Copy_6_of_Assign_Transferred_Lead_ID[\"🟰 <em></em><br/>Assign Transferred Lead ID"/]:::assignments
click Copy_6_of_Assign_Transferred_Lead_ID "#copy_6_of_assign_transferred_lead_id" "1945548346"

Flag_Selected_Opportunity_Reserved[\"🟰 <em></em><br/>Flag Selected Opportunity Reserved"/]:::assignments
click Flag_Selected_Opportunity_Reserved "#flag_selected_opportunity_reserved" "2861785439"

setLeadIDArtLeasing[\"🟰 <em></em><br/>setLeadIDArtLeasing"/]:::assignments
click setLeadIDArtLeasing "#setleadidartleasing" "597706949"

setLeadIDEliteCars[\"🟰 <em></em><br/>setLeadIDEliteCars"/]:::assignments
click setLeadIDEliteCars "#setleadidelitecars" "1235551300"

setLeadIDJetour[\"🟰 <em></em><br/>setLeadIDJetour"/]:::assignments
click setLeadIDJetour "#setleadidjetour" "55979476"

setLeadIDSoueast[\"🟰 <em></em><br/>setLeadIDSoueast"/]:::assignments
click setLeadIDSoueast "#setleadidsoueast" "3819847427"

Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Assigned_To_PG "#assigned_to_pg" "3467817994"

Branch_Division_Type{"🔀 <em></em><br/>Branch/Division Type"}:::decisions
click Branch_Division_Type "#branch_division_type" "4019129129"

Campaign_User_Found{"🔀 <em></em><br/>Campaign User Found"}:::decisions
click Campaign_User_Found "#campaign_user_found" "4242926532"

Copy_1_of_Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Copy_1_of_Assigned_To_PG "#copy_1_of_assigned_to_pg" "1606434843"

Copy_1_of_Is_Selected_Opportunity_Reserved{"🔀 <em></em><br/>Selected Opportunity Reserved ?"}:::decisions
click Copy_1_of_Is_Selected_Opportunity_Reserved "#copy_1_of_is_selected_opportunity_reserved" "1326068564"

Copy_2_of_Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Copy_2_of_Assigned_To_PG "#copy_2_of_assigned_to_pg" "3423505480"

Copy_3_of_Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Copy_3_of_Assigned_To_PG "#copy_3_of_assigned_to_pg" "734145791"

Copy_4_of_Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Copy_4_of_Assigned_To_PG "#copy_4_of_assigned_to_pg" "159830391"

Copy_5_of_Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Copy_5_of_Assigned_To_PG "#copy_5_of_assigned_to_pg" "3951608479"

Copy_6_of_Assigned_To_PG{"🔀 <em></em><br/>Assigned To PG ?"}:::decisions
click Copy_6_of_Assigned_To_PG "#copy_6_of_assigned_to_pg" "2139297216"

Decision_1{"🔀 <em></em><br/>Exists Lead or Customer?"}:::decisions
click Decision_1 "#decision_1" "2458088433"

Existing_Lead_Found{"🔀 <em></em><br/>Existing Lead Found"}:::decisions
click Existing_Lead_Found "#existing_lead_found" "1235834727"

Is_Selected_Opportunity_Reserved{"🔀 <em></em><br/>Is Selected Opportunity Reserved ?"}:::decisions
click Is_Selected_Opportunity_Reserved "#is_selected_opportunity_reserved" "2971194260"

is_Single_Account{"🔀 <em></em><br/>is Single Account?"}:::decisions
click is_Single_Account "#is_single_account" "742991983"

is_SIngle_lead{"🔀 <em></em><br/>is Single lead"}:::decisions
click is_SIngle_lead "#is_single_lead" "939017021"

Multiple_Leads_Accounts_Chosen{"🔀 <em></em><br/>Multiple Leads/Accounts Chosen"}:::decisions
click Multiple_Leads_Accounts_Chosen "#multiple_leads_accounts_chosen" "246659998"

New_Lead{"🔀 <em></em><br/>New Lead ?"}:::decisions
click New_Lead "#new_lead" "209858866"

Valid_Brand{"🔀 <em></em><br/>Valid Brand"}:::decisions
click Valid_Brand "#valid_brand" "3525287707"

Create_Account_Visit[("➕ <em></em><br/>Create Account Visit")]:::recordCreates
click Create_Account_Visit "#create_account_visit" "1231467792"

Create_Lead_Visit[("➕ <em></em><br/>Create Lead Visit")]:::recordCreates
click Create_Lead_Visit "#create_lead_visit" "2030431970"

Create_New_Lead_ArtLeasing[("➕ <em></em><br/>Create New Lead ArtLeasing")]:::recordCreates
click Create_New_Lead_ArtLeasing "#create_new_lead_artleasing" "2688413293"

Create_New_Lead_EliteCars[("➕ <em></em><br/>Create New Lead EliteCars")]:::recordCreates
click Create_New_Lead_EliteCars "#create_new_lead_elitecars" "3530518332"

Create_New_Lead_Jetour[("➕ <em></em><br/>Create New Lead Jetour")]:::recordCreates
click Create_New_Lead_Jetour "#create_new_lead_jetour" "3644030913"

Create_Note[("➕ <em></em><br/>Create Note")]:::recordCreates
click Create_Note "#create_note" "3608290960"

Create_Visit[("➕ <em></em><br/>Create Visit")]:::recordCreates
click Create_Visit "#create_visit" "59584465"

Create_Visit_for_Selected_Account[("➕ <em></em><br/>Create Visit for Selected Account")]:::recordCreates
click Create_Visit_for_Selected_Account "#create_visit_for_selected_account" "3523688943"

Create_Visit_for_Selected_Existing_Lead[("➕ <em></em><br/>Create Visit for Selected Existing Lead")]:::recordCreates
click Create_Visit_for_Selected_Existing_Lead "#create_visit_for_selected_existing_lead" "1035724308"

Create_Visit_for_Selected_Lead[("➕ <em></em><br/>Create Visit for  Selected Lead")]:::recordCreates
click Create_Visit_for_Selected_Lead "#create_visit_for_selected_lead" "1243582063"

CreateNewLeadSoueast[("➕ <em></em><br/>Create New Lead Soueast")]:::recordCreates
click CreateNewLeadSoueast "#createnewleadsoueast" "2548420613"

Get_Branch_Unit[("🔍 <em></em><br/>Get Branch Unit")]:::recordLookups
click Get_Branch_Unit "#get_branch_unit" "3828416372"

Get_Brand_by_Parent_Branch_Name[("🔍 <em></em><br/>Get Brand by Parent Branch Name")]:::recordLookups
click Get_Brand_by_Parent_Branch_Name "#get_brand_by_parent_branch_name" "1018596795"

Get_Campaign[("🔍 <em></em><br/>Get Campaign")]:::recordLookups
click Get_Campaign "#get_campaign" "96287856"

Get_Campaign_User_Records[("🔍 <em></em><br/>Get Campaign User Records")]:::recordLookups
click Get_Campaign_User_Records "#get_campaign_user_records" "489282648"

Get_Opportunities_Related_to_Account[("🔍 <em></em><br/>Get Opportunities Related to Account")]:::recordLookups
click Get_Opportunities_Related_to_Account "#get_opportunities_related_to_account" "2260531599"

Get_Opportunities_Related_To_Account_Selected[("🔍 <em></em><br/>Get Opportunities Related To Account Selected")]:::recordLookups
click Get_Opportunities_Related_To_Account_Selected "#get_opportunities_related_to_account_selected" "1768736796"

Get_Selected_Existing_Lead[("🔍 <em></em><br/>Get Selected Existing Lead")]:::recordLookups
click Get_Selected_Existing_Lead "#get_selected_existing_lead" "868706622"

Get_Service_Appointmets_Related_to_Account[("🔍 <em></em><br/>Get Service Appointmets Related to Account")]:::recordLookups
click Get_Service_Appointmets_Related_to_Account "#get_service_appointmets_related_to_account" "937743466"

Get_Service_Appointmets_Related_to_Lead[("🔍 <em></em><br/>Get Service Appointmets Related to Lead")]:::recordLookups
click Get_Service_Appointmets_Related_to_Lead "#get_service_appointmets_related_to_lead" "737811828"

Assign_to_PG_on_Selected_Existing_Lead[("🛠️ <em></em><br/>Assign to PG on Selected Existing Lead")]:::recordUpdates
click Assign_to_PG_on_Selected_Existing_Lead "#assign_to_pg_on_selected_existing_lead" "545677185"

Copy_1_of_Flag_Assign_to_PG_on_Selected_Lead[("🛠️ <em></em><br/>Flag Assign to PG on Selected Lead")]:::recordUpdates
click Copy_1_of_Flag_Assign_to_PG_on_Selected_Lead "#copy_1_of_flag_assign_to_pg_on_selected_lead" "3103060357"

Flag_Assign_to_PG_on_Selected_Lead[("🛠️ <em></em><br/>Flag Assign to PG on Selected Lead")]:::recordUpdates
click Flag_Assign_to_PG_on_Selected_Lead "#flag_assign_to_pg_on_selected_lead" "548638884"

Account_With_Related_Opportunities_Screen(["💻 <em></em><br/>Account With Related Opportunities Screen"]):::screens
click Account_With_Related_Opportunities_Screen "#account_with_related_opportunities_screen" "3256016630"

Customer_Information_Capture_Form(["💻 <em></em><br/>Customer Information Capture Form"]):::screens
click Customer_Information_Capture_Form "#customer_information_capture_form" "977030875"

Customer_Search(["💻 <em></em><br/>Customer Search"]):::screens
click Customer_Search "#customer_search" "3312760645"

EmptyScreen(["💻 <em></em><br/>EmptyScreen"]):::screens
click EmptyScreen "#emptyscreen" "777962567"

Error_Message(["💻 <em></em><br/>Error Message"]):::screens
click Error_Message "#error_message" "4013803084"

Existing_Lead_Details(["💻 <em></em><br/>Existing Lead Details"]):::screens
click Existing_Lead_Details "#existing_lead_details" "1572634736"

Existing_Leads_Screen(["💻 <em></em><br/>Existing Leads Screen"]):::screens
click Existing_Leads_Screen "#existing_leads_screen" "2211047089"

invalid_Branch(["💻 <em></em><br/>invalid Branch"]):::screens
click invalid_Branch "#invalid_branch" "280717943"

List_of_Customers(["💻 <em></em><br/>List of Customers"]):::screens
click List_of_Customers "#list_of_customers" "3508161139"

No_Campaign(["💻 <em></em><br/>No Campaign"]):::screens
click No_Campaign "#no_campaign" "1664813024"

validbanrchscreen(["💻 <em></em><br/>validbanrchscreen"]):::screens
click validbanrchscreen "#validbanrchscreen" "508536405"

Visit_Toast_Screen(["💻 <em></em><br/>Visit Toast Screen"]):::screens
click Visit_Toast_Screen "#visit_toast_screen" "1023113943"

AL --> Decision_1
Find_Lead_Duplicates --> Existing_Lead_Found
Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1 --> Customer_Information_Capture_Form
Assign_Division_Opportunities_Size --> Get_Service_Appointmets_Related_to_Account
Assign_Filtered_Opportunities --> Account_With_Related_Opportunities_Screen
Assign_Transferred_Lead_ID --> Copy_1_of_Set_Visit_ID
Assign_Transferred_Opportunity_ID --> Copy_1_of_Set_Visit_ID
Assign_Transferred_Opportunity_ID_2 --> Copy_1_of_Set_Visit_ID
Copy_1_of_Assign_Transferred_Lead_ID --> Copy_1_of_Set_Visit_ID
Copy_1_of_Flag_Selected_Opportunity_Reserved --> Copy_1_of_Set_Visit_ID
Copy_1_of_Set_Visit_ID --> Visit_Toast_Screen
Copy_2_of_Assign_Transferred_Lead_ID --> Create_Note
Copy_2_of_Set_Visit_ID --> Copy_6_of_Assigned_To_PG
Copy_3_of_Assign_Transferred_Lead_ID --> Create_Note
Copy_4_of_Assign_Transferred_Lead_ID --> Create_Note
Copy_5_of_Assign_Transferred_Lead_ID --> Create_Note
Copy_6_of_Assign_Transferred_Lead_ID --> EmptyScreen
Flag_Selected_Opportunity_Reserved --> Copy_1_of_Set_Visit_ID
setLeadIDArtLeasing --> Copy_5_of_Assigned_To_PG
setLeadIDEliteCars --> Copy_4_of_Assigned_To_PG
setLeadIDJetour --> Copy_2_of_Assigned_To_PG
setLeadIDSoueast --> Copy_3_of_Assigned_To_PG
Assigned_To_PG --> |"Yes"| Assign_Transferred_Lead_ID
Assigned_To_PG --> |"Default Outcome"| Copy_1_of_Set_Visit_ID
Branch_Division_Type --> |"Brand Jetour"| Create_New_Lead_Jetour
Branch_Division_Type --> |"Brand Soueast"| CreateNewLeadSoueast
Branch_Division_Type --> |"Brand EliteCars"| Create_New_Lead_EliteCars
Branch_Division_Type --> |"Brand ArtLeasing"| Create_New_Lead_ArtLeasing
Branch_Division_Type --> |"Default Outcome"| invalid_Branch
Campaign_User_Found --> |"Yes Campaign"| Get_Branch_Unit
Campaign_User_Found --> |"Default Outcome"| No_Campaign
Copy_1_of_Assigned_To_PG --> |"Yes"| Copy_1_of_Assign_Transferred_Lead_ID
Copy_1_of_Assigned_To_PG --> |"Default Outcome"| Copy_1_of_Set_Visit_ID
Copy_1_of_Is_Selected_Opportunity_Reserved --> |"Reserved"| Copy_1_of_Flag_Selected_Opportunity_Reserved
Copy_1_of_Is_Selected_Opportunity_Reserved --> |"Default Outcome"| Assign_Transferred_Opportunity_ID_2
Copy_2_of_Assigned_To_PG --> |"Yes"| Copy_2_of_Assign_Transferred_Lead_ID
Copy_2_of_Assigned_To_PG --> |"Default Outcome"| Create_Note
Copy_3_of_Assigned_To_PG --> |"Yes"| Copy_3_of_Assign_Transferred_Lead_ID
Copy_3_of_Assigned_To_PG --> |"Default Outcome"| Create_Note
Copy_4_of_Assigned_To_PG --> |"Yes"| Copy_4_of_Assign_Transferred_Lead_ID
Copy_4_of_Assigned_To_PG --> |"Default Outcome"| Create_Note
Copy_5_of_Assigned_To_PG --> |"Yes"| Copy_5_of_Assign_Transferred_Lead_ID
Copy_5_of_Assigned_To_PG --> |"Default Outcome"| Create_Note
Copy_6_of_Assigned_To_PG --> |"Yes"| Copy_6_of_Assign_Transferred_Lead_ID
Copy_6_of_Assigned_To_PG --> |"Default Outcome"| EmptyScreen
Decision_1 --> |"Yes"| is_SIngle_lead
Decision_1 --> |"No"| Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1
Existing_Lead_Found --> |"No"| Branch_Division_Type
Existing_Lead_Found --> |"Default Outcome"| Existing_Leads_Screen
Is_Selected_Opportunity_Reserved --> |"Reserved"| Flag_Selected_Opportunity_Reserved
Is_Selected_Opportunity_Reserved --> |"Default Outcome"| Assign_Transferred_Opportunity_ID
is_Single_Account --> |"yes"| Get_Opportunities_Related_to_Account
is_Single_Account --> |"Default Outcome"| List_of_Customers
is_SIngle_lead --> |"yes"| Get_Service_Appointmets_Related_to_Lead
is_SIngle_lead --> |"Default Outcome"| is_Single_Account
Multiple_Leads_Accounts_Chosen --> |"New Lead Checked"| Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1
Multiple_Leads_Accounts_Chosen --> |"Lead Selected from Multiple Lead"| Flag_Assign_to_PG_on_Selected_Lead
Multiple_Leads_Accounts_Chosen --> |"Account Selected from Multiple Account"| Get_Opportunities_Related_To_Account_Selected
Multiple_Leads_Accounts_Chosen --> |"Single Lead Selected"| Copy_1_of_Flag_Assign_to_PG_on_Selected_Lead
Multiple_Leads_Accounts_Chosen --> |"Single Account Selected"| Create_Account_Visit
Multiple_Leads_Accounts_Chosen --> |"Default Outcome"| END_Multiple_Leads_Accounts_Chosen
New_Lead --> |"New Lead Clicked"| Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1
New_Lead --> |"Default Outcome"| AL
Valid_Brand --> |"Yes Valid Brand"| Customer_Search
Valid_Brand --> |"Default Outcome"| validbanrchscreen
Create_Account_Visit --> Is_Selected_Opportunity_Reserved
Create_Lead_Visit --> Copy_1_of_Assigned_To_PG
Create_New_Lead_ArtLeasing --> setLeadIDArtLeasing
Create_New_Lead_ArtLeasing -. Fault .->Error_Message
Create_New_Lead_EliteCars --> setLeadIDEliteCars
Create_New_Lead_EliteCars -. Fault .->Error_Message
Create_New_Lead_Jetour --> setLeadIDJetour
Create_New_Lead_Jetour -. Fault .->Error_Message
Create_Note --> Create_Visit
Create_Visit --> EmptyScreen
Create_Visit_for_Selected_Account --> Copy_1_of_Is_Selected_Opportunity_Reserved
Create_Visit_for_Selected_Account -. Fault .->Error_Message
Create_Visit_for_Selected_Existing_Lead --> Copy_2_of_Set_Visit_ID
Create_Visit_for_Selected_Lead --> Assigned_To_PG
Create_Visit_for_Selected_Lead -. Fault .->Error_Message
CreateNewLeadSoueast --> setLeadIDSoueast
CreateNewLeadSoueast -. Fault .->Error_Message
Get_Branch_Unit --> Get_Brand_by_Parent_Branch_Name
Get_Brand_by_Parent_Branch_Name --> Valid_Brand
Get_Campaign --> Campaign_User_Found
Get_Campaign_User_Records --> Get_Campaign
Get_Opportunities_Related_to_Account --> Assign_Division_Opportunities_Size
Get_Opportunities_Related_To_Account_Selected --> Assign_Filtered_Opportunities
Get_Selected_Existing_Lead --> Existing_Lead_Details
Get_Service_Appointmets_Related_to_Account --> List_of_Customers
Get_Service_Appointmets_Related_to_Lead --> is_Single_Account
Assign_to_PG_on_Selected_Existing_Lead --> Create_Visit_for_Selected_Existing_Lead
Copy_1_of_Flag_Assign_to_PG_on_Selected_Lead --> Create_Lead_Visit
Flag_Assign_to_PG_on_Selected_Lead --> Create_Visit_for_Selected_Lead
Account_With_Related_Opportunities_Screen --> Create_Visit_for_Selected_Account
Customer_Information_Capture_Form --> Find_Lead_Duplicates
Customer_Search --> New_Lead
EmptyScreen --> END_EmptyScreen
Error_Message --> END_Error_Message
Existing_Lead_Details --> Assign_to_PG_on_Selected_Existing_Lead
Existing_Leads_Screen --> Get_Selected_Existing_Lead
invalid_Branch --> END_invalid_Branch
List_of_Customers --> Multiple_Leads_Accounts_Chosen
No_Campaign --> END_No_Campaign
validbanrchscreen --> END_validbanrchscreen
Visit_Toast_Screen --> END_Visit_Toast_Screen
START -->  Get_Campaign_User_Records
END_Multiple_Leads_Accounts_Chosen(( END )):::endClass
END_EmptyScreen(( END )):::endClass
END_Error_Message(( END )):::endClass
END_invalid_Branch(( END )):::endClass
END_No_Campaign(( END )):::endClass
END_validbanrchscreen(( END )):::endClass
END_Visit_Toast_Screen(( END )):::endClass


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
|Label|EGH Product Genius Flow|
|Status|Active|
|Description|Flow for Product Genius Application|
|Environments|Default|
|Interview Label|EGH Product Genius Flow {!$Flow.CurrentDateTime}|
|Run In Mode| System Mode Without Sharing|
| Builder Type (PM)|LightningFlowBuilder|
| Canvas Mode (PM)|AUTO_LAYOUT_CANVAS|
| Origin Builder Type (PM)|LightningFlowBuilder|
|Connector|[Get_Campaign_User_Records](#get_campaign_user_records)|
|Next Node|[Get_Campaign_User_Records](#get_campaign_user_records)|


## Variables

|Name|Data Type|Is Collection|Is Input|Is Output|Object Type|Description|
|:-- |:--:|:--:|:--:|:--:|:--:|:--  |
|BranchSpecificOpportunities|SObject|✅|⬜|⬜|Opportunity|<!-- -->|
|BranchSpecificOpportunitiesCount|Number|⬜|⬜|⬜|<!-- -->|<!-- -->|
|currentItem_Filter_Branch_Specific_Opportunities|SObject|⬜|⬜|⬜|Opportunity|<!-- -->|
|currentItem_Filter_Division_Opportunities|SObject|⬜|⬜|⬜|Opportunity|<!-- -->|
|DependentPicklistValues|Apex|✅|⬜|⬜|<!-- -->|<!-- -->|
|ListLeads|SObject|✅|⬜|⬜|Lead|List of Leads from the search|
|PotentialDuplicateInDifferentBranch|Boolean|⬜|⬜|⬜|<!-- -->|<!-- -->|
|ReservedOpportunity|Boolean|⬜|⬜|⬜|<!-- -->|<!-- -->|
|ReservedOpportunityPreferredBranch|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|selectedBrand|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|TransferredLeadId|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|TransferredOpportunityId|String|⬜|⬜|⬜|<!-- -->|<!-- -->|
|varLeadRecord|SObject|⬜|⬜|⬜|Lead|<!-- -->|
|varLeadRecordCollection|SObject|✅|⬜|⬜|Lead|<!-- -->|
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
|VehicleModelsPicklistOptions|Apex|✅|⬜|⬜|<!-- -->|<!-- -->|


## Formulas

|Name|Data Type|Expression|Description|
|:-- |:--:|:-- |:--  |
|Lead_Link_Formula|String|LEFT({!$Api.Partner_Server_URL_620}, FIND( '/services', {!$Api.Partner_Server_URL_620})) & {!TransferredLeadId}|<!-- -->|
|Opportunity_Link_Formula|String|LEFT({!$Api.Partner_Server_URL_620}, FIND( '/services', {!$Api.Partner_Server_URL_620})) & {!TransferredOpportunityId}|<!-- -->|
|userRole|String|{!$UserRole.DeveloperName}|<!-- -->|
|varCurrentDateTime|DateTime|NOW()|<!-- -->|
|varEndDateTime|DateTime|NOW() + (10 / 1440)|<!-- -->|
|varleadSource|String|IF({!$UserRole.Name}=='Product Genius','Event','Walk-In')|<!-- -->|
|varStartDateTime|DateTime|NOW()|<!-- -->|
|varVisitNameAccountSingle|String|"Visit for " + {!AL.accountSingle.Name}+" on " +TEXT(NOW())|<!-- -->|
|varVisitNameExistingLead|String|"Visit for " +{!Get_Selected_Existing_Lead.Name}+" on " +TEXT(NOW())|<!-- -->|
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
|Brand (input)|Get_Campaign.EGH_Brand__c|
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
|Brand (input)|Get_Campaign.EGH_Brand__c|
|Email (input)|Copy_1_of_Email.value|
|First Name (input)|Copy_1_of_First_Name|
|Last Name (input)|Copy_1_of_Last_Name|
|Mobile Phone (input)|Mobile.value|
|Connector|[Existing_Lead_Found](#existing_lead_found)|


### Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Action Call|
|Label|Transform semicolon-separated string values to Picklist Options Action 1|
|Action Type|Apex|
|Action Name|[EGH_StringToPicklistOptions](../apex/EGH_StringToPicklistOptions.md)|
|Flow Transaction Model|Automatic|
|Name Segment|EGH_StringToPicklistOptions|
|Offset|0|
|Output Parameters|assignToReference: VehicleModelsPicklistOptions<br/>name: output<br/>|
|Semicolon Separated String (input)|Get_Campaign.EGH_Vehicle_Models__c|
|Connector|[Customer_Information_Capture_Form](#customer_information_capture_form)|


### Assign_Division_Opportunities_Size

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Division Opportunities Size|
|Connector|[Get_Service_Appointmets_Related_to_Account](#get_service_appointmets_related_to_account)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varOpportunityListRelatedtoAccountSize| Assign Count|varOpportunityListRelatedtoAccount|




### Assign_Filtered_Opportunities

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Filtered Opportunities|
|Connector|[Account_With_Related_Opportunities_Screen](#account_with_related_opportunities_screen)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|BranchSpecificOpportunitiesCount| Assign Count|varOpportunityListSecondScreen|




### Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|leadCustomTable.outputSelectedRow.Id|




### Assign_Transferred_Opportunity_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Opportunity ID|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredOpportunityId| Assign|Opportunities.firstSelectedRow.Id|




### Assign_Transferred_Opportunity_ID_2

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Opportunity ID|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredOpportunityId| Assign|OpportunitiesAccount.firstSelectedRow.Id|




### Copy_1_of_Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|AL.leadSingle.Id|




### Copy_1_of_Flag_Selected_Opportunity_Reserved

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Flag Selected Opportunity Reserved|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|ReservedOpportunity| Assign|✅|
|ReservedOpportunityPreferredBranch| Assign|OpportunitiesAccount.firstSelectedRow.EGH_BranchUnitLookup__r.Name|




### Copy_1_of_Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[Visit_Toast_Screen](#visit_toast_screen)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Lead_Visit](#create_lead_visit)|




### Copy_2_of_Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|varNewLeadID|




### Copy_2_of_Set_Visit_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Set Visit ID|
|Connector|[Copy_6_of_Assigned_To_PG](#copy_6_of_assigned_to_pg)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varVisitID| Assign|[Create_Visit_for_Selected_Existing_Lead](#create_visit_for_selected_existing_lead)|




### Copy_3_of_Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|varNewLeadID|




### Copy_4_of_Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|varNewLeadID|




### Copy_5_of_Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[Create_Note](#create_note)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|varNewLeadID|




### Copy_6_of_Assign_Transferred_Lead_ID

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Assign Transferred Lead ID|
|Connector|[EmptyScreen](#emptyscreen)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|TransferredLeadId| Assign|Get_Selected_Existing_Lead.Id|




### Flag_Selected_Opportunity_Reserved

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|Flag Selected Opportunity Reserved|
|Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|ReservedOpportunity| Assign|✅|
|ReservedOpportunityPreferredBranch| Assign|Opportunities.firstSelectedRow.EGH_BranchUnitLookup__r.Name|




### setLeadIDArtLeasing

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDArtLeasing](#setleadidartleasing)|
|Connector|[Copy_5_of_Assigned_To_PG](#copy_5_of_assigned_to_pg)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[Create_New_Lead_ArtLeasing](#create_new_lead_artleasing)|




### setLeadIDEliteCars

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDEliteCars](#setleadidelitecars)|
|Connector|[Copy_4_of_Assigned_To_PG](#copy_4_of_assigned_to_pg)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[Create_New_Lead_EliteCars](#create_new_lead_elitecars)|




### setLeadIDJetour

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDJetour](#setleadidjetour)|
|Connector|[Copy_2_of_Assigned_To_PG](#copy_2_of_assigned_to_pg)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[Create_New_Lead_Jetour](#create_new_lead_jetour)|




### setLeadIDSoueast

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Assignment|
|Label|[setLeadIDSoueast](#setleadidsoueast)|
|Connector|[Copy_3_of_Assigned_To_PG](#copy_3_of_assigned_to_pg)|


#### Assignments

|Assign To Reference|Operator|Value|
|:-- |:--:|:--: |
|varNewLeadID| Assign|[CreateNewLeadSoueast](#createnewleadsoueast)|




### Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|
|Default Connector Label|Default Outcome|


#### Rule Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Assign_Transferred_Lead_ID](#assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG2| Equal To|✅|




### Branch_Division_Type

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Branch/Division Type|
|Default Connector|[invalid_Branch](#invalid_branch)|
|Default Connector Label|Default Outcome|


#### Rule Brand_Jetour (Brand Jetour)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_New_Lead_Jetour](#create_new_lead_jetour)|
|Condition Logic|or|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Get_Campaign.EGH_Brand__c| Equal To|Jetour|




#### Rule Brand_Soueast (Brand Soueast)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[CreateNewLeadSoueast](#createnewleadsoueast)|
|Condition Logic|or|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Get_Campaign.EGH_Brand__c| Equal To|Soueast|




#### Rule Brand_EliteCars (Brand EliteCars)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_New_Lead_EliteCars](#create_new_lead_elitecars)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Get_Campaign.EGH_Brand__c| Equal To|Elite|




#### Rule Brand_ArtLeasing (Brand ArtLeasing)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Create_New_Lead_ArtLeasing](#create_new_lead_artleasing)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Get_Campaign.EGH_Brand__c| Equal To|ArtLeasing|




### Campaign_User_Found

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Campaign User Found|
|Default Connector|[No_Campaign](#no_campaign)|
|Default Connector Label|Default Outcome|


#### Rule Yes_Campaign (Yes Campaign)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Branch_Unit](#get_branch_unit)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|[Get_Campaign_User_Records](#get_campaign_user_records)| Is Null|⬜|




### Copy_1_of_Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[Copy_1_of_Set_Visit_ID](#copy_1_of_set_visit_id)|
|Default Connector Label|Default Outcome|


#### Rule Copy_1_of_Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_1_of_Assign_Transferred_Lead_ID](#copy_1_of_assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG2| Equal To|✅|




### Copy_1_of_Is_Selected_Opportunity_Reserved

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Selected Opportunity Reserved ?|
|Default Connector|[Assign_Transferred_Opportunity_ID_2](#assign_transferred_opportunity_id_2)|
|Default Connector Label|Default Outcome|


#### Rule Copy_1_of_Reserved (Reserved)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_1_of_Flag_Selected_Opportunity_Reserved](#copy_1_of_flag_selected_opportunity_reserved)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|OpportunitiesAccount.firstSelectedRow.StageName| Equal To|Reserved/Pre Booked|




### Copy_2_of_Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[Create_Note](#create_note)|
|Default Connector Label|Default Outcome|


#### Rule Copy_2_of_Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_2_of_Assign_Transferred_Lead_ID](#copy_2_of_assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG| Equal To|✅|




### Copy_3_of_Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[Create_Note](#create_note)|
|Default Connector Label|Default Outcome|


#### Rule Copy_3_of_Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_3_of_Assign_Transferred_Lead_ID](#copy_3_of_assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG| Equal To|✅|




### Copy_4_of_Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[Create_Note](#create_note)|
|Default Connector Label|Default Outcome|


#### Rule Copy_4_of_Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_4_of_Assign_Transferred_Lead_ID](#copy_4_of_assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG| Equal To|✅|




### Copy_5_of_Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[Create_Note](#create_note)|
|Default Connector Label|Default Outcome|


#### Rule Copy_5_of_Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_5_of_Assign_Transferred_Lead_ID](#copy_5_of_assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG| Equal To|✅|




### Copy_6_of_Assigned_To_PG

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Assigned To PG ?|
|Default Connector|[EmptyScreen](#emptyscreen)|
|Default Connector Label|Default Outcome|


#### Rule Copy_6_of_Yes (Yes)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_6_of_Assign_Transferred_Lead_ID](#copy_6_of_assign_transferred_lead_id)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|AssignToPG3| Equal To|✅|




### Decision_1

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Exists Lead or Customer?|
|Description|Validate if a Lead or Customer with these data exists|
|Default Connector|[Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1](#transform_semicolon_separated_string_values_to_picklist_options_action_1)|
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




### Is_Selected_Opportunity_Reserved

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Is Selected Opportunity Reserved ?|
|Default Connector|[Assign_Transferred_Opportunity_ID](#assign_transferred_opportunity_id)|
|Default Connector Label|Default Outcome|


#### Rule Reserved (Reserved)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Flag_Selected_Opportunity_Reserved](#flag_selected_opportunity_reserved)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Opportunities.firstSelectedRow.StageName| Equal To|Reserved/Pre Booked|




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
|Connector|isGoTo: true<br/>targetReference: Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1<br/>|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|NewLeadButton2.wasButtonClicked| Equal To|✅|




#### Rule Lead_Selected_from_Multiple_Lead (Lead Selected from Multiple Lead)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Flag_Assign_to_PG_on_Selected_Lead](#flag_assign_to_pg_on_selected_lead)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|leadCustomTable.numberOfRowsSelected| Greater Than|numberValue: 0<br/>|




#### Rule Account_Selected_from_Multiple_Account (Account Selected from Multiple Account)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Get_Opportunities_Related_To_Account_Selected](#get_opportunities_related_to_account_selected)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|customerCustomTable.numberOfRowsSelected| Greater Than|numberValue: 0<br/>|




#### Rule Single_Lead_Selected (Single Lead Selected)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Copy_1_of_Flag_Assign_to_PG_on_Selected_Lead](#copy_1_of_flag_assign_to_pg_on_selected_lead)|
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
|Connector|[Transform_semicolon_separated_string_values_to_Picklist_Options_Action_1](#transform_semicolon_separated_string_values_to_picklist_options_action_1)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|NewLeadButton.wasButtonClicked| Equal To|✅|




### Valid_Brand

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Decision|
|Label|Valid Brand|
|Default Connector|[validbanrchscreen](#validbanrchscreen)|
|Default Connector Label|Default Outcome|


#### Rule Yes_Valid_Brand (Yes Valid Brand)

|<!-- -->|<!-- -->|
|:---|:---|
|Connector|[Customer_Search](#customer_search)|
|Condition Logic|and|




|Condition Id|Left Value Reference|Operator|Right Value|
|:-- |:-- |:--:|:--: |
|1|Get_Branch_Unit.Id| Is Null|⬜|
|2|selectedBrand| Is Null|⬜|




### Create_Account_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Account Visit|
|Store Output Automatically|✅|
|Connector|[Is_Selected_Opportunity_Reserved](#is_selected_opportunity_reserved)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AccountLookup__c|AL.accountSingle.Id|
|EGH_Brand__c|Get_Campaign.EGH_Brand__c|
|EGH_CampaignUserLookup__c|Get_Campaign_User_Records.Id|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_RelatedShowroomBranch__c|Get_Branch_Unit.Id|
|EGH_SR_Opportunity__c|Opportunities.firstSelectedRow.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|Name|varVisitNameAccountSingle|
|PurposeVisit__c|Event|
|Route_to_Sales__c|⬜|




### Create_Lead_Visit

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Lead Visit|
|Store Output Automatically|✅|
|Connector|[Copy_1_of_Assigned_To_PG](#copy_1_of_assigned_to_pg)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|Get_Campaign.EGH_Brand__c|
|EGH_CampaignUserLookup__c|Get_Campaign_User_Records.Id|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|AL.leadSingle.Id|
|EGH_RelatedShowroomBranch__c|Get_Branch_Unit.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|AL.leadSingle.EGH_Model_of_Interest__c|
|Name|varVisitNameLeadSingle|
|PurposeVisit__c|Event|
|Route_to_Sales__c|⬜|




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
|EGH_AssignToPG__c|AssignToPG|
|EGH_BranchCode__c|Get_Branch_Unit.BranchCode|
|EGH_BrandListPicklist__c|Get_Campaign.EGH_Brand__c|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|Get_Branch_Unit.Id|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|Model_of_Interest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Event|
|MobilePhone|Mobile.value|
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
|EGH_AssignToPG__c|AssignToPG|
|EGH_BranchCode__c|Get_Branch_Unit.BranchCode|
|EGH_BrandListPicklist__c|Get_Campaign.EGH_Brand__c|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|Get_Branch_Unit.Id|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|Model_of_Interest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|EGH_TheEliteCarsEmailOptinCheckbox__c|Email|
|EGH_TheEliteCarsPhoneOptinCheckbox__c|Phone|
|EGH_TheEliteCarsSMSOptinCheckbox__c|SMS|
|EGH_TheEliteCarsWhatsAppOptinCheckbox__c|Whatsapp|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Event|
|MobilePhone|Mobile.value|
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
|EGH_AssignToPG__c|AssignToPG|
|EGH_BranchCode__c|Get_Branch_Unit.BranchCode|
|EGH_BrandListPicklist__c|Get_Campaign.EGH_Brand__c|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_JetourEmailOptinCheckbox__c|Email|
|EGH_JetourPhoneOptinCheckbox__c|Phone|
|EGH_JetourSMSOptinCheckbox__c|SMS|
|EGH_JetourWhatsAppOptinCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|Get_Branch_Unit.Id|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|Model_of_Interest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Event|
|MobilePhone|Mobile.value|
|RecordTypeId|Lead_Type|
|Salutation|Salutationpicklist|




### Create_Note

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|Note|
|Label|Create Note|
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
|Store Output Automatically|✅|
|Connector|[EmptyScreen](#emptyscreen)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|Get_Campaign.EGH_Brand__c|
|EGH_CampaignUserLookup__c|Get_Campaign_User_Records.Id|
|EGH_CommentsRichText__c|Comments|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|varNewLeadID|
|EGH_RelatedShowroomBranch__c|Get_Branch_Unit.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|Model_of_Interest|
|Name|varVisitNameNewCustomer|
|PurposeVisit__c|Event|
|Route_to_Sales__c|⬜|




### Create_Visit_for_Selected_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit for Selected Account|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[Copy_1_of_Is_Selected_Opportunity_Reserved](#copy_1_of_is_selected_opportunity_reserved)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AccountLookup__c|customerCustomTable.selectedRowKeyValue|
|EGH_Brand__c|Get_Campaign.EGH_Brand__c|
|EGH_CampaignUserLookup__c|Get_Campaign_User_Records.Id|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_RelatedShowroomBranch__c|Get_Branch_Unit.Id|
|EGH_SR_Opportunity__c|OpportunitiesAccount.firstSelectedRow.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|Name|varVisitNameMultipleCustomer|
|PurposeVisit__c|Event|
|Route_to_Sales__c|⬜|




### Create_Visit_for_Selected_Existing_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit for Selected Existing Lead|
|Store Output Automatically|✅|
|Connector|[Copy_2_of_Set_Visit_ID](#copy_2_of_set_visit_id)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|Get_Campaign.EGH_Brand__c|
|EGH_CampaignUserLookup__c|Get_Campaign_User_Records.Id|
|EGH_CommentsRichText__c|Get_Selected_Existing_Lead.Description|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|Get_Selected_Existing_Lead.Id|
|EGH_RelatedShowroomBranch__c|Get_Branch_Unit.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|Get_Selected_Existing_Lead.EGH_Model_of_Interest__c|
|Name|varVisitNameExistingLead|
|PurposeVisit__c|Event|
|Route_to_Sales__c|⬜|




### Create_Visit_for_Selected_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Create|
|Object|EGH_ShowroomVisit__c|
|Label|Create Visit for  Selected Lead|
|Fault Connector|isGoTo: true<br/>targetReference: Error_Message<br/>|
|Store Output Automatically|✅|
|Connector|[Assigned_To_PG](#assigned_to_pg)|


#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_Brand__c|Get_Campaign.EGH_Brand__c|
|EGH_CampaignUserLookup__c|Get_Campaign_User_Records.Id|
|EGH_CommentsRichText__c|leadCustomTable.outputSelectedRow.Description|
|EGH_EndDateTime__c|varEndDateTime|
|EGH_LeadLookup__c|leadCustomTable.selectedRowKeyValue|
|EGH_RelatedShowroomBranch__c|Get_Branch_Unit.Id|
|EGH_StartDateTime__c|varStartDateTime|
|EGH_Status__c|New|
|EGH_Vehicle_Of_Interest__c|leadCustomTable.outputSelectedRow.EGH_Model_of_Interest__c|
|Name|varVisitNameMuletipleLead|
|PurposeVisit__c|Event|
|Route_to_Sales__c|⬜|




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
|EGH_AssignToPG__c|AssignToPG|
|EGH_BranchCode__c|Get_Branch_Unit.BranchCode|
|EGH_BrandListPicklist__c|Get_Campaign.EGH_Brand__c|
|EGH_ConsentEmailCheckbox__c|Email|
|EGH_ConsentPhoneCheckbox__c|Phone|
|EGH_ConsentSMSCheckbox__c|SMS|
|EGH_ConsentWhatsAppCheckbox__c|Whatsapp|
|EGH_LeadBranchUnitLookup__c|Get_Branch_Unit.Id|
|EGH_LeadLanguagePicklist__c|Language|
|EGH_LeadTypePicklist__c|Sales|
|EGH_Model_of_Interest__c|Model_of_Interest|
|EGH_PotentialLeadInDifferentShowroom__c|PotentialDuplicateInDifferentBranch|
|EGH_SoueastEmailOptinCheckbox__c|Email|
|EGH_SoueastPhoneOptinCheckbox__c|Phone|
|EGH_SoueastSMSOptinCheckbox__c|SMS|
|EGH_SoueastWhatsAppOptinCheckbox__c|Whatsapp|
|Email|Copy_1_of_Email.value|
|FirstName|Copy_1_of_First_Name|
|LastName|Copy_1_of_Last_Name|
|LeadSource|Event|
|MobilePhone|Mobile.value|
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
|Connector|[Get_Brand_by_Parent_Branch_Name](#get_brand_by_parent_branch_name)|


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
|Connector|[Valid_Brand](#valid_brand)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|EGH_ParentBranchName__c| Equal To|Get_Branch_Unit.ParentBranchUnit.Name|




### Get_Campaign

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Campaign|
|Label|Get Campaign|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Campaign_User_Found](#campaign_user_found)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|Get_Campaign_User_Records.EGH_Associated_Campaign__c|




### Get_Campaign_User_Records

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|EGH_Campaign_User__c|
|Label|Get Campaign User Records|
|Assign Null Values If No Records Found|⬜|
|Get First Record Only|✅|
|Store Output Automatically|✅|
|Connector|[Get_Campaign](#get_campaign)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|EGH_Campaign_User__c| Equal To|$User.Id|
|2|EGH_Campaign_End_Date_Time__c| Greater Than Or Equal To|varCurrentDateTime|
|3|Campaign_Start_Date_Time__c| Less Than Or Equal To|varCurrentDateTime|




### Get_Opportunities_Related_to_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Opportunity|
|Label|Get Opportunities Related to Account|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varOpportunityListRelatedtoAccount|
|Queried Fields|- Id<br/>- Name<br/>- Amount<br/>- StageName<br/>- AccountId<br/>- OwnerId<br/>- EGH_Branch_Name__c<br/>- EGH_Brand__c<br/>- Sales_Representative__c<br/>- LastModifiedDate<br/>- EGH_BranchUnitLookup__c<br/>|
|Connector|[Assign_Division_Opportunities_Size](#assign_division_opportunities_size)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|StageName| Not Equal To|Closed Lost|
|2|StageName| Not Equal To|Closed Won|
|3|AccountId| Equal To|AL.accountSingle.Id|
|4|IsClosed| Equal To|⬜|




### Get_Opportunities_Related_To_Account_Selected

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|Opportunity|
|Label|Get Opportunities Related To Account Selected|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varOpportunityListSecondScreen|
|Queried Fields|- Id<br/>- Name<br/>- Amount<br/>- StageName<br/>- AccountId<br/>- CloseDate<br/>- CreatedDate<br/>- Sales_Representative__c<br/>- OwnerId<br/>- EGH_Branch_Name__c<br/>- EGH_Brand__c<br/>- LastModifiedDate<br/>- EGH_BranchUnitLookup__c<br/>|
|Connector|[Assign_Filtered_Opportunities](#assign_filtered_opportunities)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|AccountId| Equal To|customerCustomTable.outputSelectedRow.Id|
|2|IsClosed| Equal To|⬜|
|3|StageName| Not Equal To|Closed Won|
|4|StageName| Not Equal To|Closed Lost|




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




### Get_Service_Appointmets_Related_to_Account

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Lookup|
|Object|ServiceAppointment|
|Label|Get Service Appointmets Related to Account|
|Assign Null Values If No Records Found|⬜|
|Output Reference|varServiceAppointmentRelatedToAccount|
|Queried Fields|- Id<br/>- Status<br/>- AppointmentNumber<br/>- Subject<br/>- DueDate<br/>- Service_Territory_Name__c<br/>- Visit_Type_Name__c<br/>|
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
|Queried Fields|- Id<br/>- Status<br/>- AppointmentNumber<br/>- Subject<br/>- DueDate<br/>- Service_Territory_Name__c<br/>- Visit_Type_Name__c<br/>|
|Connector|[is_Single_Account](#is_single_account)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|ParentRecordId| Equal To|AL.leadSingle.Id|
|2|Status| Not Equal To|Completed|
|3|Status| Not Equal To|Canceled|




### Assign_to_PG_on_Selected_Existing_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Object|Lead|
|Label|Assign to PG on Selected Existing Lead|
|Connector|[Create_Visit_for_Selected_Existing_Lead](#create_visit_for_selected_existing_lead)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|Get_Selected_Existing_Lead.Id|
|2|EGH_AssignToPG__c| Not Equal To|AssignToPG3|




#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AssignToPG__c|AssignToPG3|




### Copy_1_of_Flag_Assign_to_PG_on_Selected_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Object|Lead|
|Label|Flag Assign to PG on Selected Lead|
|Connector|[Create_Lead_Visit](#create_lead_visit)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|AL.leadSingle.Id|
|2|EGH_AssignToPG__c| Not Equal To|AssignToPG2|




#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AssignToPG__c|AssignToPG2|




### Flag_Assign_to_PG_on_Selected_Lead

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Record Update|
|Object|Lead|
|Label|Flag Assign to PG on Selected Lead|
|Connector|[Create_Visit_for_Selected_Lead](#create_visit_for_selected_lead)|


#### Filters (logic: **and**)

|Filter Id|Field|Operator|Value|
|:-- |:-- |:--:|:--: |
|1|Id| Equal To|leadCustomTable.outputSelectedRow.Id|
|2|EGH_AssignToPG__c| Not Equal To|AssignToPG2|




#### Input Assignments

|Field|Value|
|:-- |:--: |
|EGH_AssignToPG__c|AssignToPG2|




### Account_With_Related_Opportunities_Screen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Account With Related Opportunities Screen|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|✅|
|Connector|[Create_Visit_for_Selected_Account](#create_visit_for_selected_account)|


#### AccountName

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Name : {!customerCustomTable.outputSelectedRow.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column1](#customer_details_column1)|




#### AccountPhone

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Phone : {!customerCustomTable.outputSelectedRow.PersonMobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column1](#customer_details_column1)|




#### AccountLanguage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Language : {!customerCustomTable.outputSelectedRow.EGH_ContactLanguagePicklist__pc}</strong></p>|
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
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Email : {!customerCustomTable.outputSelectedRow.PersonEmail}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Customer_Details_Column2](#customer_details_column2)|




#### AccountNationality

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong style="background-color: rgb(255, 255, 255);">Nationality : {!customerCustomTable.outputSelectedRow.EGH_ContactNationalityPicklist__pc}</strong></p>|
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




#### OpportunitiesAccount

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type Mappings|typeName: T<br/>typeValue: Opportunity<br/>|
|Extension Name|flowruntime:datatable|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Label (input)|Opportunity List|
|Selection Mode (input)|SINGLE_SELECT|
|Min Row Selection (input)|1|
|Should Display Label (input)|✅|
|Table Data (input)|varOpportunityListSecondScreen|
|Max Row Selection (input)|1|
|Columns (input)|[{"apiName":"Name","guid":"column-d714","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Name","type":"text"},{"apiName":"Sales_Representative__c","guid":"column-19a3","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Sales Representative","type":"customRichText"},{"apiName":"StageName","guid":"column-c9f5","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Stage","type":"text"},{"apiName":"EGH_Brand__c","guid":"column-9f53","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"sortable":false,"label":"Brand","type":"text"},{"apiName":"EGH_Branch_Name__c","guid":"column-54c3","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"sortable":false,"label":"Branch Name","type":"customRichText"},{"apiName":"LastModifiedDate","guid":"column-a977","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"sortable":false,"label":"Last Modified Date","type":"customDateTime"}]|




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
|Validation Rule|errorMessage: >-<br/>&nbsp;&nbsp;<p><span style=background-color: rgb(255, 255, 255); color: rgb(255, 0,<br/>&nbsp;&nbsp;0);>Please enter a valid email address.</span></p><br/>formulaExpression: >-<br/>&nbsp;&nbsp;OR(<br/>&nbsp;&nbsp;&nbsp;ISBLANK({!Copy_1_of_Email.value}),<br/>&nbsp;&nbsp;&nbsp;REGEX({!Copy_1_of_Email.value},<br/>&nbsp;&nbsp;^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,4}$)<br/>&nbsp;&nbsp;&nbsp;)<br/>|
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




#### Mobile

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|flowruntime:phone|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Validation Rule|errorMessage: >-<br/>&nbsp;&nbsp;<p><span style=background-color: rgb(255, 255, 255); color: rgb(255, 0,<br/>&nbsp;&nbsp;0);>Mobile Number must start with +971 or 00971 followed by 9<br/>&nbsp;&nbsp;digits.</span></p><br/>formulaExpression: |-<br/>&nbsp;&nbsp;REGEX(<br/>&nbsp;&nbsp;{!Mobile.value},<br/>&nbsp;&nbsp;^(\\+971[0-9]{9}|00971[0-9]{9})$<br/>&nbsp;&nbsp;)<br/>|
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




#### Model_of_Interest

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|ModelOfInterestChoices|
|Field Text|Model of Interest|
|Field Type| Dropdown Box|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
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




#### Language

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|String|
|Choice References|EGHLeadLanguage|
|Default Value|English|
|Field Text|Language|
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




#### AssignToPG

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|{!$Label.EGH_AssignToPG}|
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
|Connector|[New_Lead](#new_lead)|


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
|Help Text|<p>Please enter First Name,Last Name,Mobile Number or Email of the Customerw</p>|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|⬜|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Validation Rule|errorMessage: >-<br/>&nbsp;&nbsp;<p><span style=color: rgb(231, 12, 12);>No special characters allowed except<br/>&nbsp;&nbsp;.,@,+ and minimum length is 3 characters.</span></p><br/>formulaExpression: REGEX({!Search}, ^[a-zA-Z0-9.@+ ]{3,}$)<br/>|




### EmptyScreen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|[EmptyScreen](#emptyscreen)|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|⬜|
|Show Header|⬜|


#### SuccesToast

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eGH_GenericToastMessage|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Var Toast Message (input)|Lead Captured Successfully|
|Var Toast Label (input)|Success|
|Var Toast Variant (input)|success|
|Var Auto Finish Flow (input)|✅|
|Var Delay Before Finish (input)|5000|




#### Lead_Link_2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><span style="font-size: 16px;">View Lead : </span><a href="{!Lead_Link_Formula}" rel="noopener noreferrer" target="_blank" style="font-size: 16px;">{!Lead_Link_Formula}</a></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: TransferredLeadId<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|




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




#### errorToastMessage

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eGH_GenericToastMessage|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Var Toast Message (input)|Lead Capture has Failed|
|Var Toast Label (input)|Error|
|Var Toast Variant (input)|error|
|Var Auto Finish Flow (input)|✅|
|Var Delay Before Finish (input)|2000|




### Existing_Lead_Details

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Existing Lead Details|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|✅|
|Connector|[Assign_to_PG_on_Selected_Existing_Lead](#assign_to_pg_on_selected_existing_lead)|


#### ExistingLeadName

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Name : {!Get_Selected_Existing_Lead.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Existing_Lead_Details_Section1_Column1](#existing_lead_details_section1_column1)|




#### ExistingLeadPhone

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Phone: {!Get_Selected_Existing_Lead.MobilePhone}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Existing_Lead_Details_Section1_Column1](#existing_lead_details_section1_column1)|




#### ExistingLeadModelOfInterest

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Model of Interest : {!Get_Selected_Existing_Lead.EGH_Model_of_Interest__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Existing_Lead_Details_Section1_Column1](#existing_lead_details_section1_column1)|




#### Existing_Lead_Details_Section1_Column1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Existing_Lead_Details_Section1](#existing_lead_details_section1)|
|Width (input)|6|




#### ExistingLeadEmail

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Email : {!Get_Selected_Existing_Lead.Email}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Existing_Lead_Details_Section1_Column2](#existing_lead_details_section1_column2)|




#### ExistingLeadBranch

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Branch : {!Get_Selected_Existing_Lead.EGH_LeadBranchUnitLookup__r.Name}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Existing_Lead_Details_Section1_Column2](#existing_lead_details_section1_column2)|




#### ExistingLeadOwner

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><strong>Owner : {!Get_Selected_Existing_Lead.EGH_Lead_Owner__c}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Parent Field|[Existing_Lead_Details_Section1_Column2](#existing_lead_details_section1_column2)|




#### Existing_Lead_Details_Section1_Column2

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region|
|Is Required|⬜|
|Parent Field|[Existing_Lead_Details_Section1](#existing_lead_details_section1)|
|Width (input)|6|




#### Existing_Lead_Details_Section1

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Region Container|
|Is Required|⬜|
|Region Container Type| Section Without Header|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### AssignToPG3

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|{!$Label.EGH_AssignToPG}|
|Field Type| Input Field|
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
|Show Header|⬜|
|Connector|[Get_Selected_Existing_Lead](#get_selected_existing_lead)|


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
|Max Row Selection (input)|1|
|Columns (input)|[{"apiName":"Name","guid":"column-092c","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Full Name","type":"text"},{"apiName":"Email","guid":"column-2260","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Email","type":"email"},{"apiName":"MobilePhone","guid":"column-3105","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Mobile Phone","type":"phone"},{"apiName":"Status","guid":"column-9320","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"sortable":false,"label":"Status","type":"text"}]|
|Should Display Label (input)|✅|




#### DuplicateError

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p><span style="color: rgb(237, 14, 14); background-color: rgb(255, 255, 255);">Error trying to find Lead duplicates : {!Find_Lead_Duplicates.findDuplicatesErrorList}</span></p>|
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




### invalid_Branch

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|invalid Branch|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|✅|


#### invalidBranch

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(247, 0, 0); background-color: rgb(255, 255, 255);">Your Campaign must have a valid brand selected.It must be either Jetour,Soueast,ArtLeasing or Elite.</strong></p>|
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
|Connector|[Multiple_Leads_Accounts_Chosen](#multiple_leads_accounts_chosen)|


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




#### CustomerPhone

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
|Label (input)|Select an Opportunity|
|Selection Mode (input)|SINGLE_SELECT|
|Min Row Selection (input)|1|
|Table Data (input)|varOpportunityListRelatedtoAccount|
|Should Display Label (input)|✅|
|Columns (input)|[{"apiName":"Name","guid":"column-b611","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Name","type":"text"},{"apiName":"Sales_Representative__c","guid":"column-de9d","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Sales Representative","type":"customRichText"},{"apiName":"StageName","guid":"column-ac91","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Stage","type":"text"},{"apiName":"EGH_Brand__c","guid":"column-637d","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"sortable":false,"label":"Brand","type":"text"},{"apiName":"EGH_Branch_Name__c","guid":"column-c8bc","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"sortable":false,"label":"Branch Name","type":"customRichText"},{"apiName":"LastModifiedDate","guid":"column-49ba","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"sortable":false,"label":"Last Modified Date","type":"customDateTime"}]|
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
|Columns (input)|[{"apiName":"AppointmentNumber","guid":"column-d745","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":0,"label":"Appointment Number","type":"text"},{"apiName":"Status","guid":"column-57d5","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":1,"label":"Status","type":"text"},{"apiName":"DueDate","guid":"column-eb9e","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":2,"label":"Due Date","type":"customDateTime"},{"apiName":"Subject","guid":"column-3e44","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":3,"label":"Subject","type":"text"},{"apiName":"Service_Territory_Name__c","guid":"column-1fda","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":4,"label":"Service Territory Name","type":"customRichText"},{"apiName":"Visit_Type_Name__c","guid":"column-2b00","editable":false,"hasCustomHeaderLabel":false,"customHeaderLabel":"","wrapText":true,"order":5,"label":"Visit Type Name","type":"customRichText"}]|
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
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: Get_Service_Appointmets_Related_to_Lead<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|
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




#### linebreak4

|<!-- -->|<!-- -->|
|:---|:---|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




#### AssignToPG2

|<!-- -->|<!-- -->|
|:---|:---|
|Data Type|Boolean|
|Field Text|{!$Label.EGH_AssignToPG}|
|Field Type| Input Field|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: AL.leadSize<br/>&nbsp;&nbsp;operator: GreaterThan<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;numberValue: 0<br/>|




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




### No_Campaign

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|No Campaign|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|⬜|


#### NoCampaignText

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(234, 9, 9);">No Associated Campaign Found.Please Check With Product Genius Admin.</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### validbanrchscreen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|[validbanrchscreen](#validbanrchscreen)|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|✅|
|Show Header|⬜|


#### ValidBrand

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(247, 0, 0);">Your showroom must belong to a valid Brand i.e. Jetour,Elite,Soueast,Artleasing or you do not have a valid showroom associated.</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|




### Visit_Toast_Screen

|<!-- -->|<!-- -->|
|:---|:---|
|Type|Screen|
|Label|Visit Toast Screen|
|Allow Back|✅|
|Allow Finish|✅|
|Allow Pause|✅|
|Show Footer|⬜|
|Show Header|⬜|


#### VisitSuccesToast

|<!-- -->|<!-- -->|
|:---|:---|
|Extension Name|c:eGH_GenericToastMessage|
|Field Type| Component Instance|
|Inputs On Next Nav To Assoc Scrn| Use Stored Values|
|Is Required|✅|
|Store Output Automatically|✅|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Var Toast Message (input)|Visit Captured Successfully|
|Var Toast Label (input)|Success|
|Var Toast Variant (input)|success|
|Var Auto Finish Flow (input)|✅|
|Var Delay Before Finish (input)|5000|




#### ReservedOpportunityMessage

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><strong style="color: rgb(228, 19, 19); font-size: 16px;">{!$Label.EGH_ReservedOpportunity} {!ReservedOpportunityPreferredBranch}</strong></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: ReservedOpportunity<br/>&nbsp;&nbsp;operator: EqualTo<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: true<br/>|




#### Lead_Link

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><span style="font-size: 16px;">View Lead : </span><a href="{!Lead_Link_Formula}" rel="noopener noreferrer" target="_blank" style="font-size: 16px;">{!Lead_Link_Formula}</a></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: TransferredLeadId<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|




#### Opportunity_Link

|<!-- -->|<!-- -->|
|:---|:---|
|Field Text|<p style="text-align: center;"><span style="font-size: 16px;">View Opportunity : </span><a href="{!Opportunity_Link_Formula}" rel="noopener noreferrer" target="_blank" style="font-size: 16px;">{!Opportunity_Link_Formula}</a></p>|
|Field Type| Display Text|
|Style Properties|verticalAlignment:<br/>&nbsp;&nbsp;stringValue: top<br/>width:<br/>&nbsp;&nbsp;stringValue: 12<br/>|
|Visibility Rule|conditionLogic: and<br/>conditions:<br/>&nbsp;&nbsp;leftValueReference: TransferredOpportunityId<br/>&nbsp;&nbsp;operator: IsNull<br/>&nbsp;&nbsp;rightValue:<br/>&nbsp;&nbsp;&nbsp;&nbsp;booleanValue: false<br/>|








___

_Documentation generated from branch null by [sfdx-hardis](https://sfdx-hardis.cloudity.com), featuring [salesforce-flow-visualiser](https://github.com/toddhalfpenny/salesforce-flow-visualiser)_
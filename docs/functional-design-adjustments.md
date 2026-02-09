---
title: Functional Design Alignment and Documentation Adjustments (Automotive Sales)
hide:
  - path
---

Overview
This document aligns the current repository metadata and documentation with the Functional Design Document - Automotive/Sales. It identifies where implementation artifacts exist (Apex, LWC, Flows, Metadata), highlights documentation gaps, and proposes concrete documentation structure and content updates.

Sources Reviewed
- Functional Design Document - Automotive/Sales (FDD)
- sfdx-project.json (API version 64.0)
- manifest/force-app-package.xml (full metadata inventory)
- docs/ (auto-generated documentation via sfdx-hardis)

Executive Summary
- The repo contains a very large Automotive Cloud footprint across Sales, Service, and Core, with strong coverage for Lead routing, Showroom Visits, Test Drive scheduling, Appraisal, and Service Appointment orchestration.
- The current docs are primarily auto-generated inventory pages and per-artifact Apex docs. They do not map business Epics/Features/Processes to the technical implementation.
- This file proposes a top-level documentation structure rooted in the FDD’s epics and processes, and cross-links those to actual metadata (Flows, Apex, LWC, Permission Sets, Tabs, Page Layouts, Paths, Queues, Matching/Duplicate Rules, EAC, Omnichannel, etc.).

Proposed Documentation Structure
Add the following new top-level navigation and pages. Pages marked (NEW) are to be created, and existing pages receive cross-links.

- Functional Design (NEW)
  - Executive Summary (NEW)
  - Key Components of the Solution (NEW)
  - Assumptions and Decisions (NEW)
  - Success Metrics (NEW)
- Epics and Features (NEW)
  - Sales (NEW)
  - Core (NEW)
  - Integrations (NEW)
  - Marketing (placeholder; owned by external team) (NEW)
- Business Processes (NEW)
  - Lead Management (Digital + Walk-in) (NEW)
  - Lead Assignment and Routing (Walk-in) (NEW)
  - Test Drive Management (NEW)
  - Opportunity Management (NEW)
  - Customer Visits (NEW)
  - Quotation Management (NEW)
  - Vehicle Events (NEW)
  - Appraisal Management (NEW)
  - Documents & e-Signature (DocuSign) (NEW)
- Data Model (NEW)
  - Overview & ERD link (NEW)
  - Core Objects and Custom Objects (map to repo) (NEW)
- System & Environment (NEW)
  - System Landscape (NEW)
  - Environment Strategy (DevOps Center pipeline) (NEW)

Epic-to-Implementation Mapping
Below, each FDD epic and feature is mapped to metadata discovered in manifest/force-app-package.xml and docs/apex, lwc, flows.

Epic 1 — Sales
- Account and Contact Management
  - Objects/Fields: Account, Contact (+ PersonAccount support), extensive FLS fields including EGH_* custom fields
  - UI: FlexiPages (EGH_BusinessAccountLightningPage, EGH_PersonAccountLightningPage), Layouts (Account-*, PersonAccount-*)
  - Security: Profiles (EGH Sales Profile), PS/PSG: EGH_SalesConsultant_PSGroup, EGH_Sales_Consultant_Omni_Channel
- Lead Management and Assignment
  - Flows:
    - EGH_Lead_Creation_Set_Defaults_Flow
    - EGH_Lead_Acknowledgement_Email
    - EGH_Lead_Update_External_ID, EGH_Lead_Routing_SubFlow
    - EGH_LeadsRejectionApprovalProcessScreenFlow
    - Lead Walk-in: EGH_LeadAndVisitShowroomAssignmentFlow, EGH_LeadShowroomOmniChannelAssignmentFlow
  - Rules:
    - AssignmentRule: Lead.EGH Lead Queue Assignment
    - Matching/Duplicate: MatchingRule Lead.EGH_Lead_Matching_Rule, DuplicateRule Lead.Standard_Lead_Duplicate_Rule
  - Apex:
    - EGH_LeadFindDuplicates, EGH_LeadRatingHelper
  - Queues/Presence:
    - Queues: EGH_Digital_Sales_Consultant_Queue, EGH_WalkInLeadsQueue
    - Presence Config: Leads_Presence_COnfig, EGH_LeadsForDigitalSalesConsultantsPresenceConfiguration
- Opportunity Management (incl. Walk-ins)
  - Flows: EGH_Update_External_ID_On_Opportunity, EGH_Opportunity_Follow_up_Tasks_Creation_Scheduled_Flow
  - UI: EGH_OpportunityLightningPage, EGH_Read_Only_Opportunity_Page; Layouts and fields (EGH_Opportunity* fields)
  - Apex: EGH_OpportunityScoringController (+ Test)
  - Quick Actions: Opportunity.* (CaptureLostReason, EGH_CreateAppraisalAction, EGH_Test_Drive_Schedule)
- Approval Processes
  - ApprovalProcess: Lead.EGH_LeadsRejectionApprovalProcess
  - Flows/WorkflowAlerts/FieldUpdates used for communications and state transitions
- Service Scheduling (Sales touchpoints, not core service design)
  - ServiceAppointment object heavily customized (EGH_* fields), Lightning Pages, ListViews; used also for Showroom/Test Drives
- Test Drive Scheduling and Assignment
  - LWC: eghTestDriveScheduler, eghTestDriveTimeline
  - Apex: EGHTestDriveTimelineController (+ Test), EGH_TestDriveSlotFinder (+ Test)
  - Flows: EGH_StartTestDriveFlow, EGH_StopTestDriveFlow, EGH_OutboundTestDriveAppointment
  - Tabs: EGH_Test_Drive_Calendar
  - QuickActions: ServiceAppointment.EGH_StartTestDriveQuickAction, ServiceAppointment.Stop_Test_Drive
- Order Management
  - Quote/Order objects present with related fields, actions, and email templates; Quotation process intersects with Approval and DocuSign (below)
- Customer Visits
  - Custom Object: EGH_ShowroomVisit__c with extensive fields and ListViews
  - Flows: EGH_Showroom_Visit_Populate_Contact, EGH_Showroom_Visit_Reopen_Related_Lead
  - FlexiPage: EGH_Showroom_Visit_Record_Page
  - QuickAction: EGH_ShowroomVisit__c.* (EGH_AcceptVisitQuickAction, End_Visit)
  - Omni/Queues: Showroom_* service channel, Meet_Greet app and permission sets
- Vehicle Events
  - Vehicle and Asset objects + Timeline definitions (EGH_CustomerInteractionsTimeline, EGH_LeadInteractionsTimeline)
  - ListViews on Vehicle, VehicleDefinition, and multiple fields reflecting status/events
- Trade-in and Evaluation (Appraisal)
  - Objects: Appraisal, AppraisalItem, AppraisalAdjustment (+ layouts, list views)
  - Apex: EGH_AppraisalAdjustmentTrigger*, EGH_AppraisalItemTriggerHandler, EGH_AppraisalTriggerHandler
  - Flows: EGH_AppraisalAssignToEvaluatorsQueueFlow, EGH_AppraisalAdjustmentUpdatedFlow
  - Quick Actions: Account.EGH_CreateNewAppraisalAction, Appraisal.EGH_SubmitToEvaluatorAction
  - Queue: EGH_EvaluatorsQueue
- Task Management
  - Flows to create follow-up tasks: EGH_Lead_Create_Follow_Up_Task, EGH_Opportunity_Follow_up_Tasks_*
  - QuickActions/Global Actions: NewTask, FeedItem.NewTaskFromFeedItem
- Document Generation (Sales)
  - EmailTemplates under EGH_SLA, EGH_LeadsEmailTemplatesFolder
  - ContentVersion dfsle__* fields (DocuSign integration markers)
  - QuickAction: Quote.SendEmail, Opportunity/Lead related actions
- Reporting
  - ReportTypes: EGH_LeadsByBranch, EGH_Service_Appointments, EGH_SurveyInvitationsReportType
  - Dashboards foldes present; ListViews across all objects

Epic 2 — Core
- Sharing & Visibility
  - Presence of SharingRules, SharingCriteriaRule, Roles, PublicGroups, PermissionSets, PermissionSetGroups, Profiles, FieldRestrictionRule
- Chatter
  - FeedItem, WorkThanks/Badges artifacts, and Chatter groups supported via metadata

Epic 3 — Integrations
- Einstein Activity Capture (EAC)
  - Settings: EAC, VideoCall, Engagement*
- Seriti, PROAXIA, Carpro
  - Named Credentials: multiple env-specific named credentials present
  - Apex REST classes: EGH_BookAppointmentRest, EGH_GetSlotsRest
  - Integration provider metadata (IntegrationProvider*), Platform Events/REST API intended per FDD
  - Mulesoft expected as middleware (document via assumptions and named credentials)

Epic 4 — Marketing
- Out of scope for this stream per FDD; connector noted. Keep placeholder.

Business Process to Implementation Mapping
Lead Management (Digital)
- Flows: EGH_Lead_Acknowledgement_Email, EGH_LeadUpdateLeadSentToBotDateTimeFlow, EGH_Digital_Interaction_* flows
- Apex: EGH_LeadFindDuplicates
- Assignment: Lead Assignment Rule, Queues, Omni presence configs
- Email Templates: Lead new/rejection alerts
Lead Management (Walk-in) and Lead Assignment (Walk-in)
- Flows: EGH_LeadAndVisitShowroomAssignmentFlow, EGH_LeadShowroomOmniChannelAssignmentFlow, EGH_MeetGreetTestFlow
- Objects: EGH_ShowroomVisit__c
- Service Channels/Queues: Showroom_*, Meet & Greet roles/PS
Test Drive Management
- LWC: eghTestDriveScheduler, eghTestDriveTimeline
- Apex: EGHTestDriveTimelineController, EGH_TestDriveSlotFinder
- Flows: EGH_StartTestDriveFlow, EGH_StopTestDriveFlow, EGH_OutboundTestDriveAppointment
- Tabs: EGH_Test_Drive_Calendar
Opportunity Management
- Apex: EGH_OpportunityScoringController
- Flows/Quick Actions, Quote/Order artifacts, ListViews
Customer Visits
- Custom object, FlexiPage, QuickActions, Flows as above
Quotation Management
- Quote/QuoteLineItem metadata, email templates, approval flows; DocuSign markers via dfsle__ fields
Vehicle Events
- Vehicle/Asset timelines and fields; ListViews
Appraisal Management
- Appraisal + AppraisalItem + AppraisalAdjustment objects, triggers, flows and queue
Documents & e-Signature
- DocuSign: dfsle__* fields on ContentVersion; Email Templates, QuickActions

Assumptions, Decisions, Success Metrics (from FDD)
- Assumptions: Standard-first (clicks not code), third-party apps out of scope, service bookings channel delineation, MuleSoft for integrations, EAC enabled, Scheduler deployed.
- Decision: Disallow duplicate leads (aligns with Matching/Duplicate rules + EGH_LeadFindDuplicates apex).
- Success Metrics: Define a simple dashboard section linking to relevant ReportTypes and Dashboard folders.

Data Model (from FDD with Repo Alignment)
- Core Standard Objects: Account, PersonAccount, Contact, Lead, Opportunity, Vehicle, Asset, ServiceAppointment, Quote, Order, Product2, Pricebook2
- Custom Objects: EGH_ShowroomVisit__c, EGH_LeadSalesTeam__c, EGH_PersonalDocumentsObject__c, EGH_TrafficFine__c, EGH_Vehicle_Damage_Capture__c, FlowTableViewDefinition__c, etc.
- ERD: Link to corporate loop ERD; note that full object/field inventory is available in manifest/force-app-package.xml and docs/objects.

Security and Access (from FDD with Repo Alignment)
- SSO: To be configured when AD/Azure AD details are available.
- Sharing and Visibility: Roles, Public Groups, SharingRules entries present.
- FLS/Profiles/PermissionSets: Dedicated Sales, Service, Digital, Meet & Greet, Product Genius sets and groups defined.

Integrations (from FDD with Repo Alignment)
- Middleware: NamedCredentials for environments exist; Apex REST endpoints for booking/slots; IntegrationProvider* metadata.
- Marketing Cloud Connector and Genesys packages referenced in metadata and FDD.
- DocuSign presence via dfsle__ fields and email templates/quick actions.

Environment Strategy
- DevOps Center chosen; multiple NamedCredentials and ConnectedApps; GitHub repository as source control per FDD.
- Recommend adding a docs/devops-center.md with pipeline stages: Dev, Integration, UAT, Prod.

Concrete Documentation Actions
Create the following new Markdown files under docs/:

1) docs/functional-design/index.md
- Purpose: Top-level FDD alignment landing page with links to epics, processes, data model, integrations, environment.
- Content: Executive Summary, Key Components, Assumptions, Decisions, Success Metrics (concise), and links below.

2) docs/functional-design/epics/sales.md
- Map each Sales feature to implementation: Flows, Apex, LWC, Objects, QuickActions, Pages, Rules, Queues, ListViews.

3) docs/functional-design/epics/core.md
- Sharing & Visibility: list of Roles, Public Groups, Permission Sets/Groups, SharingRules.
- Chatter: feed/thanks/badges references.

4) docs/functional-design/epics/integrations.md
- Sections for PROAXIA, Seriti, Carpro, EAC, DocuSign, Genesys.
- Cross-link to NamedCredentials, Apex REST classes, IntegrationProvider* metadata.

5) docs/functional-design/epics/marketing.md
- Placeholder + ownership note.

6) docs/functional-design/processes/lead-management.md
- Digital vs Walk-in flows; assignment rules; queues; presence configs; duplicate control.

7) docs/functional-design/processes/test-drive-management.md
- LWC, Apex, Flows, Tabs, Quick Actions.

8) docs/functional-design/processes/opportunity-management.md
- Scoring, follow-ups, quote/order links, document generation.

9) docs/functional-design/processes/customer-visits.md
- ShowroomVisit object, pages, flows, queues.

10) docs/functional-design/processes/quotation-management.md
- Approval processes, email templates, DocuSign markers.

11) docs/functional-design/processes/appraisal-management.md
- Objects, triggers, flows, evaluator queue, quick actions.

12) docs/functional-design/data-model.md
- Core vs Custom objects. Link to ERD (loop) and to docs/objects and manifest.

13) docs/functional-design/system-landscape.md
- Narrative + diagram link (loop). Note Mulesoft-first integration.

14) docs/functional-design/environment-strategy.md
- DevOps Center pipeline and repo usage. Reference mkdocs and sfdx-hardis doc generation.

Index Update
Update docs/index.md navigation to include:
- Functional Design (link to docs/functional-design/index.md)
- Epics and Processes subsections
- Environment Strategy

Cross-linking
- From docs/apex and docs/lwc index pages, add “Used by” references back to the relevant Functional Design process or epic pages.

Appendix: Key Implementation Artifacts by Topic
- Test Drive: LWC (eghTestDriveScheduler, eghTestDriveTimeline), Apex (EGHTestDriveTimelineController, EGH_TestDriveSlotFinder), Flows (EGH_StartTestDriveFlow, EGH_StopTestDriveFlow), Tab (EGH_Test_Drive_Calendar)
- Appraisal: Appraisal*, Apex triggers and tests, Flows (EGH_AppraisalAssignToEvaluatorsQueueFlow, EGH_AppraisalAdjustmentUpdatedFlow), Queue (EGH_EvaluatorsQueue)
- Lead Routing: Flows (EGH_Lead_Routing_SubFlow, Walk-in flows), Assignment Rules (Lead.EGH Lead Queue Assignment), Matching/Duplicate rules, Apex duplicate detection
- Customer Visits: EGH_ShowroomVisit__c, related FlexiPage, flows, quick actions, service channels
- Integrations: Apex REST for booking/slots, NamedCredentials, IntegrationProvider*, dfsle__ (DocuSign), EAC settings
- Security: Roles, Profiles, PermissionSets, PS Groups, Sharing and Presence configs
- Reporting: ReportTypes and Dashboard folders, ListViews

Next Steps (for this PR)
- Create the new files listed above with the initial structure and links.
- Update docs/index.md to surface Functional Design.
- Optionally add badges or tags on each page to indicate status: Draft, Verified, or Pending.

Changelog
- 2026-02-09: Initial alignment authored from FDD and repo metadata inventory.

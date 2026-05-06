# Construction Project Management — Feature & Functionality Survey

> Candidate #203 · Researched: 2026-05-03

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Procore | SaaS | Commercial (~$375/user/month) | https://www.procore.com |
| Autodesk Construction Cloud (Forma) | SaaS | Commercial (custom quote) | https://construction.autodesk.com |
| Oracle Primavera P6 | On-premise / Cloud | Commercial (from $3,500/licence) | https://www.oracle.com/construction-engineering/primavera-p6/ |
| Fieldwire (Hilti) | SaaS | Commercial ($0–$54/user/month + enterprise) | https://www.fieldwire.com |
| Buildertrend | SaaS | Commercial ($499–$799/month flat) | https://buildertrend.com |
| Newforma | SaaS / On-premise | Commercial (custom quote) | https://www.newforma.com |
| CMiC | SaaS / On-premise | Commercial (custom quote) | https://cmicglobal.com |
| Trimble e-Builder / Unity Construct | SaaS | Commercial (custom quote) | https://assetlifecycle.trimble.com |
| Archdesk | SaaS | Commercial (custom quote) | https://archdesk.com |
| OpenProject | Open source / SaaS | MIT / Community Edition | https://www.openproject.org |

---

## Feature Analysis by Solution

### Procore

**Core features**
- RFI creation, routing, and tracking with email-based response (no login required for external reviewers)
- Submittal management with automated workflows, deadline reminders, and version tracking
- Punch list creation pinned to digital drawings, with photos, cost/schedule impact fields, and checklists
- Budget tracking and job costing with real-time financial dashboards
- Integrated scheduling (Gantt and lookahead)
- Document management with unlimited storage, folder customisation, and drawing version control
- Daily log and site diary capture from mobile
- Safety and quality checklists and incident reporting
- Bidding and subcontractor invitation management
- Analytics and portfolio reporting across projects

**Differentiating features**
- Procore AI (Assist): natural-language search across project data, RFI Creation Agent, Daily Log Agent, Agent Studio for no-code custom agents
- Marketplace of 500+ third-party integrations (accounting, BIM, ERP, drone, IoT)
- Multilingual AI support (English, Spanish, Polish)
- Industry-leading breadth: single platform covers pre-construction through closeout

**UX patterns**
- Module-based navigation; steep initial learning curve, especially for billing and change orders
- Mobile-first field apps with offline capability
- Permission-tiered access so subcontractors and owners see relevant views
- Contextual help and in-app Copilot suggestions

**Integration points**
- REST API with versioned endpoints; OAuth 2.0 authentication
- Pre-built connectors to QuickBooks, Sage 100/300, Viewpoint Vista, Microsoft Teams
- Developer portal at https://developers.procore.com
- Webhooks for real-time event notifications

**Known gaps**
- QuickBooks integration widely criticised as shallow; financial sync errors common
- Pricing is prohibitive for SME contractors
- Bugs and incomplete feature rollouts reported by G2 reviewers
- Slow performance under heavy project loads
- Cost-code configuration complexity on bid setup

**Licence / IP notes**
- Proprietary SaaS; data portability via API export
- AI Copilot/Assist features are proprietary; no open-source equivalent

---

### Autodesk Construction Cloud (Forma / ACC)

**Core features**
- BIM coordination with model clash detection and issue linking to object tables
- RFI creation and routing with customisable form fields and "Open for Manager" workflow status
- Submittal management with bulk attachment download
- Drawing management with version history and sheet comparison
- Specification management linked to files, sheets, RFIs, and submittals for full traceability
- Cost management and budget tracking
- Schedule management with Gantt and resource views
- Document control with markup, annotation, and approval workflows
- Field issues and safety checklists
- Takeoff integrated with specs for consistent data across modules

**Differentiating features**
- Native BIM integration: clashes and issues linked directly to 3D model objects
- Autodesk Platform Services (APS) ecosystem: deep integration with Revit, Civil 3D, Navisworks
- Model coordination with cross-discipline clash management
- Design-to-build continuity in a single vendor ecosystem

**UX patterns**
- Module-fragmented experience (Docs, Build, Takeoff, Cost are separate sub-products)
- Design-led UX more intuitive for architects than for field contractors
- Linked specification viewer improves traceability across documentation

**Integration points**
- Autodesk Platform Services (APS) REST APIs at https://aps.autodesk.com
- SDKs available (JavaScript, Python); Postman collections on GitHub
- OAuth 2.0 (three-legged for user context, two-legged for service accounts)
- Third-party RFI API for integration with external tools (released 2026)

**Known gaps**
- Module fragmentation: switching between Docs, Build, and Takeoff is disjointed
- Pricing opacity; costs escalate significantly when multiple modules are licensed
- Less suitable for specialty subcontractors and small commercial contractors
- Field execution tools less mature than Procore or Fieldwire

**Licence / IP notes**
- Proprietary SaaS; Autodesk owns all platform IP
- Open standards supported: IFC, BCF for BIM data exchange

---

### Oracle Primavera P6

**Core features**
- Critical Path Method (CPM) scheduling with early/late start/finish dates and total float calculation
- Work Breakdown Structure (WBS) hierarchy management
- Resource levelling and role-based capacity planning
- Earned Value Management (EVM): cost/schedule variance, SPI, CPI
- Portfolio-level cross-project rollups of cost, schedule, and earned value
- Baseline management and schedule comparison
- Risk register integration
- Reporting and dashboard generation
- Multi-project environment with global resource pools

**Differentiating features**
- Industry-standard CPM engine used on major infrastructure and government contracts
- Deep EVM capabilities native to the platform
- Enterprise Portfolio Project Management (EPPM) for multi-programme owners

**UX patterns**
- Desktop-first interface; web and cloud versions available but less feature-complete
- Complex configuration requiring professional scheduler background
- Long implementation cycles; typically requires certified Primavera consultants

**Integration points**
- Oracle Primavera P6 EPPM API for enterprise integration
- Integration with Oracle Cost Manager, Deltek Cobra for EVMS
- REST API available in cloud EPPM version; traditional SOAP for on-premise

**Known gaps**
- Not a full construction management suite — no RFI, submittal, or field punch-list tools
- Very steep learning curve; limited self-service adoption
- Overkill and unaffordable for SME projects
- Mobile experience is minimal

**Licence / IP notes**
- Proprietary commercial licence (perpetual or subscription)
- Heavy vendor lock-in; data export in XER/XML format

---

### Fieldwire (Hilti)

**Core features**
- Plan management: version-controlled floor plans and blueprints with offline sync
- Task creation, assignment, and tracking with due dates, photos, and priority flags
- Punch list management: items pinned to plans with photos, checklists, categories, and hashtags
- Three-week lookahead scheduling with calendar view
- Daily reporting with customisable PDF export
- Drawing markup and annotation tools
- Real-time synchronisation across devices
- BIM viewer for 3D model review in the field
- Form templates for safety and quality inspections

**Differentiating features**
- Purpose-built for field crews; fastest mobile onboarding in the category
- Free tier for up to 5 users and 3 projects (unique in market)
- Strong offline-first architecture for sites with poor connectivity
- Owned by Hilti, giving construction tool ecosystem adjacency

**UX patterns**
- Mobile-first design with intuitive field-crew UX
- Progressive disclosure: simple task and punch-list views for workers, richer analytics for supervisors
- Minimal training needed to achieve basic productivity

**Integration points**
- REST API available on Enterprise plans; developer hub at https://developers.fieldwire.com
- API endpoints for plans, tasks, floorplans, attachments, and user management
- Integrations with Procore, Autodesk ACC, Sage, and Hilti ON!Track

**Known gaps**
- Limited financial management: no budgeting, invoicing, or cost management
- No native RFI or submittal workflows
- BIM coordination features are basic compared to Autodesk ACC
- API access restricted to Enterprise tier

**Licence / IP notes**
- Proprietary SaaS (Hilti-owned); no open-source components
- Free tier available; data exportable via API

---

### Buildertrend

**Core features**
- Project scheduling with Gantt charts and dependency management
- Budget management with live job costing and cost-code tracking
- Change order creation, digital approval, and automatic budget sync
- Client portal with configurable access to schedules, budgets, documents, and approvals
- Daily logs, time clock, and site reporting
- Lead management and sales pipeline (CRM)
- Purchase orders and vendor management
- Document storage and sharing
- Selection sheets and design choices for clients

**Differentiating features**
- Purpose-built for residential and light commercial builders
- Client portal is the most feature-rich in the residential segment
- Integrated sales CRM covering leads through project delivery
- Flat monthly pricing (not per-user) appeals to growing SME teams

**UX patterns**
- Approachable UX designed for builders without deep software experience
- Client-facing portal is a primary selling point; clients stay updated without calls
- Scheduling and budget views are central; field tools are secondary

**Integration points**
- Integrations with QuickBooks, Xero, and major accounting platforms
- Open API for custom integrations
- Zapier connectivity for lightweight automations

**Known gaps**
- Limited on commercial or large-scale construction workflows
- No BIM integration or model coordination
- RFI and submittal tracking is basic compared to Procore or Newforma
- Weaker subcontractor management than enterprise platforms

**Licence / IP notes**
- Proprietary SaaS
- No open-source components; data exportable

---

### Newforma (Project Center / Konekt)

**Core features**
- Email management: Outlook add-in that tags and files project emails automatically
- RFI management: create, route, log, and track requests with full audit trail
- Submittal management with review workflows and distribution logs
- Document control and version tracking
- Contract change and potential change order management
- BIM coordination and model viewing (via Newforma Konekt)
- Information management across design and construction teams

**Differentiating features**
- Best-in-class project email archiving: every email tagged to project, discipline, and action item
- Strong adoption in architect and engineering firms (design-side information management)
- Konekt platform unites design teams, contractors, and owners in a single AEC thread
- On-premise option (Project Center) for firms with strict data sovereignty requirements

**UX patterns**
- Outlook-centric workflow matches how AEC firms already operate
- Project Centre (on-premise) has legacy UX; Konekt is the modern cloud product
- Dual product portfolio (Project Center + Konekt) creates some positioning confusion

**Integration points**
- Microsoft Outlook add-in as primary capture mechanism
- REST API for integration with third-party platforms
- Integration with Autodesk, Revit, and BIM tools

**Known gaps**
- Limited field execution features (no punch lists, daily logs, or site reporting)
- Less suitable for general or specialty contractors; skewed toward design professionals
- On-premise product ageing; migration to Konekt still in progress for many users
- Smaller integration marketplace than Procore or Autodesk

**Licence / IP notes**
- Proprietary SaaS / on-premise; no open-source components
- G2 Winter 2026: 30 badges including Best ROI and Best Support

---

### CMiC

**Core features**
- Integrated construction ERP on a single database (financials + project management + field)
- General Ledger, Accounts Payable / Receivable, consolidated financial reporting
- Certified payroll, HR, and equipment management
- Job costing with WIP (Work-in-Progress) reporting
- Subcontract and procurement management
- Bidding and estimating
- Drawing management and document control
- Project scheduling and progress tracking
- Field operations: daily logs, time entry, and labour productivity tracking
- CRM and opportunity management

**Differentiating features**
- Single-database architecture eliminates the data silos common when separate PM and ERP tools are combined
- Trusted by 1 in 5 ENR Top 400 General Contractors
- Deep certified payroll and union compliance features — unmatched in the category
- Full financial consolidation from job cost through corporate financials on one platform

**UX patterns**
- Complex, enterprise-grade UI with a steep onboarding curve
- Requires long implementation cycles (typically 6–18 months)
- Configuration-heavy; professional services typically required
- Role-based dashboards for executives, project managers, and field supervisors

**Integration points**
- REST API and integration layer for ERP-to-PM data exchange
- Pre-built connectors to Oracle, SAP, and major subcontractor portals
- Field data flows directly into financial modules in real time

**Known gaps**
- Legacy UX deters adoption by younger field staff
- Long and expensive implementation cycles
- Not designed for SME contractors
- Limited AI/ML capabilities compared to Procore or Autodesk
- Mobile field experience lags behind Fieldwire or Procore

**Licence / IP notes**
- Proprietary SaaS / on-premise; commercial licence only
- No open-source components

---

### Trimble e-Builder / Unity Construct

**Core features**
- Capital planning and funding allocation across multi-year programmes
- Cost management, forecasting, and budget controls
- Business process automation with configurable forms and workflows
- Schedule management with critical path tracking
- Document management and version control
- Bid management and procurement support
- Reporting dashboards with on-demand programme performance views
- Asset handover documentation
- Contract administration and change management

**Differentiating features**
- Purpose-built for capital programme owners (hospitals, universities, government agencies)
- Programme-level visibility across hundreds of simultaneous projects
- Transitioning to Trimble Unity Construct as the next-generation platform
- Strong compliance and audit trail features for public-sector procurement

**UX patterns**
- Owner-centric dashboards and reporting
- Complex configuration suited to large owner organisations
- Less suited to contractor field execution

**Integration points**
- Trimble Connect ecosystem integration
- REST APIs for integration with owner ERP and accounting systems
- Integration with Revit, SketchUp, and Trimble design tools

**Known gaps**
- Not designed for contractors or subcontractors
- Field execution features are minimal
- Product transition to Unity Construct creates uncertainty for existing users
- Smaller partner ecosystem than Procore or Autodesk

**Licence / IP notes**
- Proprietary SaaS (Trimble); commercial licence only

---

### Archdesk

**Core features**
- Project management: scheduling, Gantt charts, task allocation, critical path analysis
- Financial management: budgeting, job costing, procurement, invoicing
- Subcontractor and supplier management
- Document management and version control
- RFI and change management workflows
- Equipment tracking
- CRM and sales pipeline
- Reporting and analytics dashboards
- Open RESTful API for integrations

**Differentiating features**
- End-to-end ERP approach without the legacy UX of CMiC
- Strong mid-market positioning with a more modern interface
- All-in-one platform reduces need for multiple subscriptions
- Integrations with Xero, NetSuite, and popular cloud accounting tools

**UX patterns**
- More modern UX than legacy ERPs; approachable for mid-market contractors
- Configurable workflows to match contractor-specific processes
- Customer support frequently cited as a strength

**Integration points**
- Open REST API for CRM and accounting integration
- Pre-built connectors to Xero, NetSuite
- Webhooks for real-time data synchronisation

**Known gaps**
- Smaller ecosystem and marketplace than Procore or Autodesk
- BIM integration is limited
- Less recognised brand in enterprise procurement cycles
- Field mobile experience less polished than Fieldwire

**Licence / IP notes**
- Proprietary SaaS; commercial licence

---

### OpenProject

**Core features**
- Project planning with Gantt charts, milestones, and dependencies
- Issue and task tracking
- Agile boards (Scrum/Kanban)
- Time and cost tracking
- Document management
- Team collaboration and commenting
- Portfolio and programme management
- Work packages and requirements management

**Differentiating features**
- Only significant open-source construction-adjacent PM option
- Self-hostable with full data sovereignty
- Community Edition is free under GNU GPL
- Active development community

**UX patterns**
- Functional UX that prioritises power over simplicity
- Suited to technically proficient teams comfortable with self-hosting
- Less industry-specific than construction-native tools

**Integration points**
- REST API for all core entities
- BCF REST API for BIM issue management (via plugin)
- Webhooks and Zapier integration
- GitHub, GitLab, and Slack integrations

**Known gaps**
- No construction-specific workflows: no RFI, submittal, punch list, or BIM coordination
- No financial management or job costing
- Field mobile app is limited
- Requires technical resources to self-host and maintain

**Licence / IP notes**
- Core: GNU GPL v3 (Community Edition); Enterprise modules under commercial licence
- No patent concerns for construction-specific features

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- RFI creation, routing, tracking, and audit trail
- Submittal management with review workflows and version control
- Document management with drawing version control and unlimited storage
- Punch list creation pinned to digital plans, with photos and status tracking
- Mobile-first field access with offline capability
- Project scheduling (Gantt chart minimum; CPM for complex projects)
- Change order management with budget integration
- Daily logs and site reporting
- Role-based permissions and access control
- Basic reporting and project dashboards

### Differentiating Features
- Native BIM model coordination and clash detection (Autodesk ACC)
- Single-database ERP integration spanning field to financials (CMiC)
- AI-powered natural-language search and RFI drafting (Procore Assist)
- Project email archiving and auto-tagging (Newforma)
- Capital programme management across multi-year portfolios (e-Builder / Unity Construct)
- Client portal with live project transparency (Buildertrend)
- Enterprise-grade CPM scheduling with earned value management (Primavera P6)
- Free tier for small teams (Fieldwire)

### Underserved Areas / Opportunities
- **Affordable, AI-native RFI drafting** for SME contractors who cannot afford Procore
- **Unified field-to-finance on a modern stack** — most tools are either field-strong or finance-strong, rarely both, and legacy ERPs have outdated UX
- **Open, standards-based BIM/BCF integration** that works across Procore, Autodesk, and open platforms without vendor lock-in
- **Predictive schedule risk scoring** using weather, subcontractor history, and procurement data — only partially addressed by incumbents
- **Cross-project natural-language search** for drawing, spec, and email archives in a cost-effective, self-hostable package
- **Safety hazard detection from site photos** — almost entirely unaddressed in open-source tools
- **Subcontractor performance tracking** with AI-assisted scoring across multiple projects

### AI-Augmentation Candidates
- RFI drafting and response suggestion from project documents and specs (replaces 2–3 days of engineer research per RFI)
- Submittal review routing: AI classifies submittal type and suggests reviewer from team roster
- Schedule delay prediction: ingests weather, procurement lead times, subcontractor performance history
- Cost-at-completion forecasting: reconciles change orders and pay applications dynamically
- Safety incident pre-emption: computer vision over site photos flags hazards before OSHA-reportable events
- Natural-language document Q&A: "What was agreed on waterproofing for Level 3?" resolved in seconds
- Change order impact analysis: AI flags specification sections and drawings affected by a proposed change

---

## Legal & IP Summary

No patent concerns were identified for construction-specific workflows (RFI, submittal, punch list, scheduling). The major commercial platforms (Procore, Autodesk, CMiC) hold proprietary rights over their implementations, but the underlying workflows are well-established industry practices. Open standards — IFC (ISO 16739-1), BCF (buildingSMART), CSI MasterFormat, and ISO 19650 — are freely implementable. OpenProject's Community Edition (GNU GPL v3) is the most reusable open-source base, though it lacks construction-specific features. No licensing or patent obstacles exist to building an AI-native open-source construction project management tool implementing these workflows from scratch.

---

## Recommended Feature Scope

**Must-have (MVP)**
- RFI lifecycle management (create, route, respond, close, audit trail)
- Submittal tracking with reviewer assignment and status tracking
- Document and drawing management with version control
- Punch list creation pinned to digital plans with photos and status
- Project scheduling (Gantt with dependencies)
- Change order management with budget impact
- Role-based permissions (owner, GC, subcontractor, architect)

**Should-have (v1.1)**
- AI-assisted RFI drafting using project specs and drawings as context
- Budget tracking and job costing with change order sync
- Mobile-first field app with offline sync
- Daily log capture and site reporting
- Natural-language search across project documents and emails
- CSI MasterFormat cost code support
- REST API with OpenAPI spec and OAuth 2.0

**Nice-to-have (backlog)**
- BIM model viewer with BCF issue linking (IFC-based)
- Predictive schedule risk scoring
- Computer-vision safety hazard detection from site photos
- Subcontractor performance analytics across projects
- Capital programme roll-up view for owner organisations
- Certified payroll and union compliance (for ERP-level ambition)

# Construction Project Management

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source construction project management platform unifying BIM integration, RFI and submittal tracking, punch lists, and budget management on a modern stack.

Construction Project Management is a candidate project to build an open alternative to Procore, Autodesk Construction Cloud, and CMiC. It targets general contractors, specialty subcontractors, project owners, and AEC firms who need full-lifecycle project controls without the six-figure platform fees and steep learning curves of incumbent suites.

---

## Why Construction Project Management?

- Procore lists at roughly $375/user/month, putting category-leading capability out of reach for most SME contractors.
- Autodesk Construction Cloud suffers from module fragmentation across Docs, Build, Takeoff, and Cost, with pricing that escalates as modules are added.
- Oracle Primavera P6 (from $3,500/licence) is industry-standard for CPM scheduling but is not a full construction management suite and demands certified consultants.
- CMiC offers single-database ERP integration but is held back by legacy UX and 6–18 month implementation cycles.
- OpenProject is the only significant open-source option in the adjacent space, but it has no construction-specific workflows: no RFI, submittal, punch list, or BIM coordination.

---

## Key Features

### Core Project Controls

- RFI lifecycle management: create, route, respond, close, with full audit trail
- Submittal tracking with reviewer assignment, review workflows, and version control
- Document and drawing management with version history
- Punch list creation pinned to digital plans, with photos and status tracking
- Change order management with budget impact integration
- Role-based permissions for owners, GCs, subcontractors, and architects

### Scheduling & Budget

- Project scheduling with Gantt charts and dependencies
- Budget tracking and job costing with change order sync
- CSI MasterFormat cost code support
- Daily log capture and site reporting

### Field Execution

- Mobile-first field app with offline synchronisation
- Daily logs, time entry, and site reporting from mobile
- Drawing markup and annotation tools
- Safety and quality checklists

### BIM & Coordination (backlog)

- BIM model viewer with BCF issue linking based on IFC
- Specification management linked across files, sheets, RFIs, and submittals
- Cross-discipline clash and issue tracking

### Analytics & Intelligence (backlog)

- Predictive schedule risk scoring
- Computer-vision safety hazard detection from site photos
- Subcontractor performance analytics across projects
- Capital programme roll-up view for owner organisations

---

## AI-Native Advantage

AI is being embedded across leading platforms (Procore Copilot, Autodesk's AI-assisted risk detection), but is paywalled behind enterprise pricing. This project applies AI as a first-class capability: automated RFI drafting and response suggestion using project documents, drawings, and specs as context; predictive schedule risk scoring driven by weather, subcontractor performance, and procurement lead times; computer-vision safety hazard detection from site photos with OSHA-aligned reporting; AI-assisted budget forecasting reconciling change orders and pay applications into dynamic cost-at-completion projections; and natural-language search across drawings, submittals, emails, and RFIs.

---

## Tech Stack & Deployment

The platform is intended to expose a REST API with an OpenAPI specification and OAuth 2.0 authentication, mirroring the integration model used by Procore, Autodesk Platform Services, and Fieldwire. Open standards drive interoperability: ISO 19650 for information management, IFC (ISO 16739-1) and BCF for BIM data exchange, CSI MasterFormat for cost coding, AIA contract document conventions for RFI and submittal procedures, and OSHA 300 schemas for safety reporting. Self-hostable deployment is a design goal so firms with data sovereignty requirements (currently served by Newforma Project Center on-premise or CMiC) have a modern alternative.

---

## Market Context

North America accounts for roughly 47.8% of the global construction management software market as of 2025, with Asia-Pacific the fastest-growing region. Pricing across incumbents spans from $39/user/month (Fieldwire) to $375+/user/month (Procore) to six-figure perpetual licences (Primavera P6), with enterprise platforms like CMiC and e-Builder custom-quoted and requiring multi-year implementation. Primary buyers are general contractors, specialty subcontractors, project owners managing capital programmes, and AEC firms managing document control and RFIs.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.

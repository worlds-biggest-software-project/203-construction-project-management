# Standards & API Reference

> Project: Construction Project Management · Generated: 2026-05-03

## Industry Standards & Specifications

### ISO Standards

**ISO 19650 — Information Management Using BIM**
- URL: https://www.iso.org/standard/68078.html
- A family of six parts covering information management concepts, delivery-phase processes, operational-phase processes, information exchange, security-minded information management, and health and safety information for built assets. Increasingly mandated on government and infrastructure tenders globally. Draft revisions released for public consultation in 2026 signal a transition from BIM-focused to full lifecycle Information Management (IM), making it the foundational governance framework for any serious construction platform.

**ISO 16739-1:2024 — Industry Foundation Classes (IFC)**
- URL: https://www.iso.org/standard/84123.html
- The formal ISO standard encoding the IFC schema, which is the open, vendor-neutral BIM data format for exchanging building and infrastructure models. Any construction platform with BIM viewing or coordination should implement IFC import/export to ensure interoperability across Autodesk, Bentley, Trimble, and open-source toolchains.

**ISO 31000 — Risk Management Guidelines**
- URL: https://www.iso.org/standard/65694.html
- Provides principles and guidelines for managing risk applicable to schedule risk registers, project risk matrices, and safety hazard logs commonly embedded in construction PM platforms.

**ISO 9001 — Quality Management Systems**
- URL: https://www.iso.org/standard/62085.html
- The international quality management standard; construction quality control workflows (inspection and test plans, non-conformance reports) in many platforms are designed to support ISO 9001 compliance.

---

### W3C & IETF Standards

**RFC 9110 — HTTP Semantics**
- URL: https://www.rfc-editor.org/rfc/rfc9110
- Defines the semantics of HTTP/1.1 and HTTP/2; foundational for all REST API implementations across construction platforms.

**RFC 6749 — OAuth 2.0 Authorization Framework**
- URL: https://www.rfc-editor.org/rfc/rfc6749
- The authorization framework used by Procore, Autodesk APS, and Fieldwire for delegated API access. Any construction platform exposing a public API must implement OAuth 2.0 for third-party app authentication.

**RFC 6750 — OAuth 2.0 Bearer Token Usage**
- URL: https://www.rfc-editor.org/rfc/rfc6750
- Specifies how Bearer tokens are transmitted in HTTP Authorization headers; required companion to RFC 6749.

**RFC 7519 — JSON Web Tokens (JWT)**
- URL: https://www.rfc-editor.org/rfc/rfc7519
- JWT is the token format used by most construction platform APIs for identity propagation across services and across microservices boundaries.

**OpenID Connect 1.0**
- URL: https://openid.net/specs/openid-connect-core-1_0.html
- The identity layer on top of OAuth 2.0; used for SSO and identity federation in enterprise construction platforms integrating with corporate IdPs (Azure AD, Okta, Google Workspace).

**W3C WebSub / Webhooks (Informal Standard)**
- No formal W3C spec, but webhook patterns (HTTP POST callbacks on events) are universal across construction platforms including Procore, Autodesk, and Fieldwire for real-time event notifications.

---

### Data Model & API Specifications

**BIM Collaboration Format (BCF) — OpenCDE BCF API**
- URL: https://technical.buildingsmart.org/standards/bcf/
- GitHub: https://github.com/buildingSMART/BCF-API
- BCF is the open standard for managing BIM issues (clash reports, design queries, punch items) linked to 3D model locations. The BCF API is a RESTful web service that enables exchange of BCF topics across platforms via JSON over HTTP. It is a member of the OpenCDE API family; all implementations must also implement the OpenCDE Foundation API. Essential for any construction platform with BIM model coordination.

**OpenCDE Foundation API**
- URL: https://github.com/buildingSMART/OpenCDE-API
- The shared common API underpinning all OpenCDE APIs (BCF, Documents, Dictionary). Defines authentication conventions and base service contracts that enable federated Common Data Environments (CDEs) to interoperate.

**OpenCDE Documents API**
- URL: https://github.com/buildingSMART/documents-API
- Standardises document discovery and access between CDEs and authoring tools; relevant for drawing and submittal document management across platforms.

**CSI MasterFormat 2026**
- URL: https://www.csiresources.org/standards/masterformat
- The consensus-based classification system for construction specifications, cost codes, and work results (50+ divisions). Standard cost code framework for budget line items, submittals, and RFI categorisation in North American practice. The 2026 edition is delivered through CSI's new digital platform (CSI Dynamic Standards). Licences are required for redistribution; free to use for internal classification.

**CSI UniFormat**
- URL: https://www.csiresources.org/standards/uniformat
- Elemental classification standard (systems and assemblies level) complementing MasterFormat; used in early-stage estimating and capital budgeting.

**OmniClass (OCCS)**
- URL: https://www.csiresources.org/standards/omniclass
- The comprehensive classification system for the construction industry, covering work results, phases, properties, and roles. Useful for tagging and interoperability with BIM object libraries.

**OpenAPI Specification 3.1 (formerly Swagger)**
- URL: https://spec.openapis.org/oas/v3.1.0
- The industry standard for describing REST APIs. Any construction platform API should publish an OpenAPI 3.1 specification for discoverability, client SDK generation, and developer experience.

**JSON Schema (Draft 2020-12)**
- URL: https://json-schema.org/draft/2020-12/schema
- Vocabulary for annotating and validating JSON documents; used in OpenAPI definitions for request/response schema validation.

---

### Security & Authentication Standards

**OWASP Application Security Verification Standard (ASVS) 5.0**
- URL: https://owasp.org/www-project-application-security-verification-standard/
- Comprehensive security requirements framework including a dedicated OAuth/OIDC chapter (V10) added in ASVS 5.0. Provides the security baseline for enterprise construction platforms handling sensitive contract, financial, and personnel data.

**OWASP Top Ten 2025**
- URL: https://owasp.org/www-project-top-ten/
- The canonical list of critical web application security risks; applicable to construction platform API and web app development.

**NIST Cybersecurity Framework 2.0**
- URL: https://www.nist.gov/cyberframework
- Widely referenced by US government and large owner organisations requiring cybersecurity governance from their software vendors; relevant for platforms targeting government capital programme management.

**GDPR (EU) / UK GDPR**
- URL: https://gdpr.eu/
- Applies to any construction platform storing personal data (workers, subcontractors, site visitors) for EU or UK projects. Requires encryption at rest (AES-256), encryption in transit (TLS 1.3), data residency options, right to erasure, and a documented privacy policy.

**TLS 1.3 (RFC 8446)**
- URL: https://www.rfc-editor.org/rfc/rfc8446
- The current transport security standard; all API and web traffic on construction platforms should enforce TLS 1.3 minimum, TLS 1.2 as fallback.

---

### MCP Server Specifications

**Model Context Protocol (MCP)**
- URL: https://modelcontextprotocol.io/
- GitHub: https://github.com/modelcontextprotocol
- Open protocol by Anthropic enabling AI models to securely access external tools and data sources. Highly relevant for the AI-native opportunity: an MCP server exposing construction project data (RFIs, submittals, drawings, specs) would allow AI agents to answer project questions, draft RFIs, and detect schedule risks without custom integration for each AI framework. Both Claude and other major LLMs support MCP tool calling.

---

## Similar Products — Developer Documentation & APIs

### Procore
- **Description:** Market-leading construction management platform covering RFIs, submittals, budgets, scheduling, and field operations across pre-construction through closeout.
- **API Documentation:** https://developers.procore.com/reference/rest/docs/rest-api-overview
- **Developer Portal:** https://developers.procore.com/documentation/introduction
- **Authentication:** OAuth 2.0 (three-legged for user-delegated access; two-legged for service accounts)
- **Standards:** REST/JSON; versioned endpoint architecture with independent resource versioning; OpenAPI-compatible
- **Webhooks:** Yes — event-based HTTP POST callbacks for project data changes
- **SDKs/Libraries:** No official SDK; community SDKs available; Postman collections provided
- **Notes:** 500+ marketplace integrations; REST API endpoints cover RFIs, submittals, drawings, budget, and all core entities

---

### Autodesk Construction Cloud (Autodesk Platform Services — APS)
- **Description:** BIM-centric construction platform covering model coordination, RFIs, submittals, cost management, and document control; part of the Autodesk Platform Services ecosystem.
- **API Documentation:** https://aps.autodesk.com/en/docs/acc/v1/overview/
- **Developer Portal:** https://aps.autodesk.com/developer/documentation
- **SDKs/Libraries:** JavaScript SDK, Python SDK (unofficial); Postman collections on GitHub at https://github.com/autodesk-platform-services
- **Authentication:** OAuth 2.0 (three-legged for user context; two-legged for service-to-service)
- **Standards:** REST/JSON; OpenAPI-compatible; IFC and BCF for BIM interoperability
- **Notes:** RFI API for third-party integration released January 2026; supports IFC import/export and BCF issue exchange

---

### Fieldwire (Hilti)
- **Description:** Field-first construction management platform for task tracking, punch lists, plan management, and daily reporting; optimised for field crews and specialty subcontractors.
- **API Documentation:** https://developers.fieldwire.com/docs/getting-started
- **Developer Hub:** https://developers.fieldwire.com/
- **Authentication:** API token-based (OAuth 2.0 not currently available for third-party apps)
- **Standards:** REST/JSON
- **Notes:** API powers the Fieldwire web and mobile apps; available on Enterprise plans (or as add-on to Pro/Business); supports bulk import, cross-platform sync, plan and attachment management

---

### Oracle Primavera P6 EPPM
- **Description:** Enterprise CPM scheduling and portfolio management platform; industry standard for major infrastructure, government, and energy projects requiring earned value management.
- **API Documentation:** https://docs.oracle.com/cd/G48902_01/English/User_Guides/p6_pro_user/introducing_primavera_project_management.htm
- **REST API (Cloud EPPM):** Available via Oracle Integration Cloud; REST endpoints for projects, activities, and resources
- **Authentication:** OAuth 2.0 for cloud; traditional user/password or SAML for on-premise
- **Standards:** REST/JSON (cloud); SOAP/XML (on-premise legacy); XER and XML for schedule export/import
- **Notes:** P6 Professional (on-premise) uses a legacy proprietary API; P6 EPPM cloud adopts REST. Integration with Oracle ERP Cloud is native.

---

### Newforma (Konekt / Project Center)
- **Description:** AEC-focused project information management platform specialising in email archiving, RFI and submittal workflows, and document control for architects and engineers.
- **API Documentation:** https://projectcenter.help.newforma.com/
- **Authentication:** OAuth 2.0 (Konekt cloud); traditional credentials (Project Center on-premise)
- **Standards:** REST/JSON; Microsoft Graph API integration for Outlook email capture
- **Notes:** Microsoft Outlook add-in is the primary integration mechanism; REST API enables synchronisation with Autodesk, Procore, and custom systems

---

### CMiC
- **Description:** Single-database construction ERP covering financials, project management, payroll, and field operations for general and specialty contractors.
- **API Documentation:** https://cmicglobal.com/ (enterprise integration documentation requires partner access)
- **Authentication:** OAuth 2.0 and SSO via SAML 2.0 for enterprise customers
- **Standards:** REST/JSON API layer; traditional SOAP/XML for legacy integrations
- **Notes:** Integration documentation primarily available through CMiC partner programme; pre-built connectors to Oracle, SAP, and major subcontractor portals

---

### Trimble Unity Construct (e-Builder successor)
- **Description:** Capital programme management platform for owners managing large infrastructure and facility construction programmes across planning, design, procurement, and construction.
- **API Documentation:** https://assetlifecycle.trimble.com/en/products/software/unity-construct
- **Authentication:** OAuth 2.0; integration with Trimble Identity and enterprise SSO
- **Standards:** REST/JSON; integration with Trimble Connect ecosystem
- **Notes:** Product transition from e-Builder to Unity Construct ongoing as of 2026; Trimble Connect provides a unified data platform across Trimble's design and construction tools

---

### OpenProject
- **Description:** Open-source project management platform (general purpose) with a BCF REST API plugin for BIM issue management; the primary self-hostable PM alternative.
- **API Documentation:** https://www.openproject.org/docs/api/
- **BCF REST API:** https://www.openproject.org/docs/api/bcf-rest-api/
- **SDKs/Libraries:** Community Ruby gem; REST API usable with any HTTP client
- **Authentication:** OAuth 2.0 and API token
- **Standards:** REST/JSON; OpenAPI 3.0 specification published; BCF REST API for BIM integration; GNU GPL v3 (Community Edition)
- **Notes:** The most viable open-source base for an AI-native construction tool; BCF support enables BIM issue integration; lacks native RFI, submittal, and financial features

---

### IfcOpenShell
- **Description:** Open-source IFC library and geometry engine for parsing, generating, and manipulating IFC BIM files; the primary open-source toolkit for IFC-native development.
- **GitHub:** https://github.com/IfcOpenShell/IfcOpenShell
- **Documentation:** https://docs.ifcopenshell.org/
- **SDKs/Libraries:** Python (primary), C++; BCF tools included
- **Authentication:** N/A (library, not a service)
- **Standards:** IFC (ISO 16739-1); BCF; MIT-like licence (LGPL v3)
- **Notes:** Essential dependency for any open-source construction platform implementing BIM model viewing, clash detection, or BCF issue management; active community; Python-first API suits AI/ML integration

---

## Notes

- **Emerging standard to watch:** The proposed ISO 19650 2026 revisions shift the focus from BIM to broader Information Management, signalling that "common data environment" (CDE) interoperability will become an increasingly mandatory platform capability in public-sector markets.
- **OpenCDE is underutilised by SME tools:** BCF and Documents APIs are well-specified but adoption is concentrated in enterprise platforms; an open-source tool implementing OpenCDE APIs would immediately be interoperable with Autodesk, Procore, and other platforms without bespoke integrations.
- **No construction-specific security standard exists:** OWASP ASVS and NIST CSF apply generically; construction platforms handling payment certificates and contract data should additionally consider PCI-DSS scope if processing card payments and GDPR/CCPA for personnel data.
- **CSI MasterFormat licensing:** The 2026 edition is now accessed through CSI's Digital Standards platform with licensing required for redistribution. Products can use MasterFormat cost codes internally without a redistribution licence; embedding the full standard in open-source code would require a commercial licence from CSI.

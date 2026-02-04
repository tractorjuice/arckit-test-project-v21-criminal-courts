# Statement of Work (SOW): Criminal Courts Technology & AI Reform

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.sow`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOW-v1.0 |
| **Document Type** | Statement of Work / Request for Proposal |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-04 |
| **Last Modified** | 2026-02-04 |
| **Review Cycle** | On-Demand |
| **Next Review Date** | 2026-03-06 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | MoJ Commercial, MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial creation from `/arckit.sow` command | [PENDING] | [PENDING] |

## Document Purpose

This Statement of Work (SOW) defines the requirements, deliverables, evaluation criteria, and contract terms for the Criminal Courts Technology & AI Reform programme. It serves as the formal Request for Proposal (RFP) document for vendor procurement via the UK Digital Marketplace. Vendors responding to this SOW must address all mandatory requirements and demonstrate capability to deliver within the governance framework of the UK criminal justice system.

---

## 1. Executive Summary

### 1.1 Purpose of This SOW

This Statement of Work defines the requirements, deliverables, and evaluation criteria for the Criminal Courts Technology & AI Reform programme. The Ministry of Justice (MoJ), on behalf of HM Courts & Tribunals Service (HMCTS), the Crown Prosecution Service (CPS), and associated criminal justice agencies, is seeking qualified vendors to deliver technology solutions across five programme pillars: AI-assisted case preparation, cross-agency digital interoperability, legacy system migration, victim and witness services, and AI governance.

### 1.2 Background

The criminal justice system in England and Wales faces an unprecedented crisis. The Independent Review of the Criminal Courts (Leveson Review, 2025–2026) identified 77,000+ outstanding Crown Court cases, fragmented digital systems across police, CPS, courts, probation, and prisons, a troubled Common Platform rollout, and 37 critical legacy applications requiring modernisation. The Review made 180 recommendations for reform, many requiring technology-enabled change.

The programme operates within a uniquely complex stakeholder landscape spanning multiple independent agencies (MoJ, HMCTS, CPS, HMPPS, Legal Aid Agency, 43 police forces, the judiciary), each with distinct operational pressures but deeply interdependent workflows. The criminal justice system processes some of the most sensitive personal data in government (criminal records, evidence, victim/witness details), governed by UK GDPR and DPA 2018 Part 3 (law enforcement processing).

Previous justice technology programmes, notably the Common Platform, experienced significant cost overruns and scope reduction. This programme must learn from those failures and demonstrate disciplined, phased delivery with robust governance.

### 1.3 Project Overview

**Objective**: Deliver technology-enabled reform of the criminal courts system, reducing the Crown Court backlog, enabling AI-assisted case preparation for prosecution and defence, achieving cross-agency interoperability, migrating legacy systems, and improving victim and witness experience — all while preserving judicial independence and ensuring equality of arms.

**Scope**: Five programme pillars delivered through phased implementation over 5 years:

1. **Pillar 1 — AI-Assisted Disclosure and Case Preparation**: AI tools for prosecution (CPS) and defence for disclosure review, digital evidence triage, case summarisation, transcription, and translation
2. **Pillar 2 — Cross-Agency Digital Interoperability**: API-based integration between police forces, CPS, HMCTS, HMPPS, and LAA for case data, evidence, and outcomes
3. **Pillar 3 — Legacy System Migration**: Phased assessment and migration of 37 critical legacy applications, prioritised by risk and operational impact
4. **Pillar 4 — Victim and Witness Services**: Real-time case tracking for victims, automated Victims' Code compliance monitoring, remote evidence facilities
5. **Pillar 5 — AI Governance and Compliance**: AI governance framework, ATRS registration, DPIA compliance, judicial steering group, ethics review board

**Expected Outcomes**:
- Crown Court outstanding caseload reduced from 77,000+ to below 50,000 within 3 years
- 80%+ of Crown Court cases using AI-assisted disclosure review by Year 3
- 90%+ of case data exchanged automatically between agencies by Year 4
- 20+ of 37 legacy applications migrated within 3 years
- 20% improvement in victim satisfaction within 2 years
- Programme expenditure within 10% of approved business case

**Budget Range**: Total programme investment approximately £281M over 5 years (per SOBC ARC-001-SOBC-v1.0). Individual lot budgets available upon request to qualified vendors.

**Timeline**: 5-year phased implementation with stage-gate funding approvals at each phase boundary.

---

## 2. Scope of Work

### 2.1 In Scope

The selected vendor(s) will be responsible for delivering the following across one or more programme pillars:

1. **Pillar 1: AI-Assisted Disclosure and Case Preparation**
   - AI disclosure review engine processing digital evidence (documents, images, video, communications) with categorisation and confidence scoring (FR-001)
   - AI case summarisation generating structured summaries from case files (FR-002)
   - AI transcription (real-time and batch) and translation for criminal proceedings (FR-003)
   - Defence technology platform providing equivalent AI tools to defence practitioners (FR-009)
   - AI governance register tracking all AI tools with ATRS and DPIA status (FR-011)

2. **Pillar 2: Cross-Agency Digital Interoperability**
   - Cross-agency API gateway enabling standardised data exchange between police, CPS, HMCTS, HMPPS, and LAA (FR-004)
   - Digital case file standard definition and enforcement (FR-005)
   - Court case management enhancement with AI-assisted scheduling (FR-006)
   - Sentence data integration for real-time feed to HMPPS (FR-012)

3. **Pillar 3: Legacy System Migration**
   - Portfolio assessment of 37 critical legacy applications (FR-010)
   - Phased migration execution prioritised by risk score
   - Data migration with parallel running and automated reconciliation
   - Legacy system decommissioning with audit trail

4. **Pillar 4: Victim and Witness Services**
   - Victim/witness case tracking service with real-time notifications (FR-007)
   - Remote evidence facilities for vulnerable witnesses (FR-008)
   - Automated Victims' Code compliance monitoring (FR-013)

5. **Pillar 5: AI Governance and Compliance**
   - AI governance framework operationalisation
   - ATRS registration process for criminal justice AI
   - DPIA support for all AI deployments
   - Benefits realisation tracking system (FR-014)

### 2.2 Out of Scope

The following are explicitly NOT part of this engagement:

- New court building or physical infrastructure
- Judicial appointment or reform of sentencing guidelines
- Police operational systems beyond case file integration interfaces
- Prison management systems beyond sentence data integration interfaces
- Legal aid policy reform (though technology for defence access is in scope)
- Predictive AI for case outcomes or sentencing (prohibited without explicit ministerial and judicial approval)
- Common Platform rebuild or replacement (stabilisation is an HMCTS prerequisite, not a vendor deliverable)
- Physical security of court premises

### 2.3 Client Responsibilities

The Ministry of Justice / HMCTS will provide:

- **Programme governance**: Programme Board, Senior Responsible Owner, architecture governance, and decision-making authority
- **Judicial engagement**: Judicial AI steering group with authority over case-affecting AI deployments
- **Cross-agency coordination**: Data sharing agreements, stakeholder engagement, and cross-agency governance
- **Existing infrastructure**: Common Platform access, cloud hosting tenancy, network connectivity between agencies
- **Subject matter expertise**: Criminal justice domain expertise, user research participants across all 8 personas
- **Security clearance facilitation**: SC clearance processing for vendor personnel requiring access to criminal justice data
- **Approvals and sign-offs**: Design approvals (HLD, DLD), go-live approvals, and GDS service assessment coordination
- **Data**: Access to anonymised test data and production environment access (subject to clearance)
- **Change management**: Court staff training coordination, judicial communication, practitioner engagement

---

## 3. Requirements

### 3.1 Business Requirements Summary

All business requirements are MUST_HAVE priority. Vendors must demonstrate capability to meet all mandatory requirements. Full details are in ARC-001-REQ-v1.0 (attached as Appendix A).

| Requirement ID | Title | Priority | Key Acceptance Criteria |
|----------------|-------|----------|------------------------|
| **BR-001** | Reduce Crown Court Case Backlog | MUST_HAVE | Outstanding caseload <50,000 by Year 3; charge-to-trial time reduced 30% |
| **BR-002** | Deploy AI for Prosecution Case Preparation and Disclosure | MUST_HAVE | 80%+ Crown Court cases using AI disclosure by Year 3; 100% ATRS registration |
| **BR-003** | Deliver Defence Equality of Arms in Technology | MUST_HAVE | 70%+ defence practitioners with AI tools; no prosecution tool without defence equivalent |
| **BR-004** | Achieve Cross-Agency Digital Interoperability | MUST_HAVE | 90%+ case data exchanged via automated API by Year 4 |
| **BR-005** | Migrate Critical Legacy Applications | MUST_HAVE | 20+ of 37 applications migrated within 3 years; zero unplanned court disruption |
| **BR-006** | Establish AI Governance Framework | MUST_HAVE | Framework operational within 12 months; 100% ATRS compliance |
| **BR-007** | Improve Victim and Witness Experience | MUST_HAVE | 20% victim satisfaction improvement; 90%+ Victims' Code compliance |
| **BR-008** | Secure Green Book Business Case Approval | MUST_HAVE | Cost within 10%; IPA Gateway Amber/Green or better |
| **BR-009** | Comply with GDS Service Standard and TCoP | MUST_HAVE | All services pass GDS assessment; WCAG 2.2 AA compliance |
| **BR-010** | Ensure Data Protection Compliance | MUST_HAVE | 100% DPIA coverage; zero ICO enforcement actions |

### 3.2 Functional Requirements

| Requirement ID | Title | Priority | Complexity | Key Dependencies |
|----------------|-------|----------|------------|------------------|
| **FR-001** | AI Disclosure Review Engine | MUST_HAVE | HIGH | BR-006, INT-002 |
| **FR-002** | AI Case Summarisation | MUST_HAVE | HIGH | FR-001 |
| **FR-003** | AI Transcription and Translation | MUST_HAVE | HIGH | — |
| **FR-004** | Cross-Agency API Gateway | MUST_HAVE | HIGH | DR-001 |
| **FR-005** | Digital Case File Standard | MUST_HAVE | MEDIUM | — |
| **FR-006** | Court Case Management Enhancement | MUST_HAVE | HIGH | INT-001 |
| **FR-007** | Victim/Witness Case Tracking Service | MUST_HAVE | MEDIUM | — |
| **FR-008** | Remote Evidence Facilities | SHOULD_HAVE | MEDIUM | — |
| **FR-009** | Defence Technology Platform | MUST_HAVE | HIGH | BR-003, FR-001 |
| **FR-010** | Legacy Application Assessment Dashboard | SHOULD_HAVE | LOW | — |
| **FR-011** | AI Governance Register | MUST_HAVE | MEDIUM | — |
| **FR-012** | Sentence Data Integration | MUST_HAVE | MEDIUM | INT-004 |
| **FR-013** | Automated Victims' Code Compliance Monitoring | SHOULD_HAVE | MEDIUM | — |
| **FR-014** | Benefits Realisation Tracking | SHOULD_HAVE | MEDIUM | — |

### 3.3 Non-Functional Requirements

#### 3.3.1 Performance Requirements

- **Response Time** (NFR-P-001): Court case management page load < 2 seconds (p95); API gateway < 500ms (p95); AI disclosure review 10,000 items within 4 hours; AI transcription < 3 second latency; victim tracking < 3 seconds (p95)
- **Throughput** (NFR-P-002): API gateway 1,000 TPS sustained, 5,000 TPS burst; event broker 10,000 events/second; 500 concurrent case updates per minute
- **Concurrency**: 15,000 concurrent professional users during court sitting hours (09:00–17:00); 50,000 concurrent public users (victim tracking)

#### 3.3.2 Availability and Resilience

- **Availability** (NFR-A-001): Mission-critical systems 99.9% during sitting hours; important systems 99.5%; supporting systems 99.0%
- **Disaster Recovery** (NFR-A-002): RPO 15 minutes (mission-critical), 1 hour (other); RTO 1 hour (mission-critical), 4 hours (important); automated failover to secondary UK region within 15 minutes
- **Fault Tolerance** (NFR-A-003): Circuit breakers, retry with exponential backoff, bulkhead isolation, graceful degradation; AI failure must not affect core case management

#### 3.3.3 Security Requirements

- **Authentication** (NFR-SEC-001): SSO with MFA (authenticator app or hardware token; SMS not permitted); cross-agency federated SSO; 30-minute inactivity timeout
- **Authorisation** (NFR-SEC-002): RBAC with ABAC for fine-grained permissions; agency-level, case-level, and data sensitivity roles; defence/prosecution segregation enforced
- **Encryption** (NFR-SEC-003): TLS 1.3 for all transport; AES-256 at rest for all case/personal/evidence data; 90-day key rotation
- **Secrets Management** (NFR-SEC-004): No secrets in code/config/env vars; automated rotation
- **Vulnerability Management** (NFR-SEC-005): SAST on every build; DAST on staging; annual pen testing by CHECK/CREST testers; Critical vulns remediated within 24 hours
- **Network Security** (NFR-SEC-006): Zero-trust architecture; micro-segmentation; DDoS protection; encrypted inter-agency channels

#### 3.3.4 Scalability Requirements

- **Horizontal Scaling** (NFR-S-001): All systems must scale horizontally without code changes; support 50% caseload growth over 5 years
- **Data Volume** (NFR-S-002): Court data to 50TB over 5 years; digital evidence to 500TB over 5 years; hot/warm/cold storage tiering

#### 3.3.5 Compliance and Regulatory Requirements

- **Data Protection** (NFR-C-001): UK GDPR and DPA 2018 Part 3 compliance; all data within UK jurisdiction; automated retention and deletion; DPIA for all AI deployments
- **Audit Logging** (NFR-C-002): Tamper-evident audit trail for all operations on case/personal/evidence data; 7-year retention; cryptographic hash integrity
- **AI Transparency** (NFR-C-003): ATRS registration for all AI tools before deployment; AI outputs labelled in all user-facing contexts; bias assessment across protected characteristics
- **GDS Service Standard** (NFR-C-004): All 14 points addressed; WCAG 2.2 AA accessibility
- **NCSC CAF** (NFR-C-005): Alignment with all 4 CAF objectives; Cyber Essentials Plus minimum

#### 3.3.6 Usability Requirements

- **Accessibility** (NFR-U-001): WCAG 2.2 Level AA; screen reader compatibility; keyboard navigation; plain language (reading age 9 for public services)
- **Multi-Language** (NFR-U-002): Full Welsh bilingual support (statutory); AI-assisted translation for top 10 non-English languages
- **Magistrate-Friendly Interface** (NFR-U-003): Simplified interfaces for volunteer magistrates; task-oriented design; minimal training required

#### 3.3.7 Maintainability and Supportability

- **Observability** (NFR-M-001): Structured JSON logs with correlation IDs; distributed tracing across agency boundaries; SLO-based alerting with actionable runbooks
- **Infrastructure as Code** (NFR-M-002): All infrastructure defined as code; no manual production changes
- **CI/CD** (NFR-M-003): Automated pipeline with security scanning, accessibility testing, and contract testing

#### 3.3.8 Portability and Interoperability

- **API Standards** (NFR-I-001): OpenAPI 3.0+ specification; RESTful with JSON; versioning with 12-month backward compatibility; AsyncAPI for event interfaces
- **Open Standards** (NFR-I-002): Open data exchange formats; data exportable in open formats; OAuth 2.0/SAML 2.0 for auth; CloudEvents for event format

### 3.4 Integration Requirements

| Requirement ID | System | Integration Type | Priority | SLA |
|----------------|--------|-----------------|----------|-----|
| **INT-001** | Common Platform (HMCTS) | Real-time API + Event-driven | MUST_HAVE | <500ms p95; 99.5% availability |
| **INT-002** | Police Case Management Systems (43 forces) | API with adapter layer | MUST_HAVE | Case file delivery <4 hours |
| **INT-003** | CPS Case Management System | Real-time API + Event-driven | MUST_HAVE | <500ms p95; 99.5% availability |
| **INT-004** | HMPPS (Prison and Probation) | Event-driven + API | MUST_HAVE | Sentence data <5 minutes; 99.9% delivery |
| **INT-005** | Legal Aid Agency | API-based | MUST_HAVE | <1 second p95; 99.0% availability |
| **INT-006** | ICO DPIA Register | Batch/API (periodic) | SHOULD_HAVE | Within statutory timeframes |

### 3.5 Data Requirements

| Requirement ID | Data Entity | Classification | Volume | Retention |
|----------------|------------|----------------|--------|-----------|
| **DR-001** | Criminal Case Record | OFFICIAL-SENSITIVE | ~500,000 new/year | Per criminal justice schedule |
| **DR-002** | Digital Evidence Package | OFFICIAL-SENSITIVE | ~100TB/year (+30% annually) | Until appeal window + per offence |
| **DR-003** | Defendant Record | OFFICIAL-SENSITIVE (special category) | Per case volume | Per PNC rules / Rehabilitation of Offenders Act |
| **DR-004** | Victim/Witness Record | OFFICIAL-SENSITIVE (enhanced protection) | Per case volume | Per Victims' Code and case schedule |

### 3.6 Technical Constraints

- **TC-001**: All data must reside within UK jurisdiction. No processing in non-UK data centres, including AI model inference.
- **TC-002**: Must integrate with existing Common Platform — not replace it.
- **TC-003**: Must accommodate 43 independently governed police forces with different case management systems.
- **TC-004**: AI models for criminal justice must be auditable and explainable. Black-box AI is not acceptable for case-affecting functions.
- **TC-005**: Judicial steering group has veto on AI tools affecting court proceedings.
- **TC-006**: DPA 2018 Part 3 applies to law enforcement processing.

---

## 4. Deliverables

### 4.1 Design Phase Deliverables

| Deliverable | Description | Format | Due Date | Acceptance Criteria |
|-------------|-------------|--------|----------|---------------------|
| **High-Level Design (HLD)** | Architecture overview, component diagrams, technology stack, integration approach, security architecture | Document (PDF/Markdown) + C4 diagrams | Week 6 | Approved by Architecture Review Board via `/arckit.hld-review` |
| **Detailed Design (DLD)** | Component specifications, API contracts (OpenAPI), data models, security controls, deployment topology | Document + OpenAPI specs + ERDs | Week 12 | Approved by technical reviewers via `/arckit.dld-review` |
| **Security Design** | Threat model, NCSC CAF mapping, security controls, pen testing plan | Document | Week 8 | Approved by MoJ CISO |
| **AI Design** | AI model selection, training approach, bias mitigation strategy, explainability architecture, ATRS draft | Document | Week 8 | Approved by MoJ Chief AI Officer |
| **Test Strategy** | Unit, integration, performance, security, accessibility, and contract testing approach | Document | Week 10 | Approved by QA Lead |
| **Data Migration Strategy** | Per-application migration plan, data mapping, reconciliation approach, rollback procedures | Document | Week 10 | Approved by HMCTS CTO |

### 4.2 Development Phase Deliverables

| Deliverable | Description | Format | Due Date | Acceptance Criteria |
|-------------|-------------|--------|----------|---------------------|
| **Source Code** | All application source code with documentation | Git repository | Ongoing | Code review approved; meets coding standards |
| **Infrastructure as Code** | All infrastructure defined in code (Terraform/CloudFormation equivalent) | Git repository | Ongoing | Deployable to all environments; no manual changes |
| **Database Schemas** | DDL scripts, migration scripts, seed data | SQL/migration scripts | Week 16 | Schema review approved |
| **API Documentation** | Interactive API documentation for all cross-agency APIs | OpenAPI 3.0 spec + documentation site | Ongoing | All endpoints documented with examples |
| **Unit Tests** | Automated unit tests | Code | Ongoing | ≥80% code coverage |
| **Integration Tests** | Automated integration tests including cross-agency API contract tests | Code | Ongoing | Critical paths covered; contract tests validate agency compatibility |
| **Security Tests** | SAST, DAST, dependency scanning results | Reports | Per sprint | No critical/high vulnerabilities in production |
| **Accessibility Tests** | WCAG 2.2 AA automated and manual test results | Reports | Per release | Full WCAG 2.2 AA compliance |

### 4.3 Deployment Phase Deliverables

| Deliverable | Description | Format | Due Date | Acceptance Criteria |
|-------------|-------------|--------|----------|---------------------|
| **Deployed Application** | Fully functional application in production | Running system | Per phase milestone | Passes UAT, performance tests, security tests |
| **CI/CD Pipeline** | Automated build, test, deploy pipeline with quality gates | Pipeline configuration | Week 14 | Deploys to all environments; includes security and accessibility gates |
| **Monitoring & Alerting** | Dashboards, alerts, SLO/SLI definitions, business metrics | Monitoring platform config | Per go-live | All key metrics tracked per NFR-M-001 |
| **Runbooks** | Operational procedures for common tasks, incidents, and DR | Markdown documents | Per go-live | Covers deployment, rollback, incidents, DR |
| **Disaster Recovery Plan** | DR procedures, tested and documented | Document + test results | Per go-live | DR drill successfully executed |

### 4.4 Documentation Deliverables

| Deliverable | Description | Format | Due Date | Acceptance Criteria |
|-------------|-------------|--------|----------|---------------------|
| **Technical Documentation** | Architecture, design decisions (ADRs), component docs | Markdown / documentation site | Ongoing | Kept current with code changes |
| **API Documentation** | Full API reference with examples for all cross-agency interfaces | OpenAPI spec + docs site | Ongoing | All endpoints documented |
| **Operations Manual** | System administration, maintenance procedures | Document | Per go-live | SRE team trained |
| **User Manuals** | End-user documentation per persona (judge, prosecutor, defence, court staff, victim) | Document / online help | Per go-live | User training completed |
| **Training Materials** | Training guides and materials per user persona | Various formats | Per go-live | Users trained successfully |
| **ATRS Records** | Algorithmic Transparency Recording Standard records for all AI tools | Structured records | Before AI deployment | Published and approved |
| **DPIAs** | Data Protection Impact Assessments for all processing activities | Documents | Before processing begins | Approved by DPO and MoJ AI Officer |

### 4.5 Knowledge Transfer

| Activity | Description | Participants | Timeline | Acceptance Criteria |
|----------|-------------|--------------|----------|---------------------|
| **Technical Training** | Architecture, codebase walkthrough, deployment procedures | Internal dev team, SRE team | Weeks before and after go-live | Team can make changes and deploy independently |
| **Operations Training** | Monitoring, incident response, maintenance, DR procedures | SRE/Ops team | Per go-live | Team can operate system 24/7 |
| **User Training** | Per-persona training for all 8 user personas | End users per persona | Per go-live | Users can perform daily tasks |
| **Documentation Review** | Review all documentation for completeness and accuracy | All stakeholders | Per go-live | Docs approved by all parties |
| **AI Model Handover** | AI model documentation, retraining procedures, bias monitoring | Internal AI team | Before warranty expiry | Team can retrain and monitor AI models |

---

## 5. Project Timeline and Milestones

### 5.1 High-Level Timeline

**Total Duration**: 5 years from contract signing (phased)

| Phase | Duration | Key Milestones |
|-------|----------|----------------|
| **Phase 1: Design & Foundation** | Months 1-6 | Kickoff, resource onboarding, HLD, DLD, AI governance framework, security design |
| **Phase 2: Build & Pilot** | Months 7-18 | AI tools pilot (prosecution + defence simultaneously), CPS-HMCTS integration, victim tracking MVP, first legacy migrations |
| **Phase 3: Scale** | Months 19-36 | Full AI disclosure rollout, police-CPS integration, 20+ legacy migrations, full victim services |
| **Phase 4: Complete** | Months 37-60 | Remaining legacy migrations, optimisation, benefits realisation |
| **Warranty & Transition** | Months 55-66 | 6-month warranty, knowledge transfer, transition to BAU |

### 5.2 Key Milestones

| Milestone | Target Month | Deliverables Due | Exit Criteria |
|-----------|-------------|------------------|---------------|
| **M1: Project Kickoff** | Month 1 | Project plan, resource assignments, environment access | Kickoff meeting held, teams introduced |
| **M2: Design Approval** | Month 6 | HLD, DLD, security design, AI design, test strategy | Architecture Review Board approval |
| **M3: AI Governance Live** | Month 9 | AI governance framework, ATRS process, judicial steering group operational | MoJ AI Officer approval |
| **M4: AI Pilot Go-Live** | Month 15 | AI disclosure tools (prosecution + defence simultaneously), AI transcription/translation | Pilot approval; judicial steering group concurrence for case-affecting AI |
| **M5: Integration MVP** | Month 15 | CPS-HMCTS API integration live; victim case tracking MVP | Functional testing complete; GDS Beta assessment |
| **M6: Phase 2 Gate** | Month 18 | Phase 1 benefits demonstrated; OBC refined costs | Programme Board and HM Treasury Phase 2 approval |
| **M7: Full AI Rollout** | Month 30 | 80%+ Crown Court cases using AI disclosure; defence platform fully operational | CPS and defence adoption metrics met |
| **M8: Police Integration** | Month 30 | Police-CPS digital case file integration (85%+ forces via adapters) | NPCC endorsement; transaction volumes confirmed |
| **M9: Legacy Milestone** | Month 36 | 20+ of 37 legacy applications migrated | Migration quality metrics; zero unplanned disruption |
| **M10: Programme Completion** | Month 60 | All 37 legacy applications migrated; all services live | Programme Board sign-off |
| **M11: Benefits Review** | Month 72 | 12-month post-completion benefits assessment | SRO sign-off; NAO readiness |

### 5.3 Proposal Timeline

| Event | Date |
|-------|------|
| **RFP Issued** | [DATE — upon approval] |
| **Vendor Questions Due** | [DATE + 2 weeks] |
| **Answers Published** | [DATE + 3 weeks] |
| **Proposals Due** | [DATE + 6 weeks] |
| **Vendor Presentations** | [DATE + 8 weeks] |
| **Final Vendor Selection** | [DATE + 10 weeks] |
| **Contract Negotiation** | [DATE + weeks 11-13] |
| **Expected Project Start** | [DATE + week 14] |

---

## 6. Vendor Qualifications and Requirements

### 6.1 Mandatory Qualifications

Vendors MUST meet the following minimum qualifications to be considered. Failure to meet any mandatory qualification results in disqualification.

**MQ-1 — Experience**: Minimum 5 years of experience delivering technology projects for UK Government departments or equivalent public sector organisations.

**MQ-2 — Criminal Justice/Legal Domain**: Demonstrable experience in criminal justice, legal technology, or law enforcement technology within the past 5 years.

**MQ-3 — AI/ML Capability**: For Pillar 1 vendors: Proven AI/ML delivery capability including natural language processing, document analysis, and evidence triage in a regulated environment.

**MQ-4 — Security Certification**: Company must hold Cyber Essentials Plus certification (minimum) and ISO 27001 or equivalent. SC-clearable personnel available for criminal justice data access.

**MQ-5 — UK Data Residency**: All proposed infrastructure must be located within UK jurisdiction. No data processing outside UK borders, including AI model inference.

**MQ-6 — Financial Stability**: Company must provide audited financial statements for the past 3 years demonstrating financial stability sufficient to support the contract duration.

**MQ-7 — Digital Marketplace Registration**: Vendor must be registered on the UK Digital Marketplace (G-Cloud 14 and/or DOS 6) for the relevant lot(s).

**MQ-8 — Reference Projects**: At least 3 reference projects in the past 5 years demonstrating relevant capabilities, including at least 1 UK Government project.

### 6.2 Preferred Qualifications

Preference will be given to vendors with:

**PQ-1**: Experience with HMCTS, CPS, MoJ, or Home Office digital programmes

**PQ-2**: Expertise in event-driven architecture and API-first design for multi-agency environments

**PQ-3**: Demonstrated AI governance and ethics capability (ATRS, DPIA, bias testing)

**PQ-4**: GDS service assessment experience with a track record of passing assessments

**PQ-5**: Experience migrating legacy applications (including mainframe and 1970s-era systems) in operational environments

**PQ-6**: Strong observability and SRE practices with SLO-based operations

**PQ-7**: Open-source contribution and open standards advocacy (TCoP alignment)

### 6.3 Approved Technology Constraints

**Cloud Platform**: Must deploy on UK Government-approved cloud hosting (Crown Hosting, AWS UK regions, Azure UK regions, or equivalent G-Cloud approved hosting). Data must remain in UK jurisdiction at all times.

**Programming Languages**: Vendor may propose technology stack with justification. Preference for widely-supported, open-source technologies with active communities.

**API Standards**: RESTful APIs with OpenAPI 3.0+ specification; AsyncAPI for event-driven interfaces; JSON payloads; OAuth 2.0 for authentication.

**Infrastructure**: Infrastructure as Code mandatory (Terraform, CloudFormation, or equivalent). Container orchestration required (Kubernetes or equivalent).

**Monitoring**: Must integrate with programme-standard observability tooling. Structured JSON logging, distributed tracing, and metrics collection mandatory.

**Proposed Alternatives**: Vendors may propose alternative technologies if they can demonstrate superior fit for requirements and compliance with Architecture Principles (ARC-000-PRIN-v1.0). Justification must be included in proposal.

### 6.4 Team Requirements

**Minimum Team Composition** (per lot — adjust to lot scope):

- 1 Solution Architect (senior, 10+ years experience, SC clearable)
- 1 Security Architect (CISSP or equivalent, SC clearable)
- 1 Technical Lead (8+ years experience)
- Senior Developers (5+ years experience, number proportionate to lot)
- Developers (3+ years experience, number proportionate to lot)
- 1 QA Lead
- QA Engineers (proportionate to lot)
- 1 DevOps/Platform Engineer
- 1 Technical Writer
- For Pillar 1: 1 AI/ML Lead (PhD or equivalent experience in NLP/ML)
- For Pillar 1: AI Engineers (3+ years ML engineering experience)

**Key Personnel Requirements**:
- Key personnel (Solution Architect, Technical Lead, AI/ML Lead) must be dedicated to this project for at least 80% allocation
- CVs for all key personnel must be included in the proposal
- Key personnel cannot be changed without client written approval
- All personnel accessing criminal justice data must be SC clearable

**Location Requirements**:
- Key personnel must be available for regular on-site working at MoJ/HMCTS offices
- Vendor must have a UK presence for support and operations

---

## 7. Proposal Requirements

### 7.1 Proposal Format

Proposals must follow this structure:

#### Section 1: Executive Summary (3 pages max)
- High-level approach and key differentiators
- Summary of relevant experience
- Summary of costs

#### Section 2: Company Overview (5 pages max)
- Company history, size, financial stability
- Relevant certifications (ISO 27001, Cyber Essentials Plus)
- UK Government experience and Digital Marketplace registration

#### Section 3: Understanding of Requirements (10 pages max)
- Demonstrate understanding of criminal justice domain challenges
- Identify risks, ambiguities, and proposed clarifications
- Explain understanding of cross-agency complexity and judicial independence requirements

#### Section 4: Technical Solution (30 pages max)
- High-level architecture (C4 Context and Container diagrams)
- Technology stack and rationale (with reference to Architecture Principles ARC-000-PRIN-v1.0)
- Integration approach (API-first, event-driven per Principles 1, 11, 12)
- Security and compliance strategy (zero-trust per Principle 3)
- AI approach (for Pillar 1): Model selection, training, bias mitigation, explainability, ATRS compliance
- Scalability and performance approach (per Principles 5, 13)
- Disaster recovery and business continuity (per Principle 6)
- DevOps and deployment strategy (per Principles 17, 18, 19)
- Data migration approach (for Pillar 3)
- Open standards and vendor lock-in avoidance (per Principle 20)

#### Section 5: Project Approach and Methodology (10 pages max)
- Agile delivery methodology
- Project phases and timeline aligned to Section 5 milestones
- Risk management approach (reference ARC-001-RISK-v1.0)
- Change management process
- Quality assurance approach (including accessibility testing)
- GDS service assessment preparation
- Communication and governance plan

#### Section 6: Team and Resources (5 pages max)
- Proposed team structure and roles
- Key personnel CVs (appendix)
- Security clearance status and timeline
- Staff augmentation plans if needed
- UK presence and on-site availability

#### Section 7: Experience and References (10 pages max)
- Minimum 3 reference projects with:
  - Client name and contact information
  - Project scope, size, and duration
  - Technologies used
  - Challenges overcome
  - Outcomes achieved and benefits delivered
- UK Government project experience
- Criminal justice or legal technology experience
- AI/ML project experience (for Pillar 1 vendors)

#### Section 8: Cost Proposal (SEPARATE DOCUMENT — see Section 7.2)

#### Section 9: Assumptions and Risks
- Key assumptions made in proposal
- Identified risks and mitigation strategies
- Dependencies on client organisation

### 7.2 Cost Proposal Format

**Cost proposal must be provided as a SEPARATE document** to allow technical evaluation independent of cost.

**7.2.1 Pricing Model**:
- Vendors must offer fixed-price milestone-based pricing for design and build phases
- Vendors must offer managed service pricing for run phases
- Time and materials pricing with a cap may be proposed for legacy migration (Pillar 3) given inherent uncertainty

**7.2.2 Cost Breakdown Required**:
- Labour costs by role and phase
- Cloud infrastructure costs (hosting, compute, storage)
- AI model licensing and compute costs (Pillar 1)
- Third-party service costs (APIs, SaaS tools)
- Travel and expenses
- Contingency (percentage and justification)

**7.2.3 Ongoing Support and Maintenance**:
- Annual support and maintenance cost (post-build)
- SLA for support response times
- Included vs. out-of-scope support activities

**7.2.4 Pricing Terms**:
- Payment terms: Net 30 days from invoice
- Invoicing: Monthly in arrears for T&M; on milestone completion for fixed-price
- Currency: GBP
- Validity: Pricing valid for 6 months from proposal submission
- Annual price review mechanism for multi-year managed services

### 7.3 Submission Instructions

**Deadline**: Proposals must be received by **[DATE] at 17:00 GMT**

**Submission Method**: Via Digital Marketplace portal for the relevant lot(s)

**Format**:
- PDF format required
- Technical proposal and cost proposal as SEPARATE files
- File naming: `[VENDOR_NAME]_CriminalCourts_SOW_Technical.pdf` and `[VENDOR_NAME]_CriminalCourts_SOW_Cost.pdf`
- Maximum total file size: 50MB per file

**Questions**:
- Submit questions by [DATE] via Digital Marketplace messaging
- All questions and answers will be published to all vendors by [DATE]
- No proprietary or confidential information in questions (visible to all vendors)

**Late Proposals**: Will not be accepted under any circumstances

---

## 8. Evaluation Criteria

### 8.1 Evaluation Process

Proposals will be evaluated in two phases:

**Phase 1: Technical Evaluation** (Cost proposals remain sealed)
- Mandatory qualifications check (pass/fail) — Section 6.1
- Technical scoring (see Section 8.2)
- Shortlisting of top 3-5 vendors per lot

**Phase 2: Combined Evaluation**
- Cost proposals opened only for shortlisted vendors
- Combined technical and cost scoring
- Vendor presentations and Q&A (2 hours per vendor: 1 hour presentation, 1 hour Q&A)
- Final selection

### 8.2 Technical Evaluation Criteria

| Criteria | Weight | Max Points | Evaluation Focus |
|----------|--------|------------|------------------|
| **Technical Approach and Solution Design** | 30% | 30 | Architecture quality, compliance with ARC-000-PRIN-v1.0, technology choices, scalability, security, AI approach |
| **Project Approach and Methodology** | 15% | 15 | Delivery methodology, risk management (alignment with ARC-001-RISK-v1.0), quality assurance, GDS readiness, realistic timeline |
| **Team Qualifications and Experience** | 20% | 20 | Team expertise, relevant certifications, key personnel quality, security clearance readiness |
| **Relevant Experience and References** | 15% | 15 | UK Government projects, criminal justice domain, AI/ML delivery, legacy migration, similar scale |
| **Understanding of Requirements** | 5% | 5 | Demonstrated understanding of criminal justice complexity, judicial independence, equality of arms, multi-agency governance |
| **Social Value** | 15% | 15 | Apprenticeships, SME supply chain (33%+ target), environmental sustainability, community skills |
| **TOTAL** | **100%** | **100** | |

### 8.3 Cost Evaluation

**Scoring Method**: Cost is evaluated separately as 30% of the final combined score.

**Final Score Calculation**:
- Technical Score (out of 100) × 0.70 = Technical weighted score
- Cost Score (out of 100, lowest cost = 100, others proportional) × 0.30 = Cost weighted score
- **Final Score** = Technical weighted score + Cost weighted score

### 8.4 Vendor Presentations

Shortlisted vendors will be invited to present:
- **Duration**: 2 hours (1 hour presentation, 1 hour Q&A)
- **Audience**: Evaluation committee (MoJ Commercial, Enterprise Architecture, Security, MoJ AI Officer, HMCTS CTO, CPS CDO, programme team)
- **Format**: In-person at MoJ offices or hybrid
- **Content**: Technical deep-dive on architecture, AI approach, team introductions, demo of relevant existing capabilities

### 8.5 Selection Decision

**Decision Authority**: Programme Board (MoJ CDIO, HMCTS CEO, Programme Director) with MoJ Commercial approval

**Selection Timeline**: Final decision within 10 weeks of RFP issue

**Notification**: All vendors notified within 5 business days of decision with brief feedback

---

## 9. Contract Terms and Conditions

### 9.1 Contract Type

**Build Phase**: Fixed-price milestone-based (with change control for scope changes)
**Run Phase**: Managed service with SLA-linked performance deductions
**Legacy Migration (Pillar 3)**: Time and materials with cap per application

### 9.2 Payment Terms

**Payment Schedule** (fixed-price build):
- 10% upon contract signing and kickoff
- 20% upon design approval (Milestone M2)
- 30% upon pilot go-live (Milestone M4/M5)
- 20% upon full rollout milestones (M7/M8)
- 10% upon programme completion (M10)
- 10% retention held for 6 months post go-live (released at end of warranty)

**Managed Service Payments**: Monthly in arrears, with SLA-linked deductions for missed performance targets

### 9.3 Acceptance Criteria

Each deliverable must meet defined acceptance criteria (Section 4). Acceptance process:
1. Vendor submits deliverable with evidence of acceptance criteria met
2. Client reviews within 10 business days
3. Client accepts, rejects with specific feedback, or requests clarifications
4. Vendor addresses feedback and resubmits (within 5 business days)
5. Formal acceptance sign-off by designated approver
6. Maximum 2 rejection cycles per deliverable before escalation to programme board

### 9.4 Warranty and Support

**Warranty Period**: 6 months from each go-live milestone

**Warranty Coverage**:
- All defects identified during warranty fixed at no additional cost
- Response time for critical defects (system down/data integrity): 1 hour
- Response time for high defects (major feature broken): 4 hours
- Response time for medium defects: 2 business days
- Response time for low defects: 5 business days

**Post-Warranty Support**: Managed service agreement with SLA (see Section 9.5)

### 9.5 Ongoing Support and Maintenance

**Support Tiers**:
- **Tier 1 — L1 Support**: Client responsibility (HMCTS service desk)
- **Tier 2 — L2 Support**: Vendor responsibility (application support)
- **Tier 3 — L3 Support**: Vendor responsibility (engineering support)

**Support Hours**: 24/7 for Severity 1 issues on mission-critical systems; business hours for other severities

**Support SLA**:

| Severity | Response Time | Resolution Time | Penalty for Breach |
|----------|---------------|-----------------|-------------------|
| Severity 1 (Critical — System down, court operations affected) | 30 minutes | 4 hours | 2% monthly fee per incident |
| Severity 2 (High — Major feature broken) | 2 hours | 8 hours | 1% monthly fee per incident |
| Severity 3 (Medium — Minor feature issue) | 1 business day | 5 business days | None |
| Severity 4 (Low — Enhancement request) | 5 business days | Next release | None |

**Annual Maintenance**: Includes bug fixes, security patches, dependency updates, minor enhancements up to 100 person-days per year

### 9.6 Intellectual Property Rights

**Work Product Ownership**: Crown owns all bespoke development, configurations, and documentation created specifically for this programme.

**Vendor Pre-Existing IP**: Vendor retains ownership of pre-existing IP, reusable frameworks, and standard components. Crown receives perpetual, irrevocable, royalty-free licence.

**Open Source**: Vendor must disclose all open-source components and licences used. Licence compatibility must be verified (no GPL-incompatible licences for Crown-owned code without approval).

**AI Models**: Crown owns all fine-tuned models trained on criminal justice data. Vendor retains ownership of base/foundation models. Model weights and training data must be transferable.

### 9.7 Data and Security

**Data Ownership**: Crown retains ownership of all criminal justice data at all times

**Data Security**: Vendor must comply with NFR-SEC-001 through NFR-SEC-006 and Architecture Principle 3 (Security by Design — NON-NEGOTIABLE)

**Data Handling**:
- Data must not be used for vendor's purposes (including AI model training on other clients' data)
- Data must be returned or securely destroyed upon contract termination (NCSC guidance for data sanitisation)
- Vendor must sign Data Processing Agreement (DPA) for all personal data processing
- DPA 2018 Part 3 requirements for law enforcement processing must be met

**Security Clearance**: Vendor staff with access to criminal justice data must hold or obtain SC clearance. Vendor is responsible for clearance costs.

**Background Checks**: Baseline Personnel Security Standard (BPSS) minimum for all vendor staff; SC clearance for data-accessing roles

### 9.8 Confidentiality

Both parties agree to maintain confidentiality of proprietary information. Non-Disclosure Agreement (NDA) required before sharing detailed requirements, data, or architecture documents.

### 9.9 Liability and Indemnification

**Liability Cap**: To be negotiated; typically 150% of annual contract value

**Indemnification**: Vendor indemnifies Crown against:
- IP infringement claims arising from vendor's solution
- Data breaches caused by vendor negligence
- Violations of DPA 2018 or UK GDPR arising from vendor's processing
- Third-party claims arising from AI outputs where vendor's AI is at fault

### 9.10 Termination

**Termination for Convenience**: Crown may terminate with 90 days written notice, paying for work completed and reasonable wind-down costs

**Termination for Cause**: Either party may terminate if the other breaches material terms and fails to cure within 30 days of written notice

**Transition Assistance**: Vendor must provide 6 months of transition assistance to replacement vendor or Crown team, at agreed daily rates

### 9.11 Change Management

**Change Request Process**:
1. Either party submits written change request with scope, cost, and schedule impact assessment
2. Vendor provides impact analysis within 5 business days
3. Programme Director approves or rejects
4. Approved changes documented in formal change order
5. Contract amended accordingly

**Approval Thresholds**:
- Changes < £50,000 or 2 weeks: Programme Director approval
- Changes £50,000–£250,000 or 1 month: SRO approval
- Changes > £250,000 or 3+ months: Programme Board approval

---

## 10. Appendices

### Appendix A: Detailed Requirements Specification

**Reference Document**: `ARC-001-REQ-v1.0.md` — Criminal Courts Technology & AI Reform Business and Technical Requirements

Contains: 10 Business Requirements, 14 Functional Requirements, 22 Non-Functional Requirements, 4 Data Requirements, 6 Integration Requirements, 5 Use Cases, 8 User Personas, 4 Requirement Conflicts (resolved)

### Appendix B: Enterprise Architecture Principles

**Reference Document**: `ARC-000-PRIN-v1.0.md` — Criminal Courts Technology & AI Reform Enterprise Architecture Principles

Contains: 23 principles across 7 categories (Strategic, Data, Integration, Quality, Development, Criminal Justice, Governance). All vendor solutions must comply with these principles. Principle 3 (Security by Design) is NON-NEGOTIABLE. Principle 21 (Equality of Arms) and Principle 22 (Judicial Independence) are criminal justice-specific and must be respected.

### Appendix C: Risk Register

**Reference Document**: `ARC-001-RISK-v1.0.md` — Criminal Courts Technology & AI Reform Risk Register

Contains: 20 risks across 6 categories. Top risks: R-002 (Defence equality of arms, Critical 20), R-001 (Treasury funding, High 16), R-005 (AI ethics controversy, Medium 12). Vendors should reference risks in their proposals and explain mitigation approaches.

### Appendix D: Strategic Outline Business Case

**Reference Document**: `ARC-001-SOBC-v1.0.md` — Strategic Outline Business Case

Contains: Green Book 5-case model business case; recommended Option 2 (Phased Comprehensive Reform); investment ~£281M over 5 years; expected benefits ~£495M over 10 years.

### Appendix E: Stakeholder Analysis

**Reference Document**: `ARC-001-STKE-v1.0.md` — Stakeholder Drivers & Goals Analysis

Contains: 15 stakeholders, 15 drivers, 10 goals, 6 outcomes, 4 stakeholder conflicts (resolved). Key insight: vendors must understand the multi-agency governance complexity and the constitutional position of the judiciary.

### Appendix F: Glossary

| Term | Definition |
|------|-----------|
| ATRS | Algorithmic Transparency Recording Standard — UK Government AI transparency requirement |
| CAF | Cyber Assessment Framework — NCSC security assessment framework |
| Common Platform | HMCTS digital case management platform for criminal courts |
| CPS | Crown Prosecution Service — prosecution agency for England and Wales |
| DPA 2018 | Data Protection Act 2018 — UK implementation of GDPR with Part 3 for law enforcement |
| DPIA | Data Protection Impact Assessment — required for high-risk processing |
| DOS | Digital Outcomes and Specialists — UK Digital Marketplace procurement framework |
| G-Cloud | Government Cloud — UK Digital Marketplace framework for cloud services |
| GDS | Government Digital Service — UK Government digital standards body |
| HMCTS | HM Courts & Tribunals Service — agency operating courts in England and Wales |
| HMPPS | HM Prison and Probation Service — manages prisons and probation |
| IPA | Infrastructure and Projects Authority — government assurance body |
| LAA | Legal Aid Agency — administers legal aid in England and Wales |
| MoJ | Ministry of Justice |
| NCSC | National Cyber Security Centre — UK Government cyber security authority |
| NPCC | National Police Chiefs' Council — coordination body for 43 police forces |
| RASSO | Rape and Serious Sexual Offences — specialist case type requiring enhanced data protection |
| SC | Security Check — UK Government personnel security clearance level |
| TCoP | Technology Code of Practice — UK Government technology standards |
| WCAG | Web Content Accessibility Guidelines — international accessibility standard |

---

## 11. Questions and Contact Information

### Questions

All questions regarding this SOW/RFP must be submitted in writing via the Digital Marketplace.

**Subject Line**: "RFP Criminal Courts Technology & AI Reform — [Lot Number] — Question"
**Deadline for Questions**: [DATE — 2 weeks after RFP issue]

**Question Format**:
- Section reference (e.g., "Section 3.3.3 — Security Requirements")
- Specific question
- Context or rationale for question

All questions and answers will be published to all vendors to ensure fairness. Do not include confidential information in questions.

### Contact Information

**Primary Contact**:
MoJ Commercial Team
[Email — via Digital Marketplace messaging]

**Technical Queries**:
MoJ Enterprise Architecture Team
[Email — via Digital Marketplace messaging]

**Procurement Lead**:
MoJ Commercial Director
[Email — via Digital Marketplace messaging]

---

## Document Approval

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 0.1 | 2026-02-04 | ArcKit AI | Initial draft generated from programme artifacts |
| 0.2 | [DATE] | [AUTHOR] | Stakeholder review feedback |
| 1.0 | [DATE] | [AUTHOR] | Approved for issue to vendors |

**Approvals**

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Executive Sponsor (Lord Chancellor's Office) | [NAME] | _________ | [DATE] |
| Senior Responsible Owner (MoJ Permanent Secretary) | [NAME] | _________ | [DATE] |
| MoJ Commercial Director | [NAME] | _________ | [DATE] |
| Enterprise Architect | [NAME] | _________ | [DATE] |
| MoJ CISO | [NAME] | _________ | [DATE] |
| MoJ Legal | [NAME] | _________ | [DATE] |

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-REQ-v1.0 | Requirements | ArcKit | 10 BR, 14 FR, 22 NFR, 4 DR, 6 INT — source of truth for SOW requirements | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 23 principles across 7 categories — vendor compliance framework | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 15 stakeholders, evaluation priorities, multi-agency governance context | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` |
| ARC-001-RISK-v1.0 | Risk Register | ArcKit | 20 risks — vendor risk allocation and mitigation requirements | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md` |
| ARC-001-SOBC-v1.0 | Strategic Outline Business Case | ArcKit | Budget envelope, phasing, benefits targets, procurement route | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-SOBC-v1.0.md` |
| Independent Review of the Criminal Courts | Policy Review | GOV.UK | 180 recommendations — programme mandate | `projects/000-global/external/` |

---

**Generated by**: ArcKit `/arckit.sow` command
**Generated on**: 2026-02-04 14:30 GMT
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)
**Generation Context**: SOW generated from ARC-001-REQ-v1.0 (56 requirements), ARC-000-PRIN-v1.0 (23 principles), ARC-001-STKE-v1.0 (15 stakeholders), ARC-001-RISK-v1.0 (20 risks), ARC-001-SOBC-v1.0 (5-case business case)

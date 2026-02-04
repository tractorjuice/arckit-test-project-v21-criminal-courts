# Project Requirements: Criminal Courts Technology & AI Reform

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.requirements`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-REQ-v1.0 |
| **Document Type** | Business and Technical Requirements |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-04 |
| **Last Modified** | 2026-02-04 |
| **Review Cycle** | Monthly |
| **Next Review Date** | 2026-03-06 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, HMPPS Digital, Criminal Justice Technology Leadership |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial creation from `/arckit.requirements` command | PENDING | PENDING |

## Document Purpose

This document defines the comprehensive business, functional, non-functional, integration, and data requirements for the Criminal Courts Technology & AI Reform programme. Requirements are traceable to stakeholder goals (ARC-001-STKE-v1.0) and aligned with enterprise architecture principles (ARC-000-PRIN-v1.0). This document will be used for vendor RFPs, architecture reviews, GDS service assessments, and programme governance.

---

## Executive Summary

### Business Context

The criminal justice system in England and Wales faces a crisis: 77,000+ outstanding Crown Court cases, fragmented digital systems across police, CPS, courts, probation, and prisons, a troubled Common Platform rollout, and 37 critical legacy applications requiring modernisation. The Independent Review of the Criminal Courts (Leveson Review, 2025–2026) made 180 recommendations including AI for case preparation and disclosure, legacy system migration, cross-agency integration, and improved victim/witness experience.

This programme will deliver technology-enabled reform across the criminal justice chain, from investigation through to sentencing and beyond. It must operate within the UK Government compliance framework (GDS Service Standard, TCoP, NCSC CAF, UK GDPR/DPA 2018 Part 3, AI Playbook, ATRS, Green Book) and respect the constitutional independence of the judiciary.

The programme's complexity is driven by the multi-agency stakeholder landscape: MoJ, HMCTS, CPS, HMPPS, Legal Aid Agency, 43 police forces, the judiciary, and the defence community — each with distinct systems, budgets, and governance.

### Objectives

- Reduce the Crown Court outstanding caseload from 77,000+ to below 50,000 within 3 years
- Deploy AI-assisted disclosure and case preparation tools across prosecution and defence
- Achieve cross-agency interoperability replacing manual data transfer between justice agencies
- Migrate 37 critical legacy applications to supported, modern platforms
- Establish an AI governance framework with judicial oversight for criminal justice AI
- Improve victim and witness experience with real-time case tracking and remote evidence

### Expected Outcomes

- **O-1**: Crown Court backlog reduced below 50,000; charge-to-trial time reduced by 30% (from 18+ months to <13 months)
- **O-2**: AI tools deployed across prosecution and defence with 100% governance compliance and zero AI-related miscarriages of justice
- **O-3**: 90%+ case data exchanged automatically between agencies; data errors reduced by 80%
- **O-4**: 20% improvement in victim satisfaction; 90%+ Victims' Code compliance
- **O-5**: <10 legacy applications remaining after 3 years; legacy incidents reduced by 60%
- **O-6**: Programme expenditure within 10% of approved business case; IPA Gateway rating Amber/Green or better

### Project Scope

**In Scope**:
- AI-assisted disclosure review and digital evidence triage (prosecution and defence)
- AI transcription, translation, and case summarisation tools
- Cross-agency API integration platform (police, CPS, HMCTS, HMPPS, LAA)
- Legacy application assessment, migration, and decommissioning
- AI governance framework with ATRS, DPIA, and judicial oversight
- Victim/witness case tracking and notification service
- Remote evidence facilities enhancement
- Common Platform stabilisation and evolution
- Defence practitioner technology access programme

**Out of Scope**:
- New court building or physical infrastructure
- Judicial appointment or reform of sentencing guidelines
- Police operational systems beyond case file integration
- Prison management systems beyond sentence data integration
- Legal aid policy reform (though technology requirements for defence access are in scope)
- Predictive AI for case outcomes or sentencing (prohibited without explicit ministerial and judicial approval)

---

## Stakeholders

| Stakeholder | Role | Organisation | Involvement Level |
|-------------|------|--------------|-------------------|
| Lord Chancellor | Ministerial lead, policy owner | MoJ | Decision maker (strategic) |
| MoJ Permanent Secretary | Accounting Officer, SRO | MoJ | Decision maker (spending) |
| MoJ CDIO | Technology strategy | MoJ Digital | Technical decision authority |
| MoJ Chief AI Officer | AI governance and ethics | MoJ | AI assurance authority |
| HMCTS Chief Executive | Operational delivery | HMCTS | Programme board, operational requirements |
| HMCTS CTO | Court systems delivery | HMCTS Digital | Technical architecture |
| DPP / CPS leadership | Prosecution technology | CPS | Cross-agency integration |
| Lady Chief Justice | Constitutional independence | Judiciary | Judicial steering group |
| Lead Judge for AI | Technology oversight | Judiciary | AI governance, judicial approval |
| NPCC | Police data sharing | 43 Police Forces | Evidence integration |
| CBA / Law Society | Defence representation | Bar/Solicitors | Equality of arms, practitioner access |
| LAA Chief Executive | Legal aid administration | LAA | Defence technology access |
| Victims' Commissioner | Victims' interests | Independent | Victim experience oversight |
| ICO | Data protection regulation | ICO | DPIA review, compliance |
| GDS / CDDO | Digital standards | Cabinet Office | Service assessments, TCoP |
| HM Treasury | Spending authority | HM Treasury | Business case approval |
| NAO | Value for money oversight | Parliament | Post-implementation review |

---

## Business Requirements

### BR-001: Reduce Crown Court Case Backlog

**Description**: The programme must deliver technology-enabled efficiency improvements that contribute to reducing the Crown Court outstanding caseload from 77,000+ to below 50,000 cases within 3 years.

**Rationale**: Addresses stakeholder goal G-1 (HMCTS CEO), stakeholder driver SD-1 (Lord Chancellor — backlog reduction and public confidence). The Leveson Review was commissioned in direct response to this crisis.

**Success Criteria**:
- Outstanding Crown Court caseload below 50,000 by Year 3
- Average charge-to-trial time reduced by 30% (from 18+ months to <13 months)
- Proportion of effective (non-cracked, non-adjourned) trials increased by 15%
- Adjournment rate due to administrative/technical reasons reduced by 50%

**Priority**: MUST_HAVE

**Stakeholder**: HMCTS Chief Executive (Goal G-1), Lord Chancellor (SD-1)

---

### BR-002: Deploy AI for Prosecution Case Preparation and Disclosure

**Description**: AI tools must be deployed to assist CPS prosecutors with disclosure review, digital evidence triage, case summarisation, and case file preparation, improving case quality and throughput.

**Rationale**: Addresses stakeholder goal G-2 (DPP/CPS), drivers SD-4 (CPS — prosecution efficiency) and SD-7 (MoJ AI Officer — responsible AI). Disclosure failure is the leading cause of collapsed trials. AI can process volumes of digital evidence impossible for humans to review manually.

**Success Criteria**:
- 80%+ of Crown Court cases use AI-assisted disclosure review by Year 3
- Disclosure-related case collapses reduced by 40%
- Average disclosure review time per case reduced by 50%
- 100% ATRS registration for all deployed AI tools
- 100% DPIA completion before deployment

**Priority**: MUST_HAVE

**Stakeholder**: Director of Public Prosecutions (Goal G-2), MoJ Chief AI Officer (Goal G-6)

---

### BR-003: Deliver Defence Equality of Arms in Technology

**Description**: Defence practitioners must have access to AI-assisted case preparation, disclosure review, and evidence analysis tools equivalent in capability to those available to prosecution agencies.

**Rationale**: Addresses stakeholder goal G-3 (LAA), driver SD-6 (CBA/Law Society — equality of arms). Aligns with Architecture Principle 21 (Equality of Arms). Without defence parity, AI-enhanced prosecution creates structural unfairness that is constitutionally unacceptable (Article 6 ECHR).

**Success Criteria**:
- 70%+ of criminal defence practitioners with access to AI case preparation tools by Year 3
- No prosecution AI tool deployed without a defence equivalent available simultaneously
- Defence practitioner satisfaction score ≥7/10 with technology tools
- Zero successful legal challenges on technology inequality grounds

**Priority**: MUST_HAVE

**Stakeholder**: LAA Chief Executive (Goal G-3), CBA/Law Society (SD-6)

---

### BR-004: Achieve Cross-Agency Digital Interoperability

**Description**: Case data, evidence, and outcomes must flow seamlessly between police, CPS, HMCTS, HMPPS, and LAA through standardised API-based integration, replacing manual data transfer and eliminating duplicate data entry.

**Rationale**: Addresses stakeholder goal G-4 (MoJ CDIO), drivers SD-3 (HMCTS — operational efficiency), SD-4 (CPS), SD-5 (NPCC — evidence sharing), SD-13 (HMPPS — sentence integration). Aligns with Architecture Principle 1 (Cross-Agency Interoperability by Design).

**Success Criteria**:
- 90%+ of case data exchanged via automated API integration by Year 4
- Data rekeying incidents reduced by 90%
- Average case data transfer time between agencies reduced from days to seconds
- Cross-agency data standards published and adopted by all agencies
- API catalogue operational with all integration specifications discoverable

**Priority**: MUST_HAVE

**Stakeholder**: MoJ CDIO (Goal G-4)

---

### BR-005: Migrate Critical Legacy Applications

**Description**: Assess and execute phased migration of 37 critical legacy applications to modern, supported platforms, prioritised by cyber risk and business impact, with zero unplanned disruption to live court operations.

**Rationale**: Addresses stakeholder goal G-5 (HMCTS CTO), drivers SD-3, SD-9 (HM Treasury — value for money), SD-15 (NAO — accountability). Aligns with Architecture Principle 4 (Legacy Modernisation). Legacy applications on unsupported platforms represent the greatest technical and cyber security risk.

**Success Criteria**:
- Portfolio assessment of all 37 applications complete within 6 months
- 20+ applications migrated or decommissioned within 3 years
- All 37 within 5 years
- Legacy-related incidents reduced by 60%
- Zero unplanned disruption to court operations during migration
- Migration costs within 10% of business case estimates

**Priority**: MUST_HAVE

**Stakeholder**: HMCTS CTO (Goal G-5)

---

### BR-006: Establish AI Governance Framework

**Description**: Establish and operationalise an AI governance framework for criminal justice with mandatory categorisation, ATRS registration, DPIA, judicial approval gates for case-affecting AI, and independent ethics review.

**Rationale**: Addresses stakeholder goal G-6 (MoJ Chief AI Officer), drivers SD-2 (judiciary — judicial independence), SD-7, SD-11 (ICO — data protection). Aligns with Architecture Principle 2 (Human-Centred AI Augmentation). Governance must precede large-scale AI deployment.

**Success Criteria**:
- AI governance framework published and operational within 12 months
- 100% of AI tools registered in ATRS within 18 months
- 100% of AI tools with approved DPIAs
- Judicial AI steering group operational with meeting cadence
- Independent ethics review board appointed with external members
- AI categorisation taxonomy agreed (productivity/insight/accessibility/predictive)

**Priority**: MUST_HAVE

**Stakeholder**: MoJ Chief AI Officer (Goal G-6)

---

### BR-007: Improve Victim and Witness Experience

**Description**: Implement technology that demonstrably improves the victim and witness experience, including real-time case tracking, automated Victims' Code compliance monitoring, and enhanced remote evidence facilities.

**Rationale**: Addresses stakeholder goal G-7 (HMCTS CEO, Victims' Commissioner), driver SD-12. Aligns with Architecture Principle 23 (Victim and Witness Protection). Victims' Code compliance is a legal obligation frequently unmet.

**Success Criteria**:
- 20% improvement in victim satisfaction score within 2 years
- 90%+ Victims' Code compliance rate (automated monitoring)
- Real-time case tracking available to all registered victims
- Remote evidence facilities available at all Crown Court centres
- Witness attendance rate improved by 10%

**Priority**: MUST_HAVE

**Stakeholder**: HMCTS CEO (Goal G-7), Victims' Commissioner (SD-12)

---

### BR-008: Secure Green Book Business Case Approval

**Description**: Produce a robust HM Treasury Green Book 5-case model business case with quantified benefits, realistic cost estimates, and phased investment gates that secures multi-year funding approval.

**Rationale**: Addresses stakeholder goal G-8 (MoJ Permanent Secretary), driver SD-9 (HM Treasury — value for money). Without Treasury approval, the programme cannot proceed. Must learn from Common Platform cost overruns.

**Success Criteria**:
- Full business case approval within 12 months
- IPA Gateway review rating Amber/Green or better
- Cost estimates within 10% of actuals at each gate
- Benefits realisation tracked quarterly with independent verification
- Lessons learned from Common Platform explicitly incorporated

**Priority**: MUST_HAVE

**Stakeholder**: MoJ Permanent Secretary (Goal G-8), HM Treasury (SD-9)

---

### BR-009: Comply with GDS Service Standard and TCoP

**Description**: All new digital services must pass GDS service assessment at alpha, beta, and live stages. All technology decisions must comply with the Technology Code of Practice.

**Rationale**: Addresses stakeholder goal G-9 (MoJ CDIO), driver SD-10 (GDS/CDDO — digital standards). GDS compliance is mandatory; TCoP compliance is required for spend approvals.

**Success Criteria**:
- All services pass GDS service assessment on first or second attempt
- TCoP compliance confirmed for all technology decisions
- Accessibility audits pass WCAG 2.2 AA for all services
- User research conducted with representative users for all services

**Priority**: MUST_HAVE

**Stakeholder**: MoJ CDIO (Goal G-9), GDS/CDDO (SD-10)

---

### BR-010: Ensure Data Protection Compliance

**Description**: Complete DPIAs for all processing activities, establish lawful bases for cross-agency data processing, and implement DPA 2018 Part 3 compliant processing for all law enforcement data.

**Rationale**: Addresses stakeholder goal G-10 (MoJ DPO), driver SD-11 (ICO — data protection). Criminal justice data is among the most sensitive categories. Aligns with Architecture Principle 10 (Privacy, Data Protection and Lawful Processing).

**Success Criteria**:
- 100% DPIA coverage for all data processing activities
- Zero ICO enforcement actions
- Data subject access requests responded to within statutory timeframes
- All cross-agency data sharing agreements formalised within 18 months
- DPA 2018 Part 3 compliance confirmed for all law enforcement processing

**Priority**: MUST_HAVE

**Stakeholder**: MoJ Data Protection Officer (Goal G-10), ICO (SD-11)

---

## Functional Requirements

### User Personas

#### Persona 1: Crown Court Judge
- **Role**: Presides over Crown Court trials and hearings
- **Goals**: Access accurate case information, manage case listings efficiently, maintain judicial discretion
- **Pain Points**: Unreliable Common Platform, manual data reconciliation, limited real-time scheduling information
- **Technical Proficiency**: Medium — uses existing digital tools but expects reliability and simplicity

#### Persona 2: CPS Prosecutor
- **Role**: Prepares and presents prosecution cases, manages disclosure
- **Goals**: Prepare cases efficiently, ensure complete disclosure, access evidence seamlessly
- **Pain Points**: Manual disclosure review of vast digital evidence, incompatible police systems, duplicate data entry
- **Technical Proficiency**: Medium — familiar with CPS digital tools, needs efficiency improvements

#### Persona 3: Defence Barrister/Solicitor
- **Role**: Represents defendants, reviews prosecution disclosure, prepares defence case
- **Goals**: Access disclosure materials efficiently, prepare defence case with equivalent tools to prosecution
- **Pain Points**: Minimal technology support, manual evidence review, no AI tools, legal aid constraints
- **Technical Proficiency**: Medium — uses basic digital tools, varies significantly across practitioners

#### Persona 4: Police Officer/Detective
- **Role**: Investigates crimes, prepares case files for CPS, provides evidence
- **Goals**: Minimise time on case file preparation, share evidence digitally, avoid rekeying
- **Pain Points**: Manual case file preparation, incompatible systems between forces and CPS, excessive paperwork
- **Technical Proficiency**: Medium — uses force-specific systems, frustrated by integration gaps

#### Persona 5: HMCTS Court Staff
- **Role**: Administers court proceedings, manages listings, handles case files
- **Goals**: Reduce manual administrative burden, access reliable systems, serve court users efficiently
- **Pain Points**: Legacy system workarounds, manual data entry across multiple systems, Common Platform issues
- **Technical Proficiency**: Medium — experienced with current systems but resistant to frequent change

#### Persona 6: Victim/Witness
- **Role**: Participant in criminal proceedings (prosecution witness, complainant, or witness)
- **Goals**: Know what is happening with their case, attend/give evidence with minimum stress, be treated with respect
- **Pain Points**: No visibility of case progress, poor communication, repeated adjournments, stressful court attendance
- **Technical Proficiency**: Low to Medium — expects simple, accessible digital services

#### Persona 7: Magistrate
- **Role**: Unpaid volunteer judicial officer presiding over magistrates' court
- **Goals**: Access case information quickly, manage case lists, make informed decisions
- **Pain Points**: Complex professional-grade systems not designed for volunteer users, limited training
- **Technical Proficiency**: Low to Medium — volunteer with varying digital skills

#### Persona 8: Probation Officer
- **Role**: Supervises offenders in the community, prepares pre-sentence reports
- **Goals**: Receive court outcomes in real time, access case history, manage caseload efficiently
- **Pain Points**: Manual collection of court outcome data, inconsistent information, delayed sentencing data
- **Technical Proficiency**: Medium — uses HMPPS systems daily

---

### Use Cases

#### UC-1: AI-Assisted Disclosure Review

**Actor**: CPS Prosecutor

**Preconditions**:
- Case file received from police with digital evidence attached
- AI disclosure tool available and ATRS-registered
- Prosecutor authenticated with appropriate permissions

**Main Flow**:
1. Prosecutor opens case in CPS case management system
2. System presents digital evidence package from police (body-worn video, communications, documents)
3. Prosecutor initiates AI-assisted disclosure review
4. System processes evidence through AI triage, flagging potentially disclosable material
5. AI presents categorised evidence with confidence scores and rationale
6. Prosecutor reviews AI recommendations, accepting or overriding each
7. System generates disclosure schedule with audit trail of AI involvement
8. Prosecutor approves disclosure schedule for service on defence

**Postconditions**:
- Disclosure schedule generated with all disclosable material identified
- Audit trail records AI involvement and prosecutor decisions
- Defence notified of disclosure availability

**Alternative Flows**:
- **Alt 3a**: If evidence volume exceeds AI processing threshold, system prioritises by relevance and processes in batches
- **Alt 6a**: If prosecutor disagrees with AI recommendation, override recorded with reason

**Exception Flows**:
- **Ex 1**: AI service unavailable — system falls back to manual disclosure workflow with notification to prosecutor

**Business Rules**:
- AI must not make final disclosure decisions — prosecutor retains full authority
- All AI-assisted outputs must be clearly labelled in the disclosure schedule
- Defence must be notified that AI was used in disclosure review process

**Priority**: CRITICAL

---

#### UC-2: Defence AI Case Preparation

**Actor**: Defence Barrister/Solicitor

**Preconditions**:
- Defence practitioner authenticated via defence technology platform
- Disclosure materials served by prosecution and accessible
- Defence AI tools available (equivalent to prosecution tools)

**Main Flow**:
1. Defence practitioner logs into defence technology platform
2. System displays case file and disclosure materials
3. Practitioner initiates AI-assisted analysis of disclosure
4. AI identifies gaps, inconsistencies, and potentially undisclosed material
5. Practitioner reviews AI analysis and prepares defence response
6. System generates defence case preparation notes with AI audit trail

**Postconditions**:
- Defence analysis complete with AI-assisted insights
- Audit trail maintained for transparency

**Priority**: CRITICAL

---

#### UC-3: Cross-Agency Case Data Exchange

**Actor**: System-to-system (police → CPS → HMCTS → HMPPS)

**Preconditions**:
- Data sharing agreements in place between agencies
- API authentication credentials configured
- Event broker operational

**Main Flow**:
1. Police complete investigation and charge suspect
2. Police system publishes "charge" event with standardised digital case file
3. CPS system receives event, creates prosecution case record
4. CPS requests additional evidence via API from police system
5. CPS files case with HMCTS via API
6. HMCTS system creates court case, schedules hearing
7. Court hearing results published as "hearing outcome" event
8. All agencies receive outcome event and update their records
9. On sentencing, HMPPS receives sentence event for offender management

**Postconditions**:
- Case data consistent across all agency systems
- No manual rekeying required
- Full audit trail of data exchanges

**Priority**: CRITICAL

---

#### UC-4: Victim Case Tracking

**Actor**: Victim

**Preconditions**:
- Victim registered for case tracking service
- Identity verified through appropriate mechanism
- Case exists in court system

**Main Flow**:
1. Victim accesses case tracking service (web or mobile)
2. System authenticates victim and displays their case(s)
3. Victim views current case status, next hearing date, and key milestones
4. When case status changes, system sends automated notification (SMS, email, or app notification)
5. Victim can view Victims' Code entitlements and contact information for support services

**Postconditions**:
- Victim informed of case progress
- Victims' Code compliance automatically logged

**Alternative Flows**:
- **Alt 4a**: If victim prefers not to receive notifications, they can check status on demand
- **Alt 1a**: If victim is a minor or vulnerable, guardian/support worker can access on their behalf

**Priority**: HIGH

---

#### UC-5: Legacy System Migration

**Actor**: HMCTS Technical Team

**Preconditions**:
- Legacy application assessed and prioritised for migration
- Target platform selected and configured
- Data migration plan validated
- Rollback plan tested

**Main Flow**:
1. Technical team initiates parallel running period
2. New system processes live workload alongside legacy system
3. Automated reconciliation verifies data consistency between systems
4. After validation period, traffic switched to new system
5. Legacy system enters read-only mode for historical reference
6. After retention period, legacy system decommissioned

**Postconditions**:
- New system operational with all data migrated
- Zero data loss verified through reconciliation
- Legacy system decommissioned with audit trail

**Priority**: HIGH

---

### Functional Requirements Detail

#### FR-001: AI Disclosure Review Engine

**Description**: System must provide AI-assisted disclosure review that analyses digital evidence (documents, images, video, communications) and flags potentially disclosable material with categorisation and confidence scoring.

**Relates To**: BR-002, UC-1

**Acceptance Criteria**:
- [ ] Given a case with 10,000+ digital evidence items, when AI disclosure review is initiated, then all items are categorised within 4 hours
- [ ] Given AI-flagged material, when a prosecutor reviews it, then confidence score and reasoning are visible for each item
- [ ] Given a prosecutor override of AI recommendation, when override is recorded, then audit trail captures the reason and original AI assessment
- [ ] Given defence request for AI methodology, when requested, then a plain-language explanation of AI process is available

**Data Requirements**:
- **Inputs**: Digital evidence files (PDF, DOCX, images, video, audio, communications data)
- **Outputs**: Categorised evidence list, disclosure schedule, audit log
- **Validations**: Evidence file integrity verified before processing; output consistency checks

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: BR-006 (AI governance framework must be operational), INT-002 (police evidence integration)

**Assumptions**: AI models will be trained/fine-tuned on criminal justice disclosure standards

---

#### FR-002: AI Case Summarisation

**Description**: System must generate plain-language case summaries from case files, witness statements, and evidence, supporting both prosecution and defence case preparation.

**Relates To**: BR-002, BR-003

**Acceptance Criteria**:
- [ ] Given a complete case file, when summarisation is requested, then a structured summary is generated within 5 minutes
- [ ] Given a summary, when reviewed by a legal professional, then key facts, charges, evidence summary, and witness list are accurate
- [ ] Given a summary, when generated, then it is clearly labelled as AI-generated with timestamp and model version
- [ ] Given the same case file, when summarised by prosecution and defence tools, then both have access to the same source material

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: FR-001 (disclosure engine provides evidence base)

---

#### FR-003: AI Transcription and Translation

**Description**: System must provide real-time and batch transcription of court proceedings, police interviews, and evidence, with translation support for the most common non-English languages used in criminal proceedings.

**Relates To**: BR-002

**Acceptance Criteria**:
- [ ] Given a live court hearing, when transcription is activated, then real-time text appears within 3 seconds of speech
- [ ] Given an audio recording, when batch transcription is requested, then transcript is produced with ≥95% accuracy
- [ ] Given a non-English language audio file, when translation is requested, then translation is available for at least the top 10 non-English languages used in criminal proceedings
- [ ] Given a transcript, when reviewed, then speaker identification is ≥90% accurate

**Priority**: MUST_HAVE

**Complexity**: HIGH

---

#### FR-004: Cross-Agency API Gateway

**Description**: System must provide a central API gateway enabling standardised, authenticated, and authorised data exchange between police, CPS, HMCTS, HMPPS, and LAA systems.

**Relates To**: BR-004, UC-3

**Acceptance Criteria**:
- [ ] Given a police system sending a charge event, when the event is published, then CPS and HMCTS systems receive it within 30 seconds
- [ ] Given an API request from an agency, when authentication is verified, then request is routed to the appropriate service
- [ ] Given API transaction data, when queried, then full audit trail is available showing source, destination, timestamp, and payload hash
- [ ] Given 43 different police systems, when they send case files, then the gateway normalises data to the common format

**Data Requirements**:
- **Inputs**: Case data, evidence metadata, hearing outcomes, sentence data in agency-specific formats
- **Outputs**: Normalised case data in common format, event notifications, audit logs
- **Validations**: Schema validation on all inbound data; referential integrity checks

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: DR-001 (common data standards)

---

#### FR-005: Digital Case File Standard

**Description**: System must define and enforce a standardised digital case file format that all agencies can produce and consume, replacing ad-hoc file formats and manual case file preparation.

**Relates To**: BR-004, UC-3

**Acceptance Criteria**:
- [ ] Given a case file from any police force, when submitted through the gateway, then it conforms to the common digital case file schema
- [ ] Given a non-conforming case file, when submitted, then validation errors are returned with specific guidance on corrections
- [ ] Given a complete digital case file, when accessed by CPS, then all elements (charges, evidence list, witness details, defendant details) are structured and searchable

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-006: Court Case Management Enhancement

**Description**: Enhanced court case management supporting digital workflows, AI-assisted scheduling recommendations, and real-time case status tracking across all court types (Crown Court and magistrates' courts).

**Relates To**: BR-001, BR-009

**Acceptance Criteria**:
- [ ] Given a Crown Court centre, when the daily list is generated, then AI scheduling recommendations are presented to the listing officer with judicial discretion preserved
- [ ] Given a case status change, when recorded in the system, then all registered parties are notified in real time
- [ ] Given a magistrates' court user, when accessing the system, then a simplified interface appropriate for volunteer magistrates is available
- [ ] Given court staff, when using the system, then manual data entry is reduced by at least 50% compared to current workflows

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: INT-001 (Common Platform integration)

---

#### FR-007: Victim/Witness Case Tracking Service

**Description**: A victim and witness-facing digital service providing real-time case tracking, notifications, and support information, accessible via web and mobile.

**Relates To**: BR-007, UC-4

**Acceptance Criteria**:
- [ ] Given a registered victim, when a case status changes, then notification is sent within 5 minutes via chosen channel
- [ ] Given a victim, when accessing the service, then current case status, next hearing date, and outcome are displayed in plain language
- [ ] Given a vulnerable victim, when accessing the service, then accessibility features (screen reader, high contrast, large text) are fully functional
- [ ] Given Victims' Code requirements, when a communication obligation arises, then automated compliance monitoring logs whether the obligation was met

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-008: Remote Evidence Facilities

**Description**: Provide secure, high-quality video link facilities for witnesses to give evidence remotely from locations outside the courtroom, including vulnerable witness suites.

**Relates To**: BR-007

**Acceptance Criteria**:
- [ ] Given a remote evidence session, when initiated, then video and audio quality supports clear communication without interruption
- [ ] Given a vulnerable witness, when using remote facilities, then special measures (screens, intermediary support) are technically supported
- [ ] Given a remote evidence session, when in progress, then the judge, jury, prosecution, and defence can all see and hear the witness clearly
- [ ] Given a Crown Court centre, when remote evidence is required, then at least one remote evidence facility is available

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-009: Defence Technology Platform

**Description**: A cloud-based platform providing defence practitioners with AI-assisted case preparation tools, secure access to disclosure materials, evidence analysis, and case management.

**Relates To**: BR-003, UC-2

**Acceptance Criteria**:
- [ ] Given a defence practitioner, when authenticated, then they can access all disclosure materials for their cases
- [ ] Given AI tools on the platform, when compared to prosecution tools, then functional capability is equivalent
- [ ] Given a defence practitioner in a small firm, when accessing the platform, then no specialist IT infrastructure is required beyond a standard browser
- [ ] Given case materials, when downloaded for offline use, then data is encrypted at rest on the practitioner's device

**Priority**: MUST_HAVE

**Complexity**: HIGH

**Dependencies**: BR-003 (defence funding mechanism), FR-001 (AI engine available for defence use)

---

#### FR-010: Legacy Application Assessment Dashboard

**Description**: A portfolio management dashboard tracking the status, risk rating, and migration plan for all 37 critical legacy applications.

**Relates To**: BR-005, UC-5

**Acceptance Criteria**:
- [ ] Given the legacy portfolio, when viewed, then each application's risk rating, support status, and migration timeline are visible
- [ ] Given a legacy application, when its risk rating changes, then automated alerts notify the programme team
- [ ] Given migration progress, when tracked, then cost, timeline, and quality metrics are visible per application

**Priority**: SHOULD_HAVE

**Complexity**: LOW

---

#### FR-011: AI Governance Register

**Description**: A register tracking all AI tools deployed across the criminal justice system with ATRS status, DPIA status, categorisation, and judicial approval status.

**Relates To**: BR-006

**Acceptance Criteria**:
- [ ] Given an AI tool, when registered, then ATRS record, DPIA status, AI category, and approval status are captured
- [ ] Given a case-affecting AI tool, when submitted for approval, then judicial steering group review is triggered
- [ ] Given an AI tool without DPIA, when deployment is attempted, then deployment is blocked with notification to MoJ AI Officer

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

---

#### FR-012: Sentence Data Integration

**Description**: Real-time feed of sentencing outcomes from court systems to HMPPS prison and probation systems, eliminating manual sentence data transfer and calculation errors.

**Relates To**: BR-004

**Acceptance Criteria**:
- [ ] Given a sentence passed in court, when recorded in the case management system, then HMPPS receives structured sentence data within 5 minutes
- [ ] Given sentence data, when received by HMPPS, then automatic sentence calculation is performed and verified against court record
- [ ] Given a sentence variation or appeal outcome, when recorded, then HMPPS is notified immediately with updated data

**Priority**: MUST_HAVE

**Complexity**: MEDIUM

**Dependencies**: INT-004 (HMPPS integration)

---

#### FR-013: Automated Victims' Code Compliance Monitoring

**Description**: System must automatically track Victims' Code obligations per case and flag non-compliance to responsible agencies.

**Relates To**: BR-007

**Acceptance Criteria**:
- [ ] Given a case, when a Victims' Code obligation deadline approaches, then the responsible agency is alerted
- [ ] Given Victims' Code compliance data, when aggregated, then compliance rates are reportable by agency, court, and case type
- [ ] Given non-compliance, when detected, then escalation to Victims' Commissioner oversight is triggered

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

#### FR-014: Benefits Realisation Tracking

**Description**: System must track programme benefits against Green Book business case projections, with quantified metrics and independent verification capability.

**Relates To**: BR-008

**Acceptance Criteria**:
- [ ] Given a business case benefit, when tracked, then actual performance vs. projection is visible quarterly
- [ ] Given programme milestones, when reached, then IPA Gateway review evidence is automatically compiled
- [ ] Given cost variances, when exceeding 10% of projection, then automated alert to programme SRO

**Priority**: SHOULD_HAVE

**Complexity**: MEDIUM

---

---

## Non-Functional Requirements (NFRs)

### Performance Requirements

#### NFR-P-001: Response Time

**Requirement**: All user-facing systems must meet response time targets appropriate to the operational context of court proceedings.
- Court case management page load: < 2 seconds (95th percentile) during court sitting hours
- API response time (gateway): < 500ms (95th percentile) for synchronous calls
- AI disclosure review: Process 10,000 evidence items within 4 hours
- AI transcription: Real-time with < 3 second latency
- AI case summarisation: Complete within 5 minutes per case file
- Victim case tracking: Page load < 3 seconds (95th percentile)

**Measurement Method**: Application Performance Monitoring (APM) tooling with SLI dashboards

**Load Conditions**:
- Peak load: 15,000 concurrent professional users across all agencies during court sitting hours (09:00–17:00)
- Batch processing: Up to 500,000 case events per day
- AI processing: Up to 5,000 disclosure reviews per day
- Public services (victim tracking): Up to 50,000 concurrent users

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 13 (Performance Under Operational Load)

---

#### NFR-P-002: Throughput

**Requirement**: System must handle the transaction volumes of the criminal justice system at current and projected caseloads.
- API gateway: 1,000 transactions per second sustained; 5,000 TPS burst
- Event broker: 10,000 events per second
- Court case management: 500 concurrent case updates per minute

**Scalability**: Must scale to support 50% caseload growth over 5 years without architecture changes

**Priority**: MUST_HAVE

---

### Availability and Resilience Requirements

#### NFR-A-001: Availability Target

**Requirement**: Tiered availability based on system criticality:
- **Mission-critical** (court case management, scheduling, video links): 99.9% during court sitting hours (09:00–17:00 Monday–Friday), equating to maximum 8.77 hours unplanned downtime per year during sitting hours
- **Important** (disclosure tools, case file management, AI services): 99.5%
- **Supporting** (analytics, reporting, governance registers): 99.0%
- **Public-facing** (victim tracking, court information): 99.5%

**Maintenance Windows**: Planned maintenance permitted Saturday 22:00–Sunday 06:00 only for mission-critical systems

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 14 (Availability and Continuity)

---

#### NFR-A-002: Disaster Recovery

**RPO (Recovery Point Objective)**: Maximum 15 minutes data loss for court case management; 1 hour for other systems

**RTO (Recovery Time Objective)**: Maximum 1 hour for mission-critical systems; 4 hours for important systems; 24 hours for supporting systems

**Backup Requirements**:
- Backup frequency: Continuous replication for mission-critical; hourly for important; daily for supporting
- Backup retention: 7 years for audit/compliance data; 90 days for operational backups
- Geographic backup location: Secondary UK data centre (data must remain within UK jurisdiction)

**Failover Requirements**:
- Automatic failover to secondary UK region: YES for mission-critical systems
- Failover time: < 15 minutes for automated failover

**Priority**: MUST_HAVE

---

#### NFR-A-003: Fault Tolerance

**Requirement**: Systems must gracefully degrade when dependencies fail, maintaining core court operations.

**Resilience Patterns Required**:
- [ ] Circuit breaker for all external agency dependencies
- [ ] Retry with exponential backoff for transient failures
- [ ] Timeout on all network calls (maximum 30 seconds)
- [ ] Bulkhead isolation for AI processing (AI failure must not affect core case management)
- [ ] Graceful degradation: If AI services fail, manual workflows remain available
- [ ] Manual fallback procedures documented for complete system outage

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 6 (Resilience and Fault Tolerance)

---

### Scalability Requirements

#### NFR-S-001: Horizontal Scaling

**Requirement**: All systems must support horizontal scaling without code changes to handle caseload growth.

**Growth Projections**:
- Year 1: 77,000 outstanding cases, 500,000+ new cases/year, 15,000 concurrent professional users
- Year 3: Projected 60,000 outstanding cases (reduced through efficiency), 550,000+ new cases/year, 20,000 concurrent users
- Year 5: Sustained <50,000 outstanding cases, 600,000+ new cases/year, 25,000 concurrent users

**Scaling Triggers**: Auto-scale when CPU > 70% or memory > 80% or response time p95 > threshold

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 5 (Scalability and Elasticity)

---

#### NFR-S-002: Data Volume Scaling

**Requirement**: Systems must handle data growth including exponential growth in digital evidence volumes.

- Court case data: Projected growth to 50TB over 5 years
- Digital evidence: Projected growth to 500TB over 5 years (body-worn video, communications data, digital forensics)
- AI processing: Model storage and inference data scaling with caseload

**Data Archival Strategy**: Hot storage (0–2 years), warm storage (2–7 years), cold archive (7+ years per retention policy)

**Priority**: MUST_HAVE

---

### Security Requirements

#### NFR-SEC-001: Authentication

**Requirement**: All users must authenticate via SSO with multi-factor authentication. Cross-agency authentication must be federated.

**Multi-Factor Authentication (MFA)**:
- Required for: All access to criminal justice systems (no exceptions)
- MFA methods: Authenticator app or hardware token (SMS not permitted for criminal justice systems)
- Cross-agency federation: SSO between MoJ, HMCTS, CPS, HMPPS, LAA

**Session Management**:
- Session timeout: 30 minutes of inactivity
- Absolute session timeout: 8 hours
- Re-authentication required for: accessing restricted evidence, approving AI outputs, making disclosure decisions

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 3 (Security by Design — NON-NEGOTIABLE)

---

#### NFR-SEC-002: Authorisation

**Requirement**: Role-based access control (RBAC) with attribute-based access control (ABAC) for fine-grained permissions. Least privilege principle enforced.

**Role Hierarchy**:
- Agency-level roles (police officer, CPS prosecutor, court clerk, defence practitioner, judge)
- Case-level roles (assigned prosecutor, defence counsel, trial judge, victim liaison)
- Data sensitivity roles (standard, sensitive, RASSO, terrorism)

**Cross-Agency Authorisation**: Defence practitioners must NOT access prosecution-only materials; prosecution must NOT access defence preparation materials; judicial access is read-only to both sides

**Priority**: MUST_HAVE

---

#### NFR-SEC-003: Data Encryption

**Requirement**:
- Data in transit: TLS 1.3 mandatory for all network communication
- Data at rest: AES-256 encryption for all data stores containing case, personal, or evidential data
- Key management: Centralised key management service with key rotation every 90 days

**Encryption Scope**:
- [ ] Database encryption at rest
- [ ] Backup encryption
- [ ] File/evidence storage encryption
- [ ] Application-level field encryption for special category data (victim PII, medical records)
- [ ] AI model inputs/outputs encrypted during processing

**Priority**: MUST_HAVE

---

#### NFR-SEC-004: Secrets Management

**Requirement**: No secrets (API keys, passwords, certificates) in code, configuration files, or environment variables. All secrets stored in approved secrets management service with automated rotation.

**Secrets Rotation**: Automatic rotation every 90 days for API keys; every 365 days for certificates

**Priority**: MUST_HAVE

---

#### NFR-SEC-005: Vulnerability Management

**Requirement**:
- Dependency scanning in CI/CD pipeline (no critical/high vulnerabilities in production)
- Static application security testing (SAST) on every build
- Dynamic application security testing (DAST) on every deployment to staging
- Penetration testing: Annually by CHECK/CREST-certified testers, plus before each major release

**Remediation SLA**:
- Critical vulnerabilities: 24 hours
- High vulnerabilities: 7 days
- Medium vulnerabilities: 30 days
- Low vulnerabilities: 90 days

**Priority**: MUST_HAVE

---

#### NFR-SEC-006: Network Security

**Requirement**: Zero-trust network architecture with micro-segmentation between services and agencies.

- No network-based trust assumptions between agencies
- All inter-agency traffic through encrypted, authenticated channels
- Network segmentation between AI processing, case management, evidence storage, and public-facing services
- DDoS protection for all internet-facing services

**Priority**: MUST_HAVE

---

### Compliance and Regulatory Requirements

#### NFR-C-001: Data Protection Compliance (UK GDPR / DPA 2018)

**Applicable Regulations**: UK GDPR, DPA 2018 Part 3 (Law Enforcement Processing), DPA 2018 Part 4

**Compliance Requirements**:
- [ ] Lawful basis documented for every data processing activity
- [ ] DPA 2018 Part 3 conditions met for all law enforcement processing
- [ ] Data subject rights supported (access, rectification, erasure where applicable, restriction, portability)
- [ ] DPIA completed for all high-risk processing (mandatory for all AI deployments)
- [ ] Data breach notification to ICO within 72 hours
- [ ] Records of processing activities maintained
- [ ] Data Protection Officer involved in all processing decisions

**Data Residency**: All criminal justice data must remain within UK jurisdiction. No processing in non-UK data centres.

**Data Retention**: Per criminal justice retention schedules — automated deletion at expiry with audit trail

**Priority**: MUST_HAVE

---

#### NFR-C-002: Audit Logging

**Requirement**: Comprehensive, tamper-evident audit trail for all system access and data processing.

**Audit Log Contents** (for all operations on case/personal/evidence data):
- Who: User/service identity (authenticated)
- What: Action performed (CRUD operation, AI processing, disclosure decision)
- When: Timestamp (UTC, millisecond precision)
- Where: System component, source IP
- Why: Context (case reference, request ID, business justification)
- Result: Success/failure with details

**Log Retention**: 7 years for compliance/audit logs (immutable storage)

**Log Integrity**: Tamper-evident logging with cryptographic hashing (write-once storage)

**Priority**: MUST_HAVE

---

#### NFR-C-003: AI Transparency and ATRS

**Requirement**: All AI tools must comply with the Algorithmic Transparency Recording Standard (ATRS) and UK AI Playbook.

**ATRS Requirements**:
- [ ] ATRS record published for every AI tool before deployment
- [ ] Plain-language description of AI purpose, inputs, and limitations
- [ ] Bias assessment across protected characteristics completed
- [ ] Human oversight mechanism documented
- [ ] AI outputs labelled as AI-generated in all user-facing contexts

**AI Playbook Compliance**:
- [ ] 10 principles assessed for each AI deployment
- [ ] Proportionality assessment for criminal justice context
- [ ] Explainability appropriate to the decision's impact

**Priority**: MUST_HAVE

---

#### NFR-C-004: GDS Service Standard Compliance

**Requirement**: All user-facing services must pass GDS service assessment at alpha, beta, and live stages.

**14 Points Coverage**:
- [ ] Point 1: Understand users and their needs (user research with all personas)
- [ ] Point 5: Make sure everyone can use the service (WCAG 2.2 AA)
- [ ] Point 6: Have a multidisciplinary team
- [ ] Point 8: Iterate and improve frequently
- [ ] Point 9: Create a secure service (NCSC CAF alignment)
- [ ] Point 11: Choose the right tools and technology (TCoP compliance)
- [ ] Point 12: Make new source code open (where appropriate for criminal justice)
- [ ] Point 14: Operate a reliable service

**Priority**: MUST_HAVE

---

#### NFR-C-005: NCSC Cyber Assessment Framework

**Requirement**: All systems must align with NCSC Cyber Assessment Framework outcomes.

**CAF Objectives**:
- [ ] Objective A: Managing security risk (governance, risk management, asset management)
- [ ] Objective B: Protecting against cyber attack (service protection policies, access control, data security)
- [ ] Objective C: Detecting cyber security events (security monitoring, anomaly detection)
- [ ] Objective D: Minimising the impact of cyber security incidents (response planning, lessons learned)

**Minimum Standard**: Cyber Essentials Plus certification for all components

**Priority**: MUST_HAVE

---

### Usability Requirements

#### NFR-U-001: Accessibility

**Requirement**: WCAG 2.2 Level AA compliance for all user-facing interfaces. Enhanced accessibility for public-facing services used by victims, witnesses, and defendants.

**Accessibility Features**:
- [ ] Keyboard navigation for all functions
- [ ] Screen reader compatibility (JAWS, NVDA, VoiceOver)
- [ ] High contrast mode
- [ ] Adjustable font sizes (minimum 200% zoom without horizontal scrolling)
- [ ] Alt text for all non-decorative images
- [ ] Captions for all video/audio content
- [ ] Clear, plain language (reading age 9 for public services per GDS guidance)

**Testing**: Automated accessibility testing in CI/CD plus manual testing with assistive technologies before each release

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 15 (Accessibility and Inclusive Design)

---

#### NFR-U-002: Multi-Language Support

**Requirement**: Support for Welsh language (legal requirement) and the 10 most common non-English languages used in criminal proceedings, leveraging AI translation where validated for accuracy.

**Language Requirements**:
- Welsh: Full bilingual support (Welsh Language Act 1993, Welsh Language (Wales) Measure 2011)
- Top 10 languages: AI-assisted translation for key user journeys, with human review for legal documents

**Priority**: MUST_HAVE (Welsh), SHOULD_HAVE (other languages)

---

#### NFR-U-003: Magistrate-Friendly Interface

**Requirement**: Magistrates' court interfaces must be designed for volunteer users with varying digital skills, with simplified workflows and guided processes.

**Design Principles**:
- Task-oriented design (what does the magistrate need to do right now?)
- Minimal training required (intuitive without extensive training programme)
- Consistent with professional interface but simplified
- Contextual help and guidance embedded

**Priority**: SHOULD_HAVE

---

### Maintainability and Supportability

#### NFR-M-001: Observability

**Requirement**: Comprehensive instrumentation for monitoring, troubleshooting, and capacity planning across all services and agencies.

**Telemetry Requirements**:
- **Logging**: Structured JSON logs with correlation IDs supporting cross-agency trace
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates, business metrics
- **Tracing**: Distributed tracing with context propagation across agency boundaries
- **Dashboards**: Real-time operational dashboards and business metric dashboards (per Leveson Review recommendation)
- **Alerts**: SLO-based alerting with actionable runbooks

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 7 (Observability and Operational Excellence)

---

#### NFR-M-002: Infrastructure as Code

**Requirement**: All infrastructure defined as code, version-controlled, and deployed through automated pipelines. No manual changes to production infrastructure.

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 17 (Infrastructure as Code)

---

#### NFR-M-003: CI/CD Pipeline

**Requirement**: Automated build, test, and deployment pipelines with quality gates including security scanning, accessibility testing, and contract testing.

**Pipeline Stages**: Source control → Build → Unit test → Integration test → Security scan → Accessibility check → Contract test → Deploy to staging → Smoke test → Production approval gate → Deploy to production → Verify

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 19 (Continuous Integration and Deployment)

---

### Portability and Interoperability

#### NFR-I-001: API Standards

**Requirement**: All APIs must follow OpenAPI 3.0+ specification, use RESTful design with JSON payloads, and be discoverable through a central API catalogue.

**API Design Principles**:
- RESTful with standard HTTP methods and status codes
- JSON request/response format (UTF-8)
- Versioning via URL path (/v1/, /v2/) with minimum 12-month backward compatibility
- Consistent error response format across all agencies
- Rate limiting and throttling with appropriate headers
- AsyncAPI specification for event-driven interfaces

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 1 (Cross-Agency Interoperability by Design), Principle 11 (Loose Coupling, Tight Contracts)

---

#### NFR-I-002: Open Standards

**Requirement**: Use open standards for all data exchange, avoiding vendor lock-in. Data must be exportable in open formats.

**Standards**:
- Data exchange: JSON, XML where legacy requires
- Document format: PDF/A for archival, ODF for editable documents
- Security: OAuth 2.0, SAML 2.0 for authentication; TLS 1.3 for transport
- Messaging: CloudEvents specification for event format

**Priority**: MUST_HAVE

**Aligns with**: Architecture Principle 20 (Open Standards and Avoid Lock-In)

---

## Integration Requirements

### INT-001: Common Platform Integration

**Purpose**: Integrate with the existing HMCTS Common Platform for case management, court scheduling, and hearing outcomes.

**Integration Type**: Real-time API + Event-driven

**Data Exchanged**:
- **From Common Platform to programme services**: Case records, hearing schedules, court outcomes, listing data
- **From programme services to Common Platform**: AI-generated summaries, cross-agency case data, victim notifications

**Authentication**: OAuth 2.0 with MoJ/HMCTS SSO

**Error Handling**: Circuit breaker with fallback to cached data; retry with exponential backoff

**SLA**: API response < 500ms p95; Event delivery < 30 seconds; 99.5% availability

**Owner**: HMCTS Digital

**Priority**: MUST_HAVE

---

### INT-002: Police Case Management Systems Integration

**Purpose**: Receive digital case files and evidence from 43 police forces operating different case management systems (Niche, Connect, Athena, and others).

**Integration Type**: API-based with adapter layer for each major system

**Data Exchanged**:
- **From Police to CPS/Courts**: Digital case files, evidence packages, witness statements, charge data
- **From CPS/Courts to Police**: Case outcomes, additional evidence requests, court dates

**Integration Pattern**: Adapter/middleware pattern normalising diverse police formats to common standard

**Authentication**: Mutual TLS with certificate-based police system identification

**Error Handling**: Dead letter queue for failed transfers; manual intervention workflow for data quality issues

**SLA**: Case file delivery < 4 hours from submission; evidence package transfer < 24 hours

**Owner**: NPCC Digital Policing Programme (coordination); individual forces (implementation)

**Priority**: MUST_HAVE

---

### INT-003: CPS Case Management System Integration

**Purpose**: Bidirectional integration with CPS case management for prosecution workflow, disclosure, and case preparation.

**Integration Type**: Real-time API + Event-driven

**Data Exchanged**:
- **From CPS**: Prosecution case data, disclosure schedules, charging decisions
- **To CPS**: Police evidence, court outcomes, defence responses, AI disclosure results

**Authentication**: OAuth 2.0 with CPS SSO federation

**SLA**: API response < 500ms p95; 99.5% availability

**Owner**: CPS Digital

**Priority**: MUST_HAVE

---

### INT-004: HMPPS Integration (Prison and Probation)

**Purpose**: Deliver real-time sentence data and court outcomes to HMPPS for sentence calculation, offender management, and probation supervision.

**Integration Type**: Event-driven (primary) + API (query)

**Data Exchanged**:
- **From Courts to HMPPS**: Sentence data, remand status, bail conditions, appeal outcomes
- **From HMPPS to Courts**: Prisoner availability for hearings, probation reports, pre-sentence reports

**Authentication**: OAuth 2.0 with HMPPS SSO federation

**Error Handling**: Critical events (sentencing) must have guaranteed delivery with acknowledgement; dead letter queue with priority alerting for failed sentence data

**SLA**: Sentence data delivery < 5 minutes; 99.9% delivery guarantee for sentence events

**Owner**: HMPPS Digital

**Priority**: MUST_HAVE

---

### INT-005: Legal Aid Agency Integration

**Purpose**: Enable defence practitioners to authenticate via LAA, access legal aid case information, and report technology usage for billing.

**Integration Type**: API-based

**Data Exchanged**:
- **From LAA**: Practitioner credentials, legal aid certificates, case assignments
- **To LAA**: Technology usage reports, defence platform access logs (for billing)

**Authentication**: OAuth 2.0 with LAA SSO

**SLA**: API response < 1 second p95; 99.0% availability

**Owner**: LAA Digital

**Priority**: MUST_HAVE

---

### INT-006: ICO DPIA Register Integration

**Purpose**: Report DPIA completion status and AI transparency data to ICO where required.

**Integration Type**: Batch file/API (periodic reporting)

**Data Exchanged**:
- **To ICO**: DPIA summaries, ATRS records, data breach notifications

**SLA**: Within statutory timeframes (72 hours for breach notification)

**Owner**: MoJ Data Protection Officer

**Priority**: SHOULD_HAVE

---

---

## Data Requirements

### Data Entities

#### DR-001: Criminal Case Record

**Description**: The central data entity representing a criminal case from charge through to disposal, shared across agencies.

**Key Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| case_reference | String(20) | Yes | Unique case reference number | Primary key, URN format |
| defendant_id | UUID | Yes | Link to defendant record | Foreign key |
| offences | Array[Offence] | Yes | Charged offences | Min 1 offence |
| case_status | Enum | Yes | Current case status | Validated state machine |
| court_centre | String(10) | Yes | Court centre code | Reference data |
| case_type | Enum | Yes | Crown/Magistrates/Appeal | Validated |
| created_at | Timestamp | Yes | Case creation timestamp | UTC, immutable |
| updated_at | Timestamp | Yes | Last update | UTC |
| prosecution_agency | Enum | Yes | CPS/SFO/etc | Validated |

**Relationships**:
- One-to-many with Hearing records
- One-to-many with Evidence items
- Many-to-one with Defendant
- One-to-many with Victim/Witness records
- One-to-one with Sentence (if convicted)

**Data Volume**: ~500,000 new cases/year; 10+ million total records over 5 years

**Data Classification**: OFFICIAL-SENSITIVE

**Data Retention**: Per criminal justice retention schedule (varies by offence type; typically 6 years after disposal for summary offences, longer for indictable)

---

#### DR-002: Digital Evidence Package

**Description**: Container for digital evidence associated with a case, including body-worn video, communications data, documents, and forensic data.

**Key Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| evidence_id | UUID | Yes | Unique evidence identifier | Primary key |
| case_reference | String(20) | Yes | Associated case | Foreign key |
| evidence_type | Enum | Yes | Video/Audio/Document/Communications/Image/Forensic | Validated |
| file_hash | String(64) | Yes | SHA-256 integrity hash | Immutable |
| source_agency | Enum | Yes | Originating agency | Validated |
| disclosure_status | Enum | No | Disclosable/Not disclosable/Under review | Validated |
| ai_reviewed | Boolean | No | Whether AI disclosure review applied | |
| file_size_bytes | Long | Yes | File size | |

**Data Volume**: Projected 100TB/year growing at 30% annually (driven by body-worn video and digital forensics growth)

**Data Classification**: OFFICIAL-SENSITIVE (may include OFFICIAL-SENSITIVE — RASSO for sexual offence evidence)

**Data Retention**: Varies by case outcome; minimum until appeal window closes; longer for serious offences

---

#### DR-003: Defendant Record

**Description**: Record of an individual charged with a criminal offence, linked to cases.

**Key Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| defendant_id | UUID | Yes | Unique identifier | Primary key |
| pnc_id | String(15) | No | Police National Computer ID | Cross-reference |
| forename | String(100) | Yes | First name | Encrypted at rest |
| surname | String(100) | Yes | Last name | Encrypted at rest |
| date_of_birth | Date | Yes | DOB | Encrypted at rest |
| bail_status | Enum | No | Remand/Bail/Conditional Bail | |
| legal_representation | Enum | No | Represented/Unrepresented/Unknown | |

**Data Classification**: OFFICIAL-SENSITIVE (special category — criminal justice data)

**Data Retention**: Per PNC retention rules and Rehabilitation of Offenders Act

---

#### DR-004: Victim/Witness Record

**Description**: Record of victims and witnesses associated with a case, with enhanced protections.

**Key Attributes**:
| Attribute | Type | Required | Description | Constraints |
|-----------|------|----------|-------------|-------------|
| person_id | UUID | Yes | Unique identifier | Primary key |
| role | Enum | Yes | Victim/Witness/Complainant | Validated |
| vulnerability_flags | Array[Enum] | No | Child/Domestic abuse/RASSO/Intimidation | Enhanced access control |
| special_measures | Array[Enum] | No | Screens/Video link/Intermediary | |
| notification_preference | Enum | No | SMS/Email/App/None | |
| anonymity_order | Boolean | No | Whether anonymity order in place | |

**Data Classification**: OFFICIAL-SENSITIVE (enhanced protection for vulnerable victims)

**Data Retention**: Per Victims' Code requirements and case retention schedule

---

### Data Quality Requirements

**Data Accuracy**: Zero tolerance for errors in defendant identity, sentence data, and bail status (justice-critical). <0.1% error rate for case data. Automated validation at point of entry.

**Data Completeness**: All mandatory fields enforced at source. Digital case file must contain all mandated elements before submission to court.

**Data Consistency**: Automated reconciliation between agency systems. Same case must reflect same facts in all systems within defined SLA (5 minutes for critical data, 1 hour for non-critical).

**Data Timeliness**: Real-time for court outcomes and sentence data. Within 4 hours for case file transfers. Within 24 hours for evidence packages.

**Data Lineage**: Full provenance tracking for all case data showing source system, transformations, and timestamps. Essential for AI transparency and audit.

---

### Data Migration Requirements

**Migration Scope**: Data from 37 legacy applications to be migrated to modern platforms. Priority: court case data, evidence records, scheduling data, sentence records.

**Migration Strategy**: Phased migration with parallel running. No "big bang" migrations for court-critical systems.

**Data Transformation**: Legacy data formats normalised to common schema. Encoding issues resolved. Historical data archived per retention schedules.

**Data Validation**: Row-level reconciliation between source and target. Sample-based manual verification. Automated integrity checks.

**Rollback Plan**: Full rollback capability with tested rollback procedures for each migration tranche. Legacy systems remain available in read-only mode for defined period.

---

## Constraints and Assumptions

### Technical Constraints

**TC-001**: All data must reside within UK jurisdiction. No processing in non-UK data centres, including AI model inference.

**TC-002**: Must integrate with existing Common Platform — not replace it. Common Platform stabilisation is a prerequisite, not a parallel track.

**TC-003**: Must accommodate 43 independently governed police forces with different case management systems. Cannot mandate a single police system.

**TC-004**: AI models for criminal justice must be auditable and explainable. Black-box AI models are not acceptable for case-affecting functions.

**TC-005**: Must comply with judiciary's existing technology governance — judicial steering group has veto on AI tools affecting court proceedings.

**TC-006**: DPA 2018 Part 3 applies to law enforcement processing, with different conditions from standard UK GDPR processing.

---

### Business Constraints

**BC-001**: Funding is contingent on Green Book business case approval by HM Treasury. Programme cannot commit to spending above approved limits without further approval.

**BC-002**: Court sitting days are a fixed constraint — technology cannot increase sitting days, only improve efficiency within available sitting time.

**BC-003**: Programme must learn from and avoid repeating Common Platform failures (scope creep, unrealistic timelines, poor change management).

**BC-004**: Defence technology access must be simultaneously available with prosecution tools — cannot be a "later phase" or the programme faces legal challenge.

**BC-005**: Magistrates' courts (handling 95% of criminal cases) must not be deprioritised in favour of Crown Court — the Magistrates' Association and Leveson Review require both.

---

### Assumptions

**A-001**: The Leveson Review recommendations will receive sustained government support across the multi-year programme.

**A-002**: Cross-agency data sharing agreements can be formalised within the first 12 months.

**A-003**: AI technology (LLMs, NLP) will be mature enough for criminal justice disclosure review by the time governance frameworks are operational.

**A-004**: Legal aid funding mechanisms for defence technology access will be agreed within Year 1, either through legal aid rate reform or central provision.

**A-005**: Existing Common Platform can be stabilised sufficiently to serve as the court case management foundation.

**A-006**: Police forces will adopt common data standards when accompanied by central funding incentives and adapter/middleware support.

**Validation Plan**: Each assumption to be validated during programme discovery phase (first 6 months). Assumptions that prove invalid will trigger re-planning and risk escalation.

---

## Success Criteria and KPIs

### Business Success Metrics

| Metric | Baseline | Target | Timeline | Measurement Method |
|--------|----------|--------|----------|-------------------|
| Crown Court outstanding caseload | 77,000+ | <50,000 | 3 years | HMCTS Criminal Court Statistics Quarterly |
| Average charge-to-trial time | 18+ months | <13 months | 3 years | Court statistics |
| Effective trial rate | ~40% | >55% | 3 years | Court statistics |
| AI-assisted disclosure coverage | 0% | 80%+ | 3 years | CPS case management data |
| Defence AI tool access | 0% | 70%+ | 3 years | LAA provider surveys |
| Cross-agency automated data exchange | <10% | >90% | 4 years | API gateway analytics |
| Legacy applications migrated | 0/37 | 20+/37 | 3 years | Portfolio register |
| Victim satisfaction improvement | Baseline TBD | +20% | 2 years | HMCTS victim survey |
| Victims' Code compliance | Low (per VC reports) | 90%+ | 2 years | Automated monitoring |
| Programme cost vs business case | N/A | Within 10% | Ongoing | Finance reports |

### Technical Success Metrics

| Metric | Target | Measurement Method |
|--------|--------|-------------------|
| System availability (mission-critical) | 99.9% during sitting hours | Uptime monitoring |
| API response time (p95) | < 500ms | APM tooling |
| API gateway error rate | < 0.1% | API analytics |
| AI disclosure processing time | < 4 hours per case | AI platform metrics |
| Data reconciliation errors | < 0.01% | Automated reconciliation |
| Security vulnerabilities (critical/high) | Zero in production | Vulnerability scanning |
| WCAG 2.2 AA compliance | 100% | Accessibility audits |
| Deployment frequency | Weekly or better | CI/CD metrics |
| Mean time to recovery (MTTR) | < 30 minutes (mission-critical) | Incident tracking |

### User Adoption Metrics

| Metric | Target | Timeline | Measurement Method |
|--------|--------|----------|-------------------|
| Prosecutor AI tool adoption | 90%+ | 2 years post-deployment | CPS usage analytics |
| Defence practitioner platform registration | 70%+ | 3 years | Platform analytics |
| Victim case tracking registrations | 50%+ of eligible victims | 2 years | Service analytics |
| Court staff satisfaction with new tools | ≥7/10 | 1 year post-deployment | Staff survey |
| Judicial satisfaction with technology | ≥6/10 | 1 year post-deployment | Judicial survey |
| Magistrate usability score | ≥7/10 | 1 year post-deployment | User testing |

---

## Dependencies and Risks

### Dependencies

| Dependency | Description | Owner | Target Date | Status | Impact if Delayed |
|------------|-------------|-------|-------------|--------|-------------------|
| Green Book business case approval | HM Treasury funding approval | MoJ Perm Sec | Year 1 Q2 | Pending | CRITICAL — programme cannot proceed |
| Common Platform stabilisation | CP must be stable before building on it | HMCTS CTO | Year 1 Q3 | At Risk | HIGH — delays court system enhancements |
| AI governance framework | Must be operational before AI deployment | MoJ AI Officer | Year 1 Q4 | Pending | HIGH — blocks all AI tool deployment |
| Cross-agency data sharing agreements | Legal agreements between all agencies | MoJ Legal | Year 1 Q4 | Pending | HIGH — blocks interoperability |
| Judicial steering group formation | Judicial oversight body for AI | Lady CJ Office | Year 1 Q2 | Pending | HIGH — blocks case-affecting AI |
| Police data standards agreement | NPCC agreement on digital case file format | NPCC | Year 1 Q3 | Pending | MEDIUM — delays police integration |
| Defence funding mechanism | LAA funding for defence technology | Lord Chancellor | Year 1 Q3 | Pending | CRITICAL — blocks BR-003 |

### Risks

| Risk ID | Description | Probability | Impact | Mitigation Strategy | Owner |
|---------|-------------|-------------|--------|---------------------|-------|
| R-1 | Judicial resistance blocks AI deployment | MEDIUM | HIGH | Early engagement via steering group; start with non-contentious AI | Lead Judge for AI |
| R-2 | Defence equality challenge in court | HIGH | HIGH | Simultaneous prosecution-defence deployment; defence technology fund | LAA CEO |
| R-3 | Police interoperability failure (43 forces) | HIGH | MEDIUM | Mandate outcomes not systems; adapter middleware; funding incentives | NPCC |
| R-4 | Treasury funding refusal | MEDIUM | CRITICAL | Robust business case; phased investment; ministerial advocacy | MoJ Perm Sec |
| R-5 | Common Platform instability during reform | MEDIUM | HIGH | Stabilise first; parallel running; separation of stabilisation and transformation | HMCTS CTO |
| R-6 | AI ethics controversy | MEDIUM | HIGH | Robust governance; ATRS/DPIA; incident response plan | MoJ AI Officer |
| R-7 | ICO enforcement action | LOW | HIGH | Early ICO engagement; comprehensive DPIAs; specialist DPA Part 3 advice | MoJ DPO |
| R-8 | Legacy migration disrupts court operations | MEDIUM | HIGH | Phased migration; parallel running; tested rollback; no "big bang" | HMCTS CTO |
| R-9 | AI model bias against protected characteristics | MEDIUM | CRITICAL | Bias testing across all protected characteristics; independent review; ATRS | MoJ AI Officer |
| R-10 | Vendor lock-in constraining future options | MEDIUM | MEDIUM | Open standards; abstraction layers; multi-vendor strategy; exit plans | MoJ CDIO |

---

## Requirement Conflicts & Resolutions

### Conflict C-1: Speed of AI Deployment vs Judicial Approval Process

**Conflicting Requirements**:
- **BR-002**: Deploy AI-assisted disclosure and case preparation tools across CPS within 2 years
- **BR-006**: AI governance framework with judicial approval gates for case-affecting AI

**Stakeholders Involved**:
- **Lord Chancellor (SD-1)**: Wants rapid AI deployment to demonstrate progress on backlog reduction
- **Lady Chief Justice (SD-2)**: Requires careful, rights-respecting implementation with judicial veto on case-affecting AI

**Nature of Conflict**: Judicial approval gates inherently slow AI deployment. The governance framework itself requires 12 months to establish. Deployment of AI disclosure tools cannot start until governance is operational, creating a Year 1 deployment gap.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| **Option 1**: Deploy AI first, governance later | Fast deployment, visible progress | Judicial opposition, legal challenge risk, ethics risk | Lord Chancellor satisfied; judiciary alarmed |
| **Option 2**: Governance first, AI delayed | Full compliance, judicial trust | Delayed benefits, political pressure | Judiciary satisfied; Lord Chancellor frustrated |
| **Option 3**: Dual-track — safe AI immediate, case-affecting AI after governance | Early wins on non-contentious AI; governance for case-affecting tools | Some deployment delay for disclosure AI; complexity of dual track | Both partially satisfied |

**Resolution Strategy**: PHASE

**Decision**: Option 3 — Dual-track approach. Deploy "safe" AI tools (transcription, translation, case summarisation for information only) immediately under standard governance. Deploy case-affecting AI (disclosure review, scheduling recommendations) only after AI governance framework is operational with judicial steering group approval.

**Rationale**: This satisfies the Lord Chancellor's need for visible progress while respecting judicial independence. Transcription and translation deliver immediate efficiency gains without affecting case outcomes. The Leveson Review's own categorisation of AI tools supports this phased approach.

**Decision Authority**: Programme Board with judicial steering group concurrence

**Impact on Requirements**:
- **Modified**: BR-002 phased — non-contentious AI tools in Year 1; disclosure AI after governance framework (Year 1 Q4+)
- **Unchanged**: BR-006 timeline (12 months for governance framework)
- **Added**: New milestone — "safe AI" deployment in Year 1 Q2

**Stakeholder Management**:
- **Lord Chancellor**: Communicate early AI wins (transcription, translation) as evidence of progress
- **Lady Chief Justice**: Genuine veto power preserved; judicial steering group has authority over case-affecting AI

---

### Conflict C-2: Prosecution AI Deployment vs Defence Equality of Arms

**Conflicting Requirements**:
- **BR-002**: Deploy AI tools for CPS prosecution (MUST_HAVE)
- **BR-003**: Defence practitioners must have equivalent tools simultaneously (MUST_HAVE)

**Stakeholders Involved**:
- **DPP/CPS (SD-4)**: Wants AI disclosure tools deployed quickly to improve case quality
- **CBA/Law Society (SD-6)**: Insists no prosecution AI without simultaneous defence equivalent

**Nature of Conflict**: CPS has existing digital infrastructure and central funding. Defence practitioners are fragmented (thousands of firms) with minimal technology and constrained legal aid budgets. Building prosecution and defence tools simultaneously requires solving fundamentally different delivery challenges — one centralised, one distributed.

**Trade-off Analysis**:

| Option | Pros | Cons | Impact |
|--------|------|------|--------|
| **Option 1**: Prosecution first, defence later | Faster prosecution efficiency | Legal challenge on equality grounds; political damage | CPS happy; defence community furious |
| **Option 2**: Simultaneous deployment | Equality of arms maintained | Slower prosecution deployment; higher cost | Both satisfied if achievable |
| **Option 3**: Shared platform (both use same tools) | True equality; lower cost | Security model complex (prosecution/defence segregation) | Innovative if feasible |
| **Option 4**: Deploy prosecution but fund defence shared-service AI tools on same timeline | Prosecution gets optimised tools; defence gets equivalent capability via shared service | Defence tools may differ in UX; shared service complexity | Pragmatic compromise |

**Resolution Strategy**: INNOVATE

**Decision**: Option 4 with safeguard — CPS deploys optimised prosecution AI tools while simultaneously funding a shared-service defence AI platform (centrally provided, cloud-based, accessible via browser). The programme commits to a "no prosecution advantage" principle: CPS AI tools go live only when defence shared-service equivalent is available. A 3-month grace period allows for beta testing differences.

**Rationale**: This is the most practical approach given the different delivery contexts. Central provision of a defence shared-service platform avoids the impossible task of upgrading thousands of individual defence firms simultaneously.

**Decision Authority**: Lord Chancellor (policy decision on defence funding mechanism)

**Impact on Requirements**:
- **Unchanged**: BR-002 (CPS prosecution AI deployment)
- **Modified**: BR-003 — defence access via centrally provided shared-service platform rather than requiring each firm to procure
- **Added**: New FR — Defence AI Shared Service Platform (FR-009 covers this)
- **Added**: New dependency — defence funding mechanism agreed before prosecution AI goes live

**Stakeholder Management**:
- **CPS**: May experience short delay if defence platform not ready — communicate clearly that this is a programme constraint, not optional
- **CBA/Law Society**: Genuine participation in defence platform requirements; central provision removes individual cost burden

---

### Conflict C-3: Cross-Agency Standardisation vs Police Force Autonomy

**Conflicting Requirements**:
- **BR-004**: Cross-agency interoperability with standardised data exchange
- **TC-003**: Must accommodate 43 independently governed police forces with different systems

**Stakeholders Involved**:
- **MoJ CDIO (G-4)**: Wants standardised APIs and data formats across all agencies
- **NPCC (SD-5)**: 43 independently governed forces cannot be mandated to adopt a single system

**Nature of Conflict**: Interoperability requires standardisation, but police forces are constitutionally independent with their own procurement and technology choices. Central government cannot mandate specific police systems.

**Resolution Strategy**: COMPROMISE

**Decision**: Mandate outcome standards (data format, schema, delivery SLA) not technology standards. Build adapter/middleware layer for the three most common police systems (Niche, Connect, Athena) that covers ~85% of forces. Remaining forces can build their own adapters to the published standard. Central funding incentives for early adopters.

**Impact on Requirements**:
- **Modified**: INT-002 — adapter layer approach rather than direct integration with each force
- **Added**: Central funding mechanism for police technology upgrades

---

### Conflict C-4: Comprehensive Legacy Migration vs Budget Constraints

**Conflicting Requirements**:
- **BR-005**: Migrate all 37 legacy applications (MUST_HAVE)
- **BR-008**: Programme expenditure within Green Book business case limits

**Stakeholders Involved**:
- **HMCTS CTO (G-5)**: Wants all legacy risk eliminated
- **HM Treasury (SD-9)**: Requires phased, affordable investment with demonstrated returns

**Nature of Conflict**: Migrating 37 legacy applications simultaneously would require enormous upfront investment. Treasury will not approve unfunded mandates. But every year of delay increases cyber risk and operational cost.

**Resolution Strategy**: PHASE

**Decision**: Prioritise legacy migration by risk score (cyber risk × business impact). Top 10 highest-risk applications in Phase 1 (Years 1-2). Next 10 in Phase 2 (Years 2-3). Remainder in Phase 3 (Years 3-5). Each phase's funding contingent on demonstrated delivery in the previous phase. Business case presents this as a rolling programme with stage-gate approvals.

**Impact on Requirements**:
- **Modified**: BR-005 — phased timeline (20+ in 3 years, all 37 in 5 years rather than all at once)
- **Added**: Priority scoring methodology for legacy applications

---

## Timeline and Milestones

### High-Level Milestones

| Milestone | Description | Target Date | Dependencies |
|-----------|-------------|-------------|--------------|
| Requirements Approval | Stakeholder sign-off on this document | Year 1 Q1 | This document |
| Green Book Business Case Approved | Treasury spending authority | Year 1 Q2 | BR-008 |
| AI Governance Framework Operational | Governance ready for AI deployment | Year 1 Q4 | BR-006 |
| "Safe AI" Deployment | Transcription, translation, summarisation live | Year 1 Q2 | Non-contentious AI |
| Cross-Agency Data Standards Published | API specifications and data schemas | Year 1 Q3 | BR-004 |
| Defence Shared Service Platform Beta | Defence AI tools in beta | Year 1 Q4 | BR-003 |
| AI Disclosure Tools Live (CPS + Defence) | Case-affecting AI operational | Year 2 Q1 | AI governance + defence parity |
| CPS-HMCTS Integration Live | First cross-agency API integration | Year 1 Q4 | INT-001, INT-003 |
| Police-CPS Digital Case File Live | Adapter-based police integration | Year 2 Q2 | INT-002 |
| Phase 1 Legacy Migration Complete | Top 10 legacy applications migrated | Year 2 Q4 | BR-005 |
| Victim Case Tracking Service Live | Public service for victims | Year 2 Q1 | FR-007, BR-007 |
| HMPPS Sentence Integration Live | Real-time sentence data to probation/prisons | Year 2 Q3 | INT-004 |
| Phase 2 Legacy Migration Complete | 20+ applications migrated | Year 3 Q4 | BR-005 |
| Full Cross-Agency Integration | 90%+ automated data exchange | Year 4 | BR-004 |
| All Legacy Applications Migrated | 37/37 complete | Year 5 | BR-005 |

---

## Approval

### Requirements Review

| Reviewer | Role | Status | Date | Comments |
|----------|------|--------|------|----------|
| [Name] | MoJ CDIO (Technical Authority) | [ ] Approved | | |
| [Name] | HMCTS CEO (Operational Owner) | [ ] Approved | | |
| [Name] | MoJ Chief AI Officer (AI Governance) | [ ] Approved | | |
| [Name] | DPP/CPS (Prosecution Technology) | [ ] Approved | | |
| [Name] | Lady Chief Justice's Office (Judicial) | [ ] Approved | | |
| [Name] | CBA/Law Society (Defence) | [ ] Approved | | |
| [Name] | MoJ DPO (Data Protection) | [ ] Approved | | |
| [Name] | GDS/CDDO (Digital Standards) | [ ] Approved | | |

### Sign-Off

By signing below, stakeholders confirm that requirements are complete, understood, and approved to proceed to design phase.

| Stakeholder | Signature | Date |
|-------------|-----------|------|
| MoJ Permanent Secretary (SRO) | _________ | |
| MoJ CDIO | _________ | |
| HMCTS CEO | _________ | |

---

## Appendices

### Appendix A: Glossary

| Term | Definition |
|------|-----------|
| ATRS | Algorithmic Transparency Recording Standard — mandatory transparency record for government AI |
| CAF | Cyber Assessment Framework (NCSC) |
| CBA | Criminal Bar Association |
| Common Platform | HMCTS/CPS shared digital case management system |
| CPS | Crown Prosecution Service |
| DPA 2018 Part 3 | Data Protection Act 2018 provisions for law enforcement processing |
| DPIA | Data Protection Impact Assessment |
| DPP | Director of Public Prosecutions |
| GDS | Government Digital Service |
| HMCTS | HM Courts & Tribunals Service |
| HMPPS | HM Prison and Probation Service |
| IPA | Infrastructure and Projects Authority |
| LAA | Legal Aid Agency |
| MoJ | Ministry of Justice |
| NPCC | National Police Chiefs' Council |
| RASSO | Rape and Serious Sexual Offences |
| TCoP | Technology Code of Practice |
| WCAG | Web Content Accessibility Guidelines |

### Appendix B: Reference Documents

- ARC-000-PRIN-v1.0 — Enterprise Architecture Principles
- ARC-001-STKE-v1.0 — Stakeholder Drivers & Goals Analysis
- Independent Review of the Criminal Courts — Overview, Part 1, Part 2 (Volumes 1 & 2)
- GDS Service Standard (14 points)
- Technology Code of Practice
- UK AI Playbook
- NCSC Cyber Assessment Framework
- HM Treasury Green Book
- DPA 2018 (Part 3 — Law Enforcement Processing)
- Victims' Code of Practice

### Appendix C: Wireframes and Mockups

*To be produced during discovery and alpha phases. User research with all personas will inform design.*

### Appendix D: Data Models

*Detailed ERD to be produced as part of `/arckit.data-model` command. See DR-001 through DR-004 for entity descriptions.*

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Independent Review of the Criminal Courts — Overview | Policy Review | GOV.UK | Programme context, 180 recommendations | `projects/000-global/external/independent-review-criminal-courts-overview.pdf` |
| Independent Review of the Criminal Courts — Part 1 | Policy Review | GOV.UK | Technology recommendations, AI guidance, interoperability | `projects/000-global/external/35.49_MOJ_Ind_Review_Criminal_Courts_v8b_FINAL_WEB.pdf` |
| Independent Review of the Criminal Courts — Part 2, Vol 1 | Policy Review | GOV.UK | Implementation proposals, legacy system analysis | `projects/000-global/external/independent-review-criminal-courts-part-2-vol-1.pdf` |
| Independent Review of the Criminal Courts — Part 2, Vol 2 | Policy Review | GOV.UK | Additional implementation detail | `projects/000-global/external/independent-review-criminal-courts-part-2-vol-2.pdf` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 23 principles across 7 categories | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 15 stakeholders, 15 drivers, 10 goals, 6 outcomes | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` |

---

**Generated by**: ArcKit `/arckit.requirements` command
**Generated on**: 2026-02-04
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)
**Generation Context**: Requirements derived from ARC-001-STKE-v1.0 (stakeholder analysis), ARC-000-PRIN-v1.0 (architecture principles), and the Independent Review of the Criminal Courts (Leveson Review, 2025-2026)

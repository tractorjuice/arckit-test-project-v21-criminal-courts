# Wardley Value Chain: Criminal Courts Technology & AI Reform

> **Template Origin**: Official | **ArcKit Version**: 1.5.0 | **Command**: `/arckit.wardley.value-chain`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-WVCH-001-v1.0 |
| **Document Type** | Wardley Value Chain |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-16 |
| **Last Modified** | 2026-03-16 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-04-15 |
| **Owner** | MoJ Chief Digital and Information Officer |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, HMPPS Digital, Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-16 | ArcKit AI | Initial creation from `/arckit:wardley.value-chain` command | PENDING | PENDING |

---

## Executive Summary

This value chain decomposes the anchor need "Justice system participants receive fair, timely, and transparent criminal case outcomes" into 35 components across 6 dependency levels. The chain serves 8 distinct user personas — from Crown Court judges to victims/witnesses — and reveals that the criminal justice system's value delivery depends critically on cross-agency data exchange, AI-assisted case processing, and a constellation of custom-built criminal justice components that have no commodity equivalents. The most strategically significant insight is that three parallel value chains (prosecution case processing, defence case preparation, and victim/witness experience) converge on a shared integration and infrastructure layer, making cross-agency data standards and integration the single highest-leverage investment in the programme.

---

## User Need / Anchor

**Anchor Statement**: Justice system participants receive fair, timely, and transparent criminal case outcomes.

```text
Anchor: Justice system participants receive fair, timely, and transparent criminal case outcomes
User: All participants in the criminal justice system (judges, prosecutors, defence, victims, witnesses, court staff, police, probation)
Outcome: Cases progress from charge to outcome without unnecessary delay; all parties have equitable access to information and tools; victims are informed and supported throughout
```

This anchor is deliberately broad because the programme serves multiple personas with interlocking needs. A narrower anchor (e.g., "Prosecutor can review disclosure efficiently") would miss the constitutional requirement for defence equality and the victim experience dimension.

---

## Users and Personas

| Persona | Role | Primary Need |
|---------|------|--------------|
| Crown Court Judge | Presides over trials and hearings | Access accurate case information; manage listings efficiently; maintain judicial discretion over AI |
| CPS Prosecutor | Prepares and presents prosecution cases | Prepare cases efficiently with AI-assisted disclosure; access evidence seamlessly from police |
| Defence Barrister/Solicitor | Represents defendants | Access AI tools equivalent to prosecution; review disclosure materials efficiently |
| Police Officer/Detective | Investigates crimes, prepares case files | Share evidence digitally; minimise case file preparation time; avoid data rekeying |
| HMCTS Court Staff | Administers court proceedings | Reduce manual administrative burden; access reliable systems |
| Victim/Witness | Participant in criminal proceedings | Know what is happening with their case; attend/give evidence with minimum stress |
| Magistrate | Volunteer judicial officer | Access case information quickly through a simple interface |
| Probation Officer | Supervises offenders, prepares pre-sentence reports | Receive court outcomes in real time; access case history |

---

## Value Chain Diagram

**View this map**: Paste the OWM syntax below into [https://create.wardleymaps.ai](https://create.wardleymaps.ai)

**ASCII Placeholder**:

```text
Visibility
    ^
1.0 | [Fair Timely Transparent Justice]
    |         |                |                    |
0.9 |  [Case Processing]  [Victim/Witness Exp]  [Defence Equality]
    |     |        |            |         |            |        |
0.8 | [AI Disc] [AI Trans] [Case Track] [Remote Ev] [Def Portal] [AI Summ]
    |     |        |            |                      |        |
0.7 | [Disc Engine] [NLP Models] [Notif Service]   [Disc Access] [Summ Engine]
    |     |    |         |            |                |
0.6 | [Evid Triage] [Human Review] [Case Status Agg] [Case File Viewer]
    |     |    |         |            |
0.5 | [Cross-Agency Data Exchange]  [AI Governance]
    |     |              |               |
0.4 | [Integration Platform] [CJS Data Standards] [Bias Testing]
    |     |         |             |
0.3 | [API Gateway] [Event Messaging] [Common Platform]
    |     |         |
0.2 | [IAM] [LLM Services] [GOV.UK Design] [GOV.UK Notify]
    |     |         |
0.1 | [Cloud Hosting] [Managed DBs] [Container Orch] [Monitoring]
    |
    +--Genesis----Custom----Product----Commodity-->  Evolution
       (0.0)     (0.25)    (0.50)     (0.75)  (1.0)
```

**OWM Syntax**:

```wardley
title Criminal Courts Technology & AI Reform — Value Chain

anchor Fair Timely Transparent Justice [0.97, 0.50]
note 8 user personas; 35 components; 6 dependency levels [0.03, 0.15]
annotation 1 [0.55, 0.20] Cross-agency data exchange is the highest-leverage investment
annotation 2 [0.75, 0.25] Three parallel chains converge on shared integration layer

component Fair Timely Transparent Justice [0.97, 0.50]

component Case Processing Efficiency [0.93, 0.30]
component Victim Witness Experience [0.91, 0.32]
component Defence Equality of Arms [0.89, 0.18]

component AI Disclosure Review [0.84, 0.25]
component AI Transcription Translation [0.82, 0.35]
component Court Case Management [0.80, 0.42]
component Victim Case Tracking [0.78, 0.30]
component Remote Evidence Giving [0.76, 0.55]
component Defence Practitioner Portal [0.74, 0.22]
component AI Case Summarisation [0.72, 0.28]

component Disclosure Engine [0.68, 0.25]
component NLP Language Models [0.66, 0.35]
component Notification Delivery [0.64, 0.88]
component Disclosure Material Access [0.62, 0.28]
component Case Summarisation Engine [0.60, 0.28]

component Evidence Triage [0.56, 0.22]
component Human Review Workflow [0.54, 0.38]
component Case Status Aggregation [0.52, 0.30]
component Digital Case File Viewer [0.50, 0.32]
component AI Governance Controls [0.48, 0.18]

component Cross-Agency Data Exchange [0.44, 0.28]
component Criminal Justice Data Standards [0.42, 0.25]
component Bias and Fairness Testing [0.40, 0.22]
component Legacy System Adapters [0.38, 0.30]

component Cross-Agency Integration Platform [0.34, 0.35]
component Common Platform APIs [0.32, 0.42]
component ATRS Registration Service [0.30, 0.20]

component API Gateway [0.26, 0.65]
component Event-Driven Messaging [0.24, 0.62]
component LLM AI Services [0.22, 0.68]
component Identity Access Management [0.20, 0.72]
component GOV.UK Design System [0.18, 0.78]
component GOV.UK Notify [0.16, 0.92]
component Security Zero Trust [0.14, 0.70]

component Cloud Hosting [0.08, 0.95]
component Managed Databases [0.06, 0.90]
component Container Orchestration [0.04, 0.82]

Fair Timely Transparent Justice -> Case Processing Efficiency
Fair Timely Transparent Justice -> Victim Witness Experience
Fair Timely Transparent Justice -> Defence Equality of Arms

Case Processing Efficiency -> AI Disclosure Review
Case Processing Efficiency -> AI Transcription Translation
Case Processing Efficiency -> Court Case Management
Case Processing Efficiency -> Cross-Agency Data Exchange

Victim Witness Experience -> Victim Case Tracking
Victim Witness Experience -> Remote Evidence Giving
Victim Witness Experience -> Notification Delivery

Defence Equality of Arms -> Defence Practitioner Portal
Defence Equality of Arms -> AI Disclosure Review
Defence Equality of Arms -> AI Case Summarisation

AI Disclosure Review -> Disclosure Engine
AI Disclosure Review -> Human Review Workflow
AI Disclosure Review -> AI Governance Controls

AI Transcription Translation -> NLP Language Models
AI Transcription Translation -> Human Review Workflow

Court Case Management -> Common Platform APIs
Court Case Management -> Cross-Agency Data Exchange

Victim Case Tracking -> Case Status Aggregation
Victim Case Tracking -> Notification Delivery
Victim Case Tracking -> GOV.UK Design System

Remote Evidence Giving -> Identity Access Management
Remote Evidence Giving -> Security Zero Trust

Defence Practitioner Portal -> Disclosure Material Access
Defence Practitioner Portal -> AI Case Summarisation
Defence Practitioner Portal -> GOV.UK Design System
Defence Practitioner Portal -> Identity Access Management

AI Case Summarisation -> Case Summarisation Engine
AI Case Summarisation -> Human Review Workflow

Disclosure Engine -> Evidence Triage
Disclosure Engine -> NLP Language Models
Disclosure Engine -> AI Governance Controls

NLP Language Models -> LLM AI Services

Case Summarisation Engine -> NLP Language Models

Notification Delivery -> GOV.UK Notify

Evidence Triage -> Cross-Agency Data Exchange
Evidence Triage -> LLM AI Services

Human Review Workflow -> Identity Access Management
Human Review Workflow -> Notification Delivery

Case Status Aggregation -> Cross-Agency Data Exchange
Case Status Aggregation -> Cross-Agency Integration Platform

Disclosure Material Access -> Cross-Agency Data Exchange
Disclosure Material Access -> Security Zero Trust

Digital Case File Viewer -> Cross-Agency Data Exchange
Digital Case File Viewer -> GOV.UK Design System

AI Governance Controls -> Bias and Fairness Testing
AI Governance Controls -> ATRS Registration Service

Cross-Agency Data Exchange -> Criminal Justice Data Standards
Cross-Agency Data Exchange -> Cross-Agency Integration Platform
Cross-Agency Data Exchange -> Legacy System Adapters

Criminal Justice Data Standards -> Cross-Agency Integration Platform

Cross-Agency Integration Platform -> API Gateway
Cross-Agency Integration Platform -> Event-Driven Messaging
Cross-Agency Integration Platform -> Security Zero Trust

Common Platform APIs -> API Gateway
Common Platform APIs -> Managed Databases

Legacy System Adapters -> API Gateway
Legacy System Adapters -> Managed Databases

ATRS Registration Service -> Managed Databases

API Gateway -> Cloud Hosting
Event-Driven Messaging -> Cloud Hosting
LLM AI Services -> Cloud Hosting
Identity Access Management -> Cloud Hosting
Security Zero Trust -> Cloud Hosting
GOV.UK Notify -> Cloud Hosting
Managed Databases -> Cloud Hosting
Container Orchestration -> Cloud Hosting

style wardley
```

---

## Component Inventory

### Level 0 — Anchor

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-00 | Fair Timely Transparent Justice | Anchor user need: all justice system participants receive fair, timely, transparent case outcomes | — | 0.97 |

### Level 1 — Primary User Outcomes

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-01 | Case Processing Efficiency | Cases progress from charge to outcome without unnecessary delay; technology reduces manual burden and enables faster throughput | C-00 | 0.93 |
| C-02 | Victim Witness Experience | Victims and witnesses are informed, supported, and able to participate in proceedings with minimum stress | C-00 | 0.91 |
| C-03 | Defence Equality of Arms | Defence practitioners have access to technology tools equivalent to those available to prosecution, ensuring constitutional fairness | C-00 | 0.89 |

### Level 2 — User-Facing Capabilities

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-04 | AI Disclosure Review | AI-assisted analysis of digital evidence to identify disclosable material with categorisation and confidence scoring (UC-1) | C-01, C-03 | 0.84 |
| C-05 | AI Transcription Translation | Real-time and batch transcription of hearings, police interviews, and evidence; translation for multilingual proceedings | C-01 | 0.82 |
| C-06 | Court Case Management | Enhanced case management supporting digital workflows, AI scheduling recommendations, and real-time status tracking (FR-006) | C-01 | 0.80 |
| C-07 | Victim Case Tracking | Victim/witness-facing service providing real-time case progress, notifications, and support information (UC-4, FR-007) | C-02 | 0.78 |
| C-08 | Remote Evidence Giving | Secure video link facilities for witnesses to give evidence remotely, including special measures support (FR-008) | C-02 | 0.76 |
| C-09 | Defence Practitioner Portal | Cloud-based platform providing defence practitioners with AI tools, disclosure access, evidence analysis, and case management (UC-2, FR-009) | C-03 | 0.74 |
| C-10 | AI Case Summarisation | AI-generated structured case summaries from case files, witness statements, and evidence for case preparation (FR-002) | C-03, C-01 | 0.72 |

### Level 3 — Processing Engines and Services

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-11 | Disclosure Engine | Core AI processing pipeline that analyses evidence items, applies disclosure rules, and produces categorised output | C-04 | 0.68 |
| C-12 | NLP Language Models | Criminal justice-specific NLP capabilities: entity extraction, legal reasoning, terminology understanding | C-05, C-11, C-17 | 0.66 |
| C-13 | Notification Delivery | Multi-channel notification service (SMS, email, letter, app push) for case updates and Victims' Code communications | C-07, C-15 | 0.64 |
| C-14 | Disclosure Material Access | Secure access to prosecution disclosure materials for defence practitioners with audit trail | C-09 | 0.62 |
| C-15 | Case Summarisation Engine | AI pipeline that produces structured case summaries from unstructured case materials | C-10 | 0.60 |

### Level 4 — Core Processing Components

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-16 | Evidence Triage | Automated initial categorisation and prioritisation of digital evidence items by type, relevance, and sensitivity | C-11 | 0.56 |
| C-17 | Human Review Workflow | Mandatory human-in-the-loop review queue for all AI outputs; captures decisions, overrides, and audit trail | C-04, C-05, C-10 | 0.54 |
| C-18 | Case Status Aggregation | Service that collects case status data from all agencies and presents a unified view of case progression | C-07 | 0.52 |
| C-19 | Digital Case File Viewer | Structured viewer for standardised digital case files with search, annotation, and bookmark capabilities | C-09, C-06 | 0.50 |
| C-20 | AI Governance Controls | Enforcement layer for AI governance: ATRS registration checks, DPIA status verification, judicial approval gate enforcement | C-04, C-11 | 0.48 |

### Level 5 — Integration and Data Layer

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-21 | Cross-Agency Data Exchange | Automated, standardised data flow between police (43 forces), CPS, HMCTS, HMPPS, and LAA (UC-3, FR-004) | C-01, C-16, C-18, C-14, C-19 | 0.44 |
| C-22 | Criminal Justice Data Standards | Cross-agency data schema, API specifications, evidence formats, and case file standard (FR-005) | C-21 | 0.42 |
| C-23 | Bias and Fairness Testing | Framework for testing AI outputs across protected characteristics (race, gender, age, socioeconomic status) | C-20 | 0.40 |
| C-24 | Legacy System Adapters | Translation and bridging components connecting 37 legacy applications to the modern integration layer | C-21 | 0.38 |
| C-25 | Cross-Agency Integration Platform | Central API-first integration layer connecting all justice agencies with routing, transformation, and orchestration | C-21, C-22 | 0.34 |
| C-26 | Common Platform APIs | API layer exposing HMCTS/CPS Common Platform capabilities for third-party integration | C-06 | 0.32 |
| C-27 | ATRS Registration Service | Service for registering AI tools in the Algorithmic Transparency Recording Standard; tracks deployments and compliance | C-20 | 0.30 |

### Level 6 — Platform Services

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-28 | API Gateway | API management, rate limiting, authentication, routing, and developer portal | C-25, C-26, C-24 | 0.26 |
| C-29 | Event-Driven Messaging | Pub/sub messaging for asynchronous case progression events across agencies | C-25 | 0.24 |
| C-30 | LLM AI Services | Large Language Model API services for NLP tasks (disclosure, summarisation, transcription, translation) | C-12, C-16 | 0.22 |
| C-31 | Identity Access Management | Authentication, SSO, role-based access control across agencies and practitioner types | C-08, C-09, C-17 | 0.20 |
| C-32 | GOV.UK Design System | Government frontend component library ensuring accessibility and consistency | C-07, C-09, C-19 | 0.18 |
| C-33 | GOV.UK Notify | Government notification utility service (SMS, email, letters) | C-13 | 0.16 |
| C-34 | Security Zero Trust | Zero-trust network architecture, encryption, WAF, SIEM for criminal justice data protection | C-08, C-14, C-25 | 0.14 |

### Level 7 — Infrastructure (Terminal Commodities)

| ID | Component | Description | Depends On | Visibility |
|----|-----------|-------------|------------|------------|
| C-35 | Cloud Hosting | AWS/Azure UK-region compute, storage, and networking (utility) | C-28 to C-34 | 0.08 |
| C-36 | Managed Databases | Cloud-managed PostgreSQL, document stores, and data warehousing | C-26, C-24, C-27 | 0.06 |
| C-37 | Container Orchestration | Managed Kubernetes for microservice deployment and scaling | C-35 | 0.04 |

---

## Dependency Matrix

Direct dependencies marked **X**; indirect dependencies marked **I**; blank = no dependency. Showing key components only (full 37x37 matrix abbreviated for readability).

| | C-04 AI Disc | C-09 Def Portal | C-07 Victim Track | C-21 Cross-Agency | C-25 Integ Platform | C-30 LLM | C-35 Cloud |
|---|---|---|---|---|---|---|---|
| **C-00 Anchor** | I | I | I | I | I | I | I |
| **C-01 Case Process** | X | | | X | I | I | I |
| **C-03 Defence Eq** | X | X | | I | I | I | I |
| **C-04 AI Disc** | — | | | I | I | I | I |
| **C-07 Victim Track** | | | — | I | I | | I |
| **C-09 Def Portal** | | — | | I | I | I | I |
| **C-11 Disc Engine** | X | | | I | I | X | I |
| **C-12 NLP Models** | I | I | | | | X | I |
| **C-16 Evid Triage** | I | | | X | I | X | I |
| **C-17 Human Review** | X | I | | | | | I |
| **C-21 Cross-Agency** | I | I | I | — | X | | I |
| **C-22 CJS Standards** | I | I | I | X | X | | |
| **C-25 Integ Platform** | I | I | I | X | — | | I |
| **C-28 API Gateway** | I | I | I | I | X | | X |
| **C-30 LLM Services** | I | I | | | | — | X |
| **C-35 Cloud** | I | I | I | I | I | I | — |

---

## Critical Path Analysis

### Critical Path 1: Prosecution Case Processing (Primary)

```text
Fair Timely Transparent Justice (0.97)
  └─> Case Processing Efficiency (0.93)
        └─> AI Disclosure Review (0.84)
              └─> Disclosure Engine (0.68)
                    └─> Evidence Triage (0.56)
                          └─> Cross-Agency Data Exchange (0.44)
                                └─> Cross-Agency Integration Platform (0.34)
                                      └─> API Gateway (0.26)
                                            └─> Cloud Hosting (0.08)
```

**Length**: 9 components, 8 dependency hops
**Risk**: Evidence Triage (C-16) and Disclosure Engine (C-11) are genesis/custom components with no fallback; failure disrupts the entire prosecution AI pipeline.

### Critical Path 2: Defence Equality (Constitutional)

```text
Fair Timely Transparent Justice (0.97)
  └─> Defence Equality of Arms (0.89)
        └─> Defence Practitioner Portal (0.74)
              └─> Disclosure Material Access (0.62)
                    └─> Cross-Agency Data Exchange (0.44)
                          └─> Criminal Justice Data Standards (0.42)
                                └─> Cross-Agency Integration Platform (0.34)
                                      └─> API Gateway (0.26)
                                            └─> Cloud Hosting (0.08)
```

**Length**: 9 components, 8 dependency hops
**Risk**: Defence Practitioner Portal (C-09) is genesis-stage with critical constitutional requirement; delayed delivery = legal challenge under Article 6 ECHR.

### Critical Path 3: Victim Experience

```text
Fair Timely Transparent Justice (0.97)
  └─> Victim Witness Experience (0.91)
        └─> Victim Case Tracking (0.78)
              └─> Case Status Aggregation (0.52)
                    └─> Cross-Agency Data Exchange (0.44)
                          └─> Cross-Agency Integration Platform (0.34)
                                └─> API Gateway (0.26)
                                      └─> Cloud Hosting (0.08)
```

**Length**: 8 components, 7 dependency hops
**Risk**: Case Status Aggregation (C-18) requires data from all 5 agencies; any agency failing to share data breaks the victim tracking chain.

### Convergence Point

All three critical paths converge at **Cross-Agency Data Exchange (C-21)** and flow through the same integration and infrastructure layer below. This makes the integration platform, data standards, and API gateway the **highest-leverage investment** — improvements here benefit all three value chains simultaneously.

### Bottlenecks and Single Points of Failure

| Component | Risk Type | Impact if Failed | Mitigation |
|-----------|-----------|------------------|------------|
| Cross-Agency Data Exchange (C-21) | Single point of convergence | All three value chains fail; prosecution, defence, and victim services lose cross-agency data | Prioritise as first integration deliverable; phased rollout (police-CPS first) |
| Criminal Justice Data Standards (C-22) | No existing standard | Integration impossible without agreed schema; agencies cannot exchange data | Cross-agency working group immediately; MoJ convening authority |
| LLM AI Services (C-30) | Vendor dependency | All AI capabilities (disclosure, summarisation, transcription) degrade | Multi-model strategy; abstraction layer; two providers minimum |
| Human Review Workflow (C-17) | Operational bottleneck | AI outputs cannot be approved; all AI-assisted cases blocked | Scale reviewer workforce; SLA for review turnaround; prioritisation queue |
| Legacy System Adapters (C-24) | 37 unique systems | Each adapter is bespoke; failure isolates legacy data from modern platform | Phased migration by risk priority; dual-running period; strangler-fig pattern |

### Resilience Gaps

- [x] Cross-Agency Integration Platform (C-25) has no fallback — if the platform is down, all cross-agency data exchange stops. Manual fallback procedures must be documented.
- [x] LLM AI Services (C-30) depend on external cloud AI providers — outage at Azure OpenAI or AWS Bedrock degrades all AI features. Multi-provider redundancy required.
- [x] Defence Practitioner Portal (C-09) serves a fragmented user base (thousands of sole practitioners) with no central IT support — if the portal is unavailable, defence practitioners have no alternative.
- [x] GOV.UK Notify (C-33) is a shared government service — if Notify experiences outage, victim notifications stop. Plan for notification queuing and retry.

---

## Validation Checklist

- [x] Chain starts with user need (anchor): "Justice system participants receive fair, timely, and transparent criminal case outcomes"
- [x] All critical dependencies captured: 35 components with 70+ dependency relationships
- [x] Chain reaches commodity level: Cloud Hosting (0.08), Managed Databases (0.06), Container Orchestration (0.04)
- [x] No orphan components: every component has at least one inbound or outbound dependency
- [x] Dependencies reflect reality: verified against use cases UC-1 through UC-5 and functional requirements FR-001 through FR-010
- [x] Visibility ordering correct: higher visibility = closer to user; infrastructure at bottom
- [x] Granularity appropriate: 35 components across 7 levels — sufficient for strategic decisions without excessive detail
- [x] All components are activities/capabilities: no teams, people, or actors in the chain
- [x] Three parallel chains (prosecution, defence, victim) converge at shared integration layer — correctly modelled

---

## Visibility Assessment

| Level | Range | Components at This Level | Count |
|-------|-------|--------------------------|-------|
| **User-facing** | 0.90 – 1.00 | Fair Timely Transparent Justice, Case Processing Efficiency, Victim Witness Experience, Defence Equality of Arms | 4 |
| **High** | 0.70 – 0.89 | AI Disclosure Review, AI Transcription Translation, Court Case Management, Victim Case Tracking, Remote Evidence Giving, Defence Practitioner Portal, AI Case Summarisation | 7 |
| **Medium-High** | 0.50 – 0.69 | Disclosure Engine, NLP Language Models, Notification Delivery, Disclosure Material Access, Case Summarisation Engine, Evidence Triage, Human Review Workflow, Case Status Aggregation, Digital Case File Viewer, AI Governance Controls | 10 |
| **Medium** | 0.30 – 0.49 | Cross-Agency Data Exchange, CJS Data Standards, Bias and Fairness Testing, Legacy System Adapters, Cross-Agency Integration Platform, Common Platform APIs, ATRS Registration Service | 7 |
| **Low** | 0.10 – 0.29 | API Gateway, Event-Driven Messaging, LLM AI Services, Identity Access Management, GOV.UK Design System, GOV.UK Notify, Security Zero Trust | 7 |
| **Infrastructure** | 0.00 – 0.09 | Cloud Hosting, Managed Databases, Container Orchestration | 3 |

**Distribution**: The chain is bottom-heavy — 17 components at medium or below (integration, platform, infrastructure) supporting 11 user-facing and high-visibility components. This reflects the programme's challenge: most investment must go into invisible infrastructure and integration to enable visible user outcomes.

---

## Strategic Insights from the Value Chain

### 1. Cross-Agency Integration is the Keystone

The convergence of all three critical paths at Cross-Agency Data Exchange (C-21) and the Integration Platform (C-25) means:
- These components are the **highest-leverage investment** — every pound spent here benefits prosecution, defence, AND victim chains
- Failure here cascades to all user outcomes
- The Criminal Justice Data Standards (C-22) component is a prerequisite for everything — without agreed schemas, no integration is possible

### 2. AI Components Form a Shared Engine

The Disclosure Engine (C-11), NLP Language Models (C-12), and Case Summarisation Engine (C-15) all depend on LLM AI Services (C-30) and feed through the Human Review Workflow (C-17). This creates an "AI processing layer" that:
- Can be built once and reused across prosecution, defence, and court administration
- Requires consistent AI governance controls (C-20) regardless of which user persona it serves
- Benefits from LLM commoditisation — as LLM prices drop, all AI capabilities improve

### 3. Defence Chain is the Most Fragile

The Defence Equality of Arms chain (C-03 → C-09 → C-14 → C-21) contains two genesis-stage components (Defence Practitioner Portal, Disclosure Material Access) and serves the most fragmented, least-resourced user base. This is simultaneously the most constitutionally critical and the most technically risky chain.

### 4. GOV.UK Services Absorb Commodity Functions

GOV.UK Notify (C-33) and GOV.UK Design System (C-32) serve as terminal dependencies for the victim tracking and defence portal chains, absorbing notification delivery and frontend rendering into commodity government services. This eliminates the need to build custom notification or UI frameworks — a significant cost avoidance.

### 5. Legacy Adapters Create a Long Tail of Custom Work

Legacy System Adapters (C-24) represent 37 individual adapter implementations — each bespoke. While the Integration Platform (C-25) is a single investment, the adapters multiply effort by system count. This is the primary driver of the legacy migration programme's cost and duration.

---

## Assumptions and Open Questions

**Assumptions Made**:

| # | Assumption | Basis | Confidence |
|---|------------|-------|------------|
| A-01 | All 5 justice agencies will agree to adopt common data standards within 18 months | MoJ convening authority; Leveson Review mandate | Medium — political inertia is real |
| A-02 | LLM AI Services are sufficiently mature for criminal justice NLP tasks (disclosure, summarisation) | Current GPT-4/Claude capability benchmarks; CJS pilot results | High — NLP is mature; CJS fine-tuning is the custom layer |
| A-03 | Defence practitioners will adopt the Defence Practitioner Portal if provided with LAA-funded access | User research hypothesis; CBA/Law Society endorsement | Medium — adoption depends on usability and practitioner trust |
| A-04 | The Common Platform can be stabilised and its APIs exposed for integration | HMCTS CTO assessment; current stabilisation programme | Medium — Common Platform has a troubled history |
| A-05 | Human review capacity can scale to match AI output volume | Workforce planning assumption; reviewer training programme | Low — this is a known operational risk |
| A-06 | 43 police forces can be connected through a common gateway within 36 months | NPCC digital strategy; pilot with Met/West Midlands | Low — police IT fragmentation is extreme |
| A-07 | Judicial steering group will approve AI disclosure tools for live case use | Engagement with Lead Judge for AI; sandbox pilot approach | Medium — judiciary is cautious but engaged |

**Open Questions**:

| # | Question | Owner | Due Date |
|---|----------|-------|----------|
| Q-01 | Will DPA 2018 Part 3 require separate data controllers per agency, or can MoJ act as joint controller for the integration platform? | MoJ DPO + ICO consultation | 2026-06-30 |
| Q-02 | Should the Defence Practitioner Portal use GOV.UK One Login or a separate authentication mechanism for non-government users? | MoJ CDIO + GDS | 2026-05-31 |
| Q-03 | Can AI Disclosure Review be deployed in magistrates' courts (lower complexity) before Crown Court (higher stakes) to reduce risk? | Programme Board | 2026-04-30 |
| Q-04 | What is the minimum number of police forces required for the Integration Platform pilot to demonstrate value? | NPCC + MoJ CDIO | 2026-05-15 |
| Q-05 | How will Human Review Workflow capacity be funded and sustained as AI output volume grows? | MoJ Permanent Secretary | 2026-06-30 |
| Q-06 | Should Criminal Justice Data Standards be published as a formal British Standard (BS) or as government guidance? | MoJ CDIO + BSI | 2026-09-30 |

---

## External References

| Document | Type | Source | Key Extractions |
|----------|------|--------|-----------------|
| ARC-001-REQ-v1.0 | Requirements | Project 001 | 10 business requirements; 10+ functional requirements; 8 user personas; 5 use cases |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | Project 001 | 15 stakeholders; power/interest grid; user persona priorities |
| ARC-000-PRIN-v1.0 | Architecture Principles | Global | 23 principles including P-01 (Interoperability), P-02 (Human-Centred AI), P-21 (Equality of Arms) |
| ARC-001-WARD-001-v1.0 | Wardley Map | Project 001 | Existing evolution positions and build/buy decisions for all components |
| ARC-001-STRAT-v1.0 | Architecture Strategy | Project 001 | Strategic vision; build/buy decisions; 5-year horizon |
| ARC-001-DPIA-v1.0 | DPIA | Project 001 | HIGH impact assessment; criminal justice data processing activities |

---

**Generated by**: ArcKit `/arckit:wardley.value-chain` command
**Generated on**: 2026-03-16 15:15 GMT
**ArcKit Version**: 1.5.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: claude-opus-4-6
**Generation Context**: Decomposed from ARC-001-REQ-v1.0 (10 business requirements, 10 functional requirements, 8 personas, 5 use cases), ARC-001-STKE-v1.0 (15 stakeholders), ARC-000-PRIN-v1.0 (23 principles), and ARC-001-WARD-001-v1.0 (existing Wardley Map evolution positions)

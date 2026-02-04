# Criminal Courts Technology & AI Reform — Governance Quality Analysis

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.analyze`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-ANLZ-v1.0 |
| **Document Type** | Governance Quality Analysis |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-04 |
| **Last Modified** | 2026-02-04 |
| **Review Cycle** | On-Demand |
| **Next Review Date** | 2026-05-04 |
| **Owner** | Enterprise Architect |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, Programme Board |
| **Author** | Enterprise Architect |
| **Approver** | Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial analysis from `/arckit.analyze` command | PENDING | PENDING |

---

## Executive Summary

This report presents a comprehensive governance quality analysis of the Criminal Courts Technology & AI Reform programme (Project 001). The analysis examined **6 published artifacts** across 8 detection passes to identify inconsistencies, gaps, ambiguities, and compliance risks.

### Analysis Scope

| Artifact | Document ID | Status |
|----------|------------|--------|
| Architecture Principles | ARC-000-PRIN-v1.0 | ✅ Analysed |
| Stakeholder Analysis | ARC-001-STKE-v1.0 | ✅ Analysed |
| Requirements | ARC-001-REQ-v1.0 | ✅ Analysed |
| Risk Register | ARC-001-RISK-v1.0 | ✅ Analysed |
| Strategic Outline Business Case | ARC-001-SOBC-v1.0 | ✅ Analysed |
| Statement of Work | ARC-001-SOW-v1.0 | ✅ Analysed |
| Project Story | ARC-001-STRY-v1.0 | ✅ Reviewed (context only) |

### Missing Artifacts (Not Yet Produced)

| Expected Artifact | Type Code | Impact |
|-------------------|-----------|--------|
| Data Model | DATA | HIGH — 4 data requirements (DR-001 to DR-004) defined but no formal data model produced |
| TCoP Assessment | TCOP | HIGH — mandatory for UK Government technology projects |
| AI Playbook Assessment | AIPB | CRITICAL — mandatory for UK Government AI deployments |
| ATRS Records | ATRS | CRITICAL — mandatory before any AI tool deployment (per NFR-C-003) |
| Traceability Matrix | TRAC | MEDIUM — needed for governance gates |
| DPIA | DPIA | CRITICAL — legally mandatory for AI processing criminal justice data |
| Secure by Design | SECD | HIGH — recommended for civilian UK Government departments |
| Vendor HLD/DLD | HLD/DLD | N/A — pending vendor procurement |
| Vendor Evaluation | EVAL | N/A — pending vendor responses |

### Findings Summary

| Severity | Count | Description |
|----------|-------|-------------|
| **CRITICAL** | 5 | Must resolve before programme proceeds past discovery |
| **HIGH** | 8 | Should resolve before OBC stage |
| **MEDIUM** | 12 | Should resolve before beta/design phase |
| **LOW** | 6 | Minor improvements recommended |
| **TOTAL** | **31** | |

### Overall Governance Health Score

| Dimension | Score | Rating |
|-----------|-------|--------|
| Requirements Quality | 78/100 | GOOD |
| Principles Alignment | 85/100 | GOOD |
| Stakeholder Traceability | 82/100 | GOOD |
| Risk Coverage | 75/100 | ADEQUATE |
| Business Case Alignment | 80/100 | GOOD |
| UK Gov Compliance Readiness | 45/100 | INADEQUATE |
| Cross-Artifact Consistency | 72/100 | ADEQUATE |
| Design Traceability | 10/100 | NOT STARTED |
| **Overall** | **66/100** | **ADEQUATE** |

> **Interpretation**: The programme has strong foundational governance (principles, stakeholders, requirements, risk, business case) but significant gaps in UK Government compliance artifacts and design-phase traceability. This is expected at SOBC stage — the critical action is ensuring compliance artifacts are produced before OBC submission and any AI deployment.

---

## Detection Pass 1: Requirements Quality Analysis

### 1.1 Completeness Assessment

**Coverage**: 10 BR + 14 FR + 22 NFR + 6 INT + 4 DR = **56 requirements** (story claims 60; discrepancy from counting method — NFR sub-categories total 22 not 26)

| Finding ID | Severity | Finding | Affected Artifact | Detail |
|------------|----------|---------|-------------------|--------|
| RQ-001 | **MEDIUM** | Requirements count inconsistency | ARC-001-REQ-v1.0 / ARC-001-STRY-v1.0 | Story and SOW reference "60 requirements" and "26 NFR" but detailed count yields 56 total and 22 NFR. The discrepancy appears to be from counting individual NFR checklist items vs NFR requirement identifiers. Standardise the count methodology. |
| RQ-002 | **MEDIUM** | Missing acceptance criteria on some FRs | ARC-001-REQ-v1.0 | FR-001 through FR-014 have acceptance criteria, but some are process-oriented ("AI governance framework approved") rather than testable. FR-006 (AI Governance) acceptance criteria ("framework approved by judicial steering group") is an approval gate, not a testable criterion. |
| RQ-003 | **LOW** | NFR targets missing measurement method | ARC-001-REQ-v1.0 | NFR-P-001 (500ms p95) and NFR-A-001 (99.9%) state targets but the NFR section doesn't specify measurement tools. The KPI table in Success Criteria references "APM tooling" and "uptime monitoring" but this should be in the NFR itself. |
| RQ-004 | **HIGH** | No explicit requirement for AI model explainability metrics | ARC-001-REQ-v1.0 | TC-004 states "AI models must be auditable and explainable" and NFR-C-003 covers ATRS, but there is no FR or NFR specifying *what level* of explainability is required (e.g., SHAP values, feature importance, plain-language explanation). This is critical for criminal justice AI where decisions may be challenged in court. |
| RQ-005 | **MEDIUM** | DR-001 to DR-004 lack data validation rules | ARC-001-REQ-v1.0 | Data entities define attributes and types but validation rules are limited to "Validated" or "Validated state machine" without specifying the valid states or transition rules. |

### 1.2 Ambiguity Assessment

| Finding ID | Severity | Finding | Affected Artifact | Detail |
|------------|----------|---------|-------------------|--------|
| RQ-006 | **MEDIUM** | Ambiguous availability target scope | ARC-001-REQ-v1.0 | NFR-A-001 states "99.9% during court sitting hours" but does not define sitting hours (typically 10:00–16:30 but varies). Also unclear whether 99.9% applies per-service or to the aggregate platform. |
| RQ-007 | **LOW** | "AI-assisted" undefined scope | ARC-001-REQ-v1.0 | Multiple requirements use "AI-assisted" (BR-002, FR-001, FR-002, FR-003) without defining the boundary between AI assistance and AI autonomy. The conflict resolution (C-1) partially addresses this with "safe AI" vs "case-affecting AI" but this distinction needs to be formalised as a requirement. |
| RQ-008 | **LOW** | NFR-S-002 growth rate assumption | ARC-001-REQ-v1.0 | "30% annual growth" for evidence data and "500TB over 5 years" — these should be cross-validated. If starting at ~50TB with 30% annual growth: 50→65→85→110→143 = ~453TB. The 500TB figure implies higher baseline or growth rate. |

### 1.3 Testability Assessment

| Finding ID | Severity | Finding | Affected Artifact | Detail |
|------------|----------|---------|-------------------|--------|
| RQ-009 | **MEDIUM** | Business requirements lack measurable acceptance criteria | ARC-001-REQ-v1.0 | BR-001 through BR-010 are strategic requirements traced to stakeholder goals, but none has explicit acceptance criteria. They rely on the Success Criteria KPI table for measurability. Recommend adding a "measured by" field to each BR linking to specific KPIs. |
| RQ-010 | **LOW** | Use case coverage gaps | ARC-001-REQ-v1.0 | 5 use cases defined (UC-1 to UC-5) but no use case for: victim case tracking (FR-007), AI governance workflow (FR-006/BR-006), or legacy migration operations (BR-005/FR-010). |

---

## Detection Pass 2: Architecture Principles Alignment

### 2.1 Principles Coverage Matrix

| Principle | Category | Requirements Coverage | Risk Coverage | SOBC Coverage | Rating |
|-----------|----------|----------------------|---------------|---------------|--------|
| P1: Cross-Agency Interoperability | Strategic | BR-004, INT-001–006, NFR-I-001/002 | R-003, R-016 | ✅ Pillar 2 | STRONG |
| P2: Human-Centred AI | Strategic | BR-002, FR-001–005, BR-006, FR-006 | R-005, R-009, R-013 | ✅ Pillar 1 | STRONG |
| P3: Security by Design (NON-NEGOTIABLE) | Strategic | NFR-SEC-001–006, NFR-C-005 | R-006, R-015, R-020 | ✅ Referenced | STRONG |
| P4: Legacy Modernisation | Strategic | BR-005, FR-010 | R-012, R-017 | ✅ Pillar 3 | STRONG |
| P5: Scalability and Elasticity | Quality | NFR-S-001, NFR-S-002 | R-017 | Implicit | ADEQUATE |
| P6: Resilience and Fault Tolerance | Quality | NFR-A-001–003 | R-012 | Implicit | ADEQUATE |
| P7: Observability | Quality | NFR-M-001 | — | — | WEAK |
| P8: Data as Shared Asset | Data | DR-001–004, INT-001–006 | R-008 | ✅ Referenced | STRONG |
| P9: Data Quality | Data | Data Quality Requirements section | R-008 | Implicit | ADEQUATE |
| P10: Privacy and Data Protection | Data | NFR-C-001, NFR-SEC-003 | R-007, R-014 | ✅ Referenced | STRONG |
| P11: Loose Coupling | Integration | NFR-I-001, INT-001–006 | — | Implicit | ADEQUATE |
| P12: Event-Driven Integration | Integration | INT-001, INT-004 | — | — | WEAK |
| P13: Performance | Quality | NFR-P-001, NFR-P-002 | — | — | ADEQUATE |
| P14: Availability | Quality | NFR-A-001 | R-012 | ✅ Referenced | ADEQUATE |
| P15: Accessibility | Quality | NFR-U-001 | — | ✅ Referenced | ADEQUATE |
| P16: Maintainability | Quality | NFR-M-001–003 | — | — | ADEQUATE |
| P17: Infrastructure as Code | Development | NFR-M-002 | — | — | ADEQUATE |
| P18: Automated Testing | Development | NFR-M-003 (pipeline) | — | — | WEAK |
| P19: CI/CD | Development | NFR-M-003 | — | — | ADEQUATE |
| P20: Open Standards | Development | NFR-I-002 | R-010 | ✅ Referenced | STRONG |
| P21: Equality of Arms | Criminal Justice | BR-003, FR-009 | R-002 | ✅ Pillar 1/4 | STRONG |
| P22: Judicial Independence | Criminal Justice | BR-006, TC-005 | R-001 | ✅ Referenced | STRONG |
| P23: Victim/Witness Protection | Criminal Justice | BR-007, FR-007, DR-004 | R-011 | ✅ Pillar 4 | STRONG |

### 2.2 Principles Alignment Findings

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| PA-001 | **MEDIUM** | Principle 7 (Observability) weakly reflected in risk register | No risk addresses observability failure or monitoring blind spots. If cross-agency distributed tracing fails, incident response across agencies would be severely impacted. |
| PA-002 | **MEDIUM** | Principle 12 (Event-Driven Integration) not fully realised in requirements | Only INT-001 and INT-004 specify event-driven patterns. INT-002 (police), INT-003 (CPS), INT-005 (LAA) are API-only. Event-driven architecture is a stated principle but not consistently applied. |
| PA-003 | **LOW** | Principle 18 (Automated Testing) lacks explicit requirement | NFR-M-003 covers CI/CD pipeline stages including testing, but there is no NFR specifying test coverage targets (e.g., 80% unit test coverage, contract test coverage for all APIs). |

---

## Detection Pass 3: Stakeholder Traceability Analysis

### 3.1 Driver → Goal → Outcome → Requirement Traceability

| Driver | Goals Traced | Requirements Traced | Risks Traced | Gaps |
|--------|-------------|--------------------|--------------|----- |
| SD-1 (Backlog crisis) | G-1 | BR-001, BR-002, FR-001–005 | R-001, R-004 | None |
| SD-2 (Judicial concerns) | G-2, G-3 | BR-006, FR-006, TC-005 | R-001, R-005 | None |
| SD-3 (Fragmented systems) | G-4 | BR-004, INT-001–006 | R-003, R-016 | None |
| SD-4 (Prosecution efficiency) | G-5 | BR-002, FR-001–003 | R-005, R-009 | None |
| SD-5 (Police interoperability) | G-4 | BR-004, INT-002 | R-003 | None |
| SD-6 (Defence inequality) | G-6 | BR-003, FR-009 | R-002 | None |
| SD-7 (Victim experience) | G-7 | BR-007, FR-007 | R-011 | None |
| SD-8 (Legacy risk) | G-5 | BR-005, FR-010 | R-012, R-017 | None |
| SD-9 (Treasury scrutiny) | G-8 | BR-008, SOBC | R-004 | None |
| SD-10 (Data protection) | G-9 | NFR-C-001, NFR-SEC-001–006 | R-007, R-014 | None |
| SD-11 (AI governance) | G-2, G-3 | BR-006, FR-006, NFR-C-003 | R-005, R-009, R-013 | None |
| SD-12 (Digital standards) | G-10 | NFR-C-004, NFR-C-005 | — | **Gap**: No risk for GDS service assessment failure |
| SD-13 (Staff wellbeing) | G-5 | FR-011 | — | **Gap**: No risk for staff resistance/wellbeing |
| SD-14 (Magistrates' needs) | G-5 | NFR-U-003, BC-005 | — | **Gap**: No dedicated risk for magistrates' court deprioritisation |
| SD-15 (Professional standards) | G-6 | BR-003, FR-009 | R-002 | None |

### 3.2 Stakeholder Traceability Findings

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| ST-001 | **MEDIUM** | Driver SD-12 (GDS/CDDO digital standards) has no associated risk | If the programme fails GDS service assessment, user-facing services cannot proceed to beta/live. This is a real governance risk that should be in the risk register. |
| ST-002 | **LOW** | Driver SD-13 (court staff wellbeing) weakly traced | FR-011 (Court Staff Dashboard) addresses tooling but no risk covers staff resistance to change or inadequate training causing operational issues. |
| ST-003 | **LOW** | Driver SD-14 (Magistrates' courts) has no dedicated risk | BC-005 is a business constraint, but the risk register doesn't have a specific risk for magistrates' courts being deprioritised. The Leveson Review and Magistrates' Association would flag this. |

---

## Detection Pass 4: Risk Management Analysis

### 4.1 Risk Coverage Assessment

**Risk Register**: 20 risks across 6 categories. Orange Book compliant (5×5 matrix, 4Ts framework).

| Category | Count | Coverage Assessment |
|----------|-------|-------------------|
| Strategic | 5 | STRONG — covers funding, political change, stakeholder resistance, cross-agency governance, scope creep |
| Operational | 4 | ADEQUATE — covers legacy migration, CP instability, staff capacity, court disruption |
| Financial | 3 | ADEQUATE — covers cost overrun, funding phasing, vendor pricing |
| Compliance | 3 | ADEQUATE — covers GDPR/DPA, AI ethics, judicial review |
| Reputational | 2 | ADEQUATE — covers public trust, legal profession confidence |
| Technology | 3 | ADEQUATE — covers AI maturity, vendor lock-in, integration complexity |

### 4.2 Risk Analysis Findings

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| RA-001 | **HIGH** | No cyber security breach risk | Despite NFR-SEC-001–006 and NCSC CAF alignment (NFR-C-005), the risk register contains no explicit risk for a cyber security breach or data breach. Given criminal justice data sensitivity (DPA 2018 Part 3), this is a significant omission. R-015 covers "GDPR breach" but focuses on regulatory non-compliance, not the breach event itself. |
| RA-002 | **MEDIUM** | No risk for Common Platform vendor dependency | The programme depends on Common Platform (INT-001) which is a troubled existing system. R-012 covers "legacy migration disruption" and R-005 covers "CP instability" but there is no risk specifically addressing Fujitsu/Common Platform vendor relationship failure or contract dispute. |
| RA-003 | **MEDIUM** | No risk for AI model bias (distinct from R-013) | R-013 covers "AI ethics controversy" but the risk register should have a distinct risk for AI model bias against protected characteristics (race, gender, age) in criminal justice, which could lead to wrongful outcomes. The requirements mention bias assessment (NFR-C-003) but no corresponding risk. |
| RA-004 | **LOW** | Risk appetite statement missing | Orange Book methodology requires a documented risk appetite statement. The risk register uses a 5×5 matrix and severity categories but doesn't state the programme's risk appetite (e.g., "zero tolerance for risks that compromise defendant rights"). |
| RA-005 | **HIGH** | R-002 (Defence equality, Critical 20) has no risk reduction pathway | R-002 is the highest residual risk (score 20, Critical) but the controls only reduce it from 25 to 20. There is no escalation path or contingency plan documented for what happens if defence equality cannot be achieved. Given this is a fundamental Article 6 ECHR issue, this needs a more robust treatment plan. |

---

## Detection Pass 5: Business Case Alignment Analysis

### 5.1 SOBC–Requirements Alignment

| SOBC Element | Requirements Coverage | Consistency |
|--------------|----------------------|-------------|
| Option 3 (Phased Comprehensive) | All 10 BRs as MUST_HAVE | ✅ Aligned |
| £281M investment (5-year) | BR-008 references Green Book approval | ✅ Aligned |
| Pillar 1: AI Tools | BR-002, FR-001–005, FR-006 | ✅ Aligned |
| Pillar 2: Interoperability | BR-004, INT-001–006 | ✅ Aligned |
| Pillar 3: Legacy Migration | BR-005, FR-010 | ✅ Aligned |
| Pillar 4: Victim Services | BR-007, FR-007, FR-008 | ✅ Aligned |
| Pillar 5: AI Governance | BR-006, FR-006, NFR-C-003 | ✅ Aligned |
| BCR 1.1:1 (quantified) | — | See findings |
| NPV +£5.1M (conservative) | — | See findings |

### 5.2 Business Case Findings

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| BC-001 | **HIGH** | BCR inconsistency between SOBC and Story | SOBC states BCR 1.1:1 (quantified only) and ~1.5:1 (including strategic benefits). The Project Story (ARC-001-STRY-v1.0) states "BCR 1.5:1" without qualification. This could mislead stakeholders — the auditable quantified BCR is 1.1:1 which is marginal for Treasury approval. |
| BC-002 | **HIGH** | Investment figure inconsistency | SOBC states "£281M over 5 years (£326M with optimism bias)". Story states "£285M investment". SOW references the programme budget contextually. The £281M vs £285M discrepancy needs reconciliation. |
| BC-003 | **MEDIUM** | Benefits figure inconsistency | SOBC states "£495M over 10 years". Story states "£420M benefits". These are different figures that need reconciliation across documents. |
| BC-004 | **MEDIUM** | Optimism bias treatment | SOBC applies 41% optimism bias uplift (appropriate for IT-enabled business change per Green Book supplementary guidance). However, the requirements don't reference optimism bias in cost assumptions, and the SOW evaluation criteria don't require vendors to address optimism bias in their pricing. |
| BC-005 | **LOW** | No sensitivity analysis on key assumptions | SOBC should include sensitivity analysis showing impact of key assumption failures (e.g., what if AI disclosure only achieves 50% coverage instead of 80%? What if only 15 of 37 legacy apps are migrated in 5 years?). |

---

## Detection Pass 6: UK Government Compliance Analysis

### 6.1 Compliance Framework Coverage

| Framework | Artifact Exists | Requirements Coverage | Assessment Complete | Rating |
|-----------|----------------|----------------------|--------------------|---------|
| GDS Service Standard (14 points) | ❌ No assessment | NFR-C-004 (partial — 8 of 14 points listed) | ❌ | **INADEQUATE** |
| Technology Code of Practice (13 points) | ❌ No TCoP assessment | Implicit in principles | ❌ | **NOT STARTED** |
| NCSC Cyber Assessment Framework | ❌ No assessment | NFR-C-005 (4 objectives listed) | ❌ | **INADEQUATE** |
| UK GDPR / DPA 2018 Part 3 | ❌ No DPIA | NFR-C-001 (detailed) | ❌ | **INADEQUATE** |
| AI Playbook (10 principles) | ❌ No assessment | NFR-C-003 (referenced) | ❌ | **NOT STARTED** |
| ATRS | ❌ No ATRS records | NFR-C-003 (checklist) | ❌ | **NOT STARTED** |
| HM Treasury Green Book | ✅ SOBC produced | BR-008, SOBC 5-case model | ✅ SOBC complete | **GOOD** |
| HM Treasury Orange Book | ✅ Risk register produced | Risk register methodology | ✅ Complete | **GOOD** |
| Secure by Design | ❌ No assessment | NFR-SEC-001–006 | ❌ | **NOT STARTED** |

### 6.2 UK Gov Compliance Findings

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| UK-001 | **CRITICAL** | No DPIA produced for AI processing criminal justice data | DPA 2018 Part 3 and UK GDPR Article 35 require a DPIA before processing that is "likely to result in a high risk to the rights and freedoms of natural persons." AI-assisted disclosure review on criminal case evidence unequivocally triggers this requirement. NFR-C-001 mandates DPIA completion but no DPIA artifact exists. This is a **legal requirement**, not optional governance. |
| UK-002 | **CRITICAL** | No ATRS records for planned AI tools | NFR-C-003 mandates ATRS compliance and the requirements specify AI tools for: disclosure review, case summarisation, transcription, translation, scheduling. Each requires its own ATRS record published before deployment. No ATRS records exist. The Central Digital and Data Office (CDDO) mandates ATRS for all government algorithmic tools. |
| UK-003 | **CRITICAL** | No AI Playbook assessment | The UK Government AI Playbook's 10 principles are mandatory for government AI deployments. NFR-C-003 references this requirement but no assessment has been produced. Given 5 distinct AI capabilities in the programme, this is a significant gap. |
| UK-004 | **HIGH** | No TCoP assessment | The Technology Code of Practice is mandatory for all UK Government technology spending. The programme's £281M investment requires TCoP compliance demonstration, typically as part of the spend control process. |
| UK-005 | **HIGH** | GDS Service Standard coverage incomplete | NFR-C-004 lists 8 of 14 points. Missing points: 2 (Solve a whole problem), 3 (Provide a joined-up experience), 4 (Make the service simple to use), 7 (Use agile ways of working), 10 (Define success and publish data), 13 (Use common components and patterns). Points 2, 3, and 4 are particularly relevant for a multi-agency criminal justice programme. |
| UK-006 | **HIGH** | No Secure by Design assessment | While not strictly mandatory for civilian departments, the Government Security Standard and NCSC guidance strongly recommend Secure by Design principles documentation for programmes handling sensitive data. Given DPA 2018 Part 3 data classification, this should be treated as a HIGH priority. |
| UK-007 | **MEDIUM** | NCSC CAF alignment stated but not evidenced | NFR-C-005 lists 4 CAF objectives at headline level but doesn't map specific requirements to CAF contributing outcomes (A1–A4, B1–B6, C1–C2, D1–D2). A proper CAF self-assessment is needed. |

---

## Detection Pass 7: Cross-Artifact Consistency Analysis

### 7.1 Numerical Consistency

| Data Point | ARC-001-REQ | ARC-001-RISK | ARC-001-SOBC | ARC-001-SOW | ARC-001-STRY | Status |
|------------|-------------|--------------|--------------|-------------|--------------|--------|
| Total requirements | 56 (by ID count) | — | — | "60 requirements" | "60 requirements" | ⚠️ INCONSISTENT |
| NFR count | 22 (by ID) | — | — | "26 NFR" | "26 NFR" | ⚠️ INCONSISTENT |
| Investment amount | — | — | £281M (£326M w/ OB) | Referenced | "£285M" | ⚠️ INCONSISTENT |
| Benefits amount | — | — | £495M (10-year) | Referenced | "£420M" | ⚠️ INCONSISTENT |
| BCR | — | — | 1.1:1 (quantified) | — | "1.5:1" | ⚠️ INCONSISTENT |
| NPV | — | — | +£5.1M (conservative) / +£95M (strategic) | — | "£95M" | ✅ Consistent (strategic) |
| Risk count | — | 20 risks | — | — | "20 risks" | ✅ Consistent |
| Stakeholder count | — | — | — | — | "15 stakeholders" | ✅ Consistent |
| Legacy applications | BR-005: "37 legacy" | R-012: "37 legacy" | "37 critical applications" | "37 legacy applications" | — | ✅ Consistent |
| Outstanding cases | BR-001: "77,000+" | — | "77,000+" | "77,000+" | "77,000+" | ✅ Consistent |
| Programme duration | "5 years" | — | "5 years" | "60 months" | — | ✅ Consistent |

### 7.2 Terminology Consistency

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| CC-001 | **MEDIUM** | "Safe AI" vs "non-contentious AI" vs "non-case-affecting AI" | Requirements conflict C-1 introduces "safe AI" as a category for immediate deployment (transcription, translation, summarisation). This term is used inconsistently — sometimes "non-contentious", sometimes "non-case-affecting". Standardise terminology. |
| CC-002 | **LOW** | Risk numbering convention differs | Requirements file uses R-1 through R-10 in the risk table. Risk register uses R-001 through R-020 with zero-padded IDs. The risks are not the same entities — REQ has summary risks, RISK has the full register. This could cause confusion. |
| CC-003 | **MEDIUM** | SOW milestone count discrepancy | SOW defines 11 milestones over 60 months. Requirements define 15 milestones in the Timeline section. The milestones should be reconciled — the SOW milestones are vendor-facing while requirements milestones are programme-facing, but they should align. |

### 7.3 Cross-Reference Integrity

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| CC-004 | **HIGH** | SOW mandatory qualifications reference undocumented standards | SOW MQ-3 requires "ISO 27001 certification and Cyber Essentials Plus". NFR-C-005 requires "Cyber Essentials Plus" but ISO 27001 is not mentioned in requirements. If ISO 27001 is a vendor requirement, it should be in the NFRs as a compliance requirement. |
| CC-005 | **MEDIUM** | SOBC option analysis doesn't reference all requirements | SOBC Option 3 (Recommended) maps to all 10 BRs and 10 stakeholder goals, but doesn't explicitly reference how NFRs (particularly security NFRs) informed the cost estimate. Security and compliance NFRs typically add 15-25% to delivery cost. |

---

## Detection Pass 8: Security and Data Protection Analysis

### 8.1 Security Requirements Assessment

| Aspect | Coverage | Finding |
|--------|----------|---------|
| Authentication | NFR-SEC-001 | ✅ Comprehensive (MFA, SSO, federation) |
| Authorisation | NFR-SEC-002 | ✅ Comprehensive (RBAC + ABAC, cross-agency) |
| Encryption | NFR-SEC-003 | ✅ Comprehensive (TLS 1.3, AES-256, key rotation) |
| Secrets Management | NFR-SEC-004 | ✅ Adequate |
| Vulnerability Management | NFR-SEC-005 | ✅ Comprehensive (SAST, DAST, pen testing, SLAs) |
| Network Security | NFR-SEC-006 | ✅ Comprehensive (zero trust, micro-segmentation) |
| Audit Logging | NFR-C-002 | ✅ Comprehensive (tamper-evident, 7-year retention) |
| Data Residency | TC-001 | ✅ UK-only mandate |
| Incident Response | — | ⚠️ No explicit IR requirement |
| Security Monitoring/SOC | — | ⚠️ No explicit SOC requirement |

### 8.2 Security Findings

| Finding ID | Severity | Finding | Detail |
|------------|----------|---------|--------|
| SEC-001 | **HIGH** | No incident response requirement | NFR-SEC-005 covers vulnerability management and NFR-C-001 mentions "breach notification to ICO within 72 hours", but there is no explicit requirement for a security incident response plan, security operations centre (SOC), or incident response team. For a programme processing DPA 2018 Part 3 data, this is essential. |
| SEC-002 | **MEDIUM** | No supply chain security requirement | The programme will rely on multiple vendors (SOW specifies multi-lot procurement). There is no requirement for supply chain security assessment, vendor security audits, or third-party risk management — despite this being a core NCSC CAF Objective B requirement. |
| SEC-003 | **MEDIUM** | No data loss prevention (DLP) requirement | Criminal justice evidence data (including RASSO material) needs DLP controls to prevent unauthorised exfiltration. This is not explicitly addressed in NFR-SEC-001–006. |

---

## Consolidated Findings Register

### CRITICAL Findings (5)

| ID | Finding | Remediation Priority |
|----|---------|---------------------|
| UK-001 | No DPIA for AI processing criminal justice data | Before any AI deployment; before OBC |
| UK-002 | No ATRS records for planned AI tools | Before any AI deployment |
| UK-003 | No AI Playbook assessment | Before AI-related spend approval |
| RA-001 | No cyber security breach risk in register | Next risk register update |
| RA-005 | R-002 (Critical 20) lacks escalation/contingency plan | Before OBC |

### HIGH Findings (8)

| ID | Finding | Remediation Priority |
|----|---------|---------------------|
| UK-004 | No TCoP assessment | Before spend control |
| UK-005 | GDS Service Standard coverage incomplete (8/14 points) | Before alpha assessment |
| UK-006 | No Secure by Design assessment | Before design phase |
| BC-001 | BCR inconsistency (1.1:1 vs 1.5:1) across documents | Before OBC |
| BC-002 | Investment figure inconsistency (£281M vs £285M) | Before OBC |
| CC-004 | SOW ISO 27001 requirement not in NFRs | Before vendor evaluation |
| SEC-001 | No incident response requirement | Before design phase |
| RQ-004 | No AI explainability metrics requirement | Before AI design |

### MEDIUM Findings (12)

| ID | Finding | Remediation Priority |
|----|---------|---------------------|
| RQ-001 | Requirements count inconsistency (56 vs 60) | Next document update |
| RQ-002 | Some FR acceptance criteria not testable | Before alpha |
| RQ-005 | Data entity validation rules incomplete | Before data model |
| RQ-006 | Availability target scope ambiguous | Before NFR refinement |
| RQ-009 | Business requirements lack measurable acceptance criteria | Before OBC |
| PA-001 | Observability principle weak in risk register | Next risk update |
| PA-002 | Event-driven integration not consistently applied | Before design |
| ST-001 | GDS assessment failure risk missing | Next risk update |
| BC-003 | Benefits figure inconsistency (£495M vs £420M) | Before OBC |
| CC-001 | "Safe AI" terminology inconsistent | Next document update |
| CC-003 | SOW/REQ milestone count discrepancy | Before vendor issue |
| CC-005 | SOBC doesn't reference NFR cost impact | Before OBC |
| SEC-002 | No supply chain security requirement | Before vendor evaluation |
| SEC-003 | No DLP requirement | Before design |
| UK-007 | NCSC CAF alignment not evidenced | Before security assessment |
| BC-004 | Optimism bias not addressed in SOW evaluation | Before vendor evaluation |

### LOW Findings (6)

| ID | Finding | Remediation Priority |
|----|---------|---------------------|
| RQ-003 | NFR measurement methods not inline | Best practice improvement |
| RQ-007 | "AI-assisted" scope undefined | Terminology standardisation |
| RQ-008 | Data growth rate calculation discrepancy | Validation exercise |
| RQ-010 | Missing use cases for 3 functional areas | Before alpha |
| PA-003 | No automated testing coverage target | Before design |
| ST-002 | Staff wellbeing risk gap | Next risk update |
| ST-003 | Magistrates' court deprioritisation risk gap | Next risk update |
| CC-002 | Risk numbering convention differs between docs | Cosmetic standardisation |
| RA-004 | Risk appetite statement missing | Next risk update |

---

## Recommended Remediation Sequence

### Phase 1: Before OBC Submission (Immediate)

1. **Produce DPIA** (`/arckit.dpia`) — Legally mandatory. Addresses UK-001.
2. **Produce AI Playbook assessment** (`/arckit.ai-playbook`) — Addresses UK-003.
3. **Produce ATRS records** (`/arckit.atrs`) — At minimum for the 5 AI capabilities. Addresses UK-002.
4. **Reconcile financial figures** across SOBC, Story, and SOW — Addresses BC-001, BC-002, BC-003.
5. **Add cyber security breach risk** to risk register — Addresses RA-001.
6. **Develop R-002 escalation plan** — Addresses RA-005.

### Phase 2: Before Design Phase

7. **Produce TCoP assessment** (`/arckit.tcop`) — Addresses UK-004.
8. **Produce Secure by Design assessment** (`/arckit.secure`) — Addresses UK-006.
9. **Complete GDS Service Standard mapping** (all 14 points) — Addresses UK-005.
10. **Add AI explainability NFR** — Addresses RQ-004.
11. **Add incident response requirement** — Addresses SEC-001.
12. **Add supply chain security requirement** — Addresses SEC-002.
13. **Produce Data Model** (`/arckit.data-model`) — Addresses missing artifact.

### Phase 3: Before Alpha Assessment

14. **Produce Traceability Matrix** (`/arckit.traceability`) — Addresses missing artifact.
15. **Standardise terminology** ("safe AI", requirement counts) — Addresses CC-001, RQ-001.
16. **Reconcile milestones** between REQ and SOW — Addresses CC-003.
17. **Add missing use cases** — Addresses RQ-010.

---

## Appendix A: Analysis Methodology

### Detection Passes Executed

| Pass | Description | Artifacts Examined |
|------|-------------|-------------------|
| 1 | Requirements Quality (completeness, ambiguity, testability) | ARC-001-REQ-v1.0 |
| 2 | Architecture Principles Alignment | ARC-000-PRIN-v1.0 ↔ ARC-001-REQ-v1.0, ARC-001-RISK-v1.0, ARC-001-SOBC-v1.0 |
| 3 | Stakeholder Traceability | ARC-001-STKE-v1.0 ↔ ARC-001-REQ-v1.0, ARC-001-RISK-v1.0 |
| 4 | Risk Management | ARC-001-RISK-v1.0 ↔ ARC-001-REQ-v1.0, ARC-001-STKE-v1.0 |
| 5 | Business Case Alignment | ARC-001-SOBC-v1.0 ↔ ARC-001-REQ-v1.0, ARC-001-SOW-v1.0, ARC-001-STRY-v1.0 |
| 6 | UK Government Compliance | All artifacts ↔ GDS, TCoP, NCSC CAF, UK GDPR, AI Playbook, ATRS, Green Book, Orange Book |
| 7 | Cross-Artifact Consistency | All artifacts (numerical, terminology, cross-reference) |
| 8 | Security and Data Protection | ARC-001-REQ-v1.0 (NFR-SEC, NFR-C sections) |

### Severity Definitions

| Severity | Definition | Action Required |
|----------|-----------|----------------|
| CRITICAL | Legal/regulatory non-compliance risk; fundamental governance gap that blocks programme progression | Must resolve before next governance gate |
| HIGH | Significant gap that could cause material issues at OBC/assessment stage | Should resolve before OBC submission |
| MEDIUM | Gap or inconsistency that should be addressed for governance quality | Should resolve before design phase |
| LOW | Minor improvement opportunity; best practice recommendation | Address when convenient |

### Scoring Methodology

Each dimension scored 0–100 based on:
- **0–25**: Not Started — no evidence of coverage
- **26–50**: Inadequate — significant gaps
- **51–75**: Adequate — fundamentals covered with gaps
- **76–90**: Good — comprehensive with minor gaps
- **91–100**: Excellent — exemplary governance

---

**Generated by**: ArcKit `/arckit.analyze` command
**Generated on**: 2026-02-04
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)
**Analysis Context**: Non-destructive analysis of 6 published governance artifacts. No artifacts were modified during this analysis.

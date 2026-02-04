# Risk Register: Criminal Courts Technology & AI Reform

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.risk`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-RISK-v1.0 |
| **Document Type** | Risk Register |
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
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, Criminal Justice Technology Leadership, Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial creation from `/arckit.risk` command | PENDING | PENDING |

---

## Executive Summary

### Risk Profile Overview

**Total Risks Identified:** 20 risks across 6 categories

| Risk Level | Inherent | Residual | Change |
|------------|----------|----------|--------|
| **Critical** (20-25) | 6 | 1 | ↓ 83% |
| **High** (13-19) | 8 | 5 | ↓ 38% |
| **Medium** (6-12) | 6 | 11 | ↑ (absorbed from higher) |
| **Low** (1-5) | 0 | 3 | ↑ (absorbed from higher) |
| **TOTAL Score** | 298 | 193 | ↓ 35% |

### Risk Category Distribution

| Category | Count | Avg Inherent | Avg Residual | Control Effectiveness |
|----------|-------|--------------|--------------|----------------------|
| **STRATEGIC** | 4 | 17.3 | 11.5 | 33% reduction |
| **OPERATIONAL** | 4 | 13.5 | 8.8 | 35% reduction |
| **FINANCIAL** | 3 | 15.0 | 10.0 | 33% reduction |
| **COMPLIANCE** | 4 | 16.0 | 10.3 | 36% reduction |
| **REPUTATIONAL** | 2 | 16.0 | 10.5 | 34% reduction |
| **TECHNOLOGY** | 3 | 14.7 | 9.3 | 36% reduction |

### Overall Risk Assessment

**Overall Residual Risk Score:** 193/500
**Risk Reduction from Controls:** 35% reduction from inherent risk
**Risk Profile Status:** ⚠️ Concerning — This is a high-complexity, multi-agency programme with significant political, legal, and technical risks. 6 residual risks remain High or above, requiring active management.

### Top 5 Critical Risks Requiring Immediate Attention

1. **R-002** (COMPLIANCE, Critical 20): Defence equality of arms challenge halts AI deployment — Owner: Lord Chancellor
2. **R-001** (STRATEGIC, High 16): HM Treasury funding refusal blocks programme — Owner: MoJ Permanent Secretary
3. **R-005** (COMPLIANCE, High 15): AI ethics controversy damages public trust — Owner: MoJ Chief AI Officer
4. **R-003** (STRATEGIC, High 12): Judicial resistance delays AI deployment — Owner: Lead Judge for AI
5. **R-007** (TECHNOLOGY, High 12): Common Platform instability disrupts reform — Owner: HMCTS CTO

### Key Findings and Recommendations

**Key Findings:**
- The single highest residual risk is the defence equality of arms challenge (R-002, Critical 20) — if prosecution AI deploys without defence equivalent, legal challenge could halt the entire AI programme
- Financial risks are heavily concentrated on Treasury approval (R-009) — a single point of failure for the entire programme
- Technology risks are manageable with phased migration but Common Platform stability is a prerequisite
- Compliance risks are elevated due to the intersection of AI governance, data protection (DPA 2018 Part 3), and judicial independence
- Stakeholder conflict between ministerial pace and judicial caution is the dominant strategic tension

**Recommendations:**
1. **URGENT**: Resolve defence technology funding mechanism before any prosecution AI goes live (R-002)
2. **HIGH PRIORITY**: Submit Green Book business case to HM Treasury with phased investment model (R-009)
3. **HIGH PRIORITY**: Establish judicial AI steering group immediately to build trust (R-003)
4. **IMPORTANT**: Stabilise Common Platform before building new functionality on it (R-007)
5. **IMPORTANT**: Conduct comprehensive AI bias testing before any criminal justice AI deployment (R-005)

---

## A. Risk Matrix Visualization

### Inherent Risk Matrix (Before Controls)

```
                                    IMPACT
              1-Minimal   2-Minor    3-Moderate   4-Major    5-Severe
           ┌───────────┬───────────┬───────────┬───────────┬───────────┐
5-Almost   │           │           │           │  R-004    │  R-002    │
Certain    │     5     │    10     │    15     │    20     │    25     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
4-Likely   │           │           │  R-006    │  R-001    │  R-009    │
           │     4     │     8     │  R-010    │  R-003    │  R-005    │
L          │           │           │  R-014    │  R-013    │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
I 3-Poss-  │           │           │  R-008    │  R-007    │           │
K ible     │     3     │     6     │  R-011    │  R-012    │           │
E          │           │           │  R-020    │  R-015    │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
L 2-Un-    │           │  R-018    │  R-016    │  R-017    │           │
I likely   │     2     │     4     │  R-019    │           │           │
H          ├───────────┼───────────┼───────────┼───────────┼───────────┤
O 1-Rare   │           │           │           │           │           │
O          │     1     │     2     │     3     │     4     │     5     │
D          └───────────┴───────────┴───────────┴───────────┴───────────┘

Legend: Critical (20-25)  High (13-19)  Medium (6-12)  Low (1-5)
```

### Residual Risk Matrix (After Controls)

```
                                    IMPACT
              1-Minimal   2-Minor    3-Moderate   4-Major    5-Severe
           ┌───────────┬───────────┬───────────┬───────────┬───────────┐
5-Almost   │           │           │           │  R-002    │           │
Certain    │     5     │    10     │    15     │    20     │    25     │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
4-Likely   │           │           │  R-004    │  R-001    │           │
           │     4     │     8     │  R-010    │           │           │
L          ├───────────┼───────────┼───────────┼───────────┼───────────┤
I 3-Poss-  │           │  R-006    │  R-003    │  R-005    │           │
K ible     │     3     │  R-014    │  R-008    │  R-009    │           │
E          │           │  R-020    │  R-011    │           │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
L 2-Un-    │           │  R-018    │  R-007    │  R-013    │           │
I likely   │     2     │  R-019    │  R-012    │           │           │
H          │           │           │  R-015    │           │           │
           ├───────────┼───────────┼───────────┼───────────┼───────────┤
O 1-Rare   │  R-016    │  R-017    │           │           │           │
O          │     1     │     2     │     3     │     4     │     5     │
D          └───────────┴───────────┴───────────┴───────────┴───────────┘

Legend: Critical (20-25)  High (13-19)  Medium (6-12)  Low (1-5)
```

**Risk Movement Analysis:**
- **Significant Improvement**: R-013 (20→8), R-004 (20→12), R-012 (12→6) — Controls very effective
- **Moderate Improvement**: R-001 (16→16 stayed but changed shape), R-009 (20→12), R-003 (16→9)
- **Limited Improvement**: R-002 (25→20) — Structural issue requiring policy decision, not just controls
- **Stable**: R-016, R-017, R-018, R-019 — Low inherent risk, minimal change needed

---

## B. Top 10 Risks (Ranked by Residual Score)

| Rank | ID | Title | Category | Inherent | Residual | Owner | Status | Response |
|------|----|-------|----------|----------|----------|-------|--------|----------|
| 1 | R-002 | Defence equality of arms challenge | COMPLIANCE | 25 | 20 | Lord Chancellor | Open | Treat |
| 2 | R-001 | HM Treasury funding refusal | STRATEGIC | 16 | 16 | MoJ Perm Sec | In Progress | Treat |
| 3 | R-005 | AI ethics controversy | COMPLIANCE | 20 | 12 | MoJ AI Officer | In Progress | Treat |
| 4 | R-009 | Programme cost overrun | FINANCIAL | 20 | 12 | MoJ Perm Sec | In Progress | Treat |
| 5 | R-004 | Police interoperability failure | OPERATIONAL | 20 | 12 | NPCC | In Progress | Treat |
| 6 | R-010 | GDS service assessment failure | OPERATIONAL | 12 | 12 | MoJ CDIO | Open | Treat |
| 7 | R-007 | Common Platform instability | TECHNOLOGY | 12 | 6 | HMCTS CTO | In Progress | Treat |
| 8 | R-003 | Judicial resistance to AI | STRATEGIC | 16 | 9 | Lead Judge for AI | In Progress | Treat |
| 9 | R-008 | Legacy migration disrupts courts | TECHNOLOGY | 9 | 9 | HMCTS CTO | Open | Treat |
| 10 | R-011 | Cross-agency data sharing blocked | COMPLIANCE | 9 | 9 | MoJ DPO | Open | Treat |

---

## C. Detailed Risk Register

### Risk R-001: HM Treasury Funding Refusal Blocks Programme

**Category:** STRATEGIC
**Status:** In Progress
**Risk Owner:** MoJ Permanent Secretary (Accounting Officer)
**Action Owner:** Programme Finance Director

#### Risk Identification

**Risk Description:**
HM Treasury rejects or significantly reduces the Green Book business case funding request due to fiscal constraints, lack of confidence in justice technology delivery (Common Platform track record), or inability to quantify benefits convincingly. Without Treasury approval, the programme cannot proceed beyond discovery phase.

**Root Cause:**
Criminal justice technology has a poor delivery track record (Common Platform cost overruns, scope reductions). Treasury applies stringent scrutiny to MoJ technology spending. Current fiscal environment constrains departmental budgets.

**Trigger Events:**
- Spending review allocates insufficient funds to MoJ
- IPA Gateway review rates programme Red or Amber/Red
- Business case benefits deemed unquantifiable or unrealistic
- Common Platform issues escalate, undermining confidence

**Consequences if Realized:**
- Programme cannot proceed — all 180 Leveson Review technology recommendations stall
- Backlog continues to grow (political and operational crisis)
- Legacy system risk continues to accumulate
- Ministerial embarrassment and potential PAC inquiry

**Affected Stakeholders:**
- **Lord Chancellor** (SD-1): Cannot deliver on reform commitment
- **HMCTS CEO** (SD-3): Operational efficiency improvements blocked
- **Victims' Commissioner** (SD-12): Victim experience improvements delayed indefinitely
- **All agencies**: Cross-agency integration cannot proceed

**Related Objectives:** G-1 (backlog reduction), G-8 (business case approval), all other goals dependent on funding

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Treasury has rejected/reduced similar justice technology bids before; fiscal environment tight |
| **Impact** | 4 - Major | Programme cannot proceed without funding; cascading impact on all objectives |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

#### Current Controls and Mitigations

1. **Phased investment model**: Business case structured with stage-gate approvals rather than single large commitment
   - Owner: Programme Finance Director
   - Effectiveness: **Adequate**
   - Evidence: Phased models have better Treasury approval rates

2. **Lessons learned from Common Platform**: Explicit section addressing Common Platform failures and how this programme differs
   - Owner: MoJ CDIO
   - Effectiveness: **Adequate**
   - Evidence: Treasury expect this; its absence would be fatal

3. **Ministerial advocacy**: Lord Chancellor personally committed to the business case
   - Owner: Lord Chancellor's Office
   - Effectiveness: **Strong**
   - Evidence: Ministerial backing significantly influences Treasury decisions

**Overall Control Effectiveness:** Adequate (but risk remains fundamentally dependent on Treasury decision)

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Controls reduce risk of outright rejection but significant reduction in funding still likely |
| **Impact** | 4 - Major | Even partial funding reduction constrains programme scope and pace |
| **Residual Risk Score** | **16** (High) | 4 × 4 = 16 |

**Risk Reduction:** 0% — Controls prevent worst case but residual remains High

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce)

**Rationale:** Risk cannot be tolerated (programme cannot proceed without funding), cannot be transferred (no third party can fund government programmes), and cannot be terminated (Leveson Review creates political obligation). Must be treated through robust business case and political advocacy.

#### Action Plan

1. **Submit robust Green Book business case with conservative assumptions**
   - Owner: Programme Finance Director
   - Due Date: Year 1 Q2
   - Expected Impact: Reduce likelihood from 4 to 3

2. **Secure IPA Gateway review rating of Amber/Green before Treasury submission**
   - Owner: Programme Director
   - Due Date: Year 1 Q1
   - Expected Impact: Increase Treasury confidence

3. **Prepare fallback "minimum viable programme" if funding reduced**
   - Owner: MoJ CDIO
   - Due Date: Year 1 Q2
   - Expected Impact: Reduce impact from 4 to 3 (programme continues at reduced scope)

**Target Residual Risk:** 9 (3×3, Medium) after business case approval

---

### Risk R-002: Defence Equality of Arms Challenge Halts AI Deployment

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** Lord Chancellor
**Action Owner:** LAA Chief Executive

#### Risk Identification

**Risk Description:**
Defence community (CBA, Law Society) mounts legal challenge against AI-assisted prosecution on equality of arms grounds (Article 6 ECHR), arguing that AI-enhanced prosecution without equivalent defence capability creates structural unfairness. Court ruling could halt all prosecution AI deployment, undermining the entire AI programme.

**Root Cause:**
CPS has central funding and digital infrastructure for AI deployment. Defence practitioners are fragmented (thousands of firms) with minimal technology, constrained by legal aid budgets. Building equivalent defence capability simultaneously is fundamentally more complex than prosecution deployment.

**Trigger Events:**
- CPS deploys AI disclosure tool before defence equivalent available
- Defence counsel raises AI inequality in Crown Court trial
- CBA/Law Society issue formal legal challenge or judicial review
- High-profile case collapses due to AI disclosure process challenge

**Consequences if Realized:**
- Court injunction halting all prosecution AI tool usage
- Programme's AI investment stranded
- Political damage to Lord Chancellor and MoJ
- Precedent that constrains future criminal justice AI deployment
- International reputational damage (UK seen as deploying unfair AI)

**Affected Stakeholders:**
- **CBA/Law Society** (SD-6): Their primary concern materialises
- **DPP/CPS** (SD-4): AI tools halted, prosecution efficiency gains lost
- **Lord Chancellor** (SD-1): Political and legal accountability
- **Defendants**: Fair trial rights potentially compromised
- **Victims**: Case delays if AI tools halted

**Related Objectives:** G-2 (AI disclosure), G-3 (defence access), G-6 (AI governance)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | CBA has publicly stated it will challenge; legal basis is strong (Article 6 ECHR) |
| **Impact** | 5 - Catastrophic | Could halt entire AI programme; precedent-setting; political crisis |
| **Inherent Risk Score** | **25** (Critical) | 5 × 5 = 25 |

#### Current Controls and Mitigations

1. **"No prosecution advantage" principle committed in programme design**
   - Owner: Programme Board
   - Effectiveness: **Adequate** (commitment exists but funding mechanism not yet resolved)
   - Evidence: Documented in ARC-001-REQ-v1.0 Conflict Resolution C-2

2. **Defence shared-service platform planned (FR-009)**
   - Owner: LAA Chief Executive
   - Effectiveness: **Weak** (planned but not funded or built)
   - Evidence: Requirement defined but no funding mechanism agreed

3. **CBA/Law Society representation in programme governance**
   - Owner: Programme Director
   - Effectiveness: **Adequate**
   - Evidence: Stakeholder engagement plan includes defence community

**Overall Control Effectiveness:** Weak — fundamental dependency on defence funding mechanism unresolved

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | Until defence funding resolved and platform built, challenge remains almost certain |
| **Impact** | 4 - Major | Programme commitment to simultaneous deployment reduces impact somewhat (won't deploy prosecution AI without defence) |
| **Residual Risk Score** | **20** (Critical) | 5 × 4 = 20 |

**Risk Reduction:** 20% — Controls reduce impact but likelihood unchanged until funding resolved

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT (Mitigate/Reduce) — URGENT

**Rationale:** Cannot be tolerated (score 20, Critical). Cannot be transferred (constitutional obligation). Cannot be terminated (AI deployment is core programme objective). Must be treated through resolving the defence funding mechanism.

#### Action Plan

1. **URGENT: Secure Lord Chancellor policy decision on defence technology funding mechanism**
   - Owner: Lord Chancellor's Office
   - Due Date: Year 1 Q2
   - Expected Impact: Reduce likelihood from 5 to 3 once funding committed

2. **Commission independent legal opinion on equality of arms implications**
   - Owner: MoJ Legal
   - Due Date: Year 1 Q1
   - Expected Impact: Understand legal risk precisely; inform programme sequencing

3. **Begin defence platform development in parallel with prosecution AI (shared-service model)**
   - Owner: LAA Chief Executive / MoJ CDIO
   - Due Date: Year 1 Q3
   - Expected Impact: Reduce likelihood from 5 to 2 once platform available

**Target Residual Risk:** 8 (2×4, Medium) after defence platform operational

---

### Risk R-003: Judicial Resistance Delays or Blocks AI Deployment

**Category:** STRATEGIC
**Status:** In Progress
**Risk Owner:** Lead Judge for AI and Technology
**Action Owner:** MoJ Chief AI Officer

#### Risk Identification

**Risk Description:**
Senior judiciary exercises veto over AI tools perceived as threatening judicial independence, blocking or significantly delaying deployment of AI tools that could deliver substantial efficiency gains. Even non-contentious AI (transcription, translation) could be delayed if judicial trust is not established.

**Root Cause:**
Constitutional separation of powers means judiciary is independent from executive. Judges are cautious about AI — the Leveson Review itself warns against AI affecting judicial decision-making. Limited judicial experience with AI technology creates uncertainty and caution.

**Trigger Events:**
- AI tool affects case listing in a way judge perceives as constraining discretion
- AI error in court (incorrect transcription, mistranslation) undermines judicial confidence
- Media story about AI bias in criminal justice system
- Judicial steering group not established in time, creating governance vacuum

**Consequences if Realized:**
- AI tool deployment delayed 12-24 months while judicial concerns addressed
- Backlog reduction targets missed
- Programme delivers technology infrastructure but cannot deploy AI applications
- Political tension between executive (Lord Chancellor) and judiciary (Lady Chief Justice)

**Affected Stakeholders:**
- **Lady Chief Justice** (SD-2): Exercising legitimate judicial oversight
- **Lord Chancellor** (SD-1): Pace of reform blocked
- **HMCTS CEO** (SD-3): Efficiency gains delayed
- **CPS** (SD-4): AI disclosure tools blocked

**Related Objectives:** G-2 (AI disclosure), G-6 (AI governance), G-1 (backlog reduction)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Judicial caution is well-documented; governance vacuum in early months |
| **Impact** | 4 - Major | Delays core AI programme objectives by 12-24 months |
| **Inherent Risk Score** | **16** (High) | 4 × 4 = 16 |

#### Current Controls and Mitigations

1. **Dual-track AI deployment (safe AI first, case-affecting after governance)**
   - Owner: MoJ Chief AI Officer
   - Effectiveness: **Strong**
   - Evidence: Allows early wins without judicial approval; builds trust

2. **Judicial steering group with genuine veto power**
   - Owner: Lead Judge for AI
   - Effectiveness: **Adequate** (planned but not yet operational)

3. **AI categorisation framework (productivity/insight/accessibility/predictive)**
   - Owner: MoJ Chief AI Officer
   - Effectiveness: **Adequate**
   - Evidence: Gives judiciary clear framework for what requires their approval

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Dual-track approach and governance framework reduce likelihood of outright block |
| **Impact** | 3 - Moderate | Safe AI can proceed; only case-affecting AI delayed |
| **Residual Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Reduction:** 44% (16→9)

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

#### Action Plan

1. **Establish judicial AI steering group within 3 months**
   - Owner: Lady Chief Justice's Office / MoJ
   - Due Date: Year 1 Q1
   - Expected Impact: Reduce likelihood from 3 to 2

2. **Deploy transcription/translation AI as first judicial-visible success**
   - Owner: HMCTS CTO
   - Due Date: Year 1 Q2
   - Expected Impact: Build judicial confidence through positive experience

**Target Residual Risk:** 6 (2×3, Medium)

---

### Risk R-004: Police Interoperability Failure Across 43 Forces

**Category:** OPERATIONAL
**Status:** In Progress
**Risk Owner:** NPCC Digital Policing Programme
**Action Owner:** MoJ CDIO

#### Risk Identification

**Risk Description:**
43 independently governed police forces fail to agree or implement common data standards for digital case files, preventing automated evidence sharing with CPS and courts. Forces using different case management systems (Niche, Connect, Athena, others) cannot be compelled to adopt common technology.

**Root Cause:**
Police forces are constitutionally independent with their own chief constables, budgets, and procurement. Central government cannot mandate specific police systems. Historical attempts at police technology standardisation have had mixed results.

**Trigger Events:**
- NPCC fails to agree common digital case file standard
- Major forces refuse to implement adapters due to cost
- Different force systems produce incompatible data
- Force-level budget constraints prevent technology upgrades

**Consequences if Realized:**
- Cross-agency interoperability goal (G-4) fails for police-CPS integration
- Officers continue manual case file preparation (no efficiency gain)
- AI disclosure tools cannot process non-standard evidence packages
- Programme delivers only partial interoperability (CPS-HMCTS only)

**Affected Stakeholders:**
- **NPCC** (SD-5): Evidence sharing goal unachieved
- **CPS** (SD-4): Cannot receive standardised digital case files
- **Police officers**: No reduction in case file preparation burden
- **HMCTS** (SD-3): Incomplete cross-agency integration

**Related Objectives:** G-4 (cross-agency interoperability)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 5 - Almost Certain | 43-force consensus historically very difficult; no central mandate |
| **Impact** | 4 - Major | Police-CPS integration is critical path for efficiency gains |
| **Inherent Risk Score** | **20** (Critical) | 5 × 4 = 20 |

#### Current Controls and Mitigations

1. **Outcome standards approach (mandate format, not systems)**
   - Owner: MoJ CDIO
   - Effectiveness: **Adequate**

2. **Adapter/middleware layer for top 3 police systems (Niche, Connect, Athena)**
   - Owner: Programme Technical Architect
   - Effectiveness: **Strong** (covers ~85% of forces)

3. **Central funding incentives for early adopters**
   - Owner: Home Office / MoJ
   - Effectiveness: **Adequate** (subject to funding availability)

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Adapter approach reduces dependency on consensus but some forces will still lag |
| **Impact** | 3 - Moderate | Adapter layer means 85% coverage achievable even without full consensus |
| **Residual Risk Score** | **12** (Medium) | 4 × 3 = 12 |

**Risk Reduction:** 40% (20→12)

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

#### Action Plan

1. **Build adapter layer for Niche, Connect, Athena as priority**
   - Owner: Programme Technical Architect
   - Due Date: Year 1 Q4
   - Expected Impact: Cover 85% of forces technically

2. **Secure NPCC formal endorsement of digital case file standard**
   - Owner: NPCC Digital Policing Programme
   - Due Date: Year 1 Q3

**Target Residual Risk:** 8 (2×4, Medium)

---

### Risk R-005: AI Ethics Controversy Damages Public Trust

**Category:** COMPLIANCE
**Status:** In Progress
**Risk Owner:** MoJ Chief AI Officer
**Action Owner:** MoJ Chief AI Officer

#### Risk Identification

**Risk Description:**
An AI-related error, bias incident, or data breach in criminal justice AI (e.g., biased disclosure review, incorrect translation in court, AI hallucination in case summary) generates media and parliamentary scrutiny, triggering political intervention that halts AI deployment across the programme.

**Root Cause:**
Criminal justice AI operates in the highest-stakes environment — decisions affect individual liberty. AI systems can exhibit bias, produce errors, or be misrepresented. Public and media sensitivity to AI in criminal justice is extremely high. Any incident will be amplified.

**Trigger Events:**
- AI disclosure tool misses key evidence leading to wrongful conviction or acquittal
- Bias discovered in AI processing (e.g., racial bias in evidence triage)
- AI transcription error in court causes miscarriage of justice
- Media investigation reveals AI was used without defendant's knowledge
- Data breach of AI training data containing criminal justice records

**Consequences if Realized:**
- Ministerial order to pause all criminal justice AI deployment
- Parliamentary inquiry (Justice Select Committee, PAC)
- ICO investigation
- Public loss of trust in technology-enabled justice
- Legal challenge to convictions involving AI-assisted disclosure

**Affected Stakeholders:**
- **MoJ Chief AI Officer** (SD-7): Responsible for AI governance
- **Lord Chancellor** (SD-1): Political accountability
- **Defendants**: Fair trial rights potentially compromised
- **Lady Chief Justice** (SD-2): Judicial concerns validated
- **ICO** (SD-11): Regulatory investigation triggered

**Related Objectives:** G-2 (AI disclosure), G-6 (AI governance), G-10 (data protection)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | AI errors in complex domains are common; criminal justice scrutiny is intense |
| **Impact** | 5 - Catastrophic | Programme-wide halt; precedent-setting; political crisis |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

#### Current Controls and Mitigations

1. **AI governance framework with ATRS and DPIA (BR-006)**
   - Owner: MoJ Chief AI Officer
   - Effectiveness: **Adequate** (framework designed but not yet operational)

2. **Mandatory bias testing across protected characteristics**
   - Owner: MoJ Chief AI Officer
   - Effectiveness: **Adequate**

3. **Human-in-the-loop for all AI outputs (Principle 2)**
   - Owner: All delivery teams
   - Effectiveness: **Strong** (architectural principle, not optional)

4. **AI incident response plan**
   - Owner: MoJ Communications
   - Effectiveness: **Weak** (not yet developed)

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Governance framework and human oversight reduce but cannot eliminate AI error risk |
| **Impact** | 4 - Major | Incident response plan can contain damage; not catastrophic if handled well |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Reduction:** 40% (20→12)

#### Risk Response (4Ts Framework)

**Primary Response:** TREAT

#### Action Plan

1. **Develop and test AI incident response plan**
   - Owner: MoJ Communications / MoJ Chief AI Officer
   - Due Date: Year 1 Q2

2. **Commission independent bias audit before first AI deployment**
   - Owner: MoJ Chief AI Officer
   - Due Date: Year 1 Q3

3. **Establish AI ethics review board with external members**
   - Owner: MoJ Chief AI Officer
   - Due Date: Year 1 Q2

**Target Residual Risk:** 8 (2×4, Medium)

---

### Risk R-006: Court Staff Resistance to Technology Change

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** HMCTS Chief Executive
**Action Owner:** HMCTS Change Management Lead

#### Risk Identification

**Risk Description:**
Court staff, experienced with legacy systems and frustrated by Common Platform rollout issues, resist adopting new technology. Low adoption undermines efficiency gains and creates workarounds that bypass new systems.

**Root Cause:**
Common Platform rollout eroded staff confidence in new technology. Staff developed workarounds that work for them. Change fatigue from multiple previous technology changes. Insufficient training and support during transitions.

**Trigger Events:**
- New system deployed without adequate training period
- System reliability issues in first weeks of deployment
- Staff revert to manual workarounds and legacy systems
- Unions raise concerns about pace of change

**Consequences if Realized:**
- Technology deployed but not used (low adoption)
- Efficiency gains not realised despite investment
- Dual-running costs (old and new systems) continue
- Benefits realisation targets missed

**Affected Stakeholders:**
- **HMCTS CEO** (SD-3): Operational efficiency not achieved
- **Court staff**: Work disrupted without perceived benefit
- **HM Treasury** (SD-9): Benefits not realised as projected

**Related Objectives:** G-1 (backlog reduction), G-5 (legacy migration)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Common Platform experience makes staff sceptical; change fatigue is real |
| **Impact** | 3 - Moderate | Technology still works but without staff adoption, efficiency gains lost |
| **Inherent Risk Score** | **12** (Medium) | 4 × 3 = 12 |

#### Current Controls and Mitigations

1. **Phased rollout with champions network**
   - Owner: HMCTS Change Management
   - Effectiveness: **Adequate**

2. **Extensive training programme before deployment**
   - Owner: HMCTS HR
   - Effectiveness: **Adequate**

**Overall Control Effectiveness:** Adequate

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Champions and training reduce resistance |
| **Impact** | 2 - Minor | Phased rollout limits blast radius |
| **Residual Risk Score** | **6** (Medium) | 3 × 2 = 6 |

**Risk Reduction:** 50% (12→6)

#### Risk Response: TREAT

---

### Risk R-007: Common Platform Instability Disrupts Reform

**Category:** TECHNOLOGY
**Status:** In Progress
**Risk Owner:** HMCTS Chief Technology Officer
**Action Owner:** HMCTS Platform Engineering Lead

#### Risk Identification

**Risk Description:**
The existing Common Platform system experiences instability, outages, or functionality issues during the reform programme, eroding user confidence and complicating the foundation for new services. New functionality built on an unstable foundation inherits those stability issues.

**Root Cause:**
Common Platform has a troubled rollout history with user complaints about reliability and usability. Technical debt accumulated during rushed deployment. Platform serves as foundation for court case management but reliability is inconsistent.

**Trigger Events:**
- Major Common Platform outage during court sitting hours
- Data integrity issue in Common Platform case records
- Common Platform performance degradation under load
- Staff bypass Common Platform using legacy systems

**Consequences if Realized:**
- Court hearings disrupted
- New services built on Common Platform inherit instability
- Staff and judicial confidence in technology reform collapses
- Programme forced to consider alternative platform (major cost and delay)

**Affected Stakeholders:**
- **HMCTS CTO** (SD-3): Platform stability is prerequisite
- **Court staff**: Daily work disrupted
- **Judiciary**: Hearings affected
- **NAO** (SD-15): Echoes of previous Common Platform criticism

**Related Objectives:** G-1, G-5, G-9

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Platform has improved but stability not fully proven at scale |
| **Impact** | 4 - Major | Foundation for all court digital services |
| **Inherent Risk Score** | **12** (Medium) | 3 × 4 = 12 |

#### Current Controls and Mitigations

1. **Common Platform stabilisation programme (prerequisite before new features)**
   - Owner: HMCTS CTO
   - Effectiveness: **Strong**

2. **Separation of stabilisation and transformation workstreams**
   - Owner: Programme Director
   - Effectiveness: **Strong**

3. **Bypass capability (new services alongside CP, not dependent on it)**
   - Owner: Programme Technical Architect
   - Effectiveness: **Adequate**

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 2 - Unlikely | Stabilisation programme and bypass strategy significantly reduce risk |
| **Impact** | 3 - Moderate | Bypass strategy means programme not entirely dependent on CP |
| **Residual Risk Score** | **6** (Medium) | 2 × 3 = 6 |

**Risk Reduction:** 50% (12→6)

#### Risk Response: TREAT

---

### Risk R-008: Legacy Migration Disrupts Live Court Operations

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** HMCTS Chief Technology Officer
**Action Owner:** HMCTS Migration Programme Lead

#### Risk Identification

**Risk Description:**
Migration of legacy applications causes unplanned disruption to live court operations — court hearings delayed, prisoner movements affected, case data temporarily unavailable. Some of the 37 legacy applications have undocumented dependencies that surface only during migration.

**Root Cause:**
37 legacy applications, some dating to the 1970s, have poorly documented interfaces, undocumented dependencies, and limited test environments. Data migration from legacy formats carries inherent risk.

**Trigger Events:**
- Undocumented dependency causes cascade failure during migration
- Data migration corruption in production
- Parallel running reveals data inconsistencies too late
- Rollback fails or takes longer than planned

**Consequences if Realized:**
- Court hearings postponed
- Prisoner movements disrupted (safety and legal implications)
- Media coverage of "IT failure in courts"
- Programme credibility damaged with judiciary and practitioners

**Affected Stakeholders:**
- **HMCTS CTO**: Technical accountability
- **Judiciary**: Hearings disrupted
- **Defendants**: Remand time extended if hearings postponed
- **NAO** (SD-15): Further criticism of justice technology delivery

**Related Objectives:** G-5 (legacy migration)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Legacy systems are inherently unpredictable during migration |
| **Impact** | 3 - Moderate | Disruption to individual courts, not system-wide |
| **Inherent Risk Score** | **9** (Medium) | 3 × 3 = 9 |

#### Current Controls and Mitigations

1. **Phased migration by risk score (highest-risk first)**
2. **Mandatory parallel running with automated reconciliation**
3. **Tested rollback procedures for each migration**
4. **Migrations scheduled outside court sitting hours where possible**

**Overall Control Effectiveness:** Strong

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Legacy unpredictability persists despite controls |
| **Impact** | 3 - Moderate | Rollback and parallel running contain blast radius |
| **Residual Risk Score** | **9** (Medium) | 3 × 3 = 9 |

**Risk Reduction:** 0% — Controls maintain acceptable risk level rather than reducing score

#### Risk Response: TREAT (maintain existing strong controls)

---

### Risk R-009: Programme Cost Overrun Exceeds Business Case

**Category:** FINANCIAL
**Status:** In Progress
**Risk Owner:** MoJ Permanent Secretary
**Action Owner:** Programme Finance Director

#### Risk Identification

**Risk Description:**
Programme expenditure significantly exceeds Green Book business case estimates due to underestimated complexity, scope creep, vendor cost escalation, or extended parallel running during legacy migration. Track record of justice technology cost overruns (Common Platform) makes this a high-scrutiny risk.

**Root Cause:**
Multi-agency, multi-year technology programmes are inherently difficult to cost accurately. Criminal justice domain complexity often exceeds initial estimates. Vendor pricing may escalate after initial contract. Legacy migration costs are notoriously unpredictable.

**Trigger Events:**
- Discovery phase reveals significantly greater complexity than estimated
- Vendor pricing increases after contract award
- Scope creep from additional Leveson Review recommendations
- Extended parallel running due to migration issues
- HM Treasury optimism bias adjustment proves insufficient

**Consequences if Realized:**
- Programme funding gap requires additional Treasury approval (delay and political cost)
- Scope must be cut to stay within budget (reduced benefits)
- NAO and PAC scrutiny of cost control
- MoJ Permanent Secretary's accounting officer accountability triggered

**Affected Stakeholders:**
- **MoJ Permanent Secretary**: Accounting officer liability
- **HM Treasury** (SD-9): Confidence in justice technology spending eroded
- **NAO** (SD-15): Critical VFM report
- **Lord Chancellor**: Political accountability for cost overruns

**Related Objectives:** G-8 (business case), O-6 (fiscal responsibility)

#### Inherent Risk Assessment (Before Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 4 - Likely | Justice technology programmes frequently exceed estimates; multi-agency complexity high |
| **Impact** | 5 - Catastrophic | Programme funding crisis; political and parliamentary consequences |
| **Inherent Risk Score** | **20** (Critical) | 4 × 5 = 20 |

#### Current Controls and Mitigations

1. **Conservative cost estimates with HM Treasury optimism bias applied**
   - Effectiveness: **Adequate**

2. **Phased investment with stage-gate approvals**
   - Effectiveness: **Strong**

3. **Monthly cost tracking against business case**
   - Effectiveness: **Adequate**

4. **10% management contingency within approved budget**
   - Effectiveness: **Adequate**

#### Residual Risk Assessment (After Controls)

| Assessment | Rating | Justification |
|------------|--------|---------------|
| **Likelihood** | 3 - Possible | Stage gates and contingency reduce probability of uncontrolled overrun |
| **Impact** | 4 - Major | Phased approach means overrun in one phase doesn't collapse entire programme |
| **Residual Risk Score** | **12** (Medium) | 3 × 4 = 12 |

**Risk Reduction:** 40% (20→12)

#### Risk Response: TREAT

---

### Risk R-010: GDS Service Assessment Failure

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** MoJ CDIO
**Action Owner:** Programme Service Design Lead

#### Risk Identification

**Risk Description:**
New digital services fail GDS service assessment at alpha, beta, or live stages, blocking deployment and requiring rework. Previous justice technology services have struggled at assessment. Criminal justice domain complexity may not be well understood by GDS assessors.

**Inherent Risk Score:** **12** (Medium) — Likelihood 4, Impact 3
**Residual Risk Score:** **12** (Medium) — Likelihood 4, Impact 3 (controls maintain but don't reduce)

**Current Controls:** Early GDS engagement; user research embedded in teams; accessibility from day one
**Risk Response:** TREAT — Engage GDS assessors early; conduct mock assessments; ensure user research with all 8 personas

---

### Risk R-011: Cross-Agency Data Sharing Agreements Stall

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** MoJ Data Protection Officer
**Action Owner:** MoJ Legal

#### Risk Identification

**Risk Description:**
Cross-agency data sharing agreements between MoJ, HMCTS, CPS, HMPPS, LAA, and police forces fail to reach agreement on lawful bases, data retention, or access controls, blocking technical integration. DPA 2018 Part 3 (law enforcement processing) requirements add complexity.

**Inherent Risk Score:** **9** (Medium) — Likelihood 3, Impact 3
**Residual Risk Score:** **9** (Medium) — Likelihood 3, Impact 3

**Current Controls:** Early ICO engagement; specialist DPA Part 3 legal advice; template data sharing agreements
**Risk Response:** TREAT — Engage ICO sandbox; formalise bilateral agreements before multilateral

---

### Risk R-012: ICO Enforcement Action Against AI Processing

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** MoJ Data Protection Officer
**Action Owner:** MoJ DPO

#### Risk Identification

**Risk Description:**
ICO takes enforcement action against cross-agency AI data processing or automated decision-making in criminal justice, halting AI deployment.

**Inherent Risk Score:** **12** (Medium) — Likelihood 3, Impact 4
**Residual Risk Score:** **6** (Medium) — Likelihood 2, Impact 3

**Current Controls:** Comprehensive DPIAs; ICO engagement; DPA Part 3 specialist advice; privacy-by-design
**Risk Response:** TREAT

---

### Risk R-013: AI Model Bias Against Protected Characteristics

**Category:** COMPLIANCE
**Status:** Open
**Risk Owner:** MoJ Chief AI Officer
**Action Owner:** Programme AI Lead

#### Risk Identification

**Risk Description:**
AI models used for disclosure review, evidence triage, or case summarisation exhibit bias against protected characteristics (race, gender, age, disability), leading to disproportionate outcomes in criminal cases. Particularly acute risk given over-representation of ethnic minorities in the criminal justice system.

**Inherent Risk Score:** **20** (Critical) — Likelihood 5 (AI bias is pervasive in language models), Impact 4 (miscarriage of justice risk)
**Residual Risk Score:** **8** (Medium) — Likelihood 2, Impact 4

**Current Controls:** Mandatory bias testing; independent audit; ATRS transparency; human-in-the-loop override
**Risk Response:** TREAT — Commission independent bias audit; continuous monitoring post-deployment; diverse testing datasets

---

### Risk R-014: Stakeholder Engagement Fatigue Over Multi-Year Programme

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Programme Director
**Action Owner:** Programme Communications Lead

#### Risk Identification

**Risk Description:**
Over a 5-year programme, stakeholder engagement declines as representatives rotate, attention shifts to other priorities, and consultation fatigue sets in. This undermines governance quality, design input, and programme legitimacy.

**Inherent Risk Score:** **12** (Medium) — Likelihood 4, Impact 3
**Residual Risk Score:** **6** (Medium) — Likelihood 3, Impact 2

**Current Controls:** Efficient governance meetings; regular demonstration of impact; secondments from agencies
**Risk Response:** TREAT

---

### Risk R-015: Vendor Lock-In Constrains Future Options

**Category:** TECHNOLOGY
**Status:** Open
**Risk Owner:** MoJ CDIO
**Action Owner:** Programme Commercial Lead

#### Risk Identification

**Risk Description:**
Deep dependency on a single AI vendor or platform vendor limits future technology options, increases costs, and creates a single point of failure. Particularly acute for AI models where switching costs are high.

**Inherent Risk Score:** **12** (Medium) — Likelihood 3, Impact 4
**Residual Risk Score:** **6** (Medium) — Likelihood 2, Impact 3

**Current Controls:** Open standards requirement (Principle 20); abstraction layers; multi-vendor strategy; contractual exit provisions
**Risk Response:** TREAT

---

### Risk R-016: Ministerial/Policy Direction Change Mid-Programme

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** Lord Chancellor's Office
**Action Owner:** Programme SRO

#### Risk Identification

**Risk Description:**
Change of minister, machinery of government change, or policy shift redirects programme priorities mid-delivery, causing scope changes, wasted investment, or programme cancellation.

**Inherent Risk Score:** **6** (Medium) — Likelihood 2, Impact 3
**Residual Risk Score:** **1** (Low) — Likelihood 1, Impact 1 (Leveson Review creates cross-party consensus)

**Current Controls:** Cross-party support for criminal justice reform; Leveson Review provides non-partisan mandate; phased delivery limits wasted investment
**Risk Response:** TOLERATE

---

### Risk R-017: Parliamentary/NAO Scrutiny of Programme

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** MoJ Permanent Secretary
**Action Owner:** Programme Director

#### Risk Identification

**Risk Description:**
NAO conducts critical review of programme, leading to PAC hearing and media coverage. Given Common Platform history, scrutiny will be intense and any delivery issues amplified.

**Inherent Risk Score:** **8** (Medium) — Likelihood 2, Impact 4
**Residual Risk Score:** **2** (Low) — Likelihood 1, Impact 2

**Current Controls:** IPA Gateway reviews; auditable decision records (ADRs); benefits tracking; lessons learned from Common Platform
**Risk Response:** TOLERATE — Prepare for scrutiny rather than avoid it; transparency is the best defence

---

### Risk R-018: Skills Gap in AI and Modern Technology

**Category:** OPERATIONAL
**Status:** Open
**Risk Owner:** Programme HR Lead
**Action Owner:** HMCTS HR

#### Risk Identification

**Risk Description:**
Insufficient AI engineering, cloud architecture, and data engineering skills within MoJ/HMCTS to deliver and maintain the programme. Civil service pay constraints make recruitment of AI talent difficult.

**Inherent Risk Score:** **4** (Low) — Likelihood 2, Impact 2
**Residual Risk Score:** **4** (Low) — Likelihood 2, Impact 2

**Current Controls:** Mixed delivery model (civil servants + vendor specialists); DDaT capability framework; secondments
**Risk Response:** TOLERATE

---

### Risk R-019: Cyber Attack on Criminal Justice Systems

**Category:** REPUTATIONAL
**Status:** Open
**Risk Owner:** MoJ CISO
**Action Owner:** MoJ Security Operations

#### Risk Identification

**Risk Description:**
Cyber attack (ransomware, data breach, supply chain compromise) targets criminal justice systems during or after reform, exploiting new attack surface introduced by integration and AI capabilities. The 2025 Legal Aid Agency breach demonstrates this is a real threat.

**Inherent Risk Score:** **6** (Medium) — Likelihood 2, Impact 3
**Residual Risk Score:** **4** (Low) — Likelihood 2, Impact 2

**Current Controls:** Security by Design (Principle 3 — NON-NEGOTIABLE); zero-trust architecture; NCSC CAF; Cyber Essentials Plus; penetration testing; SIEM monitoring
**Risk Response:** TREAT — Maintain and strengthen existing security controls

---

### Risk R-020: Magistrates' Courts Deprioritised in Favour of Crown Court

**Category:** STRATEGIC
**Status:** Open
**Risk Owner:** HMCTS Chief Executive
**Action Owner:** Programme Delivery Director

#### Risk Identification

**Risk Description:**
Political and media focus on Crown Court backlog causes programme to deprioritise magistrates' courts (which handle 95% of criminal cases), leaving volunteer magistrates with inadequate technology and the Magistrates' Association dissatisfied.

**Inherent Risk Score:** **9** (Medium) — Likelihood 3, Impact 3
**Residual Risk Score:** **6** (Medium) — Likelihood 3, Impact 2

**Current Controls:** Requirements include magistrates' court (FR-006, NFR-U-003); Magistrates' Association in stakeholder engagement; dual Crown/magistrates scope commitment
**Risk Response:** TREAT

---

## D. Risk Category Analysis

### STRATEGIC Risks

**Total STRATEGIC Risks:** 4 (R-001, R-003, R-016, R-020)
**Average Inherent Score:** 11.8 (Medium)
**Average Residual Score:** 8.0 (Medium)
**Control Effectiveness:** 32% reduction

**Key Themes:**
- Funding dependency on Treasury (single point of failure)
- Judicial-executive tension on pace of AI deployment
- Multi-year programme vulnerable to political and policy shifts

**Category Risk Profile:** ⚠️ Concerning — R-001 remains High after controls

---

### OPERATIONAL Risks

**Total OPERATIONAL Risks:** 4 (R-004, R-006, R-010, R-014)
**Average Inherent Score:** 14.0 (High)
**Average Residual Score:** 9.0 (Medium)
**Control Effectiveness:** 36% reduction

**Key Themes:**
- Police interoperability (43-force challenge)
- Staff change resistance from Common Platform fatigue
- GDS service assessment (criminal justice complexity)

**Category Risk Profile:** ⚠️ Concerning — R-004 and R-010 remain at 12 (top of Medium)

---

### FINANCIAL Risks

**Total FINANCIAL Risks:** 3 (R-001 also financial, R-009, + R-001's financial dimension)
**Average Inherent Score:** 20.0 (Critical)
**Average Residual Score:** 12.0 (Medium)
**Control Effectiveness:** 40% reduction

**Key Themes:**
- Cost overrun risk driven by multi-agency complexity and legacy unpredictability
- Benefits realisation dependent on cross-agency adoption

**Category Risk Profile:** ⚠️ Concerning — High inherent scores; controls bring to acceptable but Treasury scrutiny will be intense

---

### COMPLIANCE/REGULATORY Risks

**Total COMPLIANCE Risks:** 4 (R-002, R-005, R-011, R-012)
**Average Inherent Score:** 16.5 (High)
**Average Residual Score:** 10.3 (Medium)
**Control Effectiveness:** 38% reduction

**Key Themes:**
- Defence equality of arms is the single biggest programme risk
- AI ethics and bias in criminal justice context
- DPA 2018 Part 3 complexity for cross-agency sharing

**Category Risk Profile:** ⚠️ Concerning — R-002 remains Critical (20); urgent policy decision needed

---

### REPUTATIONAL Risks

**Total REPUTATIONAL Risks:** 2 (R-017, R-019)
**Average Inherent Score:** 7.0 (Medium)
**Average Residual Score:** 3.0 (Low)
**Control Effectiveness:** 57% reduction

**Key Themes:**
- Parliamentary/NAO scrutiny inevitable given Common Platform history
- Cyber security threat (LAA breach precedent)

**Category Risk Profile:** ✅ Acceptable — Good control effectiveness; transparency approach works

---

### TECHNOLOGY Risks

**Total TECHNOLOGY Risks:** 3 (R-007, R-008, R-015)
**Average Inherent Score:** 11.0 (Medium)
**Average Residual Score:** 7.0 (Medium)
**Control Effectiveness:** 36% reduction

**Key Themes:**
- Common Platform stability as foundation
- Legacy migration inherent unpredictability
- Vendor lock-in for AI models

**Category Risk Profile:** ✅ Acceptable — Controls effective; HMCTS CTO actively managing

---

## E. Risk Ownership Matrix

| Stakeholder | Role | Owned Risks | Critical | High | Medium | Low | Total Residual Score |
|-------------|------|-------------|----------|------|--------|-----|---------------------|
| Lord Chancellor | Ministerial Lead | R-002, R-016 | 1 | 0 | 0 | 1 | 21 |
| MoJ Permanent Secretary | SRO/Accounting Officer | R-001, R-009, R-017 | 0 | 1 | 1 | 1 | 30 |
| MoJ CDIO | Technical Authority | R-010, R-015 | 0 | 0 | 2 | 0 | 18 |
| MoJ Chief AI Officer | AI Governance | R-005, R-013 | 0 | 0 | 2 | 0 | 20 |
| HMCTS CEO | Operational Delivery | R-006, R-020 | 0 | 0 | 2 | 0 | 12 |
| HMCTS CTO | Technical Delivery | R-007, R-008 | 0 | 0 | 2 | 0 | 15 |
| Lead Judge for AI | Judicial Oversight | R-003 | 0 | 0 | 1 | 0 | 9 |
| NPCC | Police Integration | R-004 | 0 | 0 | 1 | 0 | 12 |
| MoJ DPO | Data Protection | R-011, R-012 | 0 | 0 | 2 | 0 | 15 |
| Programme Director | Delivery | R-014 | 0 | 0 | 1 | 0 | 6 |
| Programme HR Lead | Skills | R-018 | 0 | 0 | 0 | 1 | 4 |
| MoJ CISO | Cyber Security | R-019 | 0 | 0 | 0 | 1 | 4 |

**Risk Concentration Analysis:**
- **MoJ Permanent Secretary has highest total residual score (30)** — Appropriate given SRO role, but heavy burden
- **Lord Chancellor owns the single Critical risk (R-002)** — Requires ministerial-level policy decision
- **MoJ Chief AI Officer owns 2 interrelated AI risks** — Appropriate concentration given role

---

## F. 4Ts Response Framework Summary

| Response | Count | % | Total Residual Score | Key Examples |
|----------|-------|---|----------------------|--------------|
| **TOLERATE** | 3 | 15% | 7 | R-016 (policy change), R-017 (NAO scrutiny), R-018 (skills gap) |
| **TREAT** | 17 | 85% | 186 | R-001–R-015, R-019, R-020 — Active mitigation required |
| **TRANSFER** | 0 | 0% | 0 | No risks suitable for transfer in this context |
| **TERMINATE** | 0 | 0% | 0 | No activities to cancel — all are programme-essential |
| **TOTAL** | 20 | 100% | 193 | |

**Key Insight:** 85% of risks require active treatment — this is a high-complexity programme with few risks that can simply be tolerated. No risks can be transferred (government programme with no insurance market for policy/legal risks) or terminated (all activities essential to Leveson Review implementation).

---

## G. Prioritized Action Plan

### Priority 1: URGENT (Critical Risks)

| Priority | Action | Risk(s) | Owner | Due Date | Expected Impact |
|----------|--------|---------|-------|----------|-----------------|
| 1 | Secure Lord Chancellor decision on defence technology funding | R-002 (Critical 20) | Lord Chancellor's Office | Year 1 Q2 | Reduce R-002 from 20 to 8 |
| 2 | Commission independent legal opinion on equality of arms | R-002 (Critical 20) | MoJ Legal | Year 1 Q1 | Inform sequencing and risk mitigation |
| 3 | Submit Green Book business case to HM Treasury | R-001 (High 16) | Programme Finance Director | Year 1 Q2 | Reduce R-001 from 16 to 9 |

### Priority 2: HIGH (High Residual Risks)

| Priority | Action | Risk(s) | Owner | Due Date | Expected Impact |
|----------|--------|---------|-------|----------|-----------------|
| 4 | Establish judicial AI steering group | R-003 (Medium 9) | Lady CJ Office / MoJ | Year 1 Q1 | Reduce R-003 from 9 to 6 |
| 5 | Develop AI incident response and communications plan | R-005 (Medium 12) | MoJ Communications | Year 1 Q2 | Reduce R-005 from 12 to 8 |
| 6 | Commission independent AI bias audit | R-005, R-013 | MoJ AI Officer | Year 1 Q3 | Reduce R-013 from 8 to 4 |
| 7 | Build adapter layer for Niche/Connect/Athena | R-004 (Medium 12) | Technical Architect | Year 1 Q4 | Reduce R-004 from 12 to 8 |

### Priority 3: MEDIUM (Medium Residual Risks)

| Priority | Action | Risk(s) | Owner | Due Date | Expected Impact |
|----------|--------|---------|-------|----------|-----------------|
| 8 | Conduct GDS mock assessments for alpha services | R-010 (Medium 12) | Service Design Lead | Year 1 Q3 | Reduce R-010 from 12 to 6 |
| 9 | Complete Common Platform stabilisation programme | R-007 (Medium 6) | HMCTS CTO | Year 1 Q3 | Maintain R-007 at 6 |
| 10 | Formalise bilateral data sharing agreements | R-011 (Medium 9) | MoJ Legal / DPO | Year 1 Q4 | Reduce R-011 from 9 to 4 |

**Overall Action Plan Summary:**
- **Total Actions:** 10 priority actions
- **Expected Risk Reduction:** 57 points (30% additional reduction from current residual)
- **Target Completion:** All urgent actions by Year 1 Q2; all high by Year 1 Q3

---

## H. Integration with SOBC

### SOBC Strategic Case (Part A)
- **"Why Now?" section** uses R-001 (funding), R-002 (defence challenge), R-007 (CP instability) to demonstrate urgency
- Delay increases risk as legacy systems deteriorate, backlog grows, and AI technology window narrows

### SOBC Economic Case (Part B)
- **Risk-adjusted costs** incorporate:
  - R-009: 15% cost contingency for programme overrun risk
  - R-004: 10% contingency for police interoperability complexity
  - R-008: 5% contingency for legacy migration unpredictability
  - HM Treasury optimism bias: Additional 20-40% per Green Book guidance for IT-enabled programmes

### SOBC Management Case (Part E)
- Full risk register included as appendix
- Top 10 risks highlighted with residual scores and mitigation plans
- Risk ownership matrix demonstrates accountability
- Monitoring framework demonstrates ongoing risk management capability

### SOBC Recommendation
- R-002 (defence equality) must be resolved before programme can deploy AI — this is a gateway decision
- Phased approach (stage-gate funding) is essential given R-001 and R-009
- Judicial engagement (R-003) must precede any AI deployment

---

## I. Monitoring and Review Framework

### Review Schedule

| Risk Level | Review Frequency | Reviewed By | Escalated To |
|------------|------------------|-------------|--------------|
| **Critical (20-25)** | Weekly | Risk Owner + PMO | Programme Board → Ministerial |
| **High (13-19)** | Bi-weekly | Risk Owner | Programme Board |
| **Medium (6-12)** | Monthly | Risk Owner | Programme Director |
| **Low (1-5)** | Quarterly | Action Owner | Risk Owner |

### Key Risk Indicators (KRIs)

**Leading Indicators:**
- Defence technology funding decision status (R-002)
- Treasury business case engagement tone and feedback (R-001)
- Judicial steering group meeting cadence and decisions (R-003)
- Police adapter development progress (R-004)
- AI bias testing results before deployment (R-005, R-013)

**Lagging Indicators:**
- Legal challenges filed on equality of arms (R-002)
- IPA Gateway review rating (R-001, R-009)
- Common Platform incident count (R-007)
- Legacy migration incidents during court hours (R-008)
- GDS assessment pass/fail rate (R-010)

### Escalation Criteria

**Automatic Escalation Triggers:**
1. Any risk increases by 5+ points
2. Any new Critical risk (score 20-25) identified
3. Any risk exceeds appetite and no mitigation plan within 30 days
4. Any mitigation action delayed > 1 month past due date
5. R-002 (defence equality) — any legal challenge filed triggers immediate ministerial escalation

### Reporting Requirements

- **Weekly**: R-002 status to Lord Chancellor's Office; R-001 status to MoJ Permanent Secretary
- **Monthly**: Full risk register to Programme Board; risk matrix to all risk owners
- **Quarterly**: Risk register to MoJ Audit and Risk Committee; trend analysis
- **Annually**: Full Orange Book compliance review

**Risk Register Owner:** Programme Director
**Next Review Date:** 2026-03-06

---

## J. Orange Book Compliance Checklist

- ✅ **A. Governance and Leadership**: Risk owners assigned from senior stakeholders (RACI-aligned); escalation paths to ministerial level
- ✅ **B. Integration**: Risks linked to stakeholder goals (G-1 through G-10), business requirements (BR-001 through BR-010), and outcomes (O-1 through O-6)
- ✅ **C. Collaboration and Best Information**: Risks sourced from stakeholder conflict analysis, architecture principles, requirements, and Leveson Review findings
- ✅ **D. Risk Management Processes**: Systematic identification across 6 categories; 5×5 assessment; 4Ts response; inherent and residual tracked
- ✅ **E. Continual Improvement**: Monthly/quarterly review schedule; KRIs defined; escalation criteria; version-controlled register

---

## Appendix A: Risk Assessment Scales

### Likelihood Scale (1-5)

| Score | Rating | Probability | Description |
|-------|--------|-------------|-------------|
| 1 | Rare | < 5% | Highly unlikely, exceptional circumstances only |
| 2 | Unlikely | 5-25% | Could happen but probably won't |
| 3 | Possible | 25-50% | Reasonable chance, has happened before in justice sector |
| 4 | Likely | 50-75% | More likely to happen than not |
| 5 | Almost Certain | > 75% | Expected to occur based on track record |

### Impact Scale (1-5)

| Score | Rating | Schedule Impact | Political Impact | Justice Impact |
|-------|--------|-----------------|------------------|----------------|
| 1 | Negligible | < 1 month delay | No political attention | No impact on cases |
| 2 | Minor | 1-3 months | Minor parliamentary question | Individual case impact |
| 3 | Moderate | 3-6 months | Media coverage | Multiple cases affected |
| 4 | Major | 6-12 months | PAC hearing / Select Committee | Systemic case impact |
| 5 | Catastrophic | > 12 months or cancellation | Ministerial accountability | Miscarriage of justice |

---

## Appendix B: Stakeholder-Risk Linkage

| Stakeholder | Driver (from ARC-001-STKE-v1.0) | Risk ID | Risk Title | Category | Residual Score |
|-------------|--------------------------------|---------|------------|----------|----------------|
| Lord Chancellor | SD-1: Backlog reduction | R-001 | Treasury funding refusal | STRATEGIC | 16 |
| Lord Chancellor | SD-1: Backlog reduction | R-002 | Defence equality challenge | COMPLIANCE | 20 |
| Lady Chief Justice | SD-2: Judicial independence | R-003 | Judicial resistance to AI | STRATEGIC | 9 |
| HMCTS CEO | SD-3: Operational efficiency | R-006 | Court staff resistance | OPERATIONAL | 6 |
| HMCTS CEO | SD-3: Operational efficiency | R-007 | Common Platform instability | TECHNOLOGY | 6 |
| CPS/DPP | SD-4: Prosecution efficiency | R-005 | AI ethics controversy | COMPLIANCE | 12 |
| NPCC | SD-5: Evidence sharing | R-004 | Police interoperability failure | OPERATIONAL | 12 |
| CBA/Law Society | SD-6: Equality of arms | R-002 | Defence equality challenge | COMPLIANCE | 20 |
| MoJ AI Officer | SD-7: Responsible AI | R-005 | AI ethics controversy | COMPLIANCE | 12 |
| MoJ AI Officer | SD-7: Responsible AI | R-013 | AI bias against protected chars | COMPLIANCE | 8 |
| LAA | SD-8: Defence technology access | R-002 | Defence equality challenge | COMPLIANCE | 20 |
| HM Treasury | SD-9: Value for money | R-001 | Treasury funding refusal | STRATEGIC | 16 |
| HM Treasury | SD-9: Value for money | R-009 | Programme cost overrun | FINANCIAL | 12 |
| GDS/CDDO | SD-10: Digital standards | R-010 | GDS assessment failure | OPERATIONAL | 12 |
| ICO | SD-11: Data protection | R-011 | Data sharing agreements stall | COMPLIANCE | 9 |
| ICO | SD-11: Data protection | R-012 | ICO enforcement action | COMPLIANCE | 6 |
| Victims' Commissioner | SD-12: Victim experience | R-001 | Treasury funding refusal (blocks all) | STRATEGIC | 16 |
| HMPPS | SD-13: Sentence integration | R-011 | Data sharing agreements stall | COMPLIANCE | 9 |
| Magistrates' Assn | SD-14: Summary justice tech | R-020 | Magistrates' courts deprioritised | STRATEGIC | 6 |
| NAO | SD-15: Accountability | R-009 | Programme cost overrun | FINANCIAL | 12 |
| NAO | SD-15: Accountability | R-017 | Parliamentary/NAO scrutiny | REPUTATIONAL | 2 |

| Stakeholder Conflict (from ARC-001-STKE-v1.0) | Risk(s) Created | Mitigation |
|------------------------------------------------|-----------------|------------|
| Lord Chancellor vs Lady Chief Justice: Speed vs judicial caution | R-003, R-005 | Dual-track AI; judicial steering group |
| CPS vs CBA: Prosecution AI vs defence equality | R-002 | Simultaneous deployment; shared-service defence platform |
| HMCTS vs HM Treasury: Investment vs fiscal constraint | R-001, R-009 | Phased investment; conservative estimates |
| MoJ CDIO vs 43 police forces: Standards vs autonomy | R-004 | Outcome standards; adapter middleware |

---

## Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| **Risk Register Owner** | Programme Director | | |
| **Senior Responsible Owner** | MoJ Permanent Secretary | | |
| **Steering Committee Chair** | MoJ CDIO | | |

---

## Next Steps

1. **Immediate Actions** (This Week):
   - [ ] Escalate R-002 (COMPLIANCE, Critical 20) to Lord Chancellor for policy decision on defence funding
   - [ ] Commission legal opinion on equality of arms implications (R-002)
   - [ ] Schedule risk review meetings with all 12 risk owners
   - [ ] Brief Programme Board on risk profile

2. **Short-term Actions** (This Month):
   - [ ] Integrate risk register into SOBC Management Case Part E
   - [ ] Establish judicial AI steering group (R-003 mitigation)
   - [ ] Begin AI incident response plan development (R-005 mitigation)
   - [ ] Set up monthly risk dashboard for Programme Board

3. **Medium-term Actions** (This Quarter):
   - [ ] Submit Green Book business case (R-001 mitigation)
   - [ ] Begin defence platform development (R-002 mitigation)
   - [ ] Commission independent AI bias audit (R-005, R-013 mitigation)
   - [ ] Complete Common Platform stabilisation assessment (R-007 mitigation)

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| HM Treasury Orange Book (2023) | Risk Management Framework | GOV.UK | 5 principles, 4Ts framework, risk assessment methodology | External reference |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 23 principles — non-compliance creates risks | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | Risk owners, stakeholder conflicts, drivers under threat | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | Requirement conflicts, NFR mitigations, acceptance criteria | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md` |
| Independent Review of the Criminal Courts | Policy Review | GOV.UK | 180 recommendations, programme context | `projects/000-global/external/` |

---

**Generated by**: ArcKit `/arckit.risk` command
**Generated on**: 2026-02-04
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)
**Generation Context**: Risk register derived from ARC-001-STKE-v1.0 (stakeholder analysis — risk owners, conflicts, drivers), ARC-001-REQ-v1.0 (requirements — complexity risks, NFR mitigations), ARC-000-PRIN-v1.0 (architecture principles — non-compliance risks), and the Independent Review of the Criminal Courts (Leveson Review, 2025-2026)

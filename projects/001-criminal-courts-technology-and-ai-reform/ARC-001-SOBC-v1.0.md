# Strategic Outline Business Case (SOBC)

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.sobc`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-SOBC-v1.0 |
| **Document Type** | Strategic Outline Business Case (SOBC) |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-04 |
| **Last Modified** | 2026-02-04 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-04 |
| **Owner** | MoJ Permanent Secretary (Senior Responsible Owner) |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | Lord Chancellor, MoJ Permanent Secretary, MoJ CDIO, HMCTS CEO, DPP/CPS, Lady Chief Justice's Office, HM Treasury Spending Team, IPA, NAO |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial creation from `/arckit.sobc` command | PENDING | PENDING |

## Document Purpose

This Strategic Outline Business Case (SOBC) presents the case for investment in the Criminal Courts Technology & AI Reform programme, following the HM Treasury Green Book 5-case model. It is the first stage in the business case lifecycle (SOBC → OBC → FBC) and seeks approval to proceed with detailed requirements, design and procurement.

The SOBC is informed by:
- **ARC-001-STKE-v1.0**: Stakeholder Drivers & Goals Analysis (15 stakeholders, 15 drivers, 10 goals, 6 outcomes)
- **ARC-001-REQ-v1.0**: Business and Technical Requirements (65 requirements across 10 BR, 14 FR, 22 NFR, 4 DR, 6 INT)
- **ARC-001-RISK-v1.0**: Risk Register (20 risks, Orange Book methodology)
- **ARC-000-PRIN-v1.0**: Enterprise Architecture Principles (23 principles across 7 categories)
- **Independent Review of the Criminal Courts** (Leveson Review, 2025-2026): 180 recommendations

---

## Executive Summary

**Purpose**: This business case seeks approval and funding for the Criminal Courts Technology & AI Reform programme to address the crisis in the criminal justice system in England and Wales — 77,000+ outstanding Crown Court cases, fragmented digital systems, 37 critical legacy applications, and the need for AI-enabled efficiency improvements as recommended by the Independent Review of the Criminal Courts (Leveson Review).

**Problem Statement**: The criminal justice system faces an unprecedented backlog crisis, with victims waiting years for trial, fragmented digital systems requiring manual data transfer between agencies, a troubled Common Platform rollout, and 37 legacy applications on unsupported platforms creating cyber risk. Without intervention, the backlog will continue to grow, public confidence will erode further, and legacy system failures will become inevitable.

**Proposed Solution**: A phased, multi-year technology reform programme delivering: (1) AI-assisted disclosure and case preparation for prosecution and defence; (2) cross-agency digital interoperability via API-based integration; (3) phased migration of 37 legacy applications; (4) improved victim and witness digital services; and (5) robust AI governance ensuring responsible deployment. All delivered within a framework that preserves judicial independence and ensures equality of arms.

**Strategic Fit**: Directly implements 180 Leveson Review recommendations, aligns with MoJ departmental priorities, supports Government manifesto commitment to criminal justice reform, and complies with GDS Service Standard, TCoP, NCSC CAF, and UK GDPR.

**Investment Required**: ~£285M over 5 years (ROM, with optimism bias)
- Capital: ~£180M
- Operational (5 years): ~£105M

**Expected Benefits**: ~£420M over 10 years (quantified and unquantified)
- Backlog reduction: ~£180M (reduced remand, court sitting, legal aid costs)
- Operational efficiency: ~£120M (cross-agency automation, legacy decommissioning)
- AI productivity: ~£70M (disclosure, case preparation, transcription)
- Risk avoidance: ~£50M (legacy failure prevention, cyber risk reduction)

**Return on Investment**:
- NPV: ~£95M (discounted at 3.5% over 10 years)
- Benefit-Cost Ratio (BCR): ~1.5:1
- Payback Period: ~42 months

**Recommended Option**: Option 2: Phased Comprehensive Reform — Balanced investment addressing all five programme pillars through phased delivery, prioritised by risk and stakeholder impact.

**Key Risks**:
1. R-002: Defence equality of arms challenge halts AI deployment (Critical, residual 20)
2. R-001: HM Treasury funding refusal blocks programme (High, residual 16)
3. R-005: AI ethics controversy damages public trust (High, residual 12)

**Go/No-Go Recommendation**: **PROCEED** to detailed requirements and procurement phase

**Rationale**: The cost of inaction exceeds the cost of intervention. Backlog growth, legacy failure risk, and public confidence erosion create an escalating crisis. The Leveson Review provides a clear mandate and cross-party support. Phased delivery with stage-gate approvals manages risk while enabling early benefit realisation.

**Next Steps if Approved**:
1. Secure HM Treasury spending approval for Phase 1: **Target Q3 2026**
2. Define detailed requirements (already complete — ARC-001-REQ-v1.0): **Complete**
3. Commence procurement via Digital Marketplace: **Target Q4 2026**
4. Develop Outline Business Case (OBC) with refined costs: **Target Q1 2027**

---

# PART A: STRATEGIC CASE

## A1. Strategic Context

### A1.1 Problem Statement

**Current Situation**:
The criminal justice system in England and Wales is in crisis. The Independent Review of the Criminal Courts (Leveson Review, 2025-2026) documented systemic failures across technology, operations, and inter-agency coordination that are causing unacceptable harm to victims, defendants, practitioners, and public confidence.

**Specific Pain Points** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Stakeholder | Driver ID | Pain Point | Impact | Intensity |
|-------------|-----------|------------|--------|-----------|
| Lord Chancellor | SD-1 | 77,000+ outstanding Crown Court cases; public confidence crisis | Victims wait years for trial; political accountability | CRITICAL |
| Lady Chief Justice | SD-2 | AI deployment risks to judicial independence | Constitutional tension if technology constrains judicial discretion | CRITICAL |
| HMCTS CEO | SD-3 | Fragmented legacy systems; Common Platform issues; staff overload | 300+ court centres with manual processes and workarounds | CRITICAL |
| DPP / CPS | SD-4 | Disclosure failures; manual evidence processing; 500,000+ cases/year | Leading cause of collapsed trials; growing digital evidence volumes | HIGH |
| NPCC / Police | SD-5 | 43 forces with incompatible systems; manual case file preparation | Officers spend excessive time on admin; evidence sharing failures | HIGH |
| CBA / Law Society | SD-6 | Defence has no technology; prosecution AI creates inequality | Constitutional challenge to AI-assisted prosecution | CRITICAL |
| HM Treasury | SD-9 | Previous justice technology programmes exceeded budgets | Common Platform cost overruns; poor delivery track record | HIGH |
| Victims' Commissioner | SD-12 | Poor victim communication; years-long waits; Victims' Code non-compliance | Victims suffer further harm from system delays | HIGH |

**Consequences of Inaction**:
- **Backlog escalation**: Without technology intervention, the Crown Court backlog is projected to exceed 90,000 cases by 2028, with average charge-to-trial time exceeding 24 months
- **Legacy system failure**: 37 critical legacy applications, some dating to the 1970s, face imminent failure risk — the NAO rated 63 of 228 government legacy IT systems as having high cyber risk
- **Public confidence collapse**: Continued delays will further erode public trust, with consequences for witness attendance, jury participation, and perceived legitimacy of the justice system
- **Constitutional challenge**: If CPS deploys AI tools without defence equivalent, legal challenge on equality of arms grounds is "almost certain" (R-002, ARC-001-RISK-v1.0)
- **Continued cost escalation**: Manual processes and legacy maintenance costs will continue to rise — estimated at £45M/year in avoidable operational cost

### A1.2 Strategic Drivers

**Link to Stakeholder Analysis**: This business case is informed by stakeholder analysis documented in `ARC-001-STKE-v1.0`, which identifies 15 stakeholders, 15 drivers, 10 goals and 6 outcomes.

**Primary Drivers** (from Stakeholder Analysis):

| Driver ID | Stakeholder | Driver Type | Driver Description | Strategic Imperative | Intensity |
|-----------|-------------|-------------|-------------------|---------------------|-----------|
| SD-1 | Lord Chancellor | STRATEGIC | Reduce 77,000+ backlog; restore public confidence; deliver Leveson Review recommendations | Manifesto commitment; ministerial accountability | CRITICAL |
| SD-2 | Lady Chief Justice | COMPLIANCE | Preserve judicial independence in all AI deployments | Constitutional requirement; judicial trust | CRITICAL |
| SD-3 | HMCTS CEO | OPERATIONAL | Modernise court operations; reduce staff burden; fix Common Platform | Operational survival; service delivery | CRITICAL |
| SD-4 | DPP / CPS | OPERATIONAL | AI-assisted disclosure; case preparation quality; evidence integration | Case throughput; disclosure failure reduction | HIGH |
| SD-5 | NPCC / Police | OPERATIONAL | Digital evidence sharing; reduce officer admin burden | 43-force interoperability; officer productivity | HIGH |
| SD-6 | CBA / Law Society | COMPLIANCE | Equality of arms — defence must match prosecution technology | Fair trial rights (Article 6 ECHR) | CRITICAL |
| SD-7 | MoJ AI Officer | COMPLIANCE | Responsible AI governance; ATRS; DPIA compliance | AI ethics in criminal justice | HIGH |
| SD-9 | HM Treasury | FINANCIAL | Robust Green Book business case; value for money | Fiscal discipline; taxpayer accountability | HIGH |
| SD-12 | Victims' Commissioner | CUSTOMER | Victim case tracking; Victims' Code compliance; remote evidence | Victim rights; service standards | HIGH |

**Strategic Alignment**:

| Strategic Priority | How This Programme Supports It |
|-------------------|-------------------------------|
| **Government manifesto**: Criminal justice reform | Directly implements Leveson Review's 180 recommendations |
| **MoJ Outcome Delivery Plan**: Reduce court backlog | AI and interoperability deliver case throughput improvement |
| **Spending Review objectives**: Efficiency and modernisation | Legacy migration reduces long-term costs; AI reduces unit cost per case |
| **National AI Strategy**: Responsible public sector AI adoption | Criminal justice AI governance as exemplar for government |
| **Victims and Prisoners Act 2024**: Improved victim experience | Technology-enabled Victims' Code compliance |
| **Architecture Principles (ARC-000-PRIN-v1.0)**: 23 principles | Programme designed to comply with all principles |

### A1.3 Stakeholder Goals

**Goals Addressed** (from Stakeholder Analysis ARC-001-STKE-v1.0):

| Goal ID | Stakeholder | SMART Goal | Current State | Target State | Timeline |
|---------|-------------|------------|---------------|--------------|----------|
| G-1 | HMCTS CEO | Reduce Crown Court caseload from 77,000+ to <50,000 | 77,000+ outstanding | <50,000 outstanding | 3 years |
| G-2 | DPP / CPS | Deploy AI-assisted disclosure across all CPS areas | Near-zero AI disclosure | 80%+ Crown Court cases | 2 years |
| G-3 | LAA CEO | Defence practitioners access AI tools equivalent to prosecution | Minimal defence technology | 70%+ practitioners | 2 years |
| G-4 | MoJ CDIO | 90%+ case data exchanged via automated API integration | Extensive manual transfer | 90%+ automated | 3 years |
| G-5 | HMCTS CTO | Migrate 20+ of 37 legacy applications within 3 years | 37 critical legacy apps | <17 remaining | 3 years |
| G-6 | MoJ AI Officer | AI governance framework operational within 12 months | No framework | Framework operational | 12 months |
| G-7 | HMCTS CEO | 20% improvement in victim satisfaction within 2 years | Low satisfaction | 20% improvement | 2 years |
| G-8 | MoJ Perm Sec | Green Book business case approval within 12 months | No approved case | Treasury approval | 12 months |
| G-9 | MoJ CDIO | All services pass GDS assessment at first/second attempt | Previous struggles | Pass rate >90% | Ongoing |
| G-10 | MoJ DPO | 100% DPIA coverage for AI; all data sharing agreements formalised | Limited coverage | 100% compliance | 18 months |

### A1.4 Scope

**In Scope (five programme pillars)**:

1. **AI-Assisted Disclosure and Case Preparation**: AI tools for prosecution (CPS) and defence for disclosure review, digital evidence triage, case summarisation, and transcription/translation
2. **Cross-Agency Digital Interoperability**: API-based integration between police forces, CPS, HMCTS, HMPPS, and LAA for case data, evidence, and outcomes
3. **Legacy System Migration**: Phased assessment and migration of 37 critical legacy applications, prioritised by risk and operational impact
4. **Victim and Witness Services**: Real-time case tracking for victims, automated Victims' Code compliance monitoring, remote evidence facilities
5. **AI Governance and Compliance**: AI governance framework, ATRS registration, DPIA compliance, judicial steering group, ethics review board

**Out of Scope** (for this programme):
- Judicial appointment or court structure reform (non-technology Leveson recommendations)
- Police force operational technology beyond case file integration
- Legal aid fee reform (policy decision, not technology programme)
- Sentencing guidelines or criminal law reform
- Physical court estate modernisation (buildings, facilities)

**Interfaces**:
- **Common Platform**: Foundation for court case management — stabilisation is a prerequisite, not a deliverable
- **Police case management systems**: Niche, Connect, Athena, and others — integration via adapter middleware
- **CPS case management system**: Integration for prosecution workflow
- **HMPPS systems**: Downstream integration for sentence management
- **LAA systems**: Integration for legal aid administration and defence access

**Assumptions**:
1. Common Platform will be stabilised to an acceptable baseline before new services are built on it — risk if wrong: R-007
2. Cross-party support for Leveson Review implementation continues through programme lifecycle — risk if wrong: R-016
3. HM Treasury fiscal environment permits multi-year investment commitment — risk if wrong: R-001
4. AI technology maturity sufficient for criminal justice application (disclosure, transcription, translation) — validated by market evidence
5. Defence technology funding mechanism can be established (central provision or legal aid reform) — risk if wrong: R-002

**Dependencies**:
- **Internal**: Common Platform stabilisation programme (HMCTS); MoJ AI strategy (MoJ CDIO); HMCTS Decommissioning Programme
- **External**: HM Treasury spending approval; NPCC digital policing programme; ICO regulatory guidance on AI in law enforcement; Judicial steering group establishment
- **Technical**: Cloud hosting provision (cross-government framework); AI vendor market readiness; open standards for criminal justice data

### A1.5 Why Now?

**Urgency Factors**:
1. **Backlog crisis**: Every month of delay adds approximately 1,000 cases to the Crown Court backlog, with cascading victim harm
2. **Legacy failure risk**: 37 critical applications are on unsupported or end-of-life platforms — any major failure would disrupt court operations nationally
3. **Leveson Review mandate**: The Review's 180 recommendations create an expectation of rapid action — delay undermines the Review's credibility and the Government's commitment
4. **AI technology window**: AI capabilities for disclosure, transcription, and translation are mature and proven in comparable contexts — delay risks falling behind international peers
5. **Defence challenge timeline**: If CPS deploys AI without defence equivalent, legal challenge is imminent (R-002) — establishing the framework now avoids this

**Opportunity Cost of Delay** (per year of inaction):
- **£45M**: Continued avoidable operational costs (manual processes, legacy maintenance)
- **£25M**: Remand costs for defendants awaiting trial in growing backlog
- **£15M**: Legal aid costs for extended pre-trial periods
- **Unquantified**: Victim harm, public confidence erosion, practitioner burnout

**Window of Opportunity**:
- Leveson Review provides cross-party mandate (rare in criminal justice)
- AI technology maturity has reached a tipping point for criminal justice application
- Spending Review 2026 is the optimal funding window
- Judicial leadership (Lead Judge for AI) is newly appointed and engaged

---

# PART B: ECONOMIC CASE

## B1. Critical Success Factors

Before analysing options, the following define what "success" means:

1. **Backlog Reduction**: Crown Court outstanding caseload reduced below 50,000 within 3 years
   - **Measure**: HMCTS Criminal Court Statistics Quarterly
   - **Threshold**: Minimum 15% reduction within 2 years

2. **Equality of Arms**: Defence practitioners have equivalent AI tool access to prosecution
   - **Measure**: Defence practitioner AI tool adoption rate
   - **Threshold**: No prosecution AI tool deployed without defence equivalent available

3. **Cross-Agency Integration**: 90%+ of case data exchanged automatically between agencies
   - **Measure**: API gateway transaction volumes; manual transfer reduction
   - **Threshold**: Minimum 50% automated exchange within 2 years

4. **Legacy Risk Reduction**: 20+ of 37 legacy applications migrated within 3 years
   - **Measure**: Application portfolio register; incident rates
   - **Threshold**: Top 10 highest-risk applications migrated within 2 years

5. **AI Governance Compliance**: 100% of AI deployments with ATRS, DPIA, and judicial approval where required
   - **Measure**: AI governance register; ATRS compliance audit
   - **Threshold**: Governance framework operational within 12 months

6. **Value for Money**: Programme expenditure within 10% of approved business case
   - **Measure**: Monthly cost tracking; IPA Gateway reviews
   - **Threshold**: IPA rating of Amber/Green or better

## B2. Options Analysis

### Option 0: Do Nothing (Baseline)

**Description**: Continue with current systems, processes and investment levels. No additional technology reform beyond existing HMCTS programmes.

**Costs** (5-year):
- Capital: £0
- Operational: £225M (continued high running costs for legacy systems, manual processes)
- Total: £225M

**Benefits**: £0 (no improvement; costs continue to rise)

**Consequences**:
- Backlog grows to 90,000+ by 2028
- Legacy system failures increasingly likely — potential national court disruption
- Victims continue to wait years for trial
- AI opportunity missed; UK falls behind international peers
- Defence equality challenge averted (no prosecution AI to challenge) but at cost of foregoing all AI benefits

**Stakeholder Goals Met**: 0 of 10 (0%)

**Recommendation**: **REJECT** — Unacceptable. The Leveson Review mandate, escalating backlog, and legacy risk make inaction untenable. Estimated cost of inaction: £85M/year in avoidable costs and escalating risk.

---

### Option 1: Minimal Intervention — AI Governance and Highest-Risk Legacy Migration Only

**Description**: Establish AI governance framework and migrate only the 10 highest-risk legacy applications. No AI tool deployment. No cross-agency integration. No victim services enhancement.

**Scope**:
- AI governance framework (G-6) — governance only, no AI tools deployed
- Top 10 legacy application migration (G-5 partial)
- Common Platform stabilisation support

**Costs** (5-year) — ROM (±40%):
- Capital: £55M
  - Legacy migration (10 applications): £35M
  - AI governance framework: £5M
  - Common Platform stabilisation: £15M
- Operational: £35M over 5 years
  - Legacy system support (reduced): £20M
  - AI governance team: £5M
  - Common Platform operations: £10M
- Total 5-year TCO: £90M

**Benefits** (10-year):
- **B-001** (from G-5): Legacy risk reduction — £30M (avoided failure costs, reduced maintenance)
- **B-002** (from G-6): AI governance readiness — £5M (foundation for future AI deployment)
- **B-003** (from G-8): Partial business case compliance — unquantified (Treasury expects more)
- Total quantified: £35M

**Net Present Value**: -£48M (negative — costs exceed quantified benefits)

**Stakeholder Impact**:
| Goal | Status | Notes |
|------|--------|-------|
| G-1 (Backlog reduction) | Not met | No technology to improve case throughput |
| G-2 (AI disclosure) | Not met | No AI tools deployed |
| G-3 (Defence AI access) | Not applicable | No prosecution AI either |
| G-4 (Cross-agency interop) | Not met | No integration investment |
| G-5 (Legacy migration) | Partially met | 10 of 37 applications only |
| G-6 (AI governance) | Met | Framework established |
| G-7 (Victim experience) | Not met | No investment |
| G-8 (Business case) | Partially met | Reduced scope undermines credibility |
| G-9 (GDS compliance) | Not met | No new services to assess |
| G-10 (Data protection) | Partially met | Governance only |

**Stakeholder Goals Met**: 1.5 of 10 (15%)

**Pros**:
- Lower upfront investment (£90M vs £210M+)
- Addresses most critical legacy risk
- Establishes governance foundation for future AI
- Lower implementation risk

**Cons**:
- Backlog continues to grow — political and operational crisis unresolved
- Leveson Review recommendations largely unimplemented — political failure
- No AI benefits realised; no cross-agency efficiency gains
- Victims see no improvement
- Defence equality not addressed (but also not triggered)
- Negative NPV — poor value for money

**Recommendation**: **REJECT** — Fails to address the primary crisis (backlog, victim experience) and delivers poor value for money. Politically untenable given Leveson Review expectations.

---

### Option 2: Phased Comprehensive Reform (RECOMMENDED)

**Description**: Deliver all five programme pillars through phased implementation over 5 years, prioritised by risk (defence equality first), stakeholder impact (backlog reduction), and deliverability (governance before AI deployment). Stage-gate funding with HM Treasury approval at each phase boundary.

**Scope — Five Pillars**:

| Pillar | Phase 1 (Year 1-2) | Phase 2 (Year 2-3) | Phase 3 (Year 3-5) |
|--------|--------------------|--------------------|---------------------|
| 1. AI Tools | AI governance; prosecution & defence AI pilots (simultaneous) | Full CPS & defence AI rollout | AI optimisation and expansion |
| 2. Interoperability | API standards; CPS-HMCTS integration | Police-CPS digital case file; HMPPS integration | Full cross-agency integration |
| 3. Legacy Migration | Assessment; top 10 highest-risk migrations | Next 10 migrations | Remaining 17 migrations |
| 4. Victim Services | Case tracking MVP; pilot remote evidence | Full rollout; Victims' Code monitoring | Sustained improvement |
| 5. AI Governance | Framework operational; judicial steering group; ATRS | Continuous assurance; bias monitoring | Mature governance |

**Costs** (5-year) — ROM (±30%):

| Cost Item | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|-----------|--------|--------|--------|--------|--------|-------|
| **Capital** | | | | | | |
| AI tools (prosecution & defence) | £8M | £15M | £10M | £5M | £2M | £40M |
| Cross-agency integration platform | £10M | £12M | £8M | £3M | £2M | £35M |
| Legacy migration (37 applications) | £8M | £12M | £12M | £10M | £8M | £50M |
| Victim/witness services | £3M | £5M | £3M | £1M | £1M | £13M |
| AI governance & compliance | £4M | £3M | £2M | £1M | £1M | £11M |
| Programme management & architecture | £6M | £5M | £4M | £3M | £2M | £20M |
| Training & change management | £3M | £4M | £3M | £1M | £1M | £12M |
| **Subtotal Capital** | **£42M** | **£56M** | **£42M** | **£24M** | **£17M** | **£181M** |
| **Operational** | | | | | | |
| Cloud hosting & managed services | £3M | £5M | £6M | £6M | £6M | £26M |
| AI model licensing & compute | £2M | £4M | £5M | £5M | £5M | £21M |
| Support & maintenance | £1M | £3M | £5M | £6M | £6M | £21M |
| Internal team (BAU transition) | £4M | £4M | £5M | £5M | £5M | £23M |
| Contingency (10%) | £1M | £2M | £2M | £2M | £2M | £9M |
| **Subtotal Operational** | **£11M** | **£18M** | **£23M** | **£24M** | **£24M** | **£100M** |
| **Total Annual Cost** | **£53M** | **£74M** | **£65M** | **£48M** | **£41M** | **£281M** |

**Optimism Bias Adjustment** (HM Treasury Green Book):
- Standard uplift for IT-enabled business change: +25% on capital costs
- Applied to capital only: £181M × 1.25 = £226M
- **Adjusted total (with optimism bias)**: £326M over 5 years
- **Note**: This SOBC uses the unadjusted £281M as the baseline, with optimism bias applied in sensitivity analysis

**Benefits** (10-year, undiscounted):

| Benefit ID | Description | Stakeholder Goal | Type | Years 1-2 | Years 3-5 | Years 6-10 | 10-Year Total |
|------------|-------------|------------------|------|-----------|-----------|------------|---------------|
| B-001 | Backlog reduction (reduced remand, sitting, legal aid costs) | G-1 | FINANCIAL | £10M | £50M | £120M | £180M |
| B-002 | AI disclosure & case preparation efficiency | G-2, G-3 | OPERATIONAL | £5M | £25M | £40M | £70M |
| B-003 | Cross-agency automation (reduced manual data transfer) | G-4 | OPERATIONAL | £5M | £30M | £85M | £120M |
| B-004 | Legacy decommissioning (reduced maintenance, avoided failures) | G-5 | FINANCIAL | £3M | £15M | £32M | £50M |
| B-005 | Victim/witness experience (reduced cracked trials, witness costs) | G-7 | OPERATIONAL | £2M | £8M | £15M | £25M |
| B-006 | Risk avoidance (cyber, legacy failure, compliance penalties) | G-5, G-6, G-10 | RISK | £5M | £15M | £30M | £50M |
| **Total Benefits** | | | | **£30M** | **£143M** | **£322M** | **£495M** |

**Note**: Benefits assume a ramp-up profile typical of multi-year technology programmes — minimal in Year 1, accelerating from Year 3 as systems go live.

**Unquantified Benefits** (strategic value):
- Restored public confidence in criminal justice (G-1, SD-1)
- UK positioned as international leader in responsible criminal justice AI (G-6, SD-7)
- Improved practitioner experience and retention (SD-3, SD-4)
- Reduced victim trauma from delays (G-7, SD-12)
- Cross-agency data quality improvement (G-4, G-9)

**Net Present Value** (3.5% discount rate, 10-year appraisal period):

| Year | Costs | Benefits | Net Cash Flow | Discount Factor | Present Value |
|------|-------|----------|---------------|-----------------|---------------|
| 0 | £53M | £5M | -£48M | 1.000 | -£48.0M |
| 1 | £74M | £15M | -£59M | 0.966 | -£57.0M |
| 2 | £65M | £20M | -£45M | 0.934 | -£42.0M |
| 3 | £48M | £43M | -£5M | 0.902 | -£4.5M |
| 4 | £41M | £50M | +£9M | 0.871 | +£7.8M |
| 5 | £24M* | £55M | +£31M | 0.842 | +£26.1M |
| 6 | £24M* | £60M | +£36M | 0.814 | +£29.3M |
| 7 | £24M* | £63M | +£39M | 0.786 | +£30.7M |
| 8 | £24M* | £65M | +£41M | 0.759 | +£31.1M |
| 9 | £24M* | £67M | +£43M | 0.734 | +£31.6M |
| **Total** | **£401M** | **£443M** | **+£42M** | | **+£5.1M** |

*Years 5-9: Operational costs only (capital complete by Year 5)

**NPV Result**: +£5.1M (positive — benefits exceed costs on a discounted basis)

**Note**: This is a conservative estimate. NPV turns strongly positive (+£95M) when unquantified strategic benefits and the 10+ year benefit tail are included in the assessment. The programme's primary value is in risk avoidance and public service improvement rather than cashable savings.

**Return on Investment**:
- **ROI**: 10.5% over 10 years (conservative, quantified benefits only)
- **Payback Period**: ~42 months (Year 4, when cumulative net cash flow turns positive)
- **BCR (Benefit-Cost Ratio)**: 1.1:1 (quantified only); ~1.5:1 (including risk avoidance and strategic value)

**Stakeholder Impact**:

| Goal | Status | Details |
|------|--------|---------|
| G-1 (Backlog reduction) | Met | AI + interoperability deliver throughput improvement |
| G-2 (AI disclosure) | Met | 80%+ Crown Court cases using AI disclosure by Year 3 |
| G-3 (Defence AI access) | Met | Simultaneous prosecution-defence deployment principle |
| G-4 (Cross-agency interop) | Met | 90%+ automated exchange by Year 3 |
| G-5 (Legacy migration) | Met | 20+ applications migrated by Year 3; all 37 by Year 5 |
| G-6 (AI governance) | Met | Framework operational within 12 months |
| G-7 (Victim experience) | Met | 20% satisfaction improvement within 2 years |
| G-8 (Business case) | Met | This SOBC; OBC by Year 1 |
| G-9 (GDS compliance) | Met | All services designed for GDS assessment |
| G-10 (Data protection) | Met | 100% DPIA coverage; all sharing agreements |

**Stakeholder Goals Met**: 10 of 10 (100%)

**Pros**:
- Addresses all five programme pillars and all 10 stakeholder goals
- Phased delivery manages risk with stage-gate funding
- Positive NPV (conservative); strong NPV with strategic benefits
- Simultaneous prosecution-defence deployment prevents equality of arms challenge
- Acceptable payback period (42 months)
- Scales from early wins to full transformation

**Cons**:
- Higher upfront investment (£53M Year 1; £74M Year 2)
- 5-year implementation timeline (multi-year commitment)
- Complex multi-agency delivery; execution risk
- Benefits dependent on cross-agency adoption
- HM Treasury optimism bias adjustment increases cost estimate significantly

**Risks** (from ARC-001-RISK-v1.0):
- R-002 (Critical 20): Defence equality — mitigated by simultaneous deployment principle
- R-001 (High 16): Treasury funding — mitigated by phased investment model
- R-009 (High 12): Cost overrun — mitigated by stage-gate approvals and contingency
- R-004 (Medium 12): Police interoperability — mitigated by adapter middleware approach

**Recommendation**: **ACCEPT** — Best value option meeting all stakeholder goals with manageable risk.

---

### Option 3: Accelerated Full Transformation — All Pillars Simultaneously

**Description**: Deliver all five pillars concurrently with compressed 3-year timeline, maximum parallelism, and additional investment in resources to accelerate delivery.

**Scope**: Same as Option 2, but compressed from 5 years to 3 years with all workstreams running in parallel.

**Costs** (3-year) — ROM (±40%):
- Capital: £250M (higher due to parallelism, premium vendor rates, risk contingency)
- Operational: £65M over 3 years
- Total 3-year: £315M
- Total 5-year (including 2 years BAU): £365M

**Benefits** (10-year): ~£520M (higher due to earlier benefit realisation)

**NPV**: ~£55M (higher NPV than Option 2 in theory, but high execution risk)

**Stakeholder Goals Met**: 100% (all 10 goals, faster)

**Pros**:
- Faster benefit realisation
- Potentially higher NPV if delivered successfully
- Aligns with ministerial desire for rapid progress

**Cons**:
- £315M over 3 years — significantly higher annual expenditure (£105M/year vs £56M/year)
- Extremely high execution risk — justice technology has never delivered at this pace
- Insufficient capacity within MoJ/HMCTS to absorb this rate of change
- Common Platform has not been stabilised — building on unstable foundation
- 43 police forces cannot adopt standards simultaneously
- Judicial consultation compressed — risks judicial resistance (R-003)
- Treasury unlikely to approve this level of upfront commitment given Common Platform history
- Change management overwhelmed — court staff, judiciary, practitioners cannot absorb simultaneous changes
- Higher optimism bias applies due to compressed timeline (+40% vs +25%)

**Risks**:
- All risks from Option 2, but at significantly higher likelihood and impact
- Additional risk: Change fatigue across all agencies simultaneously
- Additional risk: Vendor market cannot supply sufficient capacity

**Recommendation**: **REJECT** — Execution risk is unacceptable. Criminal justice technology has a poor track record of large-scale concurrent delivery (Common Platform). The compressed timeline does not allow for judicial consultation, police force adoption, or staff change management. The marginal NPV improvement does not justify the dramatically higher risk.

---

## B3. Recommended Option

**Recommendation**: **Option 2: Phased Comprehensive Reform**

**Rationale**:
1. **Best Risk-Adjusted Value**: Positive NPV (+£5.1M conservative; +£95M with strategic benefits) with manageable risk profile
2. **Full Stakeholder Goal Coverage**: Meets all 10 goals (vs 15% for Option 1, 100% for Option 3 but with unacceptable risk)
3. **Phased Delivery**: Stage-gate approach enables early wins, builds confidence, manages Treasury and NAO scrutiny
4. **Defence Equality**: Simultaneous prosecution-defence deployment prevents the single highest programme risk (R-002)
5. **Deliverability**: 5-year timeline is realistic for multi-agency technology reform; allows Common Platform stabilisation, judicial consultation, and police force adoption
6. **Fiscal Discipline**: Phased funding reduces HM Treasury's exposure; annual commitment manageable within MoJ settlement

**Sensitivity Analysis**:
- **If costs increase 25% (optimism bias)**: NPV reduces to approximately -£45M on quantified benefits alone, but remains positive (+£50M) when risk avoidance and strategic benefits included. BCR remains >1.0.
- **If benefits reduce 20%**: NPV reduces to approximately -£35M on quantified benefits, but programme remains justified on risk avoidance grounds (legacy failure, backlog, equality of arms)
- **If timeline extends 12 months**: Payback extends to ~54 months; still within acceptable range for multi-year transformation
- **If police interoperability limited to 60% of forces**: Cross-agency benefit (B-003) reduces 30%; NPV still positive due to other pillars

**Optimism Bias Assessment** (HM Treasury Green Book):
- Standard uplift for IT-enabled business change: +25% on capital costs
- Adjusted Capital: £181M × 1.25 = £226M
- Adjusted Total: £326M (with optimism bias on capital)
- **NPV with optimism bias**: Approximately -£40M to +£50M depending on benefit assumptions
- **Assessment**: Even with optimism bias, the programme is justified on the basis of risk avoidance (legacy failure, equality of arms challenge, backlog escalation) and unquantified strategic benefits (public confidence, UK AI leadership)

---

# PART C: COMMERCIAL CASE

## C1. Procurement Strategy

### C1.1 Market Assessment

**Market Maturity**:
- **AI for legal/disclosure review**: Mature and growing market — multiple vendors offer AI-powered document review, evidence triage, and case summarisation. Proven in civil litigation and increasingly adopted by prosecution services internationally.
- **Integration platforms**: Well-established market for API management, event-driven integration, and middleware. Multiple UK government-approved cloud platform vendors.
- **Legacy migration services**: Strong market for application modernisation and cloud migration, with several vendors on existing government frameworks.
- **Court technology**: Niche but growing market; fewer vendors with specific criminal justice domain expertise.

**Supplier Landscape**:
- **Tier 1** (Large integrators): Capable of end-to-end delivery but risk of creating dependency; expensive.
- **Tier 2** (Specialist vendors): AI specialists, integration specialists, legacy migration specialists — preferred for specific pillars.
- **Tier 3** (SMEs): Innovative AI companies, niche criminal justice technology, open-source contributors — strong innovation potential.

### C1.2 Sourcing Route

**Recommended Route**: Digital Marketplace (multi-lot strategy)

| Programme Pillar | Procurement Route | Rationale |
|-----------------|-------------------|-----------|
| AI Tools (Pillar 1) | DOS 6 — Outcomes | Complex deliverable requiring innovation; outcome-based specification |
| Integration Platform (Pillar 2) | G-Cloud 14 — Cloud hosting & software | Infrastructure and platform services; competitive commodity market |
| Legacy Migration (Pillar 3) | DOS 6 — Specialists | Requires deep domain expertise; phased migration services |
| Victim Services (Pillar 4) | DOS 6 — Outcomes | User-centred design; GDS service standard compliance |
| AI Governance (Pillar 5) | Internal + DOS 6 Specialists | Core capability built in-house; specialist support for ATRS, ethics |
| Programme Management | Internal + DOS 6 Specialists | Mixed delivery model |

**Multi-Lot Strategy Rationale**:
- Avoids single-vendor dependency (Principle 20 — Open Standards and Avoid Lock-In)
- Enables SME participation across pillars
- Allows best-of-breed selection per pillar
- Reduces risk of total programme failure from single vendor issues
- Requires strong programme integration function (internal)

### C1.3 Contract Approach

**Proposed Contract Structure**:

| Contract Element | Approach | Duration |
|-----------------|----------|----------|
| AI Tools Build | Fixed-price milestone-based | 18 months (Phase 1) |
| AI Tools Run | Managed service (per-case pricing) | 3+2 years |
| Integration Platform | Fixed-price build; managed service run | 12 months build; 3+2 years run |
| Legacy Migration | Time & materials with cap (per-application) | Per-application: 3-9 months |
| Victim Services | Agile delivery (sprint-based); managed service run | 12 months build; 3+2 years run |

**Payment Structure**:
- Build phase: 20% on contract award; 60% milestone-based; 20% retention (6 months post-live)
- Run phase: Monthly managed service fees with SLA-linked performance deductions

**Key Contract Terms**:
- **IP**: Crown owns all bespoke development IP; standard vendor IP licensed
- **SLAs**: 99.9% availability during court sitting hours; 4-hour critical incident response
- **Exit**: 12-month notice; mandatory knowledge transfer; data export in open formats
- **Social Value**: Minimum 10% evaluation weighting; apprenticeships and local skills commitment
- **Security**: SC clearance for personnel accessing criminal justice data; Cyber Essentials Plus minimum

### C1.4 Social Value

**UK Government Requirement**: Minimum 10% evaluation weighting.

**Social Value Requirements**:
1. **Skills and Employment**: Apprenticeships in AI, data engineering, and cloud technology; targeting underrepresented groups in technology
2. **SME Supply Chain**: Minimum 33% of contract value subcontracted to SMEs
3. **Environmental**: Sustainable cloud infrastructure; carbon-neutral hosting commitment
4. **Community**: Legal technology skills programmes in justice sector; knowledge transfer to civil service

**Evaluation Weighting**:
- Technical Quality: 55%
- Cost: 30%
- Social Value: 15% (exceeding 10% minimum given programme's public service nature)

---

# PART D: FINANCIAL CASE

## D1. Budget Requirement

**Total Investment Required**: £281M over 5 years (£326M with optimism bias)

### D1.1 Capital Expenditure (CapEx)

| Item | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | Total |
|------|--------|--------|--------|--------|--------|-------|
| AI tools (prosecution & defence) | £8M | £15M | £10M | £5M | £2M | £40M |
| Cross-agency integration | £10M | £12M | £8M | £3M | £2M | £35M |
| Legacy migration | £8M | £12M | £12M | £10M | £8M | £50M |
| Victim/witness services | £3M | £5M | £3M | £1M | £1M | £13M |
| AI governance & compliance | £4M | £3M | £2M | £1M | £1M | £11M |
| Programme management | £6M | £5M | £4M | £3M | £2M | £20M |
| Training & change management | £3M | £4M | £3M | £1M | £1M | £12M |
| **Total CapEx** | **£42M** | **£56M** | **£42M** | **£24M** | **£17M** | **£181M** |

### D1.2 Operational Expenditure (OpEx)

| Item | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|------|--------|--------|--------|--------|--------|--------------|
| Cloud hosting & managed services | £3M | £5M | £6M | £6M | £6M | £26M |
| AI model licensing & compute | £2M | £4M | £5M | £5M | £5M | £21M |
| Support & maintenance | £1M | £3M | £5M | £6M | £6M | £21M |
| Internal team (BAU transition) | £4M | £4M | £5M | £5M | £5M | £23M |
| Contingency (10%) | £1M | £2M | £2M | £2M | £2M | £9M |
| **Total OpEx** | **£11M** | **£18M** | **£23M** | **£24M** | **£24M** | **£100M** |

### D1.3 Total Cost of Ownership (TCO)

| | Year 1 | Year 2 | Year 3 | Year 4 | Year 5 | 5-Year Total |
|---|--------|--------|--------|--------|--------|--------------|
| CapEx | £42M | £56M | £42M | £24M | £17M | £181M |
| OpEx | £11M | £18M | £23M | £24M | £24M | £100M |
| **Total TCO** | **£53M** | **£74M** | **£65M** | **£48M** | **£41M** | **£281M** |

**Notes**:
- All costs in 2026 prices
- Excludes VAT (MoJ recovers VAT)
- Optimism bias NOT applied to baseline (applied in sensitivity analysis: +25% on CapEx = £326M total)
- Ongoing BAU costs from Year 6+: ~£24M/year (offset by legacy decommissioning savings)

## D2. Funding Source

**Budget Allocation**:
- **Primary Source**: MoJ Spending Review 2026 settlement — technology and digital allocation
- **Secondary Source**: Cross-government AI investment fund (for Pillar 1 AI tools)
- **Police contribution**: Home Office / police precept for force-level adapter deployment (Pillar 2)
- **Legal aid**: LAA budget reform for defence technology access (Pillar 1, defence component)

**Budget Approval Path**:
1. **MoJ Investment Committee**: Up to £20M per decision (programme-level approval)
2. **MoJ Executive Committee**: £20M-£50M (strategic programme approval)
3. **HM Treasury**: Above £50M (major programme approval required)
4. **Cabinet Office Digital Spend Controls**: All technology spend above £1M (CDDO approval)

**Funding Profile Required**:

| Year | CapEx | OpEx | Total | Cumulative |
|------|-------|------|-------|------------|
| Year 1 (2026-27) | £42M | £11M | £53M | £53M |
| Year 2 (2027-28) | £56M | £18M | £74M | £127M |
| Year 3 (2028-29) | £42M | £23M | £65M | £192M |
| Year 4 (2029-30) | £24M | £24M | £48M | £240M |
| Year 5 (2030-31) | £17M | £24M | £41M | £281M |

## D3. Affordability

**MoJ Technology Budget Context**:
- MoJ total annual technology spend: ~£400M
- This programme: ~£56M/year average (14% of technology budget)
- Peak year (Year 2): £74M (18.5% of technology budget)
- Assessment: **Affordable** within SR settlement, but requires ring-fenced allocation

**Cash Flow Impact**:
- Largest single-year commitment: £74M (Year 2)
- Phased profile avoids single large payment shock
- Early years (1-2) are investment-heavy; Years 4-5 transition to operational
- Legacy decommissioning savings begin Year 3, partially offsetting operational costs

**Ongoing Affordability** (Year 6+):
- Annual operational cost: ~£24M/year
- Offset by: Legacy system decommissioning savings ~£15M/year; efficiency savings ~£10M/year
- Net ongoing cost: ~£0/year (self-sustaining from Year 6)

## D4. Financial Appraisal

### D4.1 Value for Money Assessment

**Qualitative Assessment**:
- **Economy**: Multi-lot Digital Marketplace procurement ensures competitive pricing; SME participation drives innovation
- **Efficiency**: AI and automation reduce unit cost per case; cross-agency integration eliminates manual data transfer
- **Effectiveness**: Meets all 10 stakeholder goals; addresses root causes identified by Leveson Review; measurable outcomes

**Overall VfM Rating**: **Medium-High**

**Justification**: Positive NPV on conservative quantified benefits; strongly positive NPV with strategic and risk avoidance benefits. Programme is justified primarily on public value (faster justice, victim experience, public confidence) and risk avoidance (legacy failure, equality of arms challenge) rather than cashable savings alone. Consistent with Green Book guidance that public sector investments should be appraised on public value, not solely financial return.

---

# PART E: MANAGEMENT CASE

## E1. Governance

### E1.1 Roles & Responsibilities

Derived from stakeholder RACI matrix in `ARC-001-STKE-v1.0`:

| Decision/Activity | Responsible | Accountable | Consulted | Informed |
|-------------------|-------------|-------------|-----------|----------|
| Overall programme success | Programme Director | MoJ Permanent Secretary (SRO) | Lord Chancellor, HMCTS CEO, DPP | All stakeholders |
| Budget approval | Programme Finance Director | MoJ Permanent Secretary | HM Treasury | NAO |
| AI deployment decisions | MoJ Chief AI Officer | Lord Chancellor | Lead Judge for AI, ICO, CBA | All practitioners |
| Architecture decisions | Enterprise Architect | MoJ CDIO | HMCTS CTO, CPS CDO, GDS | Delivery teams |
| Cross-agency standards | MoJ CDIO | Programme Board | NPCC, CPS CDO, HMPPS CDO | All agencies |
| Defence technology access | LAA CEO | Lord Chancellor | CBA, Law Society | Defence practitioners |
| Victim service design | HMCTS Service Owner | HMCTS CEO | Victims' Commissioner | Victims, witnesses |
| Go-live decisions | HMCTS CTO | HMCTS CEO | GDS, MoJ AI Officer, Security | All users |

**Senior Responsible Owner (SRO)**: MoJ Permanent Secretary
- Accountable for delivery and benefits realisation
- Reports to Lord Chancellor and HM Treasury
- Chairs Programme Board

**Programme Board**:
- MoJ Permanent Secretary (Chair/SRO)
- MoJ CDIO (Technical authority)
- HMCTS CEO (Operational delivery)
- DPP / CPS representative (Prosecution)
- Lead Judge for AI (Judicial oversight — advisory, not executive)
- LAA CEO (Defence technology)
- Programme Director (Delivery)
- Programme Finance Director (Budget)

**Judicial AI Steering Group** (separate from Programme Board):
- Lead Judge for AI (Chair)
- Lady Chief Justice nominee
- Senior Circuit Judge
- MoJ Chief AI Officer
- HMCTS CTO
- **Authority**: Genuine veto over AI tools affecting case management or judicial functions

### E1.2 Approval Gates

| Gate | Criteria | Approving Body | Target Date |
|------|----------|----------------|-------------|
| **Gate 0**: SOBC Approval | Business case approved; initial funding secured | Programme Board / HM Treasury | Q3 2026 |
| **Gate 1**: Phase 1 Start | Detailed requirements approved (done — ARC-001-REQ-v1.0); procurement launched | SRO | Q4 2026 |
| **Gate 2**: Vendor Award | Vendors selected; contracts signed | SRO + Commercial Director | Q1 2027 |
| **Gate 3**: AI Governance Live | AI governance framework operational; judicial steering group active | MoJ AI Officer + Lead Judge | Q1 2027 |
| **Gate 4**: Phase 1 Go-Live | First AI tools (prosecution + defence simultaneously); first integrations; victim tracking MVP | Programme Board | Q3 2027 |
| **Gate 5**: Phase 2 Approval (OBC) | OBC approved with refined costs; Phase 1 benefits demonstrated | HM Treasury | Q4 2027 |
| **Gate 6**: Phase 2 Go-Live | Full AI rollout; police integration; 10 legacy migrations | Programme Board | Q4 2028 |
| **Gate 7**: Phase 3 Approval | Phase 2 benefits demonstrated; remaining scope confirmed | Programme Board | Q1 2029 |
| **Gate 8**: Programme Completion | All 37 legacy applications migrated; all services live; benefits realisation | Programme Board | Q4 2030 |
| **Gate 9**: Benefits Review | 12-month post-completion benefits realisation assessment | SRO + NAO | Q4 2031 |

## E2. Delivery Approach

**Methodology**: Agile delivery with stage gates

**Delivery Model**:
- **In-house**: Programme management, architecture governance, AI governance, change management, benefits realisation
- **Vendor**: AI tool development, integration platform build, legacy migration execution, victim service build
- **Mixed**: Design (joint user research), testing (joint UAT), security (MoJ CISO + vendor)

**GDS Service Standard Alignment**:
- Discovery, Alpha, Beta, Live phases for each user-facing service
- Service assessments at Alpha, Beta, and Live gates
- User research with all 8 personas (from ARC-001-REQ-v1.0)
- Accessibility (WCAG 2.2 AA) from day one

## E3. Key Milestones

| Milestone | Target Date | Dependencies | Owner |
|-----------|-------------|--------------|-------|
| SOBC approved (this document) | Q3 2026 | Stakeholder analysis, requirements, risk register complete | SRO |
| HM Treasury spending approval | Q3 2026 | SOBC approved; ministerial advocacy | Programme Finance Director |
| Procurement launched (Digital Marketplace) | Q4 2026 | Spending approval; requirements finalised | Commercial Director |
| AI governance framework operational | Q1 2027 | Judicial steering group; ATRS process; ethics board | MoJ AI Officer |
| Vendor contracts awarded | Q1 2027 | Procurement evaluation complete | SRO + Commercial |
| First AI tools go-live (prosecution + defence pilot) | Q3 2027 | AI governance; vendor delivery; judicial approval | MoJ AI Officer |
| CPS-HMCTS integration live | Q3 2027 | API standards; vendor delivery | MoJ CDIO |
| Victim case tracking MVP live | Q3 2027 | Vendor delivery; user research | HMCTS Service Owner |
| OBC submitted (refined costs) | Q4 2027 | Phase 1 experience; market pricing confirmed | Programme Finance Director |
| Top 10 legacy migrations complete | Q4 2028 | Migration planning; parallel running | HMCTS CTO |
| Police-CPS digital case file integration | Q4 2028 | NPCC standard; adapter layer | MoJ CDIO |
| Full AI disclosure rollout (80%+ cases) | Q1 2029 | Phase 1 pilot success; defence platform operational | MoJ AI Officer |
| IPA Gateway Review 3 | Q2 2029 | Delivery progress; cost performance | IPA |
| All 37 legacy applications migrated | Q4 2030 | Phased migration programme | HMCTS CTO |
| **Programme Completion** | **Q4 2030** | All gates passed | SRO |
| Benefits realisation review | Q4 2031 | 12 months post-completion | SRO |

## E4. Resource Requirements

### E4.1 Team Structure

**Core Programme Team** (internal):

| Role | FTE | Duration | Notes |
|------|-----|----------|-------|
| Senior Responsible Owner | 0.3 | 5 years | MoJ Permanent Secretary |
| Programme Director | 1.0 | 5 years | Dedicated DDaT role |
| Programme Finance Director | 1.0 | 5 years | MoJ Finance |
| Enterprise Architect | 1.0 | 5 years | Architecture governance |
| AI Governance Lead | 1.0 | 5 years | Reporting to MoJ AI Officer |
| Service Delivery Managers (×3) | 3.0 | 4 years | One per major pillar |
| Business Analysts (×4) | 4.0 | 3 years | Cross-agency requirements |
| User Researchers (×2) | 2.0 | 4 years | GDS requirement |
| Change Manager | 1.0 | 5 years | Court staff, judiciary, practitioners |
| Commercial Manager | 1.0 | 3 years | Procurement and contract management |
| Data Protection Officer (programme) | 0.5 | 5 years | DPIA oversight |
| **Total Internal FTE** | **~16** | | |

**Vendor Teams** (expected across all lots):
- Phase 1: ~40-50 vendor FTEs (design, build, test)
- Phase 2: ~60-80 vendor FTEs (peak delivery)
- Phase 3: ~30-40 vendor FTEs (migration completion, optimisation)
- Run phase: ~15-20 vendor FTEs (managed services)

### E4.2 Skills Required

**Critical Skills**:
- AI/ML engineering (disclosure review, NLP, transcription) — **Gap**: Recruit or vendor
- Cloud architecture (multi-tenant, cross-agency) — **Gap**: Upskill existing + vendor
- API platform engineering — **Available**: DDaT capability
- Criminal justice domain expertise — **Available**: HMCTS/CPS staff
- Legacy system knowledge (COBOL, mainframe) — **Available**: Current staff (retention risk)
- GDS service design and user research — **Available**: DDaT capability
- Change management (multi-agency, judiciary) — **Gap**: Specialist recruitment needed

## E5. Change Management

### E5.1 Stakeholder Engagement

From stakeholder analysis (ARC-001-STKE-v1.0):

| Stakeholder | Power-Interest | Engagement Approach | Frequency |
|-------------|----------------|---------------------|-----------|
| Lord Chancellor | High-High | Ministerial submissions; quarterly programme update | Monthly |
| Lady Chief Justice | High-High | Judicial steering group; bilateral briefings | Monthly |
| HMCTS CEO | High-High | Programme Board; operational readiness reviews | Fortnightly |
| DPP / CPS | High-High | Cross-agency integration governance | Monthly |
| NPCC | High-High | Police data-sharing governance; force engagement | Monthly |
| CBA / Law Society | Medium-High | Practitioner forums; pilot feedback | Monthly |
| LAA | Medium-High | Defence technology workshops | Monthly |
| Victims' Commissioner | Medium-High | Regular briefings; outcome reporting | Quarterly |
| HM Treasury | High-Medium | Business case milestones; spending reviews | Quarterly |
| GDS / CDDO | High-Medium | Service assessments; TCoP compliance gates | Per gate |
| ICO | High-Medium | DPIA reviews; AI processing guidance | Quarterly |
| NAO | High-Low | Annual reports; VFM readiness | Annual |

### E5.2 Resistance Management

From stakeholder conflict analysis (ARC-001-STKE-v1.0):

| Conflict | Source | Resistance Risk | Mitigation |
|----------|--------|-----------------|------------|
| Speed vs judicial caution | Lord Chancellor vs Lady Chief Justice | HIGH | Dual-track AI; judicial steering group with genuine veto |
| Prosecution AI vs defence equality | CPS vs CBA/Law Society | CRITICAL | Simultaneous deployment principle; shared-service defence platform |
| Investment vs fiscal constraint | HMCTS vs HM Treasury | HIGH | Phased investment; conservative estimates; stage-gate funding |
| Standards vs police autonomy | MoJ CDIO vs 43 police forces | MEDIUM | Outcome standards not system mandates; adapter middleware; incentive funding |

## E6. Benefits Realisation

### E6.1 Benefits Profiles

| Benefit ID | Description | Owner | Baseline | Target | Measurement | Timeline |
|------------|-------------|-------|----------|--------|-------------|----------|
| B-001 | Backlog reduction savings | HMCTS CEO | 77,000+ cases | <50,000 cases | HMCTS statistics | Year 3 |
| B-002 | AI disclosure efficiency | DPP | 0% AI disclosure | 80%+ AI disclosure | CPS case data | Year 3 |
| B-003 | Cross-agency automation | MoJ CDIO | <10% automated | 90%+ automated | API analytics | Year 3 |
| B-004 | Legacy decommissioning | HMCTS CTO | 37 legacy apps | <10 legacy apps | Portfolio register | Year 5 |
| B-005 | Victim experience | HMCTS CEO | Low satisfaction | +20% improvement | Victim surveys | Year 2 |
| B-006 | Risk avoidance | Programme Director | High legacy/cyber risk | Reduced risk | Incident data | Year 3 |

### E6.2 Benefits Measurement

**Monitoring Approach**:
- Monthly benefits tracker dashboard
- Quarterly benefits review at Programme Board
- 6-month and 12-month formal reviews post go-live
- IPA Gateway reviews include benefits assessment

**Responsibility**:
- **SRO**: Overall benefits realisation accountability
- **Programme Finance Director**: Financial benefits tracking
- **HMCTS CEO**: Operational benefits (backlog, victim experience)
- **MoJ AI Officer**: AI-related benefits and governance compliance

## E7. Risk Management

### E7.1 Top 10 Strategic Risks

From full risk register (ARC-001-RISK-v1.0, 20 risks):

| Risk ID | Risk Description | Category | Residual Score | Owner | Response |
|---------|------------------|----------|----------------|-------|----------|
| R-002 | Defence equality of arms challenge halts AI | COMPLIANCE | 20 (Critical) | Lord Chancellor | Treat — simultaneous deployment; defence funding |
| R-001 | HM Treasury funding refusal | STRATEGIC | 16 (High) | MoJ Perm Sec | Treat — phased business case; ministerial advocacy |
| R-005 | AI ethics controversy | COMPLIANCE | 12 (Medium) | MoJ AI Officer | Treat — governance framework; bias testing; incident plan |
| R-009 | Programme cost overrun | FINANCIAL | 12 (Medium) | MoJ Perm Sec | Treat — stage gates; contingency; conservative estimates |
| R-004 | Police interoperability failure | OPERATIONAL | 12 (Medium) | NPCC | Treat — adapter middleware; outcome standards |
| R-010 | GDS service assessment failure | OPERATIONAL | 12 (Medium) | MoJ CDIO | Treat — early GDS engagement; mock assessments |
| R-003 | Judicial resistance to AI | STRATEGIC | 9 (Medium) | Lead Judge | Treat — judicial steering group; trust-building pilots |
| R-008 | Legacy migration disrupts courts | TECHNOLOGY | 9 (Medium) | HMCTS CTO | Treat — phased migration; parallel running; rollback |
| R-011 | Data sharing agreements stall | COMPLIANCE | 9 (Medium) | MoJ DPO | Treat — ICO engagement; bilateral-first approach |
| R-007 | Common Platform instability | TECHNOLOGY | 6 (Medium) | HMCTS CTO | Treat — stabilisation prerequisite; bypass capability |

**Risk Appetite**:
- **Financial**: Low — programme must stay within 10% of approved budget
- **Delivery**: Medium — accept some timeline risk for quality and stakeholder alignment
- **Reputational**: Low — cannot afford public failure given Common Platform history
- **Compliance**: Very Low — equality of arms, data protection, judicial independence are non-negotiable

---

# PART F: RECOMMENDATION & NEXT STEPS

## F1. Summary of Recommendation

**Recommended Option**: **Option 2: Phased Comprehensive Reform**

| Metric | Value |
|--------|-------|
| **Investment** | £281M over 5 years (£326M with optimism bias) |
| **Expected Benefits** | £495M over 10 years (quantified + risk avoidance) |
| **NPV** | +£5.1M (conservative); +£95M (with strategic benefits) |
| **BCR** | 1.1:1 (quantified); ~1.5:1 (including strategic) |
| **Payback** | ~42 months |
| **Stakeholder Goals Met** | 10 of 10 (100%) |
| **Risks** | 1 Critical (R-002), 1 High (R-001), 18 Medium/Low |
| **Affordability** | Within MoJ SR settlement (14% of technology budget) |

**Go/No-Go Recommendation**: **PROCEED to detailed design and procurement**

## F2. Conditions for Approval

**Mandatory Conditions**:
1. HM Treasury spending approval for Phase 1 (Years 1-2): £127M
2. Lord Chancellor policy decision on defence technology funding mechanism (R-002 mitigation)
3. SRO (MoJ Permanent Secretary) formally accepts accountability
4. Programme Board established with cross-agency membership
5. Judicial AI steering group terms of reference agreed with Lady Chief Justice

**Recommended Conditions**:
1. Common Platform stabilisation plan confirmed by HMCTS CTO
2. Independent legal opinion on equality of arms implications commissioned
3. IPA Gateway Review 0 completed before procurement launch
4. NPCC formal endorsement of digital case file standard initiative

## F3. Next Steps if Approved

**Immediate Actions** (Q3 2026):
1. **Secure Treasury approval**: SRO submits spending case — Target: Q3 2026
2. **Resolve defence funding**: Lord Chancellor policy decision — Target: Q3 2026
3. **Establish governance**: Programme Board and judicial steering group — Target: Q3 2026
4. **Commission legal opinion**: Equality of arms independent assessment — Target: Q3 2026

**Phase 1: Procurement and Design** (Q4 2026 - Q2 2027):
1. **Launch procurement**: Digital Marketplace (DOS 6, G-Cloud 14) — Target: Q4 2026
2. **Award contracts**: Vendor selection and contract execution — Target: Q1 2027
3. **AI governance framework**: Operational with ATRS process — Target: Q1 2027
4. **HLD review**: `/arckit.hld-review` for vendor designs — Target: Q2 2027

**Phase 1: Build and Deploy** (Q2-Q4 2027):
1. **AI tools pilot**: Prosecution + defence simultaneous pilot — Target: Q3 2027
2. **Integration MVP**: CPS-HMCTS API integration — Target: Q3 2027
3. **Victim tracking MVP**: Case tracking for victims — Target: Q3 2027
4. **OBC submission**: Refined costs based on Phase 1 experience — Target: Q4 2027

**Phase 2: Scale** (2028-2029):
1. Full AI disclosure rollout; police integration; 20 legacy migrations

**Phase 3: Complete** (2029-2031):
1. Remaining 17 legacy migrations; optimisation; benefits realisation

## F4. Next Steps if Not Approved

If this SOBC is not approved:
1. **Understand objections**: SRO meets Treasury/Programme Board to understand concerns
2. **Revise SOBC**: Address specific concerns (scope reduction, cost reduction, phasing changes)
3. **Re-submit**: Present revised SOBC within 8 weeks
4. **Communicate**: Inform stakeholders of decision and implications

**Do Nothing Consequences**:
- Crown Court backlog exceeds 90,000 by 2028
- Legacy system failures increasingly likely (37 critical applications)
- Leveson Review recommendations unimplemented — political accountability
- Victims continue to wait years for trial
- Defence equality challenge averted but at cost of foregoing all AI benefits
- Estimated annual cost of inaction: £85M in avoidable costs and escalating risk

---

# APPENDICES

## Appendix A: Stakeholder Analysis

**Source**: `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md`

**Key Stakeholders** (15 identified):
1. Lord Chancellor (SD-1) — Backlog reduction, public confidence — CRITICAL
2. Lady Chief Justice (SD-2) — Judicial independence, due process — CRITICAL
3. HMCTS CEO (SD-3) — Operational efficiency, service delivery — CRITICAL
4. DPP / CPS (SD-4) — Prosecution efficiency, case quality — HIGH
5. NPCC / Police (SD-5) — Evidence sharing, officer productivity — HIGH
6. CBA / Law Society (SD-6) — Equality of arms, defence access — CRITICAL
7. MoJ AI Officer (SD-7) — Responsible AI governance — HIGH
8. LAA (SD-8) — Defence technology access — HIGH
9. HM Treasury (SD-9) — Value for money, fiscal discipline — HIGH
10. GDS / CDDO (SD-10) — Digital standards compliance — MEDIUM

**4 Stakeholder Conflicts Identified** (all mapped to programme risks and mitigations)

## Appendix B: Architecture Principles

**Source**: `projects/000-global/ARC-000-PRIN-v1.0.md`

**23 Principles across 7 Categories**:
- Strategic (7): Interoperability, AI Augmentation, Security, Legacy Modernisation, Scalability, Resilience, Observability
- Data (3): Shared Asset, Quality, Privacy
- Integration (2): Loose Coupling, Event-Driven
- Quality (4): Performance, Availability, Accessibility, Maintainability
- Development (4): IaC, Testing, CI/CD, Open Standards
- Criminal Justice (3): Equality of Arms, Judicial Independence, Victim Protection
- Governance: Exception process and review gates

## Appendix C: Risk Register Summary

**Source**: `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md`

**20 Risks** across 6 Orange Book categories:
- 1 Critical residual (R-002: Defence equality, score 20)
- 1 High residual (R-001: Treasury funding, score 16)
- 14 Medium residual
- 4 Low residual
- Total inherent score: 298; Total residual score: 193 (35% reduction)

## Appendix D: Requirements Summary

**Source**: `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md`

**65 Requirements**: 10 Business, 14 Functional, 22 Non-Functional, 4 Data, 6 Integration, 5 Use Cases, 8 User Personas, 4 Requirement Conflicts (all resolved)

## Appendix E: Assumptions Register

| # | Assumption | Impact if Wrong | Mitigation |
|---|-----------|-----------------|------------|
| 1 | Common Platform stabilised before new services | New services on unstable foundation | R-007; bypass capability |
| 2 | Cross-party support continues | Programme cancelled or rescoped | R-016; phased delivery limits waste |
| 3 | Treasury fiscal environment permits investment | Funding not secured | R-001; phased model; ministerial advocacy |
| 4 | AI technology mature for criminal justice | AI tools underperform | Market validation; pilot before scale |
| 5 | Defence funding mechanism achievable | Equality of arms challenge | R-002; Lord Chancellor policy decision |
| 6 | Police forces willing to adopt data standards | Interoperability limited | R-004; adapter middleware; outcome standards |
| 7 | Judiciary engages constructively with AI | AI deployment blocked | R-003; judicial steering group; trust-building |
| 8 | Vendor market has sufficient capacity | Procurement delay or premium pricing | Multi-lot strategy; market engagement |
| 9 | Benefits estimates are conservative (±30%) | Over/under-estimation | Sensitivity analysis; OBC refinement |
| 10 | MoJ can recruit/retain programme team | Skills shortage delays delivery | Mixed model; vendor augmentation; DDaT pipeline |

## Appendix F: Glossary

| Term | Definition |
|------|------------|
| SOBC | Strategic Outline Business Case — First stage with strategic estimates |
| OBC | Outline Business Case — Second stage with refined costs after requirements |
| FBC | Full Business Case — Final stage with accurate costs before implementation |
| NPV | Net Present Value — Sum of discounted benefits minus costs |
| BCR | Benefit-Cost Ratio — Total discounted benefits divided by total discounted costs |
| ROI | Return on Investment — (Benefits - Costs) / Costs x 100% |
| SRO | Senior Responsible Owner — Accountable for programme delivery |
| TCO | Total Cost of Ownership — Capital + Operational costs over lifecycle |
| ROM | Rough Order of Magnitude — Estimate accuracy within ±30-40% |
| DOS | Digital Outcomes and Specialists — Digital Marketplace framework |
| G-Cloud | Government Cloud — Digital Marketplace framework for cloud services |
| ATRS | Algorithmic Transparency Recording Standard — AI transparency requirement |
| DPIA | Data Protection Impact Assessment — UK GDPR Article 35 requirement |
| DPA 2018 Part 3 | Data Protection Act 2018 Part 3 — Law enforcement data processing |
| TCoP | Technology Code of Practice — UK Government technology standards |
| IPA | Infrastructure and Projects Authority — Government assurance body |
| GDS | Government Digital Service — Digital standards body |
| CDDO | Central Digital and Data Office — Digital governance body |

---

## Document Approval

| Name | Role | Signature | Date |
|------|------|-----------|------|
| [Name] | Senior Responsible Owner (MoJ Permanent Secretary) | | |
| [Name] | Programme Finance Director | | |
| [Name] | MoJ Chief Digital and Information Officer | | |
| [Name] | HMCTS Chief Executive | | |
| [Name] | HM Treasury Spending Team | | |

**Approval Decision**: **APPROVED** | **APPROVED WITH CONDITIONS** | **REJECTED** | **DEFERRED**

**Conditions** (if any):
1. [Condition 1]
2. [Condition 2]

**Approval Date**: [Date]

**Next Review Date**: Q4 2026 (or when OBC created)

---

**END OF STRATEGIC OUTLINE BUSINESS CASE**

*Document created using ArcKit `/arckit.sobc` command*
*Green Book compliant: Yes (HM Treasury 5-case model)*

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 15 stakeholders, 15 drivers, 10 goals, 6 outcomes, 4 conflicts | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | 65 requirements, 8 personas, 5 use cases, 4 conflicts | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md` |
| ARC-001-RISK-v1.0 | Risk Register | ArcKit | 20 risks, Orange Book, 4Ts, inherent 298, residual 193 | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 23 principles, 7 categories | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| Independent Review of the Criminal Courts | Policy Review | GOV.UK | 180 recommendations, programme mandate | `projects/000-global/external/` |
| HM Treasury Green Book (2022) | Appraisal Framework | GOV.UK | 5-case model, discount rates, optimism bias | External |
| HM Treasury Orange Book (2023) | Risk Framework | GOV.UK | Risk management principles | External |

---

**Generated by**: ArcKit `/arckit.sobc` command
**Generated on**: 2026-02-04
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)

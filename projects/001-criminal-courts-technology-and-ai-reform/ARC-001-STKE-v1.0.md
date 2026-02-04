# Stakeholder Drivers & Goals Analysis: Criminal Courts Technology & AI Reform

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.stakeholders`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-STKE-v1.0 |
| **Document Type** | Stakeholder Drivers & Goals Analysis |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-04 |
| **Last Modified** | 2026-02-04 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-04 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, HMPPS Digital, Criminal Justice Technology Leadership |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial creation from `/arckit.stakeholders` command | PENDING | PENDING |

---

## Executive Summary

### Purpose
This document identifies key stakeholders across the criminal justice system, their underlying drivers (motivations, concerns, needs), how these drivers manifest into goals, and the measurable outcomes that will satisfy those goals. This analysis ensures stakeholder alignment and provides traceability from individual concerns to project success metrics for the Criminal Courts Technology & AI Reform programme.

### Key Findings
The criminal justice system involves an unusually complex stakeholder landscape spanning multiple independent agencies (MoJ, HMCTS, CPS, HMPPS, 43 police forces, judiciary), each with distinct operational pressures but deeply interdependent workflows. The dominant shared driver is clearing the 77,000+ Crown Court case backlog through technology-enabled efficiency, but significant tensions exist between speed-of-delivery pressures from ministers and the judiciary's insistence on preserving judicial independence in any AI deployment. The defence community (Criminal Bar Association, Law Society, Legal Aid Agency) represents a critical constituency whose concerns about equality of arms and access to justice must be addressed to avoid political and legal challenge.

### Critical Success Factors
- Cross-agency agreement on data standards and interoperability protocols
- Judiciary confidence that AI augmentation preserves judicial independence and due process
- Defence community trust that technology reforms deliver equality of arms, not just prosecution efficiency
- Sustained multi-year funding commitment aligned to HM Treasury Green Book business case approval
- Successful legacy system migration without disrupting live court operations

### Stakeholder Alignment Score
**Overall Alignment**: MEDIUM

While all stakeholders agree on the need to reduce the Crown Court backlog, fundamental tensions exist around pace of change (ministers want rapid delivery; judiciary and legal profession want careful, rights-respecting implementation), AI governance (prosecution agencies see productivity gains; defence community fears asymmetric advantage), and funding (HM Treasury requires robust business cases; operational agencies need investment upfront before benefits materialise). These tensions are manageable but require active governance.

---

## Stakeholder Identification

### Internal Stakeholders (Central Government / Justice System)

| Stakeholder | Role/Department | Influence | Interest | Engagement Strategy |
|-------------|----------------|-----------|----------|---------------------|
| Lord Chancellor / Secretary of State for Justice | MoJ — Ministerial lead, policy owner | HIGH | HIGH | Active involvement, ministerial submissions, decision authority |
| MoJ Permanent Secretary | MoJ — Accounting Officer | HIGH | HIGH | Governance board membership, business case approval |
| MoJ Chief Digital and Information Officer (CDIO) | MoJ Digital — Technology strategy | HIGH | HIGH | Architecture review board, technical decision authority |
| MoJ Chief AI Officer | MoJ — AI governance and ethics | HIGH | HIGH | AI assurance, ATRS compliance, ethics review |
| HMCTS Chief Executive | HMCTS — Operational delivery of courts | HIGH | HIGH | Programme board, operational requirements |
| HMCTS Chief Technology Officer | HMCTS Digital — Court systems delivery | HIGH | HIGH | Technical architecture, Common Platform evolution |
| Director of Public Prosecutions (DPP) | CPS — Prosecution technology strategy | HIGH | HIGH | Cross-agency integration, prosecution workflow |
| CPS Chief Digital Officer | CPS Digital — Case management systems | MEDIUM | HIGH | Integration requirements, data sharing |
| HMPPS Chief Digital Officer | HMPPS — Probation and prison systems | MEDIUM | MEDIUM | Sentence management integration, offender data |
| Legal Aid Agency (LAA) Chief Executive | LAA — Legal aid administration | MEDIUM | HIGH | Defence access to technology, equality of arms |
| GDS / CDDO | Cabinet Office — Digital standards | HIGH | MEDIUM | Service assessments, TCoP compliance |
| HM Treasury | HM Treasury — Spending authority | HIGH | MEDIUM | Business case approval, spending reviews |
| National Audit Office (NAO) | Parliament — Value for money oversight | HIGH | LOW | Post-implementation reviews, lessons learned |

### External Stakeholders

| Stakeholder | Organisation | Relationship | Influence | Interest |
|-------------|--------------|--------------|-----------|----------|
| Lady Chief Justice / Senior Judiciary | Judiciary of England and Wales | Constitutional independence | HIGH | HIGH |
| Lead Judge for AI and Technology | Judiciary — Technology oversight | HIGH | HIGH | AI governance, judicial approval |
| Criminal Bar Association (CBA) | Barristers — Defence representation | MEDIUM | HIGH | Equality of arms, practitioner access |
| Law Society | Solicitors — Defence representation | MEDIUM | HIGH | Legal aid technology, practitioner access |
| Magistrates' Association | Magistrates — Summary justice | MEDIUM | HIGH | Magistrates' court technology |
| National Police Chiefs' Council (NPCC) | 43 Police Forces — Investigation data | HIGH | HIGH | Evidence sharing, case file preparation |
| Victims' Commissioner | Independent — Victims' interests | MEDIUM | HIGH | Victim communication, case tracking |
| Information Commissioner's Office (ICO) | Regulator — Data protection | HIGH | MEDIUM | UK GDPR compliance, DPA 2018 Part 3 |
| Defendants and their representatives | Public — Justice recipients | LOW | HIGH | Fair trial rights, access to justice |
| Witnesses | Public — Justice participants | LOW | HIGH | Witness care, scheduling, remote evidence |

### Stakeholder Power-Interest Grid

```
                          INTEREST
              Low                         High
        ┌─────────────────────┬─────────────────────┐
        │                     │                     │
        │   KEEP SATISFIED    │   MANAGE CLOSELY    │
   High │                     │                     │
        │  • NAO              │  • Lord Chancellor   │
        │  • GDS/CDDO         │  • MoJ Perm Sec     │
        │  • HM Treasury      │  • MoJ CDIO         │
        │  • ICO              │  • MoJ AI Officer    │
 P      │                     │  • HMCTS CEO/CTO    │
 O      │                     │  • DPP/CPS          │
 W      │                     │  • Lady Chief Justice│
 E      │                     │  • Lead Judge AI     │
 R      │                     │  • NPCC              │
        ├─────────────────────┼─────────────────────┤
        │                     │                     │
        │      MONITOR        │    KEEP INFORMED    │
   Low  │                     │                     │
        │                     │  • CBA/Law Society  │
        │                     │  • Magistrates' Assn│
        │                     │  • LAA              │
        │                     │  • Victims' Commr   │
        │                     │  • Defendants       │
        │                     │  • Witnesses         │
        │                     │  • HMPPS            │
        └─────────────────────┴─────────────────────┘
```

| Stakeholder | Power | Interest | Quadrant | Engagement Strategy |
|-------------|-------|----------|----------|---------------------|
| Lord Chancellor | HIGH | HIGH | Manage Closely | Ministerial submissions, quarterly progress |
| MoJ Permanent Secretary | HIGH | HIGH | Manage Closely | Governance board, business case approval |
| MoJ CDIO | HIGH | HIGH | Manage Closely | Architecture review board, technical decisions |
| MoJ Chief AI Officer | HIGH | HIGH | Manage Closely | AI assurance gates, ATRS reviews |
| HMCTS CEO | HIGH | HIGH | Manage Closely | Programme board, operational readiness |
| HMCTS CTO | HIGH | HIGH | Manage Closely | Technical architecture, sprint reviews |
| DPP / CPS | HIGH | HIGH | Manage Closely | Cross-agency integration governance |
| Lady Chief Justice | HIGH | HIGH | Manage Closely | Judicial steering group, AI approval |
| Lead Judge for AI | HIGH | HIGH | Manage Closely | AI governance committee, pilot approval |
| NPCC | HIGH | HIGH | Manage Closely | Police data-sharing governance |
| HM Treasury | HIGH | MEDIUM | Keep Satisfied | Business case milestones, spending reviews |
| GDS / CDDO | HIGH | MEDIUM | Keep Satisfied | Service assessments, TCoP compliance gates |
| ICO | HIGH | MEDIUM | Keep Satisfied | DPIA reviews, compliance checkpoints |
| NAO | HIGH | LOW | Keep Satisfied | Annual reports, VFM readiness |
| CBA / Law Society | MEDIUM | HIGH | Keep Informed | Practitioner forums, pilot feedback |
| Magistrates' Association | MEDIUM | HIGH | Keep Informed | Consultation, pilot participation |
| LAA | MEDIUM | HIGH | Keep Informed | Requirements workshops, equality of arms |
| HMPPS | MEDIUM | MEDIUM | Keep Informed | Integration milestones, data sharing |
| Victims' Commissioner | MEDIUM | HIGH | Keep Informed | Regular briefings, outcome reporting |
| Defendants | LOW | HIGH | Keep Informed | Public consultations, rights impact assessments |
| Witnesses | LOW | HIGH | Keep Informed | User research, service design feedback |

---

## Stakeholder Drivers Analysis

### SD-1: Lord Chancellor / Secretary of State for Justice — Backlog Reduction and Public Confidence

**Stakeholder**: Lord Chancellor (Secretary of State for Justice)

**Driver Category**: STRATEGIC

**Driver Statement**: Reduce the 77,000+ outstanding Crown Court case backlog to restore public confidence in the criminal justice system and deliver on the Government's manifesto commitment to reform, while demonstrating responsible use of technology and AI.

**Context & Background**:
The Leveson Review was commissioned in response to a crisis: record Crown Court backlogs, victims waiting years for trial, and collapsed public confidence. The Lord Chancellor is politically accountable for delivering reform. The Review's 180 recommendations create an expectation of rapid, visible progress. Failure is a ministerial risk.

**Driver Intensity**: CRITICAL

**Enablers**:
- Sustained multi-year funding settlement from HM Treasury
- Cross-agency cooperation on technology integration
- Successful AI pilot programmes demonstrating efficiency gains
- Positive judicial engagement with technology reforms

**Blockers**:
- HM Treasury fiscal constraints limiting investment
- Judicial resistance to technology-imposed pace of change
- Legacy system failures disrupting court operations during migration
- Public controversy over AI use in criminal justice

**Related Stakeholders**:
- MoJ Permanent Secretary (accounting officer accountability)
- HMCTS CEO (operational delivery)
- Lady Chief Justice (judicial cooperation)
- HM Treasury (funding)

---

### SD-2: Lady Chief Justice / Senior Judiciary — Judicial Independence and Due Process

**Stakeholder**: Lady Chief Justice and senior judiciary

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure that all technology and AI deployments preserve judicial independence, the integrity of the trial process, and defendants' right to a fair trial. Technology must serve the court, not constrain judicial discretion.

**Context & Background**:
The judiciary is constitutionally independent from the executive. The Leveson Review explicitly states that AI must "augment rather than replace" judicial decision-making. Judges are cautious about predictive AI, automated scheduling that constrains listing decisions, and any system that appears to fetter judicial discretion. The Lead Judge for AI and Technology has been appointed to provide judicial oversight of technology deployments.

**Driver Intensity**: CRITICAL

**Enablers**:
- Judicial steering group with genuine authority over AI deployments
- Transparent AI governance with judicial veto on tools affecting case outcomes
- Positive pilot experiences demonstrating judicial benefit
- Training and support for judicial technology adoption

**Blockers**:
- Perception that technology reforms are executive-driven efficiency measures
- AI tools deployed without judicial consultation or approval
- Inadequate training or support for technology-resistant judges
- Systems that reduce judicial discretion in listing or case management

**Related Stakeholders**:
- Lord Chancellor (tension between speed and judicial caution)
- Lead Judge for AI (operational judicial oversight)
- MoJ Chief AI Officer (AI governance framework)
- Criminal Bar Association (shared concern about fairness)

---

### SD-3: HMCTS Chief Executive — Operational Efficiency and Service Delivery

**Stakeholder**: HMCTS Chief Executive and senior leadership

**Driver Category**: OPERATIONAL

**Driver Statement**: Modernise court operations to process cases faster, reduce administrative burden on court staff, and deliver reliable digital services, while managing the transition from legacy systems without disrupting live court operations.

**Context & Background**:
HMCTS operates 300+ court centres with a workforce under pressure from backlogs and outdated systems. The Common Platform rollout has been troubled, with user complaints and functionality gaps. Staff spend significant time on manual data entry, cross-system reconciliation, and workarounds. HMCTS needs technology that works reliably and reduces — not increases — operational burden.

**Driver Intensity**: CRITICAL

**Enablers**:
- Phased, low-risk migration approach with rollback capability
- Investment in staff training and change management
- Common Platform stabilisation before further expansion
- AI tools that demonstrably reduce administrative workload

**Blockers**:
- Forced "big bang" system migrations
- Technology deployments without adequate training and support
- Continued Common Platform instability eroding staff confidence
- Budget constraints preventing adequate parallel running during migration

**Related Stakeholders**:
- HMCTS CTO (technical delivery)
- Lord Chancellor (political pressure for pace)
- Court staff and HMCTS operational teams
- GDS/CDDO (service standard compliance)

---

### SD-4: Director of Public Prosecutions / CPS — Prosecution Efficiency and Case Quality

**Stakeholder**: Director of Public Prosecutions (DPP) and CPS leadership

**Driver Category**: OPERATIONAL

**Driver Statement**: Leverage AI and technology to improve case preparation quality, accelerate disclosure, reduce discontinued cases, and enable seamless data sharing with police and courts.

**Context & Background**:
CPS handles 500,000+ cases annually. Disclosure failures are a leading cause of collapsed trials. Case file preparation involves reviewing vast volumes of digital evidence (body-worn video, communications data, social media). The Leveson Review specifically recommends AI for disclosure review and case summarisation. CPS also needs seamless integration with police case management systems and court listings.

**Driver Intensity**: HIGH

**Enablers**:
- AI tools for automated disclosure review and digital evidence triage
- Standardised digital case file format across police and CPS
- Real-time case tracking integration with HMCTS
- Investment in CPS digital infrastructure

**Blockers**:
- Police forces using incompatible case management systems
- Defence concerns about AI-assisted prosecution creating inequality
- Data protection constraints on cross-agency data sharing
- Legacy CPS systems resistant to integration

**Related Stakeholders**:
- NPCC / Police forces (evidence sharing)
- Criminal Bar Association (disclosure fairness)
- HMCTS (case management integration)
- ICO (data protection compliance)

---

### SD-5: National Police Chiefs' Council (NPCC) / Police Forces — Evidence Sharing and Investigation Support

**Stakeholder**: NPCC and 43 police forces in England and Wales

**Driver Category**: OPERATIONAL

**Driver Statement**: Enable efficient digital evidence sharing with CPS and courts, reduce the burden of case file preparation on officers, and ensure interoperability despite 43 independently governed forces with different systems.

**Context & Background**:
Police forces operate independently with varied technology estates. The Leveson Review highlights that officers spend excessive time preparing case files, often manually transferring data between incompatible systems. Digital evidence volumes (body-worn video, phone data, CCTV) are growing exponentially. Forces need a standardised, automated approach to evidence packaging and sharing.

**Driver Intensity**: HIGH

**Enablers**:
- National data standards for digital case files
- Automated evidence packaging and transfer
- API-based integration avoiding mandated single systems
- Central funding for police technology upgrades

**Blockers**:
- 43 independently governed forces with procurement autonomy
- Multiple legacy case management systems (Niche, Connect, Athena, etc.)
- Limited central authority to mandate technology standards
- Budget pressures on individual forces

**Related Stakeholders**:
- CPS (primary consumer of police case files)
- HMCTS (evidence presentation at trial)
- Home Office (police funding and governance)
- ICO (evidence data protection)

---

### SD-6: Criminal Bar Association / Law Society — Equality of Arms and Practitioner Access

**Stakeholder**: Criminal Bar Association (CBA) and Law Society

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure that technology and AI reforms deliver genuine equality of arms — defence practitioners must have equivalent access to technology tools as prosecution agencies, particularly for disclosure review, case preparation, and digital evidence analysis.

**Context & Background**:
The Leveson Review's principle of "equality of arms" is fundamental to fair trial rights (Article 6 ECHR). If CPS deploys AI-assisted disclosure review and case summarisation while defence practitioners rely on manual processes and underfunded legal aid, the technology gap creates structural unfairness. The Criminal Bar has warned that AI-enhanced prosecution without equivalent defence capability would be constitutionally unacceptable.

**Driver Intensity**: CRITICAL

**Enablers**:
- Defence access programme providing equivalent AI tools
- Legal aid funding reform to support technology adoption
- Open-source or shared-service AI tools available to both sides
- Defence practitioner input into technology design

**Blockers**:
- Legal aid funding constraints preventing defence technology investment
- Prosecution-first deployment creating temporal inequality
- Proprietary AI tools available only to state agencies
- Lack of defence representation in technology governance

**Related Stakeholders**:
- LAA (legal aid funding for defence technology)
- CPS (prosecution technology parity)
- Judiciary (fair trial oversight)
- Lord Chancellor (policy responsibility)

---

### SD-7: MoJ Chief AI Officer — Responsible AI Governance

**Stakeholder**: MoJ Chief AI Officer

**Driver Category**: COMPLIANCE

**Driver Statement**: Establish robust AI governance ensuring all AI deployments comply with the UK AI Playbook, ATRS requirements, UK GDPR (DPA 2018 Part 3 for law enforcement), and ethical standards, while enabling beneficial AI adoption at pace.

**Context & Background**:
Criminal justice AI raises the highest category of ethical concern — decisions affecting liberty, fair trial rights, and vulnerable individuals. The MoJ Chief AI Officer must balance enabling AI productivity gains (transcription, translation, scheduling) with preventing harmful applications (predictive sentencing, automated charging decisions). The AI Playbook and ATRS framework provide governance rails but require operationalisation.

**Driver Intensity**: HIGH

**Enablers**:
- Clear AI categorisation framework (productivity / insight / accessibility / predictive)
- Mandatory ATRS registration for all AI tools
- Independent ethics review board with external membership
- Judicial approval gate for AI tools affecting case outcomes

**Blockers**:
- Pressure to deploy AI quickly before governance frameworks are mature
- Ambiguity in categorising AI use cases (e.g., does case summarisation affect outcomes?)
- Lack of in-house AI ethics and assurance expertise
- Vendor lock-in to proprietary AI systems limiting transparency

**Related Stakeholders**:
- Lead Judge for AI (judicial AI governance)
- Lord Chancellor (ministerial accountability)
- ICO (data protection in AI)
- GDS/CDDO (AI Playbook compliance)

---

### SD-8: Legal Aid Agency — Defence Technology Access and Legal Aid Reform

**Stakeholder**: Legal Aid Agency (LAA) Chief Executive

**Driver Category**: FINANCIAL

**Driver Statement**: Modernise legal aid administration and enable defence practitioners to access technology tools, while managing within constrained budgets and demonstrating value for money to HM Treasury.

**Context & Background**:
Legal aid funding has been cut substantially since LASPO 2012. Defence practitioners operate with minimal technology support. If the programme provides AI tools to prosecution but not defence, it creates inequality of arms. LAA must find funding mechanisms — whether through shared services, central provision, or legal aid rate reform — to ensure defence access.

**Driver Intensity**: HIGH

**Enablers**:
- Central provision of shared AI tools accessible to defence
- Legal aid fee reform to fund technology adoption
- Cloud-based defence technology platform
- Partnership with CBA and Law Society on requirements

**Blockers**:
- Constrained legal aid budgets
- HM Treasury resistance to legal aid funding increases
- Fragmented defence practitioner landscape (thousands of firms)
- Data security concerns with defence access to prosecution-grade tools

**Related Stakeholders**:
- CBA / Law Society (defence practitioner needs)
- Lord Chancellor (legal aid policy)
- HM Treasury (funding)
- MoJ CDIO (shared technology platform)

---

### SD-9: HM Treasury — Value for Money and Fiscal Discipline

**Stakeholder**: HM Treasury spending team

**Driver Category**: FINANCIAL

**Driver Statement**: Ensure that programme expenditure is justified by a robust Green Book business case with quantified benefits, phased investment aligned to delivery milestones, and credible cost-benefit analysis demonstrating value for taxpayer money.

**Context & Background**:
HM Treasury applies Green Book appraisal to all major spending proposals. Criminal justice technology has a poor track record — the Common Platform programme experienced significant cost overruns and scope reduction. Treasury will require a compelling business case, realistic cost estimates, and phased approval gates before releasing multi-year funding.

**Driver Intensity**: HIGH

**Enablers**:
- Robust Green Book business case with 5-case model
- Phased investment with stage-gate approvals
- Clear benefits realisation framework with quantified metrics
- Independent assurance (IPA Gateway reviews)

**Blockers**:
- Unrealistic cost estimates or optimism bias
- Inability to quantify benefits in monetary terms
- Poor track record of previous justice technology programmes
- Fiscal environment constraining departmental budgets

**Related Stakeholders**:
- MoJ Permanent Secretary (accounting officer)
- Lord Chancellor (political business case)
- NAO (post-implementation VFM review)
- HMCTS (operational benefits evidence)

---

### SD-10: GDS / CDDO — Digital Standards Compliance

**Stakeholder**: Government Digital Service / Central Digital and Data Office

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure all services meet the GDS Service Standard (14 points), comply with the Technology Code of Practice (TCoP), and follow government-mandated approaches to open standards, cloud-first, and accessibility.

**Context & Background**:
GDS service assessments are mandatory for all government digital services. TCoP compliance is required for technology spend approvals. Criminal justice services must be accessible (WCAG 2.2 AA), meet the service standard, and use open standards. Previous justice technology programmes have faced challenges at service assessments.

**Driver Intensity**: MEDIUM

**Enablers**:
- Early engagement with GDS assessment teams
- User research-driven design approach
- Open standards and cloud-first architecture
- Accessibility built in from the start

**Blockers**:
- Legacy system constraints preventing full compliance
- Specialist criminal justice requirements not well understood by GDS assessors
- Pace pressure conflicting with thorough service assessment preparation

**Related Stakeholders**:
- MoJ CDIO (technical compliance)
- HMCTS CTO (service delivery)
- All delivery teams (service standard adherence)

---

### SD-11: Information Commissioner's Office (ICO) — Data Protection Compliance

**Stakeholder**: Information Commissioner's Office

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure all data processing complies with UK GDPR and, for law enforcement processing, DPA 2018 Part 3. Particular attention to AI processing of criminal justice data (special category), automated decision-making safeguards, and cross-agency data sharing agreements.

**Context & Background**:
Criminal justice data is among the most sensitive categories — it includes data about suspects, defendants, victims, and witnesses, much of which constitutes special category data under UK GDPR. Law enforcement processing under DPA 2018 Part 3 has specific requirements. AI processing of this data requires Data Protection Impact Assessments (DPIAs), and any automated decision-making with legal effects requires human review safeguards.

**Driver Intensity**: HIGH

**Enablers**:
- Comprehensive DPIAs for all AI deployments
- Clear lawful bases for cross-agency data sharing
- Data Protection Officers embedded in programme governance
- Privacy-by-design architecture

**Blockers**:
- Cross-agency data sharing without proper legal frameworks
- AI processing without adequate impact assessment
- Automated decisions without human review safeguards
- Data retention policies that conflict across agencies

**Related Stakeholders**:
- MoJ Chief AI Officer (AI governance)
- All agencies sharing criminal justice data
- Defendants and their representatives (data subject rights)

---

### SD-12: Victims' Commissioner — Victim Experience and Communication

**Stakeholder**: Victims' Commissioner for England and Wales

**Driver Category**: CUSTOMER

**Driver Statement**: Ensure technology reforms improve the victim experience — better communication about case progress, reduced delays, support for vulnerable witnesses giving evidence remotely, and compliance with the Victims' Code.

**Context & Background**:
The Leveson Review identifies victim and witness experience as a critical outcome. Victims currently receive poor communication about case progress, face repeated adjournments, and endure years-long waits for trial. The Victims' Code sets service standards that are frequently unmet. Technology must demonstrably improve victim outcomes, not just system efficiency.

**Driver Intensity**: HIGH

**Enablers**:
- Real-time case tracking and notification for victims
- Automated Victims' Code compliance monitoring
- Remote evidence facilities for vulnerable witnesses
- Victim feedback mechanisms integrated into service design

**Blockers**:
- Technology focused solely on professional users, not victims/witnesses
- Lack of victim/witness user research in service design
- Privacy constraints on sharing case information with victims
- Fragmented victim support services across agencies

**Related Stakeholders**:
- HMCTS (court-based victim services)
- CPS (Victim Liaison Units)
- Police (initial victim contact)
- Witness Care Units

---

### SD-13: HMPPS — Sentence Management and Rehabilitation Integration

**Stakeholder**: HM Prison and Probation Service Chief Digital Officer

**Driver Category**: OPERATIONAL

**Driver Statement**: Integrate sentence management, probation supervision, and prison systems with court outcomes to ensure seamless transfer of sentencing data and support rehabilitation pathways.

**Context & Background**:
HMPPS manages the downstream consequences of court decisions. Currently, sentence calculation errors occur due to manual transfer of court data. Probation officers lack real-time access to court outcomes. Integration between court and prison/probation systems is essential for accurate sentence management and effective rehabilitation.

**Driver Intensity**: MEDIUM

**Enablers**:
- Real-time court outcome feeds to prison and probation systems
- Standardised sentence data format
- Integration with Common Platform for case outcomes
- Shared offender management data model

**Blockers**:
- HMPPS legacy systems (older than many court systems)
- Different data models and identifiers across agencies
- Lower priority relative to court-facing reforms
- Budget constraints within HMPPS

**Related Stakeholders**:
- HMCTS (source of court outcomes)
- Judiciary (sentencing data accuracy)
- LAA (post-sentence legal aid)

---

### SD-14: Magistrates' Association — Summary Justice Technology

**Stakeholder**: Magistrates' Association

**Driver Category**: OPERATIONAL

**Driver Statement**: Ensure technology reforms address magistrates' courts (which handle 95% of criminal cases), not just Crown Court, and provide magistrates with modern, user-friendly digital tools for case management.

**Context & Background**:
Media and political attention focuses on Crown Court backlogs, but magistrates' courts handle the vast majority of criminal cases. Magistrates are unpaid volunteers who need intuitive technology. The Common Platform has been criticised for poor usability in magistrates' courts. Technology reforms must not neglect summary justice.

**Driver Intensity**: MEDIUM

**Enablers**:
- User research with magistrates informing design
- Simplified interfaces for non-professional judicial users
- Training and support for volunteer magistrates
- Investment in magistrates' court technology alongside Crown Court

**Blockers**:
- Crown Court backlog dominating political attention and funding
- Complex technology designed for professional users
- Insufficient training provision for volunteer magistrates
- Magistrates' courts closures reducing access to justice

**Related Stakeholders**:
- HMCTS (court operations)
- Judiciary (magistrates' oversight)
- Defendants (majority experience magistrates' courts)

---

### SD-15: National Audit Office — Accountability and Lessons Learned

**Stakeholder**: National Audit Office (NAO)

**Driver Category**: COMPLIANCE

**Driver Statement**: Ensure the programme demonstrates proper use of public funds, learns from the failures of previous justice technology programmes (particularly Common Platform), and maintains auditable decision trails.

**Context & Background**:
The NAO has been critical of previous justice technology programmes. The Common Platform programme was the subject of a critical PAC hearing. The NAO will expect the programme to demonstrate that lessons have been learned, governance is robust, and benefits are being realised as claimed in the business case.

**Driver Intensity**: MEDIUM

**Enablers**:
- Auditable decision records and architecture decision records (ADRs)
- Benefits realisation tracking with independent verification
- Lessons learned register from Common Platform and other programmes
- IPA Gateway review compliance

**Blockers**:
- Repeating Common Platform mistakes (scope creep, unrealistic timelines)
- Inadequate benefits tracking
- Governance gaps allowing unchallenged decisions
- Poor documentation of architectural and procurement decisions

**Related Stakeholders**:
- HM Treasury (spending authority)
- MoJ Permanent Secretary (accounting officer)
- Public Accounts Committee (parliamentary oversight)

---

## Driver-to-Goal Mapping

### Goal G-1: Reduce Crown Court Outstanding Caseload

**Derived From Drivers**: SD-1, SD-3, SD-4, SD-12

**Goal Owner**: HMCTS Chief Executive

**Goal Statement**: Reduce the outstanding Crown Court caseload from 77,000+ to below 50,000 cases within 3 years through technology-enabled efficiency improvements, without compromising the quality of justice.

**Why This Matters**: Directly addresses the Lord Chancellor's political imperative, HMCTS's operational pressure, CPS's case throughput needs, and victims' experience of unacceptable delays.

**Success Metrics**:
- **Primary Metric**: Outstanding Crown Court caseload count (published quarterly by HMCTS)
- **Secondary Metrics**:
  - Average time from charge to trial completion
  - Proportion of effective trials (not adjourned/cracked)
  - Victim satisfaction with timeliness

**Baseline**: 77,000+ outstanding cases (2025-26)
**Target**: Below 50,000 outstanding cases by 2028-29
**Measurement Method**: HMCTS published statistics, Criminal Court Statistics Quarterly

**Dependencies**:
- Sitting day allocation (judicial and court availability)
- Successful deployment of AI case preparation tools
- Cross-agency interoperability reducing administrative delays

**Risks to Achievement**:
- New case volumes exceeding capacity gains
- Technology deployment delays
- Judicial or practitioner resistance slowing adoption

---

### Goal G-2: Deploy AI-Assisted Disclosure and Case Preparation

**Derived From Drivers**: SD-4, SD-5, SD-7, SD-11

**Goal Owner**: Director of Public Prosecutions (CPS)

**Goal Statement**: Deploy AI-assisted tools for disclosure review, digital evidence triage, and case summarisation across all CPS areas within 2 years, with full ATRS registration and DPIA compliance.

**Why This Matters**: Disclosure failure is the leading cause of collapsed trials. AI can process volumes of digital evidence that are impossible for humans to review manually within current timescales. This directly supports case throughput and trial effectiveness.

**Success Metrics**:
- **Primary Metric**: Percentage of cases using AI-assisted disclosure review
- **Secondary Metrics**:
  - Disclosure-related case collapses (reduction)
  - Average disclosure review time per case
  - ATRS registration compliance rate

**Baseline**: Near-zero AI-assisted disclosure (2025-26)
**Target**: 80%+ of Crown Court cases using AI-assisted disclosure by 2028
**Measurement Method**: CPS case management data, ATRS register

**Dependencies**:
- AI governance framework approval (MoJ Chief AI Officer)
- Judicial approval for AI use in disclosure (Lead Judge for AI)
- Data sharing agreements with police forces
- Defence access to equivalent tools (equality of arms — SD-6)

**Risks to Achievement**:
- AI errors in disclosure causing miscarriage of justice
- Defence challenge to AI-assisted disclosure on fairness grounds
- Police data quality insufficient for AI processing
- Vendor lock-in to proprietary AI systems

---

### Goal G-3: Deliver Defence Access to AI Tools (Equality of Arms)

**Derived From Drivers**: SD-6, SD-8, SD-2

**Goal Owner**: Legal Aid Agency Chief Executive

**Goal Statement**: Provide defence practitioners with access to AI-assisted case preparation, disclosure review, and evidence analysis tools equivalent in capability to those available to prosecution, funded through reformed legal aid mechanisms or central provision.

**Why This Matters**: Without defence parity, AI-enhanced prosecution creates structural unfairness that is constitutionally unacceptable and will face legal challenge. The Leveson Review's equality of arms principle requires simultaneous defence capability.

**Success Metrics**:
- **Primary Metric**: Percentage of defence practitioners with access to AI case preparation tools
- **Secondary Metrics**:
  - Defence practitioner satisfaction with technology tools
  - Legal challenge rate on technology inequality grounds
  - Legal aid technology expenditure per case

**Baseline**: Minimal defence technology access (2025-26)
**Target**: 70%+ of criminal defence practitioners with AI tool access by 2028
**Measurement Method**: LAA provider surveys, tool usage analytics

**Dependencies**:
- Funding mechanism for defence technology (legal aid reform or central provision)
- Shared or open-source AI tools suitable for defence use
- Data security model allowing defence access
- CBA and Law Society engagement in requirements

**Risks to Achievement**:
- Legal aid funding insufficient for technology investment
- Prosecution deploys AI years before defence equivalent available
- Defence practitioner fragmentation preventing unified technology approach
- Data protection barriers to defence access

---

### Goal G-4: Achieve Cross-Agency Interoperability

**Derived From Drivers**: SD-1, SD-3, SD-4, SD-5, SD-13

**Goal Owner**: MoJ Chief Digital and Information Officer

**Goal Statement**: Establish API-based interoperability between police, CPS, HMCTS, HMPPS, and LAA systems for case data, evidence, and outcomes, replacing manual data transfer and eliminating duplicate data entry.

**Why This Matters**: Fragmented systems cause delays, errors, and wasted effort across the entire criminal justice chain. Interoperability is the single most impactful technical enabler for efficiency.

**Success Metrics**:
- **Primary Metric**: Percentage of case data exchanged via automated API integration (vs. manual)
- **Secondary Metrics**:
  - Data rekeying incidents per month
  - Average time for case data to transfer between agencies
  - Number of live API integrations between agencies

**Baseline**: Limited automated integration, extensive manual data transfer (2025-26)
**Target**: 90%+ of case data exchanged automatically by 2029
**Measurement Method**: API gateway analytics, user surveys, error reports

**Dependencies**:
- Cross-agency data standards agreement
- API catalogue and governance framework
- Data sharing agreements (DAPF) between all agencies
- Legacy system capability to expose APIs (or middleware/adapter layer)

**Risks to Achievement**:
- 43 police forces unable to agree common standards
- Legacy systems incapable of API integration without replacement
- Data governance disagreements blocking sharing agreements
- Insufficient central authority to mandate interoperability

---

### Goal G-5: Migrate 37 Critical Legacy Applications

**Derived From Drivers**: SD-3, SD-9, SD-15

**Goal Owner**: HMCTS Chief Technology Officer

**Goal Statement**: Complete assessment and begin phased migration of 37 critical legacy applications identified by the Leveson Review, prioritised by risk and business impact, with zero unplanned disruption to live court operations.

**Why This Matters**: Legacy applications represent the greatest technical risk — unsupported platforms, single points of failure, inability to integrate with modern systems. Migration is essential for sustainability but must not disrupt courts.

**Success Metrics**:
- **Primary Metric**: Number of legacy applications migrated or decommissioned
- **Secondary Metrics**:
  - Legacy-related incidents per quarter
  - Percentage of applications on supported platforms
  - Migration cost vs. business case estimates

**Baseline**: 37 critical legacy applications on unsupported or end-of-life platforms
**Target**: 20+ applications migrated/decommissioned within 3 years; all 37 within 5 years
**Measurement Method**: Application portfolio register, incident management data

**Dependencies**:
- Application assessment and prioritisation complete
- Phased migration plan with rollback capability
- Parallel running budget during transitions
- Staff training for replacement systems

**Risks to Achievement**:
- Undocumented legacy system dependencies causing unexpected failures
- Insufficient budget for parallel running
- Staff resistance to new systems
- Data migration errors

---

### Goal G-6: Establish AI Governance Framework

**Derived From Drivers**: SD-2, SD-7, SD-10, SD-11

**Goal Owner**: MoJ Chief AI Officer

**Goal Statement**: Establish and operationalise an AI governance framework for criminal justice that includes mandatory categorisation, ATRS registration, DPIA, judicial approval gates for case-affecting AI, and independent ethics review, within 12 months.

**Why This Matters**: AI governance must be established before large-scale AI deployment. Without it, individual AI deployments will face legal challenge, regulatory action, or public backlash. The framework provides the guardrails that enable beneficial AI adoption at pace.

**Success Metrics**:
- **Primary Metric**: AI governance framework published and operational
- **Secondary Metrics**:
  - Percentage of AI tools with ATRS registration
  - Percentage of AI tools with approved DPIA
  - Number of AI ethics review decisions made
  - Judicial AI steering group operational

**Baseline**: No operationalised criminal justice AI governance framework (2025-26)
**Target**: Framework operational within 12 months; all AI deployments compliant within 18 months
**Measurement Method**: Governance register, ATRS compliance audit

**Dependencies**:
- Judicial steering group established
- MoJ AI categorisation taxonomy agreed
- Ethics review board appointed with external members
- ATRS process operationalised for criminal justice context

**Risks to Achievement**:
- Governance perceived as blocking beneficial AI adoption
- Disagreement between judicial and executive stakeholders on AI boundaries
- Insufficient AI ethics expertise within MoJ
- Evolving regulatory landscape (EU AI Act influence on UK approach)

---

### Goal G-7: Improve Victim and Witness Experience

**Derived From Drivers**: SD-12, SD-1, SD-3

**Goal Owner**: HMCTS Chief Executive (with Victims' Commissioner oversight)

**Goal Statement**: Implement real-time case tracking for victims, automated Victims' Code compliance monitoring, and enhanced remote evidence facilities, achieving measurable improvement in victim satisfaction within 2 years.

**Why This Matters**: Victims and witnesses are the most directly affected stakeholders but have the least power. Improving their experience is both a moral imperative and a legal obligation under the Victims' Code. It also supports trial effectiveness (witness attendance, evidence quality).

**Success Metrics**:
- **Primary Metric**: Victim satisfaction score (Crime Survey / HMCTS survey)
- **Secondary Metrics**:
  - Percentage of victims receiving timely case updates
  - Victims' Code compliance rate
  - Remote evidence facility availability and usage
  - Witness attendance rate at trial

**Baseline**: Poor victim satisfaction; low Victims' Code compliance (per Victims' Commissioner reports)
**Target**: 20% improvement in victim satisfaction within 2 years
**Measurement Method**: HMCTS victim surveys, Victims' Code compliance data, court statistics

**Dependencies**:
- Case tracking system with victim notification capability
- Cross-agency data sharing to provide end-to-end case visibility
- Investment in remote evidence technology
- Victim service design informed by user research

**Risks to Achievement**:
- Technology focused on professional users, victims deprioritised
- Data protection constraints limiting victim access to case information
- Budget constraints limiting remote evidence facility investment
- Victim engagement in user research difficult to achieve

---

### Goal G-8: Achieve Green Book Business Case Approval

**Derived From Drivers**: SD-9, SD-15, SD-1

**Goal Owner**: MoJ Permanent Secretary

**Goal Statement**: Produce a robust HM Treasury Green Book 5-case model business case that secures multi-year funding approval for the programme, with quantified benefits, realistic cost estimates, and phased investment gates.

**Why This Matters**: Without Treasury funding approval, the programme cannot proceed. The business case must be compelling, realistic, and learn from Common Platform's cost overrun experience. It unlocks the resources for all other goals.

**Success Metrics**:
- **Primary Metric**: Treasury spending approval granted
- **Secondary Metrics**:
  - IPA Gateway review rating (Amber/Green or Green)
  - Business case cost estimates within 10% of actuals at each gate
  - Benefits realisation on track at each quarterly review

**Baseline**: No approved business case (2025-26)
**Target**: Full business case approval within 12 months
**Measurement Method**: Treasury approval letter, IPA Gateway reports, benefits tracker

**Dependencies**:
- Credible cost estimates informed by market research
- Quantified benefits model with defensible assumptions
- Lessons learned from Common Platform incorporated
- Ministerial support for spending case

**Risks to Achievement**:
- Optimism bias in cost and benefit estimates
- Treasury fiscal constraints in spending review
- Poor track record of justice technology programmes undermining credibility
- Inability to quantify all benefits in monetary terms

---

### Goal G-9: Comply with GDS Service Standard and TCoP

**Derived From Drivers**: SD-10, SD-3

**Goal Owner**: MoJ Chief Digital and Information Officer

**Goal Statement**: Ensure all new digital services pass GDS service assessment at alpha, beta, and live stages, and all technology decisions comply with the Technology Code of Practice.

**Why This Matters**: GDS compliance is mandatory for government digital services. TCoP compliance is required for technology spend approvals. Non-compliance blocks deployment and funding.

**Success Metrics**:
- **Primary Metric**: GDS service assessment pass rate
- **Secondary Metrics**:
  - TCoP compliance score per technology decision
  - Accessibility audit pass rate (WCAG 2.2 AA)
  - User satisfaction scores from user research

**Baseline**: Previous justice services have struggled at assessment
**Target**: All services pass GDS assessment on first or second attempt
**Measurement Method**: GDS assessment reports, TCoP review records

**Dependencies**:
- User research capability embedded in all delivery teams
- Accessibility expertise available
- Open standards adopted for data and interfaces
- Cloud-first approach for hosting

**Risks to Achievement**:
- Legacy system constraints preventing full compliance
- Pace pressure conflicting with assessment preparation
- Specialist criminal justice context not understood by assessors

---

### Goal G-10: Ensure Data Protection Compliance Across AI Deployments

**Derived From Drivers**: SD-11, SD-7, SD-2

**Goal Owner**: MoJ Data Protection Officer

**Goal Statement**: Complete Data Protection Impact Assessments (DPIAs) for all AI deployments, establish lawful bases for cross-agency data processing, and implement DPA 2018 Part 3 compliant processing for all law enforcement data.

**Why This Matters**: Criminal justice data processing carries the highest risk. ICO enforcement action or legal challenge could halt AI deployments. Proactive compliance builds public trust and enables sustainable AI adoption.

**Success Metrics**:
- **Primary Metric**: Percentage of AI deployments with approved DPIAs
- **Secondary Metrics**:
  - ICO enforcement actions (target: zero)
  - Data subject access request response times
  - Data sharing agreements in place between all agencies

**Baseline**: Limited DPIA coverage, ad-hoc data sharing agreements
**Target**: 100% DPIA coverage for AI deployments; all cross-agency sharing agreements formalised within 18 months
**Measurement Method**: DPIA register, ICO correspondence, data sharing agreement register

**Dependencies**:
- Data protection expertise embedded in programme
- Cross-agency agreement on lawful bases
- Privacy-by-design architecture
- AI governance framework (G-6) operational

**Risks to Achievement**:
- Cross-agency disagreement on lawful bases for sharing
- AI vendors unable to demonstrate compliance
- Evolving ICO guidance changing requirements mid-programme
- Data subject rights exercised at scale (e.g., mass subject access requests)

---

## Goal-to-Outcome Mapping

### Outcome O-1: Reduced Case Backlog and Faster Justice

**Supported Goals**: G-1, G-2, G-4, G-5

**Outcome Statement**: The outstanding Crown Court caseload is reduced below 50,000 and average time from charge to trial completion is reduced by 30%, delivering faster justice for victims, defendants, and the public.

**Measurement Details**:
- **KPI**: Outstanding Crown Court caseload; average charge-to-trial time
- **Current Value**: 77,000+ cases; average 18+ months charge to trial
- **Target Value**: <50,000 cases; <13 months average charge to trial
- **Measurement Frequency**: Quarterly
- **Data Source**: HMCTS Criminal Court Statistics Quarterly
- **Report Owner**: HMCTS Chief Executive

**Business Value**:
- **Financial Impact**: Reduced court sitting costs, fewer remand costs, reduced legal aid spend on delayed cases
- **Strategic Impact**: Restored public confidence in criminal justice system
- **Operational Impact**: Reduced pressure on court staff, judiciary, and practitioners
- **Customer Impact**: Victims and defendants receive timely justice

**Timeline**:
- **Year 1**: Stabilise backlog growth; deploy first AI tools; begin legacy migration
- **Year 2**: 10-15% backlog reduction; cross-agency integration live
- **Year 3**: Below 50,000 target achieved; full AI tool deployment
- **Sustainment (Year 4+)**: Maintain sustainable caseload levels

**Stakeholder Benefits**:
- **Lord Chancellor**: Demonstrable delivery on reform commitment
- **Victims**: Reduced waiting times for trial
- **Defendants**: Reduced time on remand or bail
- **HMCTS**: Manageable operational workload
- **Practitioners**: More effective trial scheduling

**Leading Indicators**: AI tool adoption rates, effective trial rates, adjournment rates
**Lagging Indicators**: Quarterly caseload statistics, victim satisfaction surveys

---

### Outcome O-2: Trustworthy AI in Criminal Justice

**Supported Goals**: G-2, G-3, G-6, G-10

**Outcome Statement**: AI tools are deployed across prosecution and defence with full governance compliance, zero AI-related miscarriages of justice, and measurable public trust in AI use within the justice system.

**Measurement Details**:
- **KPI**: AI governance compliance rate; AI-related case challenges
- **Current Value**: No operational AI governance framework
- **Target Value**: 100% compliance; zero successful AI-related case challenges
- **Measurement Frequency**: Monthly (compliance); Quarterly (challenges)
- **Data Source**: AI governance register, ATRS, court records
- **Report Owner**: MoJ Chief AI Officer

**Business Value**:
- **Financial Impact**: Avoided litigation costs from AI-related challenges
- **Strategic Impact**: UK positioned as leader in responsible criminal justice AI
- **Operational Impact**: Confident AI adoption across agencies
- **Customer Impact**: Public trust that AI is used fairly and transparently

**Timeline**:
- **Year 1**: AI governance framework operational; first AI tools deployed with full compliance
- **Year 2**: Defence AI tools available; 80%+ prosecution AI coverage
- **Year 3**: Full AI ecosystem operational across prosecution and defence
- **Sustainment**: Continuous governance and ethics review

**Stakeholder Benefits**:
- **Judiciary**: Confidence that AI preserves judicial independence
- **Defence community**: Equality of arms in technology access
- **ICO**: Compliant data processing
- **Public**: Trust in fair, transparent AI use

**Leading Indicators**: ATRS registration rates, DPIA completion rates, judicial steering group decisions
**Lagging Indicators**: AI-related case challenges, public trust surveys

---

### Outcome O-3: Seamless Cross-Agency Digital Justice

**Supported Goals**: G-4, G-5, G-9

**Outcome Statement**: Criminal justice agencies share case data seamlessly through standardised APIs, eliminating manual data transfer, reducing data errors by 80%, and enabling end-to-end digital case management from investigation to sentence.

**Measurement Details**:
- **KPI**: Automated data exchange percentage; data error rate
- **Current Value**: Extensive manual data transfer; frequent data discrepancies
- **Target Value**: 90%+ automated exchange; 80% reduction in data errors
- **Measurement Frequency**: Monthly
- **Data Source**: API gateway analytics, error reporting systems
- **Report Owner**: MoJ CDIO

**Business Value**:
- **Financial Impact**: Reduced administrative staff costs, fewer errors requiring correction
- **Strategic Impact**: Modern, integrated criminal justice platform
- **Operational Impact**: Faster case processing, less manual work
- **Customer Impact**: Fewer delays caused by administrative errors

**Timeline**:
- **Year 1**: API standards published; first integrations live (CPS-HMCTS)
- **Year 2**: Police-CPS digital case file integration; HMPPS integration
- **Year 3**: Full cross-agency integration; legacy systems replaced or wrapped
- **Sustainment**: API governance and evolution

**Stakeholder Benefits**:
- **Police**: Reduced case file preparation burden
- **CPS**: Faster access to evidence and case data
- **HMCTS**: Accurate, timely case information
- **HMPPS**: Real-time sentence and outcome data
- **Victims**: Fewer errors and delays in their case

**Leading Indicators**: Number of live API integrations, API transaction volumes
**Lagging Indicators**: Data error rates, staff survey on manual processes

---

### Outcome O-4: Improved Victim and Witness Experience

**Supported Goals**: G-7, G-1

**Outcome Statement**: Victims and witnesses report measurably improved experience of the criminal justice system, with real-time case tracking, timely communication, and accessible remote evidence facilities.

**Measurement Details**:
- **KPI**: Victim satisfaction score; Victims' Code compliance rate
- **Current Value**: Low satisfaction; poor compliance (per Victims' Commissioner)
- **Target Value**: 20% improvement in satisfaction; 90%+ Victims' Code compliance
- **Measurement Frequency**: Quarterly
- **Data Source**: HMCTS victim surveys, Victims' Code monitoring data
- **Report Owner**: HMCTS CEO with Victims' Commissioner oversight

**Business Value**:
- **Financial Impact**: Reduced witness non-attendance costs, fewer cracked trials
- **Strategic Impact**: Justice system seen as victim-centred
- **Operational Impact**: Better witness attendance, more effective trials
- **Customer Impact**: Victims feel informed, supported, and respected

**Timeline**:
- **Year 1**: Case tracking MVP for victims; pilot remote evidence expansion
- **Year 2**: Full case tracking rollout; automated Victims' Code monitoring
- **Year 3**: Sustained improvement demonstrated
- **Sustainment**: Continuous improvement informed by victim feedback

**Stakeholder Benefits**:
- **Victims' Commissioner**: Demonstrable compliance improvement
- **Victims**: Real-time visibility of case progress
- **Witnesses**: Accessible remote evidence facilities
- **HMCTS**: Fewer cracked trials from witness non-attendance

**Leading Indicators**: Case tracking registrations, remote evidence facility usage
**Lagging Indicators**: Victim satisfaction surveys, Victims' Code compliance data

---

### Outcome O-5: Sustainable Technology Estate

**Supported Goals**: G-5, G-8, G-9

**Outcome Statement**: The criminal justice technology estate is modernised to supported, maintainable platforms with documented APIs, reducing legacy risk and operational incidents by 60%.

**Measurement Details**:
- **KPI**: Percentage of applications on supported platforms; legacy incident rate
- **Current Value**: 37 critical legacy applications; high incident rate
- **Target Value**: <10 legacy applications remaining; 60% incident reduction
- **Measurement Frequency**: Quarterly
- **Data Source**: Application portfolio register, incident management system
- **Report Owner**: HMCTS CTO

**Business Value**:
- **Financial Impact**: Reduced support costs, avoided legacy failure costs
- **Strategic Impact**: Sustainable, evolvable technology platform
- **Operational Impact**: Reliable systems, fewer incidents
- **Customer Impact**: Consistent, available court services

**Timeline**:
- **Year 1**: Portfolio assessment complete; top 10 highest-risk migrations started
- **Year 2**: 15+ applications migrated; remaining applications on roadmap
- **Year 3**: 25+ migrated; critical legacy risk eliminated
- **Year 5**: All 37 migrated or decommissioned

**Stakeholder Benefits**:
- **HMCTS CTO**: Manageable technology estate
- **Court staff**: Reliable, modern tools
- **HM Treasury**: Reduced long-term maintenance costs
- **NAO**: Evidence of sound technology management

**Leading Indicators**: Migration pipeline progress, legacy risk scores
**Lagging Indicators**: Incident rates, support costs, platform currency metrics

---

### Outcome O-6: Fiscally Responsible Programme Delivery

**Supported Goals**: G-8, G-1

**Outcome Statement**: Programme expenditure is within 10% of approved business case estimates, benefits realisation is on track, and IPA Gateway reviews rate the programme Amber/Green or better.

**Measurement Details**:
- **KPI**: Cost variance from business case; IPA Gateway rating
- **Current Value**: No business case yet
- **Target Value**: <10% cost variance; Amber/Green rating
- **Measurement Frequency**: Quarterly (finance); Per gate (IPA)
- **Data Source**: Programme finance reports, IPA Gateway reports
- **Report Owner**: MoJ Permanent Secretary

**Business Value**:
- **Financial Impact**: Controlled expenditure, demonstrable value for money
- **Strategic Impact**: Credibility for future justice technology investment
- **Operational Impact**: Sustained funding through phased delivery

**Timeline**:
- **Year 1**: Business case approved; initial spending authority
- **Year 2**: First gateway review; benefits tracking operational
- **Year 3**: Full gateway review; benefits realisation evidence
- **Sustainment**: Annual benefits realisation reviews

**Stakeholder Benefits**:
- **HM Treasury**: Confidence in departmental spending control
- **NAO**: Auditable, evidence-based programme
- **Lord Chancellor**: Political credibility of delivery
- **MoJ Permanent Secretary**: Accounting officer assurance

**Leading Indicators**: Monthly spend vs. forecast, milestone delivery rate
**Lagging Indicators**: IPA Gateway ratings, NAO value-for-money assessments

---

## Complete Traceability Matrix

### Stakeholder → Driver → Goal → Outcome

| Stakeholder | Driver ID | Driver Summary | Goal ID | Goal Summary | Outcome ID | Outcome Summary |
|-------------|-----------|----------------|---------|--------------|------------|-----------------|
| Lord Chancellor | SD-1 | Backlog reduction, public confidence | G-1 | Reduce caseload to <50k | O-1 | Faster justice |
| Lord Chancellor | SD-1 | Backlog reduction, public confidence | G-8 | Green Book business case | O-6 | Fiscal responsibility |
| Lady Chief Justice | SD-2 | Judicial independence, due process | G-6 | AI governance framework | O-2 | Trustworthy AI |
| Lady Chief Justice | SD-2 | Judicial independence, due process | G-3 | Defence AI access | O-2 | Trustworthy AI |
| HMCTS CEO | SD-3 | Operational efficiency | G-1 | Reduce caseload | O-1 | Faster justice |
| HMCTS CEO | SD-3 | Operational efficiency | G-5 | Legacy migration | O-5 | Sustainable estate |
| HMCTS CEO | SD-3 | Operational efficiency | G-7 | Victim experience | O-4 | Victim experience |
| DPP / CPS | SD-4 | Prosecution efficiency | G-2 | AI disclosure tools | O-2 | Trustworthy AI |
| DPP / CPS | SD-4 | Prosecution efficiency | G-4 | Cross-agency interop | O-3 | Seamless digital justice |
| NPCC / Police | SD-5 | Evidence sharing | G-4 | Cross-agency interop | O-3 | Seamless digital justice |
| CBA / Law Society | SD-6 | Equality of arms | G-3 | Defence AI access | O-2 | Trustworthy AI |
| MoJ AI Officer | SD-7 | Responsible AI governance | G-6 | AI governance framework | O-2 | Trustworthy AI |
| MoJ AI Officer | SD-7 | Responsible AI governance | G-10 | Data protection compliance | O-2 | Trustworthy AI |
| LAA | SD-8 | Defence technology access | G-3 | Defence AI access | O-2 | Trustworthy AI |
| HM Treasury | SD-9 | Value for money | G-8 | Green Book business case | O-6 | Fiscal responsibility |
| GDS / CDDO | SD-10 | Digital standards | G-9 | GDS/TCoP compliance | O-3 | Seamless digital justice |
| ICO | SD-11 | Data protection | G-10 | Data protection compliance | O-2 | Trustworthy AI |
| Victims' Commissioner | SD-12 | Victim experience | G-7 | Victim experience | O-4 | Victim experience |
| HMPPS | SD-13 | Sentence integration | G-4 | Cross-agency interop | O-3 | Seamless digital justice |
| Magistrates' Assn | SD-14 | Summary justice tech | G-1 | Reduce caseload | O-1 | Faster justice |
| NAO | SD-15 | Accountability | G-8 | Green Book business case | O-6 | Fiscal responsibility |

### Conflict Analysis

**Competing Drivers**:

- **Conflict 1**: **Lord Chancellor (SD-1)** wants rapid technology deployment to demonstrate progress on backlog reduction, but **Lady Chief Justice (SD-2)** requires careful, rights-respecting implementation with judicial approval gates for any AI affecting case outcomes.
  - **Resolution Strategy**: Dual-track approach — deploy "safe" AI tools (transcription, translation, scheduling) at pace while running parallel judicial consultation for case-affecting AI. Judicial steering group has genuine veto power over AI tools that affect case management or outcomes. This respects judicial independence while enabling rapid wins on non-contentious technology.

- **Conflict 2**: **CPS (SD-4)** wants to deploy AI-assisted disclosure tools quickly to improve case throughput, but **CBA/Law Society (SD-6)** insist defence must have equivalent tools simultaneously to maintain equality of arms.
  - **Resolution Strategy**: Simultaneous deployment model — no prosecution AI tool goes live without a defence equivalent available. This may require central provision of shared-service AI tools, or legal aid funding reform to support defence technology. The programme must explicitly commit to a "no prosecution advantage" principle in its AI deployment sequencing.

- **Conflict 3**: **HMCTS (SD-3)** needs to migrate legacy systems to improve reliability, but **HM Treasury (SD-9)** requires robust business cases before releasing funding, and previous programmes have had poor cost control.
  - **Resolution Strategy**: Phased investment model with stage-gate approvals. Start with highest-risk/highest-value migrations, demonstrate delivery within budget, then unlock subsequent tranches. Build credibility through early, smaller successes before seeking major funding commitments.

- **Conflict 4**: **NPCC/Police (SD-5)** operate 43 independently governed forces with different systems, but **cross-agency interoperability (G-4)** requires common data standards and integration.
  - **Resolution Strategy**: Mandate outcomes (standard data formats, API compliance) not systems. Allow forces to choose their own technology provided they meet interoperability standards. Central funding incentives for forces that adopt early. Build adapter/middleware layer to connect diverse police systems to common APIs.

**Synergies**:

- **Synergy 1**: SD-1 (Lord Chancellor — backlog reduction) and SD-3 (HMCTS — operational efficiency) are naturally aligned — both benefit from every technology improvement that speeds case processing.

- **Synergy 2**: SD-7 (MoJ AI Officer — responsible AI) and SD-2 (Judiciary — judicial independence) share the same governance objective — robust AI oversight. Their combined advocacy creates strong political cover for governance investment.

- **Synergy 3**: SD-4 (CPS — prosecution efficiency) and SD-5 (Police — evidence sharing) both drive toward Goal G-4 (cross-agency interoperability) — success for either requires the same data sharing infrastructure.

- **Synergy 4**: SD-12 (Victims' Commissioner) and SD-1 (Lord Chancellor) are aligned on reducing delays — victim experience improvement is both morally right and politically beneficial.

- **Synergy 5**: SD-9 (HM Treasury — value for money) and SD-15 (NAO — accountability) create aligned pressure for disciplined programme management, which benefits all stakeholders through sustainable delivery.

---

## Communication & Engagement Plan

### Lord Chancellor / Ministers

**Primary Message**: The programme is delivering measurable backlog reduction through responsible technology reform, grounded in the Leveson Review recommendations, with robust governance and fiscal discipline.

**Key Talking Points**:
- Quarterly caseload reduction figures demonstrating progress
- AI adoption rates across prosecution and defence (equality of arms)
- Business case milestones and spending within approved limits
- Risk management for any issues before they become political

**Communication Frequency**: Monthly ministerial briefing; quarterly full programme update
**Preferred Channel**: Ministerial submission with data dashboard
**Success Story**: "Crown Court backlog reduced by X thousand cases this quarter through AI-assisted case preparation"

### Judiciary (Lady Chief Justice, Lead Judge for AI)

**Primary Message**: Technology reforms preserve and strengthen judicial independence, with the judiciary having genuine authority over AI deployment affecting case outcomes.

**Key Talking Points**:
- Judicial steering group decisions and their impact
- AI categorisation demonstrating no judicial decision replacement
- Practitioner (including judicial) feedback on technology tools
- Due process safeguards maintained in all technology designs

**Communication Frequency**: Monthly judicial steering group; quarterly judicial leadership briefing
**Preferred Channel**: Judicial steering group meetings; formal judicial communications
**Success Story**: "AI transcription saves 2 hours per trial day while judges retain full control over case management"

### Defence Community (CBA, Law Society, LAA)

**Primary Message**: Equality of arms is a non-negotiable programme principle — defence will have equivalent technology access to prosecution, and defence practitioners are partners in shaping technology.

**Key Talking Points**:
- Defence AI tool availability timeline (matched to prosecution deployment)
- Practitioner involvement in requirements and design
- Legal aid funding for technology access
- Open-source/shared-service approach benefiting all parties

**Communication Frequency**: Monthly practitioner forum; quarterly CBA/Law Society briefing
**Preferred Channel**: Practitioner forums, professional body briefings
**Success Story**: "Defence practitioners now have AI-assisted disclosure review equivalent to CPS capability"

### HM Treasury / NAO

**Primary Message**: The programme is fiscally disciplined, learning from Common Platform experience, with robust business cases, phased investment, and auditable benefits realisation.

**Key Talking Points**:
- Cost performance against business case (within 10%)
- Benefits realisation tracker showing quantified outcomes
- Lessons learned from Common Platform actively applied
- IPA Gateway review ratings

**Communication Frequency**: Quarterly finance report; annual spending review input
**Preferred Channel**: Green Book business case updates, IPA Gateway reports
**Success Story**: "Programme delivered Phase 1 within approved budget with quantified benefits exceeding projections"

### Victims and Public

**Primary Message**: Technology is making the justice system faster, fairer, and more accessible for victims and witnesses.

**Key Talking Points**:
- Case tracking service for victims
- Reduced waiting times for trial
- Remote evidence facilities for vulnerable witnesses
- AI used responsibly with full transparency

**Communication Frequency**: Quarterly public updates; ongoing user research
**Preferred Channel**: GOV.UK updates, victim support channels, media briefings
**Success Story**: "Victims can now track their case in real-time and receive automatic updates at every stage"

---

## Change Impact Assessment

### Impact on Stakeholders

| Stakeholder | Current State | Future State | Change Magnitude | Resistance Risk | Mitigation Strategy |
|-------------|---------------|--------------|------------------|-----------------|---------------------|
| Court staff (HMCTS) | Manual data entry, legacy systems, workarounds | Modern digital tools, automated workflows, AI assistance | HIGH | MEDIUM | Phased rollout, extensive training, champions network |
| CPS prosecutors | Manual disclosure review, limited digital evidence tools | AI-assisted disclosure, digital case preparation | HIGH | LOW | Demonstrated efficiency gains, prosecutor involvement in design |
| Police officers | Manual case file preparation, varied systems | Automated evidence packaging, standardised digital case files | HIGH | MEDIUM | Force-by-force engagement, incentive funding, local champions |
| Defence practitioners | Minimal technology, manual processes | AI-assisted case preparation, digital evidence tools | HIGH | LOW | Free/funded tool access, training, practitioner design input |
| Judges | Paper-based or basic digital, full discretion | AI-augmented case management, digital courtrooms | MEDIUM | HIGH | Judicial steering group, opt-in pilots, preserved discretion |
| Magistrates | Basic digital tools, volunteer capacity | Modern case management, AI assistance | MEDIUM | MEDIUM | Simplified interfaces, training programme, peer support |
| Victims/Witnesses | Poor communication, manual processes | Real-time tracking, remote evidence, automated updates | MEDIUM | LOW | User research-driven design, accessibility focus |

### Change Readiness

**Champions** (Enthusiastic supporters):
- CPS leadership — see immediate efficiency gains from AI disclosure tools
- Lord Chancellor's office — political commitment to reform
- HMCTS digital team — want to modernise the estate
- Victims' Commissioner — technology improving victim experience

**Fence-sitters** (Neutral, need convincing):
- Police forces — supportive in principle but concerned about funding and mandated systems
- HMPPS — lower priority for them, need to see integration benefits
- Magistrates — open to technology but need usability assurance
- HM Treasury — supportive if business case is robust

**Resisters** (Opposed or skeptical):
- Some senior judiciary — concerned about AI threatening judicial independence — **Strategy**: judicial steering group with genuine veto, opt-in pilot approach, demonstrate augmentation not replacement
- Some defence practitioners — sceptical that equality of arms will be delivered — **Strategy**: simultaneous deployment commitment, defence representatives in governance, funded access
- Court staff with long legacy system experience — resistant to change — **Strategy**: early involvement, training investment, champions network, phased rollout with support

---

## Risk Register (Stakeholder-Related)

### Risk R-1: Judicial Resistance Blocks AI Deployment

**Related Stakeholders**: Lady Chief Justice, Lead Judge for AI, Judiciary

**Risk Description**: Judicial stakeholders exercise veto over AI tools perceived as threatening judicial independence, blocking or significantly delaying AI deployment that could deliver efficiency gains.

**Impact on Goals**: G-2 (AI disclosure), G-6 (AI governance)

**Probability**: MEDIUM
**Impact**: HIGH

**Mitigation Strategy**: Early judicial engagement through steering group; start with non-contentious AI (transcription, translation); build trust through successful pilots with judicial champions; ensure judicial veto applies only to case-affecting AI, not administrative tools.

**Contingency Plan**: If judicial resistance is broad, focus AI investment on pre-trial processes (disclosure, case preparation) that don't directly touch judicial decision-making.

---

### Risk R-2: Defence Inequality Challenge

**Related Stakeholders**: CBA, Law Society, LAA, Defendants

**Risk Description**: Defence community challenges AI-assisted prosecution in court on equality of arms grounds, potentially causing case collapses or legal precedent blocking AI use.

**Impact on Goals**: G-2, G-3

**Probability**: HIGH
**Impact**: HIGH

**Mitigation Strategy**: Commit to simultaneous prosecution-defence deployment; establish defence technology fund; involve CBA/Law Society in technology governance; obtain independent legal opinion on equality of arms implications before prosecution AI deployment.

**Contingency Plan**: If defence parity cannot be achieved simultaneously, delay prosecution AI deployment until defence equivalent is available. The programme cannot risk creating a two-tier justice system.

---

### Risk R-3: Police Interoperability Failure

**Related Stakeholders**: NPCC, 43 police forces

**Risk Description**: Independent police forces fail to agree or implement common data standards, preventing digital case file integration and perpetuating manual evidence sharing.

**Impact on Goals**: G-4

**Probability**: HIGH
**Impact**: MEDIUM

**Mitigation Strategy**: Mandate outcome standards (what data, what format) not systems; central funding incentives for early adopters; adapter/middleware layer for common police systems; NPCC digital policing programme alignment.

**Contingency Plan**: Build middleware adapters for the most common police systems (Niche, Connect, Athena) as a pragmatic workaround, rather than waiting for 43-force consensus.

---

### Risk R-4: Treasury Funding Refusal

**Related Stakeholders**: HM Treasury, MoJ Permanent Secretary

**Risk Description**: HM Treasury rejects or significantly reduces the business case funding request due to fiscal constraints or lack of confidence in justice technology delivery.

**Impact on Goals**: G-8 (business case), and cascading impact on all goals

**Probability**: MEDIUM
**Impact**: CRITICAL

**Mitigation Strategy**: Robust Green Book business case with conservative assumptions; phased investment model reducing upfront commitment; lessons learned from Common Platform explicitly addressed; ministerial advocacy; IPA assurance from the outset.

**Contingency Plan**: If full funding not approved, prioritise highest-value interventions (AI disclosure, highest-risk legacy migration) within available budget. Seek smaller initial approval with expansion contingent on demonstrated delivery.

---

### Risk R-5: Common Platform Instability During Reform

**Related Stakeholders**: HMCTS, Court staff, All court users

**Risk Description**: The existing Common Platform system experiences instability or failures during the technology reform programme, eroding user confidence and complicating migration planning.

**Impact on Goals**: G-1, G-5

**Probability**: MEDIUM
**Impact**: HIGH

**Mitigation Strategy**: Stabilise Common Platform as a prerequisite before adding new functionality; maintain parallel running during migration; invest in Common Platform resilience alongside reform programme; clear separation between stabilisation and transformation work.

**Contingency Plan**: If Common Platform issues persist, consider bypass strategies (new services alongside Common Platform rather than building on it) and accelerate alternative platform assessment.

---

### Risk R-6: AI Ethics Controversy

**Related Stakeholders**: MoJ AI Officer, ICO, Public, Media

**Risk Description**: An AI-related error or controversy (e.g., biased outcome, data breach, automation failure) damages public trust and triggers political intervention halting AI deployment.

**Impact on Goals**: G-2, G-6, G-10

**Probability**: MEDIUM
**Impact**: HIGH

**Mitigation Strategy**: Robust AI governance framework (G-6) as prerequisite; mandatory DPIA and ATRS for all AI tools; independent ethics review; transparent public reporting on AI use; incident response plan specifically for AI failures.

**Contingency Plan**: Pre-prepared communications plan for AI incidents; ability to rapidly pause specific AI tool deployment without affecting wider programme; independent review mechanism for any AI-related concerns.

---

### Risk R-7: Data Protection Enforcement Action

**Related Stakeholders**: ICO, All agencies processing criminal justice data

**Risk Description**: ICO takes enforcement action against cross-agency data sharing or AI processing, halting critical programme components.

**Impact on Goals**: G-4, G-10

**Probability**: LOW
**Impact**: HIGH

**Mitigation Strategy**: Early ICO engagement and sandbox participation; comprehensive DPIAs before deployment; DPA 2018 Part 3 specialist legal advice; cross-agency data sharing agreements formalised before technical integration.

**Contingency Plan**: If enforcement action occurs, immediately pause affected processing; remediate; seek ICO guidance on compliant approach before resuming.

---

### Risk R-8: Stakeholder Fatigue and Disengagement

**Related Stakeholders**: All stakeholders, particularly defence community and police

**Risk Description**: Over a multi-year programme, stakeholder engagement fatigue leads to declining participation in governance, consultation, and feedback, undermining programme legitimacy and design quality.

**Impact on Goals**: All goals dependent on stakeholder engagement

**Probability**: MEDIUM
**Impact**: MEDIUM

**Mitigation Strategy**: Efficient, outcome-focused governance meetings; regular demonstration of how stakeholder input shaped decisions; rotate governance representation to prevent burnout; celebrate and communicate successes publicly.

**Contingency Plan**: If engagement drops, refresh governance membership; hold stakeholder re-engagement events; consider paid secondments from key stakeholder organisations.

---

## Governance & Decision Rights

### Decision Authority Matrix (RACI)

| Decision Type | Responsible | Accountable | Consulted | Informed |
|---------------|-------------|-------------|-----------|----------|
| Programme strategy and scope | MoJ CDIO | Lord Chancellor | HMCTS CEO, DPP, Lady CJ | All stakeholders |
| Budget allocation | Programme Director | MoJ Permanent Secretary | HM Treasury, HMCTS CFO | NAO, all delivery teams |
| AI deployment approval | MoJ AI Officer | Lord Chancellor | Lead Judge for AI, ICO, CBA | All practitioners |
| Architecture decisions | Enterprise Architect | MoJ CDIO | HMCTS CTO, CPS CDO, GDS | All delivery teams |
| Data sharing agreements | Programme DPO | MoJ Permanent Secretary | ICO, all agency DPOs | All stakeholders |
| Cross-agency standards | MoJ CDIO | Programme Board | NPCC, CPS CDO, HMPPS CDO | All agencies |
| Service go-live | HMCTS CTO | HMCTS CEO | GDS, Security, MoJ AI Officer | All users |
| Legacy migration sequencing | HMCTS CTO | HMCTS CEO | Court staff, MoJ CDIO | All stakeholders |
| Defence technology access | LAA CEO | Lord Chancellor | CBA, Law Society, MoJ CDIO | All practitioners |
| Victim service design | HMCTS Service Owner | HMCTS CEO | Victims' Commissioner, User Research | Victims, witnesses |

### Escalation Path

1. **Level 1**: Programme Director / Delivery Leads (day-to-day decisions, within approved scope and budget)
2. **Level 2**: Programme Board — MoJ CDIO, HMCTS CEO, CPS CDO (scope, timeline, budget variances up to 10%)
3. **Level 3**: Senior Responsible Owner — MoJ Permanent Secretary (major scope changes, budget >10% variance, cross-agency disputes)
4. **Level 4**: Ministerial — Lord Chancellor (strategic direction, political decisions, judicial relationship management)
5. **Judicial Track**: Lead Judge for AI → Lady Chief Justice (AI deployment affecting judicial functions — separate from executive escalation)

---

## Validation & Sign-off

### Stakeholder Review

| Stakeholder | Review Date | Comments | Status |
|-------------|-------------|----------|--------|
| Lord Chancellor's Office | PENDING | | PENDING |
| HMCTS CEO | PENDING | | PENDING |
| DPP / CPS | PENDING | | PENDING |
| Lady Chief Justice's Office | PENDING | | PENDING |
| Criminal Bar Association | PENDING | | PENDING |
| Law Society | PENDING | | PENDING |
| NPCC | PENDING | | PENDING |
| Victims' Commissioner | PENDING | | PENDING |
| MoJ Chief AI Officer | PENDING | | PENDING |
| ICO | PENDING | | PENDING |

### Document Approval

| Role | Name | Signature | Date |
|------|------|-----------|------|
| Programme SRO | | | |
| MoJ CDIO | | | |
| Enterprise Architect | | | |

---

## Appendices

### Appendix A: Stakeholder Interview Summaries

*Stakeholder interviews to be conducted as part of programme mobilisation. This section will be populated with interview summaries, key quotes, and follow-up actions.*

### Appendix B: Survey Results

*Stakeholder surveys to be designed and conducted during programme discovery phase. This section will be populated with survey methodology and results.*

### Appendix C: References

- ARC-000-PRIN-v1.0 — Criminal Courts Technology & AI Reform Enterprise Architecture Principles
- Independent Review of the Criminal Courts — Overview (2025)
- Independent Review of the Criminal Courts — Part 1 Report (July 2025)
- Independent Review of the Criminal Courts — Part 2 Report, Volume 1 (February 2026)
- Independent Review of the Criminal Courts — Part 2 Report, Volume 2 (February 2026)
- UK AI Playbook (DSIT, 2024)
- Algorithmic Transparency Recording Standard (CDDO)
- GDS Service Standard (14 points)
- Technology Code of Practice (TCoP)
- HM Treasury Green Book (2022)
- NCSC Cyber Assessment Framework
- Data Protection Act 2018, Part 3 (Law Enforcement Processing)
- UK GDPR
- Victims' Code of Practice

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Independent Review of the Criminal Courts — Overview | Policy Review | GOV.UK | Programme context, 180 recommendations, efficiency principles | `projects/000-global/external/independent-review-criminal-courts-overview.pdf` |
| Independent Review of the Criminal Courts — Part 1 | Policy Review | GOV.UK | Technology recommendations, AI guidance, interoperability mandate | `projects/000-global/external/35.49_MOJ_Ind_Review_Criminal_Courts_v8b_FINAL_WEB.pdf` |
| Independent Review of the Criminal Courts — Part 2, Vol 1 | Policy Review | GOV.UK | Detailed implementation proposals, legacy system analysis | `projects/000-global/external/independent-review-criminal-courts-part-2-vol-1.pdf` |
| Independent Review of the Criminal Courts — Part 2, Vol 2 | Policy Review | GOV.UK | Additional implementation detail, stakeholder evidence | `projects/000-global/external/independent-review-criminal-courts-part-2-vol-2.pdf` |
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 23 principles across 7 categories governing technology decisions | `projects/000-global/ARC-000-PRIN-v1.0.md` |

---

**Generated by**: ArcKit `/arckit.stakeholders` command
**Generated on**: 2026-02-04
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (001)
**Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)

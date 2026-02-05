# Data Protection Impact Assessment (DPIA)

> **Template Status**: Beta | **Version**: 1.5.0 | **Command**: `/arckit.dpia`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-DPIA-v1.0 |
| **Document Type** | Data Protection Impact Assessment |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL-SENSITIVE |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-02-05 |
| **Last Modified** | 2026-02-05 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-05 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MoJ Data Protection Officer, MoJ Chief AI Officer, HMCTS CDIO, CPS CDO, ICO (for consultation), Programme Board |
| **Project Name** | Criminal Courts Technology & AI Reform |
| **Assessment Date** | 2026-02-05 |
| **Data Protection Officer** | MoJ Data Protection Officer |
| **Data Controller** | Ministry of Justice (joint controller with HMCTS, CPS, HMPPS, LAA for cross-agency processing) |
| **Author** | Enterprise Architect |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-05 | ArcKit AI | Initial creation from `/arckit.dpia` command | PENDING | PENDING |

## Executive Summary

**Processing Activity**: Criminal Courts Technology & AI Reform Programme — cross-agency digital case management, AI-assisted disclosure review, AI transcription/translation, victim/witness case tracking, cross-agency data integration, and legacy system migration across the criminal justice system of England and Wales.

**DPIA Outcome**: HIGH residual risk to data subjects

**Approval Status**: PENDING

**Key Findings**:
- The programme processes criminal offence data, special category data (health, biometric, ethnicity), and data relating to children and vulnerable adults at national scale across multiple agencies
- DPA 2018 Part 3 applies to law enforcement processing, imposing specific conditions distinct from standard UK GDPR
- AI-assisted disclosure review introduces algorithmic bias risk that could affect defendants' fair trial rights, including liberty
- Cross-agency data integration across 5+ agencies creates novel data-sharing risks that data subjects would not reasonably expect
- Victim and witness data requires enhanced protections due to vulnerability, intimidation risk, and RASSO sensitivity
- Children appear as defendants, victims, and witnesses — the programme processes data of an estimated 30,000+ children annually

**Recommendation**: Proceed with conditions — all conditions must be met before case-affecting AI deployment

**ICO Consultation Required**: YES — recommended due to scale, sensitivity, AI processing, and cross-agency nature

---

## 1. DPIA Screening Assessment

### 1.1 Screening Criteria (ICO's 9 Criteria)

| # | Criterion | YES/NO | Evidence |
|---|-----------|--------|----------|
| 1 | **Evaluation or scoring** including profiling and predicting | **YES** | AI disclosure review evaluates evidence relevance and categorises material by disclosability with confidence scores (FR-001, UC-1). AI case summarisation evaluates case complexity. Scheduling algorithms evaluate case readiness. |
| 2 | **Automated decision-making with legal or similarly significant effect** | **YES** | AI-assisted disclosure review directly affects what evidence is presented to defence, with legal consequences for fair trial rights. While human-in-the-loop is mandated (Principle 2), the AI pre-filters evidence that prosecutors review, creating de facto influence on legally significant decisions. Scheduling recommendations affect hearing dates and bail duration. |
| 3 | **Systematic monitoring** of data subjects | **YES** | Victim case tracking system (FR-007, UC-4) systematically monitors case progression and sends automated notifications. Cross-agency case data exchange (UC-3) creates systematic tracking of defendants through the justice system from charge through sentencing. AI audit trails record all interactions with case data. |
| 4 | **Sensitive data or data of highly personal nature** | **YES** | Criminal offence data (DPA 2018 Part 3), health data (mental health assessments for defendants, victim medical records), biometric data (body-worn video, forensic data), ethnicity data, victim/witness vulnerability information, RASSO case data, children's data. All classified OFFICIAL-SENSITIVE. DR-003 (defendant record) explicitly classified as special category criminal justice data. |
| 5 | **Processing on a large scale** | **YES** | ~500,000 new criminal cases per year (DR-001). 10+ million records over 5 years. 100TB/year of digital evidence (DR-002). Processing affects every criminal case in England and Wales across 300+ court centres. Geographic scope: national (England and Wales). Data subjects: millions of defendants, victims, witnesses, and legal practitioners. |
| 6 | **Matching or combining datasets** from different sources | **YES** | Cross-agency integration (BR-004, UC-3) combines data from police (43 forces), CPS, HMCTS, HMPPS, and LAA. Defendant records linked across PNC, case management systems, and court records via common identifiers. Evidence packages combine body-worn video, communications data, and forensic data from multiple police sources. Data subjects would not expect this level of cross-agency data combination. |
| 7 | **Data concerning vulnerable data subjects** | **YES** | Defendants (power imbalance with state), children (as defendants, victims, witnesses), victims of domestic abuse, RASSO victims/complainants, intimidated witnesses, defendants with mental health conditions, unrepresented defendants, individuals lacking legal capacity. DR-004 explicitly includes vulnerability_flags. |
| 8 | **Innovative use or application of new technological or organisational solutions** | **YES** | AI/ML for criminal justice disclosure review (FR-001), AI transcription and translation in court proceedings (FR-002, FR-003), AI case summarisation, cross-agency event-driven data integration, defence AI shared-service platform (FR-009). First large-scale AI deployment in English criminal courts. |
| 9 | **Processing that prevents data subjects from exercising a right or using a service/contract** | **NO** | Data subjects retain rights under DPA 2018 Part 3 (subject access, rectification, erasure where applicable). However, defendants cannot meaningfully opt out of criminal justice processing, and processing is compulsory by nature of criminal proceedings. The "NO" reflects the legal framework rather than absence of concern. |

**Screening Score**: **8**/9 criteria met

### 1.2 DPIA Necessity Decision

**Decision**: **DPIA REQUIRED**

**Rationale**:
- 8 of 9 ICO criteria met — DPIA required (threshold is ≥2)
- Processing involves special category data (criminal offence data, health data, biometric data) at national scale — DPIA required
- Innovative AI technology with unknown risks in criminal justice context — DPIA required
- DPA 2018 Part 3 applies — law enforcement processing at this scale requires DPIA
- Processing affects vulnerable individuals (defendants, children, victims) — DPIA required
- Article 35(3)(a) UK GDPR: systematic and extensive evaluation of natural persons based on automated processing, including profiling, on which decisions are based that produce legal effects
- Article 35(3)(b) UK GDPR: processing on a large scale of special categories of data

**Decision Authority**: MoJ Data Protection Officer

**Decision Date**: 2026-02-05

---

## 2. Description of Processing

### 2.1 Nature of Processing

**What operations are being performed?**
- [x] Collection
- [x] Recording
- [x] Organisation
- [x] Structuring
- [x] Storage
- [x] Adaptation/alteration
- [x] Retrieval
- [x] Consultation
- [x] Use
- [x] Disclosure by transmission
- [x] Dissemination
- [x] Alignment/combination
- [x] Restriction
- [x] Erasure/destruction

**Processing Method**:
- [x] Combination of automated and manual

**Profiling Involved**: YES
- AI disclosure review evaluates evidence relevance and assigns confidence scores, constituting evaluation of data to make recommendations about disclosability
- AI case summarisation evaluates case complexity and key issues
- Scheduling algorithms evaluate case characteristics to recommend hearing slots

**Automated Decision-Making**: YES
- AI-assisted disclosure review pre-categorises evidence into disclosable/non-disclosable/under review categories
- Human oversight: YES — Principle 2 (Human-Centred AI Augmentation) mandates human-in-the-loop for all AI outputs. Prosecutors must review and approve/override every AI recommendation (UC-1, step 6). Defence practitioners have equivalent review capability (UC-2)
- AI does NOT make final decisions — human decision-maker retains full authority
- However, AI pre-filtering creates framing effects that influence human decisions

### 2.2 Scope of Processing

#### What data are we processing?

**Personal Data Categories** (from Requirements DR-001 through DR-004):

| Entity ID | Entity Name | Data Categories | Special Category? | PII Level |
|-----------|-------------|-----------------|-------------------|-----------|
| DR-001 | Criminal Case Record | Case reference, offences, court centre, case status, prosecution agency, timestamps | NO (but linked to defendants) | HIGH |
| DR-002 | Digital Evidence Package | Body-worn video, communications data, documents, forensic data, images, audio | YES (may contain biometric, health, RASSO) | VERY HIGH |
| DR-003 | Defendant Record | Name, DOB, PNC ID, bail status, legal representation, ethnicity, health data | YES (Article 10 criminal offence data; potentially Article 9 health/ethnicity) | VERY HIGH |
| DR-004 | Victim/Witness Record | Name, contact details, vulnerability flags, special measures, anonymity orders | YES (vulnerability, health, children) | VERY HIGH |
| — | Court Staff Record | Name, role, court centre, authentication credentials, activity logs | NO | MEDIUM |
| — | Legal Practitioner Record | Name, SRA/BSB number, firm, authentication, case access history | NO | MEDIUM |
| — | AI Audit Trail | User actions, AI recommendations, overrides, confidence scores, timestamps | NO (but linked to case data) | HIGH |
| — | Hearing Record | Date, time, court room, judge, outcome, participants, transcript | YES (contains case/defendant data by reference) | HIGH |

**Total Data Items**: ~50+ personal data fields across 8+ entity types

**Special Category Data**: YES
- **Criminal offence data** (DPA 2018 Part 3): All defendant records, case records, evidence
- **Health data**: Mental health assessments, medical reports in evidence, vulnerability assessments
- **Biometric data**: Body-worn video (facial images), forensic data (DNA, fingerprints in evidence packages)
- **Racial/ethnic origin data**: Defendant demographic data, ethnicity monitoring
- **Data relating to sex life**: RASSO case evidence (rape and serious sexual offences)

**Children's Data**: YES
- Age range: 10-17 years (age of criminal responsibility is 10 in England and Wales)
- Children appear as: defendants (Youth Court cases), victims, witnesses
- Estimated volume: 30,000+ children annually (based on Youth Court caseload and child witnesses)
- Enhanced protections required: DR-004 vulnerability_flags includes "Child"

#### Whose data are we processing?

**Data Subject Categories** (from Stakeholder Analysis ARC-001-STKE-v1.0 and Requirements user personas):

| Data Subject Type | Description | Volume | Vulnerable? |
|-------------------|-------------|--------|-------------|
| **Defendants** | Individuals charged with criminal offences | ~500,000/year | YES — power imbalance with state; includes children, mental health, unrepresented |
| **Victims** | Complainants and victims of crime | ~400,000/year | YES — victims of crime; includes domestic abuse, RASSO, children, intimidated witnesses |
| **Witnesses** | Prosecution and defence witnesses | ~300,000/year | YES — includes children, intimidated, vulnerable |
| **CPS Prosecutors** | Crown Prosecution Service lawyers | ~6,000 | NO |
| **Defence Practitioners** | Barristers and solicitors (criminal defence) | ~15,000 | NO |
| **Police Officers** | Officers providing evidence and case files | ~50,000+ | NO |
| **Court Staff** | HMCTS court administrators and clerks | ~15,000 | NO |
| **Judges and Magistrates** | Judicial officers | ~30,000 (including ~12,000 magistrates) | NO |
| **Probation Officers** | HMPPS officers receiving sentencing data | ~10,000 | NO |
| **Children** (cross-cutting) | Children as defendants, victims, or witnesses | ~30,000/year | YES — children are inherently vulnerable |

**Total Data Subjects**: Approximately 1.3+ million individuals per year; 5+ million over the programme lifecycle

**Vulnerable Groups**:
- Children (10-17 years) as defendants, victims, and witnesses
- Victims of domestic abuse and sexual violence (RASSO)
- Intimidated witnesses subject to anonymity orders or special measures
- Defendants with mental health conditions
- Unrepresented defendants (limited understanding of data rights)
- Individuals lacking legal capacity
- Non-English speakers (relying on AI translation)

#### How much data?

**Volume Metrics**:
- **Records**: ~500,000 new case records/year; 10+ million over 5 years
- **Data subjects**: 1.3+ million individuals/year
- **Storage size**: 100TB/year of digital evidence (growing 30% annually) plus structured data
- **Transaction rate**: Millions of API calls/day across 5+ agencies; thousands of AI processing operations/day
- **Geographic scope**: England and Wales — national scope, 300+ court centres

**Scale Classification**: **Large scale**
- National geographic scope (England and Wales)
- 1.3+ million data subjects per year
- Covers the entire criminal justice system
- Processing is continuous and ongoing

#### How long are we keeping it?

**Retention Periods** (from Requirements and criminal justice retention schedules):

| Data Type | Retention Period | Legal Basis for Retention | Deletion Method |
|-----------|------------------|---------------------------|-----------------|
| Criminal case records (summary) | 6 years after disposal | MoJ retention schedule; Rehabilitation of Offenders Act 1974 | Secure deletion with audit trail |
| Criminal case records (indictable) | 10+ years after disposal | MoJ retention schedule; serious crime provisions | Secure deletion with audit trail |
| Digital evidence | Until appeal window closes + retention schedule | Criminal Procedure Rules; case-specific orders | Cryptographic erasure of storage keys |
| Defendant records | Per PNC retention rules (varies: 5 years to indefinite for serious offences) | Police Act 1997; Rehabilitation of Offenders Act 1974 | PNC deletion procedures |
| Victim/witness records | Duration of case + 6 years (or longer if ongoing risk) | Victims' Code; MoJ retention schedule | Secure deletion |
| AI audit trails | 7 years minimum | NCSC CAF; criminal justice audit requirements | Secure deletion |
| Court staff/practitioner records | Duration of employment/registration + 6 years | Employment law; regulatory requirements | Secure deletion |
| Security/authentication logs | 7 years minimum | NCSC CAF Principle 7 (Observability) | Automated archival then deletion |

**Maximum Retention**: Indefinite for the most serious offences (murder, terrorism); typically 6-10 years for standard criminal cases

**Automated Deletion**: YES — retention policies configured with automated deletion at expiry, per Architecture Principle 10 and NFR-DP-001. Automated alerts 90 days before retention expiry for manual review of edge cases.

### 2.3 Context of Processing

#### Why are we processing this data?

**Processing Purpose** (from Requirements):

| Requirement ID | Purpose | Stakeholder Goal |
|----------------|---------|------------------|
| BR-001 | Reduce Crown Court backlog through technology-enabled efficiency | G-1: Backlog reduction |
| BR-002 | AI-assisted disclosure review and case preparation for prosecution | G-2: AI disclosure and case preparation |
| BR-003 | Equivalent AI tools for defence practitioners (equality of arms) | G-3: Defence technology access |
| BR-004 | Cross-agency digital interoperability replacing manual data transfer | G-4: Cross-agency interoperability |
| BR-005 | Legacy system migration to modern, secure platforms | G-5: Legacy modernisation |
| BR-006 | AI governance framework with judicial oversight | G-6: AI governance |
| BR-007 | Victim/witness case tracking and improved experience | G-7: Victim/witness experience |
| BR-010 | Data protection compliance across all processing | G-10: Data protection |

**Primary Purpose**: Administration of criminal justice — enabling efficient, fair, and transparent processing of criminal cases across the justice system of England and Wales, from charge through to disposal and beyond.

**Secondary Purposes**:
- Operational analytics and performance monitoring (case progression rates, court utilisation)
- AI model training and validation (using anonymised/pseudonymised data only)
- Audit and accountability (ATRS transparency, decision audit trails)
- Policy development and research (using aggregated, anonymised data)

#### What is the relationship with data subjects?

**Relationship Type**:
- [x] Citizen/public service user
- Criminal justice processing is a compulsory state function — defendants, victims, and witnesses do not choose to participate

**Power Balance**:
- [x] Imbalanced relationship (government-citizen in criminal justice context)
- If imbalanced: This is among the most extreme power imbalances in any data processing context. The state is prosecuting defendants who may face imprisonment. Victims and witnesses are compelled or strongly encouraged to participate. Defendants cannot opt out.
- Safeguards: Architecture Principle 21 (Equality of Arms) ensures defence has equivalent technology access. Principle 22 (Judicial Independence) preserves independent oversight. Principle 23 (Victim and Witness Protection) provides enhanced protections. DPA 2018 Part 3 provides specific safeguards for law enforcement processing. Legal representation provides advocacy for defendants' data rights.

#### How much control do data subjects have?

**Control Mechanisms**:
- [x] Can access their data (Subject Access Request)
- [x] Can correct inaccurate data (rectification)
- [x] Can object to automated decisions
- [x] Can request restriction of processing

**Limitations on Control**:
- **No consent withdrawal**: Processing is based on public task/legal obligation, not consent. Defendants cannot withdraw consent to criminal justice processing.
- **No right to erasure during proceedings**: Criminal case data cannot be deleted while proceedings are active or within retention periods mandated by law.
- **Limited right to object**: DPA 2018 Part 3 does not provide a general right to object to law enforcement processing, though data subjects can object to automated decision-making.
- **No data portability**: Not applicable to law enforcement processing under DPA 2018 Part 3.
- **SAR limitations**: Subject Access Requests may be refused or limited where disclosure would prejudice criminal proceedings (DPA 2018 Part 3, s.45).
- **AI override right**: Data subjects (via legal representatives) can request human review of any AI-assisted decision affecting their case, and can challenge AI outputs in court proceedings.

#### Would data subjects expect this processing?

**Reasonable Expectation Assessment**:
- **Transparency**: Are data subjects informed about processing? PARTIALLY — defendants are informed of charges and evidence via disclosure. Victims receive privacy notices via Victims' Code. However, AI involvement in evidence processing may not be widely understood.
- **Privacy Notice**: Is a clear privacy notice provided? YES — required to be provided to all data subjects per DPA 2018 Part 3
- **Expectation**: Would an average person in this context expect this processing? MAYBE
  - Case management and evidence processing: YES — expected in criminal proceedings
  - Cross-agency data sharing at this scale: MAYBE — data subjects may not expect seamless integration across 5+ agencies
  - AI-assisted disclosure review: NO — novel use of AI in criminal justice; defendants unlikely to expect AI involvement in evidence triage
  - AI transcription/translation: MAYBE — technology-assisted language services are increasingly expected
  - Victim case tracking: YES — victims expect to be kept informed of their case

**If unexpected processing**: Additional safeguards for AI processing:
- ATRS transparency records published for all AI tools
- AI involvement disclosed to defendants and their representatives
- Defence can challenge AI-assisted disclosure in court
- Human-in-the-loop mandatory for all AI outputs (Principle 2)
- Audit trail of all AI processing available for review

### 2.4 Purpose and Benefits

#### What do we want to achieve?

**Intended Outcomes** (from Stakeholder Goals):

| Stakeholder Goal | Processing Contribution | Measurable Benefit |
|------------------|------------------------|-------------------|
| G-1: Reduce backlog to <50,000 | Cross-agency data integration eliminates manual rekeying; AI reduces disclosure time | 30% reduction in charge-to-trial time |
| G-2: AI-assisted disclosure | AI processes vast digital evidence volumes impossible for manual review | 50% reduction in disclosure review time per case |
| G-3: Defence equality of arms | Defence AI platform provides equivalent tools to prosecution | Zero successful legal challenges on technology inequality |
| G-4: Cross-agency interoperability | Automated API-based data exchange across all agencies | 90%+ automated case data exchange; 90% reduction in rekeying errors |
| G-7: Victim/witness experience | Real-time case tracking; automated Victims' Code compliance | 20% improvement in victim satisfaction; 90%+ Victims' Code compliance |
| G-10: Data protection compliance | DPIAs for all processing; automated retention; lawful basis documented | Zero ICO enforcement actions |

**Primary Benefit**: Faster, fairer criminal justice — reducing the backlog that causes victims to wait years for trial, while ensuring technology enhances rather than undermines fair trial rights.

#### Who benefits?

- [x] Data subjects:
  - **Defendants**: Faster case resolution (reduced time on bail/remand); AI-assisted defence preparation; fair trial preserved through equality of arms
  - **Victims**: Real-time case tracking; faster case disposal (reduced waiting); Victims' Code compliance
  - **Witnesses**: Better scheduling; reduced wasted attendance; remote evidence options
- [x] Organisation: Reduced operational costs; improved efficiency; legacy risk reduction
- [x] Society/public: Faster justice; reduced backlog; public confidence in criminal courts
- [x] Third parties: Defence practitioners (better tools); police (reduced case file burden)

---

## 3. Consultation

### 3.1 Data Protection Officer (DPO) Consultation

**DPO Name**: MoJ Data Protection Officer

**Date Consulted**: PENDING — to be consulted as part of DPIA approval process

**DPO Advice**:
- PENDING — DPO review required before any processing commences
- Preliminary guidance: DPA 2018 Part 3 applies to all law enforcement processing; joint controller arrangements required for cross-agency processing
- Early ICO engagement recommended given scale and novelty of AI in criminal justice

**DPO Recommendations**:
- Formal ICO consultation under Article 36 UK GDPR (prior consultation for high-risk processing)
- Joint controller agreements between MoJ, HMCTS, CPS, HMPPS, and LAA
- Specialist DPA 2018 Part 3 legal advice for all cross-agency data flows

**How DPO Advice Addressed**: PENDING — will be addressed in DPIA v1.1 after DPO review

### 3.2 Data Subject Consultation

**Consultation Method**:
- [ ] Not consulted (explain why: DPIA is at architecture stage; data subject consultation will occur during alpha/beta phases via GDS service assessment user research)

**Planned Consultation**:
- User research with all 8 personas (per GDS Service Standard Point 2) during alpha phase
- Specific privacy consultations with:
  - Victim representative groups (including RASSO victims via specialist charities)
  - Defence practitioners (Criminal Bar Association, Law Society)
  - Defendant representative groups (via solicitors and Legal Aid Agency)
  - Children's rights organisations (for Youth Court processing)
- Public consultation on AI use in criminal justice planned for Year 1

**Date(s) Consulted**: PENDING

### 3.3 Stakeholder Consultation

**Stakeholders Consulted** (from Stakeholder RACI):

| Stakeholder | Role | Date Consulted | Feedback Summary |
|-------------|------|----------------|------------------|
| MoJ Chief AI Officer | AI governance authority | PENDING | AI governance framework design input |
| ICO | Regulatory oversight | PENDING | DPA 2018 Part 3 compliance guidance |
| Lady Chief Justice | Judicial independence | PENDING | Judicial oversight of AI in court proceedings |
| CBA / Law Society | Defence representation | PENDING | Equality of arms in data access |
| Victims' Commissioner | Victims' interests | PENDING | Victim data protection and tracking |
| NPCC | Police data sharing | PENDING | Cross-agency data standards and sharing |

**Key Stakeholder Concerns** (anticipated from ARC-001-STKE-v1.0):
- Defence community: AI-assisted prosecution without equivalent defence capability creates data processing inequality
- Judiciary: AI must not influence judicial decisions; audit trails must be complete and accessible
- ICO: DPA 2018 Part 3 compliance for cross-agency law enforcement processing; AI fairness and transparency
- Victims' Commissioner: Enhanced protections for victim/witness data; no re-victimisation through data breaches

**Resolution**: To be addressed through stakeholder engagement plan during programme discovery phase

---

## 4. Necessity and Proportionality Assessment

### 4.1 Lawful Basis Assessment

**Primary Lawful Basis** (GDPR Article 6):

- [x] **(e) Public task** — Processing is necessary to perform a task in the public interest or for official functions
  - Public task: Administration of criminal justice in England and Wales
  - Statutory basis: Courts Act 2003 (HMCTS functions); Prosecution of Offences Act 1985 (CPS functions); Police and Criminal Evidence Act 1984 (police powers); Offender Management Act 2007 (HMPPS); Legal Aid, Sentencing and Punishment of Offenders Act 2012 (LAA)

**DPA 2018 Part 3 — Law Enforcement Processing**:

The primary processing basis for this programme is **DPA 2018 Part 3** (law enforcement processing), which applies to processing by competent authorities for law enforcement purposes. This provides a distinct legal framework from standard UK GDPR:

- **Section 35(2)**: Processing is lawful if necessary for the performance of a task carried out for law enforcement purposes by a competent authority
- **Competent authorities**: CPS (prosecution), police forces (investigation), HMCTS (court administration), HMPPS (offender management)
- **Section 35(3)**: Processing of sensitive data (equivalent to special category) requires Schedule 8 conditions

**Justification for Chosen Basis**: Criminal justice processing is a compulsory state function — the processing of defendant, victim, and witness data is inherent to the administration of justice. Consent is not appropriate because defendants cannot meaningfully consent to prosecution data processing, and the power imbalance makes consent inherently unfree. Public task/law enforcement purpose is the only appropriate basis.

### 4.2 Special Category Data Basis (Article 9)

**Applicable**: YES

Conditions:
- [x] **(f) Legal claims** or judicial acts — Processing is necessary for the establishment, exercise or defence of legal claims, or whenever courts are acting in their judicial capacity
- [x] **(g) Substantial public interest** (with UK law basis) — Administration of justice is a substantial public interest

**DPA 2018 Part 3 Sensitive Processing (Schedule 8)**:
- **Paragraph 1**: Processing is necessary for the exercise of a function conferred by an enactment or rule of law
- **Paragraph 2**: Processing is necessary for the administration of justice
- **Paragraph 3**: Processing is necessary for the exercise of a function of the Crown, a Minister, or a government department

**UK DPA 2018 Schedule 1 Condition**: Condition 6 (statutory purposes) and Condition 10 (preventing or detecting unlawful acts) for processing outside Part 3 scope

**Justification**: Criminal justice data processing inherently involves special category data — criminal offence data is the core of every case. Health data (mental health assessments), biometric data (forensic evidence), and ethnicity data are regularly part of case files. The legal basis is well-established through centuries of criminal justice administration; this programme modernises the technology through which lawful processing occurs, not the processing itself.

### 4.3 Necessity Assessment

**Is processing necessary to achieve the purpose?**

| Question | Answer | Justification |
|----------|--------|---------------|
| Can we achieve the purpose without processing personal data? | NO | Criminal cases inherently involve personal data — defendant identity, victim details, witness testimony, evidence. Justice cannot be administered without identifying the parties. |
| Can we achieve the purpose with less personal data? | PARTIALLY | Data minimisation applied: only case-relevant data processed; victim data subject to enhanced access restrictions (Principle 23); evidence packages limited to relevant material. However, reducing data further risks incomplete disclosure (a miscarriage of justice risk). |
| Can we achieve the purpose with less intrusive processing? | NO | Manual processing (the status quo) is slower but equally intrusive — the same data is processed, just less efficiently. AI processing is no more intrusive than manual review; it processes the same data with additional safeguards (audit trails, human oversight). The alternative of not modernising perpetuates the backlog, causing greater harm to victims and defendants. |
| Can we achieve the purpose by processing data for less time? | NO | Criminal justice retention periods are legally mandated. Cases can be appealed years after conviction. Evidence must be preserved. Shorter retention risks destroying data needed for appeal or review. |

**Necessity Conclusion**: Processing is **NECESSARY**

**Alternatives Considered**:
1. **Continue manual processing (status quo)** — Rejected because: 77,000+ case backlog growing; manual processing causes greater delays and harm to victims and defendants; legacy systems create higher security risk; manual data transfer between agencies creates higher error rates
2. **Process only anonymised data** — Rejected because: Criminal proceedings require identified individuals. Anonymised data cannot support case management, hearing scheduling, sentencing, or victim notification. Anonymisation is used for secondary purposes (analytics, research) but cannot replace identified processing for primary justice functions.

### 4.4 Proportionality Assessment

**Is the processing proportionate to the purpose?**

**Data Minimization**:
- [x] We only collect data that is adequate for the purpose — Case data limited to what is relevant to proceedings
- [x] We only collect data that is relevant for the purpose — Evidence packages contain only case-relevant material
- [x] We do not collect excessive data — DR-004 (victim/witness) collects minimum fields; vulnerability flags are purpose-specific

**Proportionality Factors**:

| Factor | Assessment | Score (1-5) |
|--------|------------|-------------|
| Severity of intrusion into private life | High — criminal proceedings are inherently intrusive | 4 |
| Benefits to data subjects | High — faster justice, fair trial, victim protection | 4 |
| Benefits to organisation | High — efficiency, cost reduction, risk reduction | 4 |
| Benefits to society | Very High — functioning criminal justice system is foundational | 5 |
| Reasonable alternatives exist | No — manual processing is equally intrusive and less effective | 1 |

**Proportionality Conclusion**: Processing is **PROPORTIONATE**

**Justification**: The intrusion into private life, while significant, is inherent to criminal justice administration — not created by this programme. The programme modernises how existing lawful processing occurs, adding safeguards (AI audit trails, automated retention, enhanced access controls) that do not exist in current manual processes. The benefits to data subjects (faster justice, victim tracking, equality of arms) and society (functioning courts, public safety) are substantial. No reasonable alternative exists that achieves the same outcomes with less intrusion.

---

## 5. Risk Assessment to Data Subjects

**CRITICAL**: These risks assess harm to **individuals' rights and freedoms**, NOT organisational risks. Organisational risks are in ARC-001-RISK-v1.0.

### 5.1 Risk Identification

**Risk Categories Considered**:
- Physical harm (safety of victims/witnesses, defendant welfare)
- Material damage (wrongful conviction/acquittal, discrimination, prolonged detention)
- Non-material damage (distress, loss of privacy, reputational damage, re-traumatisation)

### 5.2 Inherent Risks (Before Mitigation)

| Risk ID | Risk Description | Impact on Data Subjects | Likelihood | Severity | Risk Level | Risk Source |
|---------|------------------|-------------------------|------------|----------|------------|-------------|
| DPIA-001 | Unauthorised access to criminal justice data | Defendant/victim personal data exposed; potential intimidation, harm | Medium | Very High | **VERY HIGH** | Security vulnerability, insider threat |
| DPIA-002 | Data breach exposing victim/witness identity | Victims at risk of harm from perpetrators; witness intimidation; RASSO re-traumatisation | Low | Very High | **HIGH** | Cyber attack, system failure, human error |
| DPIA-003 | AI disclosure bias against protected characteristics | Disproportionate disclosure outcomes for ethnic minority defendants; unfair trial | Medium | Very High | **VERY HIGH** | Algorithm design, training data bias |
| DPIA-004 | AI error leads to missed disclosure | Relevant evidence not disclosed to defence; wrongful conviction risk | Medium | Very High | **VERY HIGH** | AI model limitation, data quality |
| DPIA-005 | Cross-agency data combination creates unexpected profiles | Data subjects tracked across agencies in ways they don't expect; function creep | Medium | High | **HIGH** | Data integration design |
| DPIA-006 | Excessive data retention beyond legal requirement | Personal data held longer than necessary; rehabilitation undermined | Medium | Medium | **MEDIUM** | Retention policy failure |
| DPIA-007 | Inaccurate data in cross-agency exchange | Wrong defendant identity linked to case; incorrect bail/remand status | Medium | Very High | **VERY HIGH** | Data migration, integration error |
| DPIA-008 | Children's data processed without adequate safeguards | Children's welfare compromised; development harmed; re-identification risk | Low | Very High | **HIGH** | Insufficient age-appropriate protections |
| DPIA-009 | AI transcription/translation error in court | Defendant misunderstood; witness testimony distorted; miscarriage of justice | Medium | High | **HIGH** | AI model accuracy, language limitations |
| DPIA-010 | Defence data inequality (prosecution access advantage) | Defendant's fair trial right undermined; structural unfairness | High | Very High | **VERY HIGH** | Programme sequencing, funding |
| DPIA-011 | Function creep — data used for purposes beyond original collection | Data collected for case management used for predictive policing or profiling | Low | High | **MEDIUM** | Mission creep, policy change |
| DPIA-012 | Re-identification of pseudonymised/anonymised data | Individuals identified from supposedly anonymised analytics data | Low | High | **MEDIUM** | De-anonymisation attack, data linkage |

**Likelihood Scale**:
- **Low**: Unlikely to occur (0-33% chance)
- **Medium**: May occur (34-66% chance)
- **High**: Likely to occur (67-100% chance)

**Severity Scale** (Impact on Individuals):
- **Low**: Minimal or no impact; temporary inconvenience
- **Medium**: Significant inconvenience or distress; some financial loss; minor reputational impact
- **High**: Serious consequences; significant financial loss; significant reputational damage; psychological harm
- **Very High**: Irreversible harm; severe financial loss; severe psychological trauma; physical safety risk; loss of liberty

**Risk Level Matrix**:

|            | Low Severity | Medium Severity | High Severity | Very High Severity |
|------------|-------------|-----------------|---------------|-------------------|
| **Low Likelihood**    | LOW  | LOW  | MEDIUM | HIGH |
| **Medium Likelihood** | LOW  | MEDIUM | HIGH | VERY HIGH |
| **High Likelihood**   | MEDIUM | HIGH | VERY HIGH | VERY HIGH |

### 5.3 Detailed Risk Analysis

**DPIA-001: Unauthorised Access to Criminal Justice Data**

**Description**: An unauthorised individual (external attacker or insider) gains access to criminal case records, defendant personal data, victim/witness details, or digital evidence. This could occur through compromised credentials, privilege escalation, or exploitation of a vulnerability in the cross-agency integration layer.

**Data Subjects Affected**: All categories — defendants, victims, witnesses, children. Estimated 1.3+ million individuals per year at risk.

**Harm to Individuals**:
- Physical: Victims at risk of harm from perpetrators if identity or location exposed. Witnesses at risk of intimidation.
- Material: Identity theft using defendant/victim personal data. Fraud using financial information in case files.
- Non-material: Severe distress from exposure of sensitive case details (RASSO, domestic abuse, mental health). Reputational damage. Loss of trust in criminal justice system.

**Likelihood Analysis**: Medium — Criminal justice systems are high-value targets (demonstrated by 2025 Legal Aid Agency breach). Cross-agency integration creates new attack surface. However, zero-trust architecture (Principle 3) and defence-in-depth significantly reduce probability.

**Severity Analysis**: Very High — Criminal justice data includes the most sensitive categories. Exposure of defendant data could affect employment and reputation. Exposure of victim data in RASSO or domestic abuse cases could endanger physical safety.

**Existing Controls**: Architecture Principle 3 (Security by Design — NON-NEGOTIABLE) mandates zero-trust, MFA, encryption, least privilege.

---

**DPIA-003: AI Disclosure Bias Against Protected Characteristics**

**Description**: AI models used for disclosure review exhibit systematic bias against protected characteristics — for example, language processing algorithms that flag communications from ethnic minority communities differently, or evidence triage that systematically undervalues certain types of evidence associated with particular demographic groups.

**Data Subjects Affected**: Defendants from ethnic minority backgrounds (disproportionately represented in the criminal justice system — Black defendants are overrepresented ~3x in Crown Court), defendants with mental health conditions, young defendants, defendants who are non-native English speakers.

**Harm to Individuals**:
- Physical: None directly, but wrongful conviction leads to imprisonment (loss of liberty)
- Material: Wrongful conviction; disproportionate prosecution outcomes; employment and life consequences
- Non-material: Discrimination; reinforcement of systemic injustice; loss of trust in justice system; psychological harm from unfair treatment

**Likelihood Analysis**: Medium — AI bias in language models is well-documented. Criminal justice datasets reflect historical systemic biases. The Lammy Review (2017) identified ethnic disproportionality across the justice system. AI trained on historical data will inherit these biases unless actively mitigated.

**Severity Analysis**: Very High — Biased disclosure could lead to wrongful conviction (loss of liberty), the most severe consequence in criminal justice. Even where bias does not cause wrongful conviction, systematic disproportionality undermines justice system legitimacy and violates Equality Act 2010 obligations.

**Existing Controls**: Architecture Principle 2 (Human-Centred AI Augmentation) mandates bias assessment; mandatory human-in-the-loop.

---

**DPIA-004: AI Error Leads to Missed Disclosure**

**Description**: AI disclosure review tool fails to identify material that should be disclosed to the defence — relevant evidence is categorised as non-disclosable due to AI model limitation, unusual file format, corrupted data, or contextual understanding failure. Prosecutor relies on AI categorisation and misses the material during human review.

**Data Subjects Affected**: Defendants whose fair trial rights depend on complete disclosure. Potentially hundreds of defendants per year if AI error is systematic.

**Harm to Individuals**:
- Physical: If wrongfully convicted, imprisonment (loss of liberty)
- Material: Wrongful conviction; criminal record affecting employment, housing, relationships
- Non-material: Miscarriage of justice; severe psychological harm; loss of years to wrongful imprisonment

**Likelihood Analysis**: Medium — AI models have known limitations with edge cases, unusual formats, and contextual understanding. Disclosure review requires nuanced understanding of legal relevance that AI may lack. However, AI processes evidence that humans also miss in manual review — the question is comparative, not absolute.

**Severity Analysis**: Very High — Missed disclosure is the leading cause of wrongful convictions and collapsed trials. The consequences for individuals (imprisonment, criminal record, destruction of reputation) are among the most severe possible.

**Existing Controls**: UC-1 mandates prosecutor review of all AI outputs; AI confidence scores flag uncertain categorisations; defence can challenge disclosure.

---

**DPIA-007: Inaccurate Data in Cross-Agency Exchange**

**Description**: Data errors introduced during cross-agency integration — incorrect defendant identity linked to a case (mistaken identity), wrong bail status transmitted (defendant released or detained in error), incorrect sentence data sent to HMPPS (wrong sentence length), or corrupted evidence integrity during transfer.

**Data Subjects Affected**: Defendants (incorrect detention/release; wrong identity), victims (incorrect case status), witnesses (incorrect scheduling).

**Harm to Individuals**:
- Physical: Defendant detained in error or released when dangerous. Victim safety if perpetrator released incorrectly.
- Material: Wrongful detention (habeas corpus implications); incorrect criminal record; employment consequences
- Non-material: Severe distress from incorrect case information; loss of trust in justice system

**Likelihood Analysis**: Medium — Data migration from 37 legacy systems is inherently risky. Cross-agency data exchange involves format translation, encoding conversion, and identifier matching. Historical incidents include prisoners released in error due to data errors.

**Severity Analysis**: Very High — Incorrect bail status can result in wrongful detention (loss of liberty) or dangerous release. Incorrect sentence data has direct consequences for individuals' freedom.

**Existing Controls**: DR-001 integrity constraints; automated reconciliation between systems; data quality requirements (zero tolerance for defendant identity/sentence/bail errors).

---

**DPIA-010: Defence Data Inequality (Prosecution Access Advantage)**

**Description**: Prosecution agencies (CPS with central funding and infrastructure) deploy AI tools for case preparation and disclosure while defence practitioners (fragmented, legally-aided, under-resourced) do not have equivalent tools. This creates a structural data processing advantage for the prosecution — the state can process and analyse evidence at scale while defence relies on manual review.

**Data Subjects Affected**: All defendants, particularly legally-aided defendants who cannot fund private technology. Approximately 400,000+ defendants per year.

**Harm to Individuals**:
- Physical: None directly
- Material: Structurally unfair trials; higher risk of wrongful conviction for defendants without AI-assisted defence; discrimination against legally-aided defendants
- Non-material: Violation of fair trial rights (Article 6 ECHR); erosion of equality of arms; systemic injustice; loss of public confidence in justice

**Likelihood Analysis**: High — This is the programme's most likely risk. CPS has centralised infrastructure; defence is fragmented across thousands of firms. Building defence capability simultaneously is "fundamentally more complex" (ARC-001-RISK-v1.0, R-002). Risk R-002 is rated Critical (residual score 20).

**Severity Analysis**: Very High — Fair trial rights are fundamental human rights. A structural prosecution advantage in evidence processing would be constitutionally unacceptable and could result in successful ECHR challenge halting the entire programme.

**Existing Controls**: BR-003 (MUST_HAVE) mandates simultaneous defence capability; Principle 21 (Equality of Arms); FR-009 (Defence Platform).

---

## 6. Mitigation Measures

### 6.1 Technical Measures

**Data Security** (per Principle 3 — Security by Design, NON-NEGOTIABLE):
- [x] **Encryption at rest** — AES-256 for all data stores containing case, personal, or evidential data; field-level encryption for special category data (victim PII, medical records)
- [x] **Encryption in transit** — TLS 1.3 for all API communication between agencies; mTLS for service-to-service authentication
- [x] **Pseudonymization** — Defendant/victim identifiers pseudonymised for analytics and secondary processing; separate key management
- [x] **Anonymization** — k-anonymity applied to statistical outputs; differential privacy for published analytics
- [x] **Access controls** — Role-Based Access Control (RBAC) with least privilege; Multi-Factor Authentication (MFA) for all human access; time-limited access tokens; need-to-know enforcement
- [x] **Audit logging** — All data access, AI processing, and administrative actions logged with immutable audit trail; 7-year retention; cross-agency correlation
- [x] **Data masking** — Dynamic masking of victim/witness identity for users without "enhanced protection" role; RASSO data masked by default
- [x] **Secure deletion** — Cryptographic erasure at retention expiry; automated deletion pipelines; verified destruction certification

**Data Minimization**:
- [x] **Collection limitation** — Only case-relevant personal data collected; DR-004 vulnerability fields are optional
- [x] **Storage limitation** — Automated deletion after retention period; alerts before expiry; no indefinite retention without legal basis
- [x] **Processing limitation** — Purpose binding enforced at API level; data tagged with processing purpose; cross-purpose use blocked without additional lawful basis
- [x] **Disclosure limitation** — Cross-agency sharing governed by data-sharing agreements; API-level access controls enforce which agencies can access which data categories

**Technical Safeguards for AI/ML** (per Principle 2 — Human-Centred AI Augmentation):
- [x] **Bias testing** — Mandatory bias testing across all 9 protected characteristics (Equality Act 2010) before deployment; quarterly retesting in production
- [x] **Model explainability** — LIME/SHAP explanations for all AI disclosure categorisations; decision path visible to prosecutors and defence
- [x] **Human oversight** — Human-in-the-loop for all AI outputs; prosecutors must review and approve/override every AI recommendation; no solely automated decisions
- [x] **Fairness metrics** — Demographic parity, equal opportunity, and calibration metrics monitored continuously; automatic alerts if metrics breach thresholds

**Privacy-Enhancing Technologies**:
- [x] **Differential privacy** for statistical analysis and published analytics
- [ ] Homomorphic encryption — considered for future phases; not currently feasible at required scale
- [ ] Secure multi-party computation — evaluated for cross-agency analytics; not in initial scope
- [ ] Zero-knowledge proofs — not applicable to current use cases

### 6.2 Organisational Measures

**Policies and Procedures**:
- [x] **Privacy Policy** — Clear, accessible privacy notices for all data subjects (defendants via legal representatives; victims via Victim Liaison Officers; witnesses via Witness Care Units)
- [x] **Data Protection Policy** — Internal MoJ data protection policy applicable to all staff with access to criminal justice data
- [x] **Retention and Disposal Policy** — Defined retention periods per criminal justice retention schedule; automated deletion; manual review for edge cases
- [x] **Data Breach Response Plan** — 72-hour notification to ICO; data subject notification where risk is high; coordinated cross-agency breach response; specific RASSO breach escalation procedure
- [x] **Data Subject Rights Procedures** — SAR, rectification, and erasure request processes tested and operational for all agencies

**Training and Awareness**:
- [x] **Staff training** — DPA 2018 Part 3 awareness for all staff; UK GDPR principles; secure handling of criminal justice data
- [x] **Role-specific training** — Enhanced training for AI tool users (prosecutors, defence practitioners) on data protection implications of AI-assisted processing
- [x] **Regular refresher training** — Frequency: Annual mandatory refresher; additional training on system changes

**Vendor Management**:
- [x] **Data Processing Agreements (DPAs)** — Contracts with all processors (technology vendors) compliant with DPA 2018 Part 3 s.59
- [x] **Vendor due diligence** — Security and privacy assessments before engagement; SC-cleared staff where required
- [x] **Regular audits** — Annual audits of processor compliance; additional audits for AI model vendors
- [ ] Data transfer safeguards — Not applicable: TC-001 mandates all processing within UK jurisdiction; no international transfers

**Governance**:
- [x] **Data Protection Officer (DPO)** — MoJ DPO appointed and accessible; each agency has own DPO for their processing
- [x] **Privacy by Design** — Architecture Principle 10 mandates privacy built into system design; DPIA completed before processing begins
- [x] **Privacy by Default** — Strictest privacy settings by default; data masked by default; access-on-request not access-by-default
- [x] **Regular reviews** — DPIA reviewed quarterly or on significant change (new AI model, new data category, new agency, regulatory change)

**Data Subject Rights Facilitation**:
- [x] **Subject Access Request (SAR) process** — Response within 1 month; identity verification; legal privilege exemptions applied; DPA 2018 Part 3 s.45 exemptions for prejudice to criminal proceedings
- [x] **Rectification process** — Mechanism to correct inaccurate data across all agency systems; cascade rectification to consuming systems
- [x] **Erasure process** — Limited applicability in criminal justice (legal retention obligations prevail); erasure available where no legal obligation to retain
- [x] **Restriction process** — Mechanism to restrict processing where accuracy contested or processing is unlawful
- [x] **Objection process** — Mechanism to object to automated decision-making; human review of any AI-assisted output on request

### 6.3 Mitigation Mapping

**Risk-by-Risk Mitigation**:

| Risk ID | Risk Title | Mitigations Applied | Responsibility | Implementation Date |
|---------|------------|---------------------|----------------|---------------------|
| DPIA-001 | Unauthorised access | Zero-trust architecture, MFA, RBAC, AES-256 encryption, audit logging, network segmentation | MoJ CISO / HMCTS CTO | Year 1 Q3 |
| DPIA-002 | Victim/witness data breach | Enhanced access controls for DR-004, dynamic data masking, RASSO escalation procedure, encrypted storage, breach response plan | MoJ DPO / HMCTS CISO | Year 1 Q3 |
| DPIA-003 | AI disclosure bias | Bias testing (9 protected characteristics), fairness metrics, LIME/SHAP explainability, human-in-the-loop, independent bias audit | MoJ Chief AI Officer | Year 1 Q3 (before AI deployment) |
| DPIA-004 | AI missed disclosure | Human-in-the-loop (mandatory), AI confidence scores, uncertain-category escalation, defence challenge right, AI audit trail | MoJ Chief AI Officer / CPS CDO | Year 1 Q3 (before AI deployment) |
| DPIA-005 | Cross-agency profiling | Purpose limitation at API level, data-sharing agreements, purpose tags on all data, prohibition on secondary use without new DPIA | MoJ DPO / All agency DPOs | Year 1 Q4 |
| DPIA-006 | Excessive retention | Automated deletion at retention expiry, 90-day alerts, retention schedule enforcement, annual audit | MoJ DPO / Data Governance | Year 1 Q2 |
| DPIA-007 | Inaccurate cross-agency data | Automated reconciliation, zero-tolerance validation (identity/sentence/bail), data quality metrics, cascade correction | HMCTS CTO / Programme Data Steward | Year 1 Q3 |
| DPIA-008 | Children's data safeguards | Enhanced access controls, age-appropriate privacy notices, minimisation, restricted AI processing of children's data | MoJ DPO / Programme Child Safeguarding | Year 1 Q3 |
| DPIA-009 | AI transcription/translation error | Human verification of AI outputs, confidence scoring, multi-language testing, fallback to human interpreters | MoJ Chief AI Officer / HMCTS | Year 1 Q2 |
| DPIA-010 | Defence data inequality | Simultaneous prosecution-defence deployment (BR-003), defence shared-service platform (FR-009), equality of arms assessment | Lord Chancellor / LAA CEO | Year 1 Q3 |
| DPIA-011 | Function creep | Purpose limitation policy, cross-purpose use prohibition, DPIA update for any new purpose, audit trail | MoJ DPO | Year 1 Q2 |
| DPIA-012 | Re-identification risk | k-anonymity (k≥5), differential privacy, aggregation thresholds, disclosure control review | MoJ DPO / Programme Data Science | Year 1 Q4 |

### 6.4 Residual Risk Assessment

**Risks After Mitigation**:

| Risk ID | Risk Title | Mitigations | Residual Likelihood | Residual Severity | Residual Risk Level | Acceptable? | Justification |
|---------|------------|-------------|---------------------|-------------------|---------------------|-------------|---------------|
| DPIA-001 | Unauthorised access | Zero-trust + MFA + RBAC + encryption + audit | Low | Very High | **HIGH** | YES (with conditions) | Zero-trust and defence-in-depth are industry best practice; residual risk reflects that no system is impenetrable |
| DPIA-002 | Victim/witness breach | Enhanced access + masking + RASSO procedure + encryption | Low | Very High | **HIGH** | YES (with conditions) | Enhanced controls beyond standard; RASSO-specific escalation; residual risk inherent to any system holding sensitive data |
| DPIA-003 | AI disclosure bias | Bias testing + fairness metrics + explainability + human-in-the-loop + independent audit | Low | Very High | **HIGH** | YES (with conditions) | Bias testing before deployment; ongoing monitoring; human override; cannot guarantee zero bias but controls are comprehensive |
| DPIA-004 | AI missed disclosure | Human-in-the-loop + confidence scores + escalation + defence challenge | Low | Very High | **HIGH** | YES (with conditions) | AI augments human review (does not replace it); defence can challenge; audit trail enables post-hoc review |
| DPIA-005 | Cross-agency profiling | Purpose limitation + sharing agreements + tags + prohibition | Low | High | **MEDIUM** | YES | Strong technical and organisational controls prevent unauthorised cross-purpose use |
| DPIA-006 | Excessive retention | Automated deletion + alerts + audit | Low | Medium | **LOW** | YES | Technical controls ensure compliance; automated enforcement removes human error |
| DPIA-007 | Inaccurate data | Reconciliation + zero-tolerance validation + quality metrics | Low | Very High | **HIGH** | YES (with conditions) | Validation catches most errors; zero-tolerance for identity/sentence/bail; residual risk from edge cases |
| DPIA-008 | Children's data | Enhanced controls + age-appropriate notices + minimisation | Low | High | **MEDIUM** | YES | Specific safeguards for children; limited processing; enhanced access controls |
| DPIA-009 | AI translation error | Human verification + confidence scores + fallback interpreters | Low | High | **MEDIUM** | YES | AI augments (not replaces) human interpreters; fallback available; confidence scoring flags uncertainty |
| DPIA-010 | Defence inequality | Simultaneous deployment + defence platform + equality assessment | Medium | Very High | **VERY HIGH** | NO (without conditions) | Requires Lord Chancellor funding decision (R-002). PROCESSING MUST NOT COMMENCE for prosecution AI until defence equivalent available. |
| DPIA-011 | Function creep | Purpose limitation + prohibition + DPIA update + audit | Low | High | **MEDIUM** | YES | Strong governance prevents mission creep; any new purpose requires fresh DPIA |
| DPIA-012 | Re-identification | k-anonymity + differential privacy + disclosure control | Low | Medium | **LOW** | YES | Standard statistical disclosure control adequate |

**Overall Residual Risk Level**: **HIGH**

**Acceptability Assessment**:
- [ ] All residual risks are LOW or MEDIUM → ACCEPTABLE
- [x] Some residual risks are HIGH → ACCEPTABLE WITH CONDITIONS (describe conditions)
- DPIA-010 remains VERY HIGH — NOT ACCEPTABLE without resolution of defence equality funding

**Conditions for Acceptance**:
1. **CRITICAL**: Prosecution AI tools (FR-001, UC-1) MUST NOT be deployed until defence equivalent (FR-009, UC-2) is available. This is a gateway condition — violation would expose defendants to structural unfairness.
2. **CRITICAL**: Independent AI bias audit must be completed before any AI tool processes live criminal justice data (DPIA-003).
3. **HIGH**: ICO prior consultation must be completed before programme-wide data processing commences (DPIA-001, DPIA-002).
4. **HIGH**: Cross-agency data-sharing agreements with DPA 2018 Part 3 compliant terms must be signed before automated data exchange begins (DPIA-005, DPIA-007).
5. **HIGH**: Children's data safeguarding review completed before Youth Court data processed through new systems (DPIA-008).
6. **MEDIUM**: AI incident response plan operational before AI tools go live (DPIA-003, DPIA-004, DPIA-009).

---

## 7. ICO Prior Consultation

**ICO Consultation Required**: **YES**

**Trigger**: ICO prior consultation is recommended because:
- Multiple residual risks remain HIGH after mitigation
- Processing involves law enforcement data at national scale under DPA 2018 Part 3
- Novel use of AI in criminal justice (first large-scale deployment in England and Wales)
- Cross-agency data integration between 5+ agencies with joint controller arrangements
- Processing affects vulnerable data subjects including children
- Aligns with ARC-001-RISK-v1.0, R-012 (ICO enforcement risk) mitigation strategy

**ICO Consultation Details**:

| Field | Value |
|-------|-------|
| ICO Reference Number | PENDING |
| Consultation Date | PENDING — Target Year 1 Q2 |
| ICO Case Officer | PENDING |
| ICO Advice Received | PENDING |
| ICO Recommendations | PENDING |
| ICO Approval | PENDING |
| Conditions | PENDING |
| How Conditions Addressed | PENDING |

**ICO Engagement Strategy**:
- Early informal engagement via ICO Sandbox (innovation advice service) for AI processing questions
- Formal Article 36 consultation submitted with full DPIA
- Specific DPA 2018 Part 3 advice sought for cross-agency law enforcement processing
- Joint controller agreement template reviewed with ICO

---

## 8. Sign-Off and Approval

### 8.1 DPIA Approval

| Role | Name | Decision | Date | Signature |
|------|------|----------|------|-----------|
| **Data Protection Officer** | MoJ DPO | PENDING | | |
| **Data Controller** | MoJ Permanent Secretary | PENDING | | |
| **Senior Responsible Owner** | MoJ CDIO | PENDING | | |

### 8.2 Conditions of Approval

**Conditions** (if any):
1. Lord Chancellor must confirm defence technology funding mechanism before prosecution AI deployment
2. Independent AI bias audit completed before live deployment
3. ICO prior consultation completed
4. Cross-agency data-sharing agreements signed
5. Children's data safeguarding review completed
6. AI incident response plan operational

**How Conditions Will Be Met**:
- Condition 1: Lord Chancellor's Office policy decision — Due: Year 1 Q2 — Responsibility: Lord Chancellor
- Condition 2: Independent audit commissioned — Due: Year 1 Q3 — Responsibility: MoJ Chief AI Officer
- Condition 3: ICO formal consultation — Due: Year 1 Q2 — Responsibility: MoJ DPO
- Condition 4: Bilateral then multilateral agreements — Due: Year 1 Q4 — Responsibility: MoJ Legal
- Condition 5: Safeguarding review — Due: Year 1 Q3 — Responsibility: MoJ DPO
- Condition 6: Incident response plan — Due: Year 1 Q2 — Responsibility: MoJ Communications / MoJ Chief AI Officer

### 8.3 Final Decision

**Decision**: **PROCEED WITH CONDITIONS**

**Rationale**: The processing is necessary, proportionate, and lawful under DPA 2018 Part 3 and UK GDPR Article 6(1)(e). The benefits to data subjects (faster justice, victim protection, equality of arms) and society (functioning criminal courts) are substantial. Risks are significant but mitigable through comprehensive technical and organisational measures. However, 6 conditions must be met before full deployment, with the defence equality condition being a gateway requirement that must be resolved at ministerial level.

**Effective Date**: Processing may commence in phases once conditions are met for each phase

---

## 9. Integration with Information Security Management

### 9.1 Link to Security Controls

**Security Assessment Reference**: Not yet generated — recommend `/arckit.secure` to create Secure by Design assessment

**DPIA Mitigations → Security Controls Mapping**:

| DPIA Mitigation | Security Control | NCSC CAF Principle | Implementation Status |
|-----------------|------------------|--------------------|-----------------------|
| Encryption at rest (AES-256) | Data security — encryption | A.3 Asset Management | Planned |
| Access controls (RBAC, MFA) | Identity and access management | B.1 Identity and Access | Planned |
| Audit logging (7-year retention) | Monitoring and audit | C.1 Security Monitoring | Planned |
| Zero-trust architecture | Network security | B.2 Device Security | Planned |
| Staff training (DPA Part 3) | Security awareness | D.1 People | Planned |
| Encryption in transit (TLS 1.3) | Communications security | B.3 Resilient Networks | Planned |
| Data masking (victim/witness) | Data protection | A.3 Asset Management | Planned |
| Breach response plan | Incident management | C.2 Proactive Security Event Discovery | Planned |

### 9.2 Link to Risk Register

**Risk Register Reference**: `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md`

**DPIA Risks to Add to Risk Register**:

| DPIA Risk ID | Suggested Risk Register ID | Risk Category | Owner | Treatment |
|--------------|---------------------------|---------------|-------|-----------|
| DPIA-001 | R-019 (existing: Cyber Attack) | TECHNOLOGY | MoJ CISO | Treat (mitigate) |
| DPIA-002 | NEW: R-021 | COMPLIANCE | MoJ DPO | Treat (mitigate) |
| DPIA-003 | R-013 (existing: AI Bias) | COMPLIANCE | MoJ Chief AI Officer | Treat (mitigate) |
| DPIA-004 | NEW: R-022 | COMPLIANCE | MoJ Chief AI Officer | Treat (mitigate) |
| DPIA-007 | NEW: R-023 | TECHNOLOGY | HMCTS CTO | Treat (mitigate) |
| DPIA-010 | R-002 (existing: Defence Equality) | COMPLIANCE | Lord Chancellor | Treat (mitigate — URGENT) |

---

## 10. Review and Monitoring

### 10.1 Review Triggers

**DPIA must be reviewed when**:
- [x] Significant change to processing (new data, new purpose, new systems)
- [x] New technology introduced (new AI model, new vendor, new integration)
- [x] New risks identified (e.g., new attack vectors, regulatory changes)
- [x] Data breach or security incident occurs
- [x] ICO guidance changes (particularly DPA 2018 Part 3 guidance)
- [x] Data subjects raise concerns (via SAR, complaints, or legal challenge)
- [x] Periodic review date reached
- [x] New agency added to cross-agency integration
- [x] AI model retrained or updated
- [x] Legislative change affecting criminal justice data (e.g., Victims and Prisoners Act implementation)

**Periodic Review Frequency**: Every **6** months (elevated frequency due to HIGH residual risk)

### 10.2 Review Schedule

| Review Type | Frequency | Next Review Date | Responsibility |
|-------------|-----------|------------------|----------------|
| **Periodic review** | 6 months | 2026-08-05 | MoJ DPO |
| **Post-implementation review** | 3 months after each major deployment phase | TBD per deployment schedule | Enterprise Architect |
| **Annual review** | Annually | 2027-02-05 | MoJ Permanent Secretary (Data Controller) |
| **AI model review** | On each model update or retrain | TBD | MoJ Chief AI Officer |

### 10.3 Monitoring Activities

**Ongoing Monitoring**:
- [x] Track number of SARs received and response times (target: <1 month)
- [x] Track data breaches and near-misses (target: 0 breaches)
- [x] Monitor audit logs for unauthorised access attempts (target: <10/month)
- [x] Review AI bias metrics quarterly (target: fairness ratio >0.8 across all protected characteristics)
- [x] Review data subject complaints (target: <5/month)
- [x] Track compliance with retention periods (target: 100% automated enforcement)
- [x] Monitor cross-agency data quality (target: <0.01% reconciliation errors)
- [x] Track defence equality metrics (prosecution vs defence tool availability)

**Monitoring Metrics**:

| Metric | Target | Measurement Frequency | Responsibility |
|--------|--------|----------------------|----------------|
| SAR response time | <1 month | Monthly | MoJ DPO |
| Data breaches | 0 | Continuous | MoJ CISO |
| Unauthorised access attempts | <10/month | Weekly | Security Team |
| AI bias fairness metrics | Ratio >0.8 across all protected characteristics | Quarterly | MoJ Chief AI Officer |
| AI disclosure accuracy | <0.1% missed material vs human-only review | Quarterly | CPS CDO |
| Defence tool parity | 100% parity with prosecution | Monthly | LAA CEO |
| Retention compliance | 100% automated | Monthly | Data Governance |
| Cross-agency data errors | <0.01% | Weekly | Programme Data Steward |

### 10.4 Change Management

**Change Control Process**:
1. Any change to processing must be assessed for DPIA impact by MoJ DPO
2. If change is significant (new data category, new AI model, new agency, new purpose), DPIA must be updated
3. Updated DPIA must be re-approved by DPO and Data Controller
4. Data subjects must be notified of significant changes via updated privacy notices
5. ICO must be informed of material changes to processing

**Change Log**:

| Change Date | Change Description | DPIA Impact | Updated Sections | Approved By |
|-------------|-------------------|-------------|------------------|-------------|
| 2026-02-05 | Initial DPIA creation | N/A — initial version | All | PENDING |

---

## 11. Traceability to ArcKit Artifacts

### 11.1 Source Artifacts

**This DPIA was generated from**:

| Artifact | Location | Information Extracted |
|----------|----------|----------------------|
| **Architecture Principles** | `projects/000-global/ARC-000-PRIN-v1.0.md` | Principle 2 (AI Augmentation), Principle 3 (Security by Design), Principle 10 (Privacy/Data Protection), Principle 21 (Equality of Arms), Principle 22 (Judicial Independence), Principle 23 (Victim/Witness Protection) |
| **Requirements** | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md` | BR-010 (data protection compliance), DR-001 to DR-004 (data entities), use cases UC-1 to UC-5, data volume/retention, functional requirements FR-001 to FR-014, TC-001 (UK jurisdiction), TC-006 (DPA Part 3) |
| **Stakeholder Analysis** | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` | Data subject categories, vulnerable groups, ICO stakeholder (SD-11), DPO role, power-interest analysis, stakeholder conflicts |
| **Risk Register** | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md` | R-002 (defence equality, Critical 20), R-005 (AI ethics), R-011 (data sharing), R-012 (ICO enforcement), R-013 (AI bias), R-019 (cyber attack) |
| **Architecture Strategy** | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STRAT-v1.0.md` | Technology approach, multi-vendor strategy, phased deployment, £281M investment |
| **Platform Design** | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-PLAT-v1.0.md` | Criminal Justice Digital Platform architecture, cross-agency integration design, data flows |
| **Data Model** | *Not yet generated* | Note: Data model (ARC-001-DATA-v*.md) would provide entity-level PII inventory, GDPR lawful basis mapping, and retention policies. Recommend generating via `/arckit.data-model`. |
| **Secure by Design Assessment** | *Not yet generated* | Note: SBD assessment would provide security controls mapping. Recommend generating via `/arckit.secure`. |

### 11.2 Traceability Matrix: Data → Requirements → DPIA

| Data Entity | PII Level | DR Requirement | Processing Purpose | DPIA Risk(s) | Lawful Basis |
|-------------|-----------|----------------|-------------------|-------------|--------------|
| Criminal Case Record | HIGH | DR-001 | Case management, cross-agency tracking | DPIA-005, DPIA-007, DPIA-011 | DPA 2018 Part 3 s.35(2) |
| Digital Evidence Package | VERY HIGH | DR-002 | Disclosure review (AI-assisted), evidence presentation | DPIA-003, DPIA-004, DPIA-012 | DPA 2018 Part 3 s.35(2) + Schedule 8 |
| Defendant Record | VERY HIGH (Special) | DR-003 | Case identification, bail management, sentencing | DPIA-001, DPIA-003, DPIA-007, DPIA-010 | DPA 2018 Part 3 s.35(2) + Schedule 8 |
| Victim/Witness Record | VERY HIGH (Enhanced) | DR-004 | Case tracking, witness care, special measures | DPIA-002, DPIA-008 | DPA 2018 Part 3 s.35(2) + Article 6(1)(e) |

### 11.3 Traceability Matrix: Stakeholder → Data Subject → Rights

| Stakeholder | Data Subject Type | Volume | Rights Processes Implemented | Vulnerability Safeguards |
|-------------|-------------------|--------|------------------------------|--------------------------|
| Defendants | Defendant | ~500,000/year | SAR (with s.45 limitations), Rectification, Restriction, AI override | Legal representation; equality of arms; human-in-the-loop |
| Victims/Witnesses | Victim/Witness | ~700,000/year | SAR, Rectification, Restriction | Enhanced access controls; data masking; RASSO escalation; special measures |
| Children | Child (defendant/victim/witness) | ~30,000/year | SAR (via guardian), Rectification, Restriction | Age-appropriate notices; enhanced access controls; minimisation; safeguarding review |
| Legal Practitioners | Professional | ~21,000 | SAR, Rectification, Erasure, Portability | Standard GDPR protections |
| Court Staff | Employee | ~15,000 | SAR, Rectification, Erasure, Portability | Standard GDPR protections |

### 11.4 Downstream Artifacts Informed by DPIA

**This DPIA informs**:

| Artifact | How DPIA Informs It |
|----------|---------------------|
| **Risk Register** (ARC-001-RISK-v1.0) | DPIA risks (DPIA-002, DPIA-004, DPIA-007) recommended for addition as R-021, R-022, R-023 |
| **Secure by Design Assessment** (planned) | DPIA mitigations become security control requirements |
| **AI Playbook Assessment** (planned) | DPIA-003 (AI bias) and DPIA-004 (AI error) findings inform AI ethics assessment |
| **ATRS Records** (planned) | DPIA AI processing assessment provides transparency information for ATRS |
| **TCoP Review** (ARC-001-TCOP-v1.0) | This DPIA addresses the CRITICAL blocker identified in Point 7 (non-compliant due to absent DPIA) |
| **Service Assessment** (planned) | DPIA demonstrates GDS Service Standard Point 9 (security/privacy) compliance |
| **Statement of Work** (ARC-001-SOW-v1.0) | DPIA requirements flow into vendor RFP data protection requirements |
| **Data Model** (planned) | DPIA findings should inform data model PII classification and retention design |

---

## 12. Data Subject Rights Implementation

### 12.1 Rights Checklist

**Right of Access (DPA 2018 Part 3, s.45)**:
- [x] Process implemented: SAR process via MoJ central SAR team with agency-specific data retrieval
- [x] Response time: Within 1 month (extendable by 2 months if complex; extendable by 1 month for large volumes)
- [x] Identity verification: Government-accepted ID verification; for defendants, verification via legal representative or prison/probation service
- [x] Information provided: Copy of data, processing purpose, categories, recipients, retention period, rights, source
- [x] Exemptions: s.45(4) — refusal where disclosure would prejudice criminal proceedings, national security, or detection of crime

**Right to Rectification (DPA 2018 Part 3, s.46)**:
- [x] Process implemented: Rectification via agency data stewards; cascade to all consuming systems
- [x] Verification: Accuracy verified against authoritative source (PNC, court record, agency system of record)
- [x] Notification: All agencies that received inaccurate data notified within 72 hours

**Right to Erasure (DPA 2018 Part 3, s.47)**:
- [x] Process implemented: Erasure where no legal retention obligation exists
- [x] Exceptions: Criminal justice retention schedule prevails; Rehabilitation of Offenders Act provisions; ongoing proceedings; legal hold
- [x] Third parties notified: All agencies that received data notified of erasure

**Right to Restriction of Processing (DPA 2018 Part 3, s.47(2))**:
- [x] Process implemented: Data flagged as restricted in all agency systems
- [x] Technical implementation: Restriction flag at record level; processing blocked except storage

**Right to Data Portability**:
- [ ] Not applicable under DPA 2018 Part 3 for law enforcement processing

**Right to Object (DPA 2018 Part 3)**:
- [x] Process implemented: Right to object to solely automated decision-making (s.49)
- [x] Human review available on request for any AI-assisted decision

**Rights Related to Automated Decision-Making (DPA 2018 Part 3, s.49-50)**:
- [x] Applicable: YES — AI-assisted disclosure review, scheduling, case summarisation
- [x] Safeguards: Human-in-the-loop (mandatory); explanation of AI logic; ability to challenge in court
- [x] Process: Data subjects (via legal representatives) can request human review of any AI-assisted decision; tribunal route available under s.50

### 12.2 Rights Fulfillment Procedures

**Standard Operating Procedures**:
1. **Receipt**: Rights requests received via MoJ central SAR email, web form, or postal address; agency-specific channels also accepted
2. **Verification**: Identity verified using government-accepted ID; defendants verified via solicitor or prison service
3. **Logging**: Request logged in central case management system with unique reference number
4. **Acknowledgement**: Acknowledgement sent within 5 working days
5. **Retrieval**: Data retrieved from all relevant agency systems (cross-agency data retrieval may be required)
6. **Review**: Legal/DPO review for exemptions (s.45(4) prejudice to proceedings; legal privilege)
7. **Response**: Response provided within 1 month (calendar)
8. **Escalation**: Complex requests escalated to MoJ DPO; cross-agency requests coordinated centrally

**Training**: All staff trained on rights fulfilment procedures — annual refresher training

---

## 13. International Data Transfers

**Applicable**: **NO**

TC-001 (Technical Constraint) mandates: "All data must reside within UK jurisdiction. No processing in non-UK data centres, including AI model inference."

Architecture Principle 10 (Privacy and Data Protection) reinforces: "Data residency within UK jurisdiction unless explicit legal basis for transfer."

All processing, including AI model inference, cloud hosting, and backup/DR, must occur within UK data centres. This eliminates international transfer risks but must be verified with each vendor and cloud provider.

**Verification Requirements**:
- All cloud hosting regions confirmed as UK (e.g., AWS eu-west-2, Azure UK South/West, GCP europe-west2)
- AI model inference endpoints confirmed within UK
- Backup and disaster recovery sites within UK
- Vendor sub-processor locations verified as UK-only
- Contractual prohibition on processing outside UK in all DPAs

---

## 14. Children's Data

**Processing Children's Data**: **YES**

### 14.1 Age Verification

**Age Threshold**: 10 years (age of criminal responsibility in England and Wales) to 17 years

**Age Verification Method**: Date of birth verified at charge/first hearing; Youth Court jurisdiction confirmed by age at offence date; child witnesses identified by victim/witness liaison

**Parental Consent**: Not applicable — processing is based on law enforcement purpose (DPA 2018 Part 3), not consent. However, parents/guardians are engaged:
- Parent/guardian informed of data processing at first court appearance
- Subject access requests for children under 13 typically made by parent/guardian
- Youth Offending Teams liaison ensures appropriate adult involvement

### 14.2 Additional Safeguards for Children

- [x] **Privacy notice for children** — Age-appropriate language privacy notice for Youth Court; simplified explanation of data use
- [x] **Minimization** — Only data essential to proceedings collected; non-relevant personal data excluded
- [x] **No profiling** — Children's data not used for profiling or risk assessment by AI tools (enhanced restriction)
- [x] **No AI decision-making** — AI-assisted processing of children's cases subject to enhanced human oversight; additional review step for Youth Court cases
- [x] **Secure processing** — Enhanced access controls for children's data; separate access role required
- [x] **Timely deletion** — Children's data subject to Rehabilitation of Offenders Act provisions; spent convictions deleted from active records
- [x] **No sharing** — Children's data shared only with agencies with lawful basis; enhanced restrictions on secondary use

### 14.3 Best Interests Assessment

**Assessment**: Is processing in the child's best interests? **YES — with conditions**

**Justification**: Processing children's data is inherent to criminal justice administration when children are involved as defendants, victims, or witnesses. Faster case processing benefits child defendants (reduced time in uncertain status), child victims (reduced waiting for justice), and child witnesses (reduced trauma from prolonged proceedings). AI translation benefits non-English-speaking children. However, AI processing of children's cases requires enhanced human oversight to ensure that algorithmic decisions do not disproportionately affect children, and children's rehabilitation prospects must be protected through appropriate data handling.

---

## 15. Algorithmic/AI Processing

**Algorithmic Processing**: **YES**

Also complete `/arckit.ai-playbook` and `/arckit.atrs` assessments.

### 15.1 Algorithm Description

**Algorithm Type**:
- [x] Natural language processing (disclosure review, case summarisation)
- [x] Machine learning (supervised — evidence categorisation)
- [x] Rule-based system (scheduling optimisation, retention enforcement)
- [x] Deep learning (transcription, translation)

**Processing Type**:
- [x] Classification (evidence categorisation: disclosable/non-disclosable/under review)
- [x] Recommendation (scheduling recommendations, case priority)
- [x] Anomaly detection (data quality anomalies in cross-agency exchange)

**Human Oversight**:
- [x] Human-in-the-loop (human can override) — MANDATORY for all AI outputs per Principle 2

### 15.2 Algorithmic Bias Assessment

**Protected Characteristics Considered** (all 9 Equality Act 2010 characteristics):
- [x] Age
- [x] Disability
- [x] Gender reassignment
- [x] Marriage and civil partnership
- [x] Pregnancy and maternity
- [x] Race
- [x] Religion or belief
- [x] Sex
- [x] Sexual orientation

**Bias Testing**:
- [x] Training data reviewed for bias — mandatory before deployment
- [x] Fairness metrics calculated (demographic parity, equal opportunity, equalized odds) — quarterly
- [x] Disparate impact analysis conducted — before deployment and quarterly
- [x] Regular monitoring for bias in production — continuous with alerting

**Bias Mitigation**:
- [x] Diverse training data — representative of criminal justice population demographics
- [x] Fairness constraints in model — optimisation includes fairness objectives
- [x] Human review of edge cases — uncertain AI outputs escalated to human reviewer
- [x] Regular retraining — models retrained on representative data; bias regression testing
- [x] Explainability tools (LIME, SHAP) — feature attributions available for all AI outputs

**Key Bias Concerns for Criminal Justice**:
- **Racial bias**: Black defendants are overrepresented ~3x in Crown Court. Training data reflecting this overrepresentation may perpetuate discriminatory patterns. Specific testing required for racial fairness in disclosure categorisation.
- **Socioeconomic bias**: Legally-aided defendants may use different language patterns in communications data. AI must not disadvantage based on socioeconomic indicators.
- **Language bias**: Non-native English speakers' communications may be processed differently by NLP models. AI translation accuracy must be equivalent across languages.

### 15.3 Explainability and Transparency

**Explainability Level**:
- [x] Limited explainability (feature importance) — for ML classification models
- [x] Full explainability (decision path visible) — for rule-based systems

**Explanation Mechanism**:
- AI disclosure categorisation provides: confidence score, top contributing features (via SHAP), and natural language explanation of why material was categorised as disclosable/non-disclosable
- Defence practitioners can view AI reasoning and challenge categorisations
- Audit trail records full AI decision path for each evidence item
- ATRS record published publicly for each AI tool

**ATRS Compliance**: To be generated via `/arckit.atrs` — records to be published at `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-ATRS-v*.md`

---

## 16. Summary and Conclusion

### 16.1 Key Findings

**Processing Summary**:
- Processing 8+ categories of personal data across 4 core data entities (DR-001 to DR-004)
- Processing 5 special category data types (criminal offence, health, biometric, ethnicity, sexual offence)
- Affecting 1.3+ million data subjects per year (5+ million over programme)
- For purposes: administration of criminal justice (case management, disclosure, victim tracking, cross-agency integration)
- Using lawful basis: DPA 2018 Part 3 s.35(2) — law enforcement processing by competent authorities
- Using special category basis: DPA 2018 Part 3 Schedule 8 — statutory functions, administration of justice

**Risk Summary**:
- 12 risks identified to data subjects' rights and freedoms
- 4 VERY HIGH risks before mitigation (DPIA-001, DPIA-003, DPIA-004, DPIA-007, DPIA-010)
- 5 HIGH risks after mitigation (DPIA-001, DPIA-002, DPIA-003, DPIA-004, DPIA-007)
- 1 VERY HIGH risk after mitigation (DPIA-010 — defence equality, dependent on ministerial decision)
- Overall residual risk: **HIGH**

**Compliance Summary**:
- [x] Necessity and proportionality demonstrated (Section 4)
- [x] Lawful basis identified — DPA 2018 Part 3 s.35(2) + Schedule 8
- [ ] Data subjects consulted — PENDING (planned for alpha phase)
- [ ] DPO consulted — PENDING (required before processing)
- [x] Risks identified and mitigated (Section 5 and 6)
- [x] Data subject rights processes in place (Section 12)
- [x] Security measures designed (Section 6.1; full implementation pending)
- [x] Review schedule established (Section 10)

### 16.2 Recommendations

**Recommendations**:
1. **CRITICAL**: Resolve defence equality funding mechanism (DPIA-010) before any prosecution AI deployment — this is the single most important condition
2. **CRITICAL**: Commission independent AI bias audit across all 9 protected characteristics before AI tools process live criminal justice data
3. **HIGH**: Complete formal ICO prior consultation under Article 36 UK GDPR given the scale, sensitivity, and novelty of processing
4. **HIGH**: Generate data model (`/arckit.data-model`) to provide entity-level PII inventory, GDPR lawful basis mapping, and retention policy design that this DPIA can reference
5. **HIGH**: Generate Secure by Design assessment (`/arckit.secure`) to map DPIA mitigations to NCSC CAF security controls
6. **HIGH**: Generate ATRS records (`/arckit.atrs`) for each AI tool to provide algorithmic transparency
7. **MEDIUM**: Conduct user research with all 8 personas specifically on data protection and AI transparency concerns
8. **MEDIUM**: Establish joint controller agreements between MoJ, HMCTS, CPS, HMPPS, and LAA

**Actions Required Before Go-Live**:

| Action | Responsibility | Due Date | Status |
|--------|----------------|----------|--------|
| Lord Chancellor decision on defence funding mechanism | Lord Chancellor's Office | Year 1 Q2 | Not Started |
| Independent AI bias audit | MoJ Chief AI Officer | Year 1 Q3 | Not Started |
| ICO formal prior consultation | MoJ DPO | Year 1 Q2 | Not Started |
| Cross-agency data-sharing agreements (DPA Part 3) | MoJ Legal | Year 1 Q4 | Not Started |
| Joint controller agreements | MoJ Legal / All agency DPOs | Year 1 Q3 | Not Started |
| Children's data safeguarding review | MoJ DPO / Safeguarding Lead | Year 1 Q3 | Not Started |
| AI incident response plan | MoJ Communications / AI Officer | Year 1 Q2 | Not Started |
| Data subject privacy notices (DPA Part 3 compliant) | MoJ DPO | Year 1 Q2 | Not Started |
| Generate data model (ARC-001-DATA) | Enterprise Architect | Year 1 Q1 | Not Started |
| Generate Secure by Design assessment (ARC-001-SECD) | Enterprise Architect | Year 1 Q1 | Not Started |
| Generate ATRS records | Enterprise Architect | Year 1 Q2 | Not Started |

### 16.3 Final Conclusion

**Conclusion**: **PROCEED WITH CONDITIONS**

**Rationale**: This DPIA confirms that the Criminal Courts Technology & AI Reform programme's data processing is necessary, proportionate, and lawful. The processing modernises existing criminal justice administration — the same data that is currently processed manually will be processed more efficiently and with stronger safeguards. The benefits to data subjects (faster justice, victim protection, equality of arms, enhanced security) and to society (functioning criminal courts, reduced backlog, public confidence) are substantial and well-evidenced. However, the residual risks are HIGH due to the sensitivity of criminal justice data, the scale of processing, and the novel use of AI. Six conditions must be met before full deployment, with defence equality being the gateway condition.

**Conditions**:
1. CRITICAL: Defence AI capability must be available simultaneously with prosecution AI deployment
2. CRITICAL: Independent AI bias audit completed before live AI processing of criminal justice data
3. HIGH: ICO prior consultation completed
4. HIGH: Cross-agency data-sharing agreements signed
5. HIGH: Children's data safeguarding review completed
6. HIGH: AI incident response plan operational

**Sign-Off**: This DPIA has been completed and is PENDING APPROVAL. Processing may commence subject to conditions above once DPO and Data Controller sign-off is obtained.

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | Principles 2, 3, 10, 21, 22, 23 | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | BR-010, DR-001-004, UC-1-5, TC-001, TC-006 | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md` |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | Data subjects, ICO (SD-11), DPO role, conflicts | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` |
| ARC-001-RISK-v1.0 | Risk Register | ArcKit | R-002, R-005, R-011, R-012, R-013, R-019 | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md` |
| ARC-001-STRAT-v1.0 | Architecture Strategy | ArcKit | Technology approach, investment, phasing | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STRAT-v1.0.md` |
| ARC-001-PLAT-v1.0 | Platform Design | ArcKit | CJDP architecture, data flows | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-PLAT-v1.0.md` |
| ARC-001-TCOP-v1.0 | TCoP Review | ArcKit | Point 7 non-compliance (DPIA absence) | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-TCOP-v1.0.md` |

---

## Generation Metadata

**Generated by**: ArcKit `/arckit.dpia` command
**Generated on**: 2026-02-05
**ArcKit Version**: 1.5.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**Model**: Claude Opus 4.6 (claude-opus-4-6)

**Traceability**: This DPIA is traceable to architecture principles, requirements, stakeholders, and risk register via the ArcKit governance framework. Data model (ARC-001-DATA-v*.md) and Secure by Design assessment (ARC-001-SECD-v*.md) not yet generated — recommend generating these to strengthen DPIA traceability.

---

## Appendix A: ICO DPIA Screening Checklist

Full screening questionnaire (9 criteria) with detailed YES/NO/N/A responses:

1. ☑ Evaluation or scoring (including profiling) — **YES**: AI disclosure review evaluates evidence
2. ☑ Automated decision-making with legal/significant effect — **YES**: AI pre-categorises evidence affecting disclosure
3. ☑ Systematic monitoring — **YES**: Victim case tracking; defendant progression tracking
4. ☑ Sensitive data or highly personal data — **YES**: Criminal offence, health, biometric, RASSO
5. ☑ Large scale processing — **YES**: 500,000+ cases/year; national scope; 100TB evidence/year
6. ☑ Matching or combining datasets — **YES**: 5+ agency data integration
7. ☑ Vulnerable data subjects — **YES**: Defendants, children, victims, witnesses
8. ☑ Innovative technology — **YES**: First large-scale AI in English criminal courts
9. ☐ Processing prevents exercising rights — **NO**: Rights preserved under DPA 2018 Part 3

**Score: 8/9 — DPIA REQUIRED**

---

## Appendix B: GDPR Article 35 Requirements Checklist

| Article 35 Requirement | Addressed in Section | Complete? |
|------------------------|---------------------|-----------|
| Systematic description of processing | Section 2 | ✓ |
| Purposes of processing | Section 2.4 | ✓ |
| Assessment of necessity and proportionality | Section 4 | ✓ |
| Assessment of risks to data subjects | Section 5 | ✓ |
| Measures to address risks | Section 6 | ✓ |
| Safeguards, security measures | Section 6 | ✓ |
| Demonstrate compliance with GDPR | Throughout | ✓ |

---

## Appendix C: Data Protection Principles Compliance

**GDPR Article 5 Principles** (as applied through DPA 2018 Part 3, s.34-40):

| Principle | Assessment | Evidence |
|-----------|------------|----------|
| **(a) Lawfulness, fairness, transparency** | COMPLIANT | DPA 2018 Part 3 lawful basis identified (s.35(2)); privacy notices planned; AI transparency via ATRS |
| **(b) Purpose limitation** | COMPLIANT | Purposes clearly defined in Section 2.4; purpose tags on data; function creep controls in Section 6 |
| **(c) Data minimization** | COMPLIANT | Only case-relevant data collected; DR-004 optional fields; evidence limited to relevant material |
| **(d) Accuracy** | COMPLIANT | Zero-tolerance validation for identity/sentence/bail; automated reconciliation; rectification process |
| **(e) Storage limitation** | COMPLIANT | Retention periods defined per criminal justice schedule; automated deletion; 90-day expiry alerts |
| **(f) Integrity and confidentiality** | COMPLIANT | Security by Design (Principle 3, NON-NEGOTIABLE); AES-256 encryption; zero-trust; MFA; audit logging |
| **Accountability** | PARTIAL | DPIA completed; DPO involvement planned; policies designed. Full compliance requires DPO sign-off and ICO consultation. |

---

## Appendix D: Glossary

| Term | Definition |
|------|------------|
| **Data Subject** | An identified or identifiable natural person whose personal data is being processed |
| **Data Controller** | The organisation that determines the purposes and means of processing personal data |
| **Data Processor** | An organisation that processes personal data on behalf of the controller |
| **Personal Data** | Any information relating to an identified or identifiable natural person |
| **Special Category Data** | Sensitive personal data (race, health, biometric, etc.) requiring Article 9 basis |
| **Criminal Offence Data** | Data relating to criminal convictions and offences (Article 10 UK GDPR / DPA 2018 Part 3) |
| **Processing** | Any operation performed on personal data (collection, storage, use, disclosure, deletion) |
| **Profiling** | Automated processing to evaluate personal aspects (predict performance, behaviour, preferences) |
| **Pseudonymization** | Processing that prevents identification without additional information kept separately |
| **Anonymization** | Irreversibly removing identifying information so re-identification is not possible |
| **Lawful Basis** | Legal ground for processing under GDPR Article 6 (consent, contract, legal obligation, etc.) |
| **DPIA** | Data Protection Impact Assessment — required for high-risk processing |
| **ICO** | Information Commissioner's Office — UK data protection supervisory authority |
| **UK GDPR** | UK General Data Protection Regulation (retained EU GDPR post-Brexit) |
| **DPA 2018** | Data Protection Act 2018 — UK law supplementing GDPR |
| **DPA 2018 Part 3** | Law enforcement processing provisions of the Data Protection Act 2018, implementing the EU Law Enforcement Directive |
| **ATRS** | Algorithmic Transparency Recording Standard — UK Government requirement for public sector algorithmic tools |
| **RASSO** | Rape and Serious Sexual Offences — cases requiring enhanced data protections |
| **PNC** | Police National Computer — national database of criminal records |
| **NCSC CAF** | National Cyber Security Centre Cyber Assessment Framework |
| **SCC** | Standard Contractual Clauses — mechanism for international data transfers (not applicable — UK-only processing) |
| **Joint Controller** | Two or more controllers that jointly determine purposes and means of processing |

---

**END OF DPIA**

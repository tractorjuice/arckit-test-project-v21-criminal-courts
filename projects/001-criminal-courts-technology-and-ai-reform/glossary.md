# Glossary: Criminal Courts Technology & AI Reform

> **Template Origin**: Official | **ArcKit Version**: 1.5.0 | **Command**: `/arckit.glossary`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-GLOS-v1.0 |
| **Document Type** | Project Glossary |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.0 |
| **Created Date** | 2026-03-16 |
| **Last Modified** | 2026-03-16 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-06-14 |
| **Owner** | MoJ Chief Digital and Information Officer |
| **Reviewed By** | PENDING |
| **Approved By** | PENDING |
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, HMPPS Digital, Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-16 | ArcKit AI | Initial creation from `/arckit:glossary` command | PENDING | PENDING |

---

## Purpose

This glossary provides a single, authoritative reference for all terminology, acronyms, and abbreviations used within the Criminal Courts Technology & AI Reform project. It ensures consistent understanding across all stakeholders — including MoJ, HMCTS, CPS, HMPPS, LAA, police forces, judiciary, and defence practitioners — reduces ambiguity in architecture artifacts, and supports onboarding of new team members.

**Scope**: All terms, acronyms, and abbreviations referenced in the 19 project architecture documents, 6 Wardley mapping artifacts, and global architecture principles.

**Authority**: MoJ Enterprise Architecture team, with contributions from all programme workstreams.

**Usage**: All project documentation SHOULD reference this glossary for canonical definitions. When a term has a project-specific meaning that differs from common usage, the glossary definition takes precedence.

> **Note**: The Wardley Doctrine Assessment (ARC-001-WDOC-v1.0) identifies "Common Language" as the programme's most critical doctrine gap (Score: 1/5). This glossary is a first step toward addressing that gap. Cross-agency terminology alignment requires active governance beyond this document.

---

## Conventions

- Terms are listed in **alphabetical order** within each section
- **Bold** terms within definitions indicate cross-references to other glossary entries
- The **Source Artifact** column references the document where the term was first defined or is most relevant
- The **Category** column classifies terms to aid filtering and navigation
- Acronyms and abbreviations are listed separately for quick lookup
- Where a term has multiple meanings in different contexts, each meaning is listed as a separate row with the context noted

---

## Glossary

### Business Terms

| Term | Definition | Source Artifact | Category |
|------|------------|-----------------|----------|
| Adjournment | Postponement of a court hearing to a future date, often due to administrative, legal, or technical reasons. The programme targets a 50% reduction in adjournments caused by administrative/technical failures. | ARC-001-REQ-v1.0 | Business |
| Backlog (Crown Court) | The number of outstanding criminal cases awaiting hearing in the Crown Court. At programme inception: 77,000+ cases. Target: below 50,000 within 3 years. | ARC-001-REQ-v1.0 | Business |
| Case collapse | A criminal trial that cannot proceed on the scheduled date due to failures in preparation, disclosure, witness attendance, or other factors. Disclosure-related collapses are a primary target for AI intervention. | ARC-001-REQ-v1.0 | Business |
| Case file (digital) | A structured electronic package containing all materials relating to a criminal case: charges, evidence list, witness statements, defendant details, and case history. The programme defines a standardised **Digital Case File Standard** (FR-005). | ARC-001-REQ-v1.0 | Business |
| Case progression | The movement of a criminal case through the justice system from charge to outcome (conviction, acquittal, or other disposal). | ARC-001-STKE-v1.0 | Business |
| Charge-to-trial time | The elapsed time between a suspect being charged and the trial taking place. Target: 30% reduction, from 18+ months to < 13 months. | ARC-001-REQ-v1.0 | Business |
| Common Platform | The existing HMCTS/CPS court case management system. A modern web-based application with £250M+ investment, experiencing troubled rollout. Programme strategy: stabilise and extend via API-first refactoring, not replace. | ARC-001-STRAT-v1.0 | Business |
| Cracked trial | A trial listed as effective that does not proceed because the defendant changes their plea or the prosecution offers no evidence on the day. | ARC-001-REQ-v1.0 | Business |
| Criminal justice chain | The sequence of organisations a criminal case passes through: police → CPS → HMCTS → HMPPS → LAA. Also referred to as the "justice pipeline". | ARC-001-STRAT-v1.0 | Business |
| Crown Court | The higher criminal court in England and Wales, hearing serious criminal cases before a judge and jury. Distinct from **Magistrates' Court**. | ARC-001-REQ-v1.0 | Business |
| Defence equality of arms | The principle that defence practitioners must have access to technology tools equivalent to those available to prosecution agencies. A constitutional requirement derived from Article 6 ECHR. Architecture Principle P-21. | ARC-001-STRAT-v1.0 | Business |
| Disclosure | The legal obligation on the prosecution to disclose to the defence all material that might reasonably undermine the prosecution case or assist the defence. Disclosure failure is the leading cause of collapsed trials. | ARC-001-REQ-v1.0 | Business |
| Effective trial | A trial that proceeds as scheduled without being cracked, adjourned, or vacated. Target: 15% increase in effective trial rates. | ARC-001-REQ-v1.0 | Business |
| Judicial independence | The constitutional principle that judges make decisions free from external influence. Architecture Principle P-22: technology must not constrain judicial discretion. The judiciary holds effective veto over case-affecting AI. | ARC-000-PRIN-v1.0 | Business |
| Leveson Review | The Independent Review of the Criminal Courts (2025-2026). Made 180 recommendations including AI for case preparation, legacy migration, and cross-agency integration. The programme's primary mandate. | ARC-001-STRAT-v1.0 | Business |
| Listing | The process of scheduling cases for hearing in court. AI-assisted scheduling is a programme capability (FR-006). | ARC-001-REQ-v1.0 | Business |
| Magistrates' Court | The lower criminal court handling summary offences and initial hearings. Staffed by volunteer magistrates or district judges. | ARC-001-REQ-v1.0 | Business |
| Pre-sentence report | A report prepared by a probation officer for the sentencing judge, assessing the offender's circumstances and recommending sentencing options. | ARC-001-STKE-v1.0 | Business |
| Special measures | Court arrangements to support vulnerable or intimidated witnesses when giving evidence, including screens, video links, and intermediaries. | ARC-001-REQ-v1.0 | Business |
| Victims' Code | The Code of Practice for Victims of Crime. Strengthened by Victims and Prisoners Act 2024. The programme targets 90%+ automated compliance monitoring. | ARC-001-REQ-v1.0 | Business |

### Technical Terms

| Term | Definition | Source Artifact | Category |
|------|------------|-----------------|----------|
| AI augmentation | The approach where AI assists human decision-making rather than replacing it. Architecture Principle P-02: "AI augments rather than replaces human decision-making." All criminal justice AI must operate with mandatory human-in-the-loop. | ARC-000-PRIN-v1.0 | Technical |
| AI categorisation taxonomy | Classification system for CJS AI tools: productivity AI (low risk), insight AI (medium risk), accessibility AI (medium risk), predictive AI (high risk, prohibited without ministerial and judicial approval). | ARC-001-REQ-v1.0 | Technical |
| AI disclosure review | AI-assisted capability analysing digital evidence to identify potentially disclosable material with confidence scores. HIGH-RISK AI requiring human-in-the-loop, ATRS, DPIA, and judicial approval. | ARC-001-REQ-v1.0 | Technical |
| API-first | Architectural approach where all capabilities are exposed through versioned APIs before any UI is built. Architecture Principle P-01. | ARC-000-PRIN-v1.0 | Technical |
| Bias testing | Systematic evaluation of AI outputs across protected characteristics to detect discriminatory patterns. Required for all HIGH-RISK AI. | ARC-001-DPIA-v1.0 | Technical |
| CJS Data Standards | Cross-agency data schema, API specifications, evidence formats, and digital case file standards. Currently in development (evolution 0.28). Planned for open publication. | ARC-001-WARD-001-v1.0 | Technical |
| Cloud-native | Approach exploiting cloud computing: containers, microservices, immutable infrastructure, declarative APIs. Programme-mandated architecture. | ARC-001-STRAT-v1.0 | Technical |
| Confidence score | Numerical value (0.0-1.0) from an AI model indicating certainty about a classification. Shown to prosecutors alongside disclosure recommendations. | ARC-001-REQ-v1.0 | Technical |
| Cross-agency integration platform | Central API-first integration layer connecting all 5 justice agencies. Evolution 0.35 (custom, moving toward product). | ARC-001-WARD-001-v1.0 | Technical |
| Event-driven architecture | Integration pattern using asynchronous events (e.g., "charge filed", "hearing outcome"). Architecture Principle P-12. | ARC-000-PRIN-v1.0 | Technical |
| Evolution (Wardley) | Movement of a component from Genesis (novel) through Custom-Built and Product to Commodity (utility). Driven by supply and demand competition. | ARC-001-WARD-001-v1.0 | Technical |
| Fitness function | Automated test assessing whether an architecture characteristic meets a threshold. Used in evolutionary architecture. | ARC-001-WCLM-001-v1.0 | Technical |
| Human-in-the-loop | Design pattern where AI outputs must be reviewed by a human before being acted upon. Mandatory for all case-affecting CJS AI. Implemented as the Human Review Queue component. | ARC-001-REQ-v1.0 | Technical |
| Infrastructure as Code (IaC) | Managing infrastructure through machine-readable files rather than manual configuration. Architecture Principle P-17. | ARC-000-PRIN-v1.0 | Technical |
| LLM (Large Language Model) | AI model trained on large text datasets for understanding and generating language. Programme uses Azure OpenAI and AWS Bedrock. Evolution 0.68 (product, rapidly commoditising). | ARC-001-WARD-001-v1.0 | Technical |
| Strangler-fig pattern | Migration approach where a new system gradually replaces legacy by intercepting calls. Used for the 37 legacy application migrations. | ARC-001-STRAT-v1.0 | Technical |
| Wardley Map | Strategic situational awareness technique mapping components by visibility (user needs → infrastructure) and evolution (genesis → commodity). | ARC-001-WARD-001-v1.0 | Technical |
| Zero Trust | Security architecture requiring strict identity verification for every access request. Architecture Principle P-03: defence-in-depth with zero-trust principles. | ARC-000-PRIN-v1.0 | Technical |

### Governance Terms

| Term | Definition | Source Artifact | Category |
|------|------------|-----------------|----------|
| AI governance framework | Programme framework for CJS AI: categorisation, ATRS registration, DPIA, judicial approval gates, ethics review, bias testing. Genesis component (evolution 0.20) — first globally for criminal justice. | ARC-001-REQ-v1.0 | Governance |
| Doctrine (Wardley) | Universal strategic principles across 4 phases and 6 categories. Programme maturity: 2.1/5.0. | ARC-001-WDOC-v1.0 | Governance |
| GDS Service Standard | 14-point standard for UK Government digital services. Assessed at alpha, beta, and live. | ARC-001-TCOP-v1.1 | Governance |
| Green Book | HM Treasury guidance on appraisal and evaluation. Programme SOBC follows the 5-case model. | ARC-001-SOBC-v1.0 | Governance |
| IPA Gateway Review | Assurance review by the Infrastructure and Projects Authority. Programme targets Amber/Green or better. | ARC-001-REQ-v1.0 | Governance |
| Judicial steering group | Governance body of senior judges providing oversight of AI in criminal proceedings. Effective veto over case-affecting AI. | ARC-001-REQ-v1.0 | Governance |
| Orange Book | HM Treasury risk management guidance. Programme risk register follows Orange Book methodology. | ARC-001-RISK-v1.0 | Governance |
| Peace/War/Wonder cycle | Wardley's macro-strategic cycle. CJS technology assessed as entering early War phase — AI industrialisation forcing transformation. | ARC-001-WCLM-001-v1.0 | Governance |
| Programme board | Multi-agency governance body chaired by MoJ CDIO with cross-agency representation. | ARC-001-STKE-v1.0 | Governance |
| Technology Code of Practice (TCoP) | 13-point UK Government technology standard. Programme assessed at 6/13 compliant. | ARC-001-TCOP-v1.1 | Governance |

### Financial Terms

| Term | Definition | Source Artifact | Category |
|------|------------|-----------------|----------|
| Benefits realisation | Systematic tracking of whether investment benefits are achieved. Quarterly tracking with independent verification required. | ARC-001-SOBC-v1.0 | Financial |
| DOS (Digital Outcomes and Specialists) | Digital Marketplace framework for procuring digital outcomes and specialist individuals. Used for genesis/custom components. | ARC-001-WARD-001-v1.0 | Financial |
| G-Cloud | Digital Marketplace framework for cloud hosting, software, and support. Used for product/commodity components. | ARC-001-WARD-001-v1.0 | Financial |
| Jevons Paradox | Efficiency improvements in resource use lead to increased total consumption, not reduced spending. Applied: AI efficiency will increase total AI compute demand. | ARC-001-WCLM-001-v1.0 | Financial |
| NPV (Net Present Value) | Present value of benefits minus costs, discounted at Treasury rate. Programme SOBC demonstrates positive NPV. | ARC-001-SOBC-v1.0 | Financial |

### Data Terms

| Term | Definition | Source Artifact | Category |
|------|------------|-----------------|----------|
| Criminal justice data | Personal data processed for criminal offence prevention, investigation, detection, or prosecution. Subject to DPA 2018 Part 3, stricter than general UK GDPR. | ARC-001-DPIA-v1.0 | Data |
| Data rekeying | Manual re-entry of data that already exists in another system. Currently occurs 5+ times per case. Target: 90% reduction. | ARC-001-REQ-v1.0 | Data |
| Digital evidence | Evidence in electronic form: body-worn video, communications data, documents, images, social media. | ARC-001-REQ-v1.0 | Data |
| DPIA (Data Protection Impact Assessment) | Systematic assessment of data processing impact on privacy. Mandatory under UK GDPR Article 35 for high-risk processing. Programme DPIA: HIGH impact. | ARC-001-DPIA-v1.0 | Data |
| Special category data | Data revealing racial/ethnic origin, political opinions, religious beliefs, health, etc. Requires additional safeguards in criminal justice. | ARC-001-DPIA-v1.0 | Data |

### Security Terms

| Term | Definition | Source Artifact | Category |
|------|------------|-----------------|----------|
| NCSC CAF | National Cyber Security Centre Cyber Assessment Framework. Required for government systems processing sensitive data. | ARC-000-PRIN-v1.0 | Security |
| OFFICIAL | UK Government security classification for information not subject to heightened threat. Programme default classification. | ARC-001-DPIA-v1.0 | Security |
| Security by Design | Security controls embedded from inception, not retrospectively. Architecture Principle P-03: NON-NEGOTIABLE. | ARC-000-PRIN-v1.0 | Security |

---

## Acronyms & Abbreviations

| Acronym | Expansion | Context |
|---------|-----------|---------|
| ADR | Architecture Decision Record | Programme governance |
| AI | Artificial Intelligence | Technology capability |
| ATRS | Algorithmic Transparency Recording Standard | UK Government AI transparency; mandatory for public sector AI |
| BR | Business Requirement | Requirement ID prefix (BR-001 to BR-010) |
| CAF | Cyber Assessment Framework | NCSC security assessment |
| CAPEX | Capital Expenditure | Financial planning (£181M programme allocation) |
| CBA | Criminal Bar Association | Professional body for criminal barristers |
| CDDO | Central Digital and Data Office | Cabinet Office digital standards |
| CDIO | Chief Digital and Information Officer | MoJ technology leadership |
| CJS | Criminal Justice System | System of agencies handling criminal cases in England and Wales |
| CJDP | Criminal Justice Digital Platform | Target-state integrated digital platform |
| COTS | Commercial Off-The-Shelf | Pre-built software products |
| CPS | Crown Prosecution Service | Prosecution agency for England and Wales |
| DOS | Digital Outcomes and Specialists | Digital Marketplace procurement framework |
| DPA | Data Protection Act (2018) | UK data protection legislation; Part 3 = law enforcement |
| DPO | Data Protection Officer | Statutory data protection oversight role |
| DPP | Director of Public Prosecutions | Head of CPS |
| DR | Data Requirement | Requirement ID prefix |
| ECHR | European Convention on Human Rights | Article 6 = right to a fair trial |
| EqIA | Equality Impact Assessment | Impact on protected characteristics |
| FR | Functional Requirement | Requirement ID prefix (FR-001 to FR-010+) |
| GDS | Government Digital Service | UK Government digital standards body |
| GDPR | General Data Protection Regulation (UK) | Data protection regulation (retained EU law) |
| HMCTS | His Majesty's Courts and Tribunals Service | Courts and tribunals agency |
| HMPPS | His Majesty's Prison and Probation Service | Prisons and probation agency |
| IAM | Identity and Access Management | Authentication and authorisation technology |
| ICO | Information Commissioner's Office | UK data protection regulator |
| ILC | Innovate, Leverage, Commoditise | Wardley gameplay pattern |
| INT | Integration Requirement | Requirement ID prefix |
| IPA | Infrastructure and Projects Authority | Government major projects oversight |
| LAA | Legal Aid Agency | Legal aid administration agency |
| LLM | Large Language Model | AI model type for NLP tasks |
| MoJ | Ministry of Justice | Government department for justice policy |
| MoSCoW | Must, Should, Could, Won't | Requirements prioritisation method |
| NAO | National Audit Office | Parliamentary spending auditor |
| NCSC | National Cyber Security Centre | UK Government cyber security authority |
| NFR | Non-Functional Requirement | Requirement ID prefix (NFR-P, NFR-SEC, NFR-A sub-prefixes) |
| NLP | Natural Language Processing | AI technique for human language |
| NPCC | National Police Chiefs' Council | Police force coordination body |
| NPV | Net Present Value | Financial appraisal metric |
| OPEX | Operational Expenditure | Financial planning (£100M programme allocation) |
| OWM | OnlineWardleyMaps | Wardley Map rendering tool (create.wardleymaps.ai) |
| RACI | Responsible, Accountable, Consulted, Informed | Stakeholder responsibility matrix |
| SLA | Service Level Agreement | Service quality commitment |
| SOBC | Strategic Outline Business Case | Green Book business case format |
| SRO | Senior Responsible Owner | Named programme accountable (MoJ Permanent Secretary) |
| TCoP | Technology Code of Practice | UK Government technology standards (13 points) |
| TCO | Total Cost of Ownership | Full lifecycle cost metric |
| WCAG | Web Content Accessibility Guidelines | W3C standard; programme targets 2.2 AA |

---

## Standards Reference Table

| Standard | Version | Relevance | URL |
|----------|---------|-----------|-----|
| GDS Service Standard | 2024 | Mandatory for all UK Government digital services | https://www.gov.uk/service-manual/service-standard |
| Technology Code of Practice | 2024 | 13-point technology standard; 6/13 compliant | https://www.gov.uk/guidance/the-technology-code-of-practice |
| UK GDPR | 2018 (retained) | Data protection regulation | https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/ |
| Data Protection Act 2018 Part 3 | 2018 | Law enforcement data processing | https://www.legislation.gov.uk/ukpga/2018/12/part/3 |
| NCSC Cyber Assessment Framework | 2023 | Cyber resilience for government systems | https://www.ncsc.gov.uk/collection/caf |
| AI Playbook | 2024 | Responsible AI in public services | https://www.gov.uk/government/publications/ai-playbook |
| ATRS | 2023 | Government AI transparency reporting | https://www.gov.uk/government/collections/algorithmic-transparency-recording-standard-hub |
| WCAG | 2.2 AA | Web accessibility; mandatory for government | https://www.w3.org/TR/WCAG22/ |
| HM Treasury Green Book | 2022 | Appraisal and evaluation guidance | https://www.gov.uk/government/publications/the-green-book-appraisal-and-evaluation-in-central-government |
| HM Treasury Orange Book | 2023 | Risk management guidance | https://www.gov.uk/government/publications/orange-book |
| Victims' Code | 2024 | Code of Practice for Victims of Crime | https://www.gov.uk/government/publications/the-code-of-practice-for-victims-of-crime |
| OpenAPI Specification | 3.1 | API description standard; mandated for APIs | https://spec.openapis.org/oas/v3.1.0 |
| Wardley Mapping | 2024 | Strategic situational awareness (CC BY-SA 4.0) | https://learnwardleymapping.com/ |

---

## Requirement ID Prefix Reference

| Prefix | Expansion | Description | Example |
|--------|-----------|-------------|---------|
| BR | Business Requirement | High-level business outcomes | BR-001: Reduce Crown Court case backlog |
| FR | Functional Requirement | Specific system capabilities | FR-001: AI Disclosure Review Engine |
| NFR | Non-Functional Requirement | Quality attributes and constraints | NFR-P-001: Response time |
| NFR-P | Performance NFR | Response time, throughput, scalability | |
| NFR-SEC | Security NFR | Authentication, encryption, access control | |
| NFR-A | Availability NFR | Uptime, resilience, disaster recovery | |
| INT | Integration Requirement | Cross-system data exchange | INT-001: Police-CPS evidence integration |
| DR | Data Requirement | Data storage, quality, retention | DR-001: Common data standards |

---

## Terminology Inconsistencies Identified

The following terms are used inconsistently across project artifacts and require cross-agency alignment:

| Term | Usage in Context A | Usage in Context B | Recommended Resolution |
|------|---------------------|---------------------|----------------------|
| "Case" | HMCTS: a court matter with a URN | CPS: a prosecution file; Police: an investigation | Adopt CJS Data Standards definition: "A criminal proceeding identified by a URN, encompassing investigation, prosecution, court proceedings, and sentence management" |
| "Outcome" | HMCTS: result of a hearing (guilty/not guilty/adjourned) | HMPPS: the sentence imposed; Programme: a strategic objective | Disambiguate: "hearing outcome" (HMCTS), "sentence outcome" (HMPPS), "programme outcome" (strategic) |
| "Evidence" | Police: all material gathered during investigation | CPS: material meeting the evidential test; Defence: material disclosed by prosecution | Adopt categories: "investigation material" (all), "prosecution evidence" (tested), "disclosure material" (shared with defence) |
| "Platform" | Programme: "CJDP" vision | HMCTS: "Common Platform" (existing system) | Always qualify: "Common Platform" (existing) vs. "CJDP" (target-state) |

---

## Traceability

| Document | Document ID | Terms Contributed |
|----------|-------------|-------------------|
| Architecture Principles | ARC-000-PRIN-v1.0 | 18 terms |
| Requirements | ARC-001-REQ-v1.0 | 32 terms |
| Stakeholder Analysis | ARC-001-STKE-v1.0 | 14 terms |
| Risk Register | ARC-001-RISK-v1.0 | 6 terms |
| Strategic Outline Business Case | ARC-001-SOBC-v1.0 | 8 terms |
| Architecture Strategy | ARC-001-STRAT-v1.0 | 15 terms |
| TCoP Assessment | ARC-001-TCOP-v1.1 | 5 terms |
| DPIA | ARC-001-DPIA-v1.0 | 10 terms |
| Platform Design | ARC-001-PLAT-v1.0 | 4 terms |
| Wardley Map (Current) | ARC-001-WARD-001-v1.0 | 12 terms |
| Wardley Map (Future) | ARC-001-WARD-002-v1.0 | 3 terms |
| Wardley Value Chain | ARC-001-WVCH-001-v1.0 | 4 terms |
| Wardley Doctrine | ARC-001-WDOC-v1.0 | 6 terms |
| Wardley Gameplay | ARC-001-WGAM-001-v1.0 | 5 terms |
| Wardley Climate | ARC-001-WCLM-001-v1.0 | 8 terms |

---

**Generated by**: ArcKit `/arckit:glossary` command
**Generated on**: 2026-03-16 20:00 GMT
**ArcKit Version**: 1.5.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: claude-opus-4-6
**Generation Context**: Extracted from 15 project artifacts across requirements, stakeholders, strategy, risk, SOBC, DPIA, TCoP, platform design, and 6 Wardley mapping artifacts

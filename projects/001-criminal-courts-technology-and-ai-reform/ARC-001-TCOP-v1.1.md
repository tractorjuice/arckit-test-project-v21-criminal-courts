# Technology Code of Practice (TCoP) Review

> **Template Status**: Beta | **Version**: 1.5.0 | **Command**: `/arckit.tcop`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-TCOP-v1.1 |
| **Document Type** | Technology Code of Practice Review |
| **Project** | Criminal Courts Technology & AI Reform (Project 001) |
| **Classification** | OFFICIAL |
| **Status** | DRAFT |
| **Version** | 1.1 |
| **Created Date** | 2026-02-05 |
| **Last Modified** | 2026-02-05 |
| **Review Cycle** | Quarterly |
| **Next Review Date** | 2026-05-05 |
| **Owner** | [OWNER_NAME_AND_ROLE] |
| **Reviewed By** | [PENDING] |
| **Approved By** | [PENDING] |
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, GDS/CDDO, Programme Board |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-05 | ArcKit AI | Initial creation from `/arckit.tcop` command | [PENDING] | [PENDING] |
| 1.1 | 2026-02-05 | ArcKit AI | Refreshed assessment: Point 7 upgraded from Non-Compliant to Partially Compliant following DPIA completion (ARC-001-DPIA-v1.0); overall score improved 5/13 → 6/13; template aligned to latest version; added DPIA as source artifact | [PENDING] | [PENDING] |

## Document Purpose

This document assesses the Criminal Courts Technology & AI Reform programme's compliance with the UK Government Technology Code of Practice (TCoP) — a set of 13 criteria to help government design, build and buy technology. This review supports Digital Spend Control submissions and programme governance, identifying compliance strengths, gaps, and actions required before progression through delivery phases. The programme is currently in the **pre-Discovery/strategic planning phase** — assessments reflect planned approach rather than implemented capability.

**Changes from v1.0**: This revision incorporates the completed Data Protection Impact Assessment (ARC-001-DPIA-v1.0), which was the CRITICAL BLOCKER identified in v1.0. Point 7 (Make Privacy Integral) has been upgraded from Non-Compliant to Partially Compliant.

---

## Executive Summary

**Overall TCoP Compliance**: ⚠️ Partially Compliant

**Project Phase**: Pre-Discovery / Strategic Planning

**Key Findings**:
- **Strengths**: The programme has strong strategic foundations — comprehensive stakeholder analysis (ARC-001-STKE-v1.0), 23 architecture principles explicitly aligned to TCoP (ARC-000-PRIN-v1.0), cloud-first strategy (ARC-001-STRAT-v1.0), open standards commitment (Principle 20), robust purchasing strategy via Digital Marketplace procurement (ARC-001-SOW-v1.0), and a completed DPIA (ARC-001-DPIA-v1.0) addressing law enforcement data processing
- **Gaps**: No user research conducted yet (Point 1), no accessibility testing (Point 2), no security assessment completed (Point 6), no sustainability assessment (Point 12), and no GDS service assessment preparation (Point 13)
- **Critical Actions**: Complete Secure by Design assessment; commission accessibility audit during Alpha; conduct user research with all 8 identified personas; conduct sustainability assessment for AI workloads
- **Improvement since v1.0**: Point 7 CRITICAL BLOCKER resolved — DPIA completed with 8/9 ICO criteria, 12 risks identified, 6 conditions for deployment

**Phase-Appropriate Assessment**: At the pre-Discovery stage, many points cannot be fully compliant. This review establishes the baseline and identifies what must be completed at each subsequent phase gate.

---

## TCoP Point 1: Define User Needs

**Guidance**: Understand your users and their needs. Develop knowledge of your users and what that means for your technology project or programme.

**Reference**: https://www.gov.uk/guidance/define-user-needs

### Assessment

**Status**: ⚠️ Partially Compliant

**Evidence**:
The programme has completed a comprehensive stakeholder analysis (ARC-001-STKE-v1.0) identifying 15 stakeholder groups with drivers, goals, and measurable outcomes. The requirements document (ARC-001-REQ-v1.0) defines 8 user personas across the criminal justice ecosystem:

1. **CPS Prosecutor** — disclosure review, case preparation
2. **Defence Barrister/Solicitor** — equivalent AI tools, case analysis
3. **Court Staff (HMCTS)** — case management, scheduling
4. **Judge/Magistrate** — digital courtroom, AI-augmented listing
5. **Victim** — case tracking, notifications, Victims' Code compliance
6. **Witness** — remote evidence, scheduling
7. **Police Officer** — digital case file preparation, evidence sharing
8. **HMPPS Probation Officer** — sentence data, pre-sentence reports

Five use cases are defined (UC-1 through UC-5) with detailed actor flows, preconditions, and postconditions. The DPIA (ARC-001-DPIA-v1.0) further identifies data subjects across all 8 personas, including volume estimates (1.3M+ data subjects/year) and vulnerability classifications.

However, no primary user research has been conducted. Personas and use cases are derived from the Leveson Review's findings and stakeholder analysis rather than direct user interviews, contextual inquiry, or usability testing.

**User Research Conducted**:
- [ ] User interviews completed
- [x] User personas created (8 personas in ARC-001-REQ-v1.0 — derived from stakeholder analysis, not primary research)
- [ ] User journey mapping done
- [x] Accessibility needs identified (Principle 15 — WCAG 2.2 AA target; NFR-U-003 requires magistrate-appropriate interfaces)
- [x] Digital inclusion considerations documented (ARC-001-REQ-v1.0 considers low-digital-skill magistrates, vulnerable witnesses, defendants)

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Commission primary user research programme with all 8 personas during Discovery phase. Must include court staff (who experienced Common Platform frustrations), defence practitioners (who have minimal technology experience), and victims/witnesses (who are hard-to-reach users under stress)
- **MEDIUM PRIORITY**: Create validated user journey maps for the 5 core use cases
- **MEDIUM PRIORITY**: Conduct accessibility audit of existing Common Platform to baseline current experience

---

## TCoP Point 2: Make Things Accessible and Inclusive

**Guidance**: Make sure your technology, infrastructure and systems are accessible and inclusive for all users.

**Reference**: https://www.gov.uk/guidance/make-things-accessible

### Assessment

**Status**: ⚠️ Partially Compliant

**Evidence**:
Architecture Principle 15 (Accessibility and Inclusive Design) mandates WCAG 2.2 Level AA for all user-facing systems and requires testing with assistive technologies. Requirements NFR-U-001 through NFR-U-004 specify:
- WCAG 2.2 Level AA compliance target
- Multi-language support (leveraging AI translation — FR-003)
- Simplified interfaces for volunteer magistrates (FR-006)
- Usability for users under stress (defendants, victims, witnesses)

The programme explicitly recognises diverse user needs: volunteer magistrates with limited digital skills, defendants who may have learning difficulties, victims in distress, witnesses with disabilities, and practitioners using assistive technology. The platform design (ARC-001-PLAT-v1.0) identifies accessibility as a cross-cutting capability. The DPIA (ARC-001-DPIA-v1.0) reinforces this by identifying children (30,000+/year) and vulnerable adults as data subjects requiring age-appropriate interfaces and enhanced safeguards.

However, no accessibility testing has been conducted and no accessibility statement exists.

**Accessibility Standards**:
- [x] WCAG 2.2 Level AA compliance target set (Principle 15, NFR-U-001)
- [ ] Accessibility audit completed
- [ ] Assistive technology testing done
- [ ] Accessibility statement published
- [ ] Regular accessibility testing scheduled

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Ensure accessibility expertise is embedded in all delivery teams from Alpha onwards
- **HIGH PRIORITY**: Commission accessibility audit of Common Platform (baseline) and all new services during Beta
- **MEDIUM PRIORITY**: Test with assistive technologies including screen readers, voice control, and magnification
- **MEDIUM PRIORITY**: Publish accessibility statement for each public-facing service before Beta assessment
- **LOW PRIORITY**: Establish regular accessibility regression testing in CI/CD pipeline (Principle 18)

---

## TCoP Point 3: Be Open and Use Open Source

**Guidance**: Publish your code and use open source software to improve transparency, flexibility and accountability.

**Reference**: https://www.gov.uk/guidance/be-open-and-use-open-source

### Assessment

**Status**: ⚠️ Partially Compliant

**Evidence**:
Architecture Principle 20 (Open Standards and Avoid Lock-In) commits to using open standards and open-source components where appropriate. The architecture strategy (ARC-001-STRAT-v1.0) Technology Radar places open-source infrastructure tooling in the "Adopt" ring (Terraform/CDK, event-driven integration). The SOW (ARC-001-SOW-v1.0) requires vendors to demonstrate open-source usage and data export capability.

The multi-vendor procurement strategy explicitly aims to avoid lock-in, and the SOW requires vendors to provide exit provisions and data portability. The defence technology platform (FR-009) is envisaged as potentially open-source or shared-service to ensure equality of arms.

However, no code has been written yet, and no decisions on code publication or open-source licence selection have been made.

**Open Source Practices**:
- [ ] Code published in open repositories
- [x] Open source libraries to be used where appropriate (Principle 20, Strategy Technology Radar)
- [ ] Contribution guidelines published
- [ ] Open source licenses reviewed and documented
- [x] Proprietary software justified where used (SOW requires justification; abstraction layers mandated by Principle 20)

**Gaps/Actions Required**:
- **MEDIUM PRIORITY**: Establish code publication policy during Discovery — define which components will be published openly and which require restricted access (given criminal justice sensitivity)
- **MEDIUM PRIORITY**: Define open-source licence strategy (consider GDS Service Manual guidance on open source)
- **LOW PRIORITY**: Create contribution guidelines for any openly published code

---

## TCoP Point 4: Make Use of Open Standards

**Guidance**: Build technology that uses open standards to ensure your technology works and communicates with other technology, and can easily be upgraded and expanded.

**Reference**: https://www.gov.uk/guidance/make-use-of-open-standards

### Assessment

**Status**: ✅ Compliant

**Evidence**:
Open standards are comprehensively embedded in the programme's architecture:

- **Principle 1** (Cross-Agency Interoperability): Mandates API-first approach with published interface specifications using open standards (OpenAPI, AsyncAPI, event schemas)
- **Principle 20** (Open Standards and Avoid Lock-In): Requires open standards for data formats, protocols, and interfaces
- **FR-004** (Cross-Agency API Gateway): Specifies standardised data exchange using open formats
- **FR-005** (Digital Case File Standard): Defines a common, open schema for police → CPS case file transfer
- **Strategy Technology Radar**: REST APIs, JSON, OAuth 2.0/OIDC, HTML5 all in "Adopt" ring
- **SOW Section 2**: Vendors must use open standards for all integrations

The event-driven architecture (Principle 12) specifies versioned event schemas for case progression, and the API gateway design uses OpenAPI specifications.

**Open Standards Used**:
- [x] RESTful APIs with OpenAPI/Swagger specs (Principle 1, FR-004)
- [x] JSON/XML for data interchange (FR-005, Digital Case File Standard)
- [x] OAuth 2.0/OIDC for authentication (Principle 3, zero-trust architecture)
- [x] HTML5, CSS3 for web interfaces (implied by WCAG 2.2 AA target)
- [x] Open standards documented in architecture (Principle 20, Strategy Technology Radar)

**Gaps/Actions Required**:
- **LOW PRIORITY**: Formally document the approved open standards catalogue during Alpha
- **LOW PRIORITY**: Confirm specific event schema standards (CloudEvents, AsyncAPI) during architecture design

---

## TCoP Point 5: Use Cloud First

**Guidance**: Consider using public cloud solutions first as stated in the Cloud First policy.

**Reference**: https://www.gov.uk/guidance/use-cloud-first

### Assessment

**Status**: ✅ Compliant

**Evidence**:
The programme has explicitly adopted a cloud-first, cloud-native strategy:

- **Architecture Strategy** (ARC-001-STRAT-v1.0): Cloud-native is a key strategic decision. "Cloud-native services" are in the "Adopt" ring of the Technology Radar. "On-premises infrastructure for new services" is explicitly in the "Hold" (Avoid) ring.
- **Principle 5** (Scalability and Elasticity): Mandates horizontal scaling and auto-scaling, which requires cloud infrastructure
- **Principle 4** (Legacy Modernisation): Directs migration of 37 legacy applications to supported platforms (cloud-hosted)
- **SOW**: Procurement via G-Cloud framework for cloud infrastructure
- **SOBC** (ARC-001-SOBC-v1.0): Business case models cloud hosting costs
- **Risk Register** (ARC-001-RISK-v1.0): No risk identified related to on-premises hosting — cloud assumed throughout
- **DPIA** (ARC-001-DPIA-v1.0): UK data residency confirmed (TC-001); cloud regions must be UK-located (AWS eu-west-2, Azure UK South/West, GCP europe-west2)

Data residency is addressed: Principle 10 requires UK jurisdiction for criminal justice data, and the SOW mandates UK-located data centres for all cloud hosting.

**Cloud First Considerations**:
- [x] Public cloud considered as first option (Strategy: Cloud-Native decision)
- [x] Cloud hosting decision documented (ARC-001-STRAT-v1.0)
- [x] If not public cloud, justification documented (N/A — public cloud adopted)
- [ ] Cloud security controls implemented (planned — Principle 3, not yet implemented)
- [x] Data residency requirements met (UK/EU) (Principle 10: UK jurisdiction mandated; DPIA Section 13 confirms no international transfers)

**Cloud Provider**: To be determined via G-Cloud procurement. Strategy is cloud-agnostic to avoid vendor lock-in (Principle 20).

**Gaps/Actions Required**:
- **MEDIUM PRIORITY**: Complete cloud security assessment using NCSC Cloud Security Principles during Alpha
- **LOW PRIORITY**: Document cloud provider selection rationale when procurement completes

---

## TCoP Point 6: Make Things Secure

**Guidance**: Keep systems and data safe with the appropriate level of security.

**Reference**: https://www.gov.uk/guidance/make-things-secure

### Assessment

**Status**: ⚠️ Partially Compliant

**Evidence**:
Security is given the highest priority in the programme's architecture — Principle 3 (Security by Design) is explicitly marked **NON-NEGOTIABLE** with no exceptions permitted. The security architecture is comprehensive in design:

- **Zero-Trust Architecture**: Identity-based access, least privilege, encryption everywhere, continuous verification
- **Mandatory Controls**: MFA for all human access, service-to-service authentication, secrets management via secure vault, network segmentation, encryption at rest and in transit, structured security logging
- **Compliance Frameworks**: NCSC Cyber Assessment Framework, UK Government Security Classifications (OFFICIAL, OFFICIAL-SENSITIVE), Cyber Essentials Plus (minimum standard), ISO 27001 alignment
- **Risk Register**: R-019 (Cyber attack) identified with controls including Security by Design, zero-trust, NCSC CAF, Cyber Essentials Plus, penetration testing, SIEM monitoring
- **SOW**: Vendors must demonstrate SC clearance capability, Cyber Essentials Plus certification, and compliance with NCSC guidance
- **DPIA** (ARC-001-DPIA-v1.0): Security measures documented in Section 6 including encryption (AES-256), access controls (RBAC + ABAC), audit logging (7+ years), and incident response procedures

The programme recognises the criminal justice system processes highly sensitive data (criminal records, evidence, victim/witness details) including special category data under UK GDPR. The 2025 Legal Aid Agency cyberattack is cited as a real precedent for the threat.

However, no security assessment, threat model, or penetration test has been completed — the programme is in strategic planning, not implementation.

**Security Controls**:
- [ ] Threat modelling completed (planned — Principle 3 validation gates)
- [x] Security by design principles applied (Principle 3, NON-NEGOTIABLE)
- [ ] Penetration testing planned/completed (planned in Principle 18, SOW)
- [x] Security risk register maintained (ARC-001-RISK-v1.0 — R-019 Cyber Attack)
- [ ] NCSC Cloud Security Principles assessed (planned)
- [ ] Cyber Essentials / Cyber Essentials Plus certified (required of vendors in SOW)
- [x] Data classification completed (OFFICIAL / OFFICIAL-SENSITIVE documented in Principle 3; DPIA confirms classification)
- [ ] Encryption at rest and in transit (mandated in Principle 3 and DPIA Section 6, not yet implemented)

**Data Sensitivity**: OFFICIAL-SENSITIVE (criminal justice data including law enforcement data under DPA 2018 Part 3)

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Complete threat model during Alpha for each component
- **HIGH PRIORITY**: Conduct Secure by Design assessment (run `/arckit.secure`) before Beta
- **HIGH PRIORITY**: Schedule penetration testing before Private Beta go-live
- **MEDIUM PRIORITY**: Assess against NCSC Cloud Security Principles when cloud provider selected
- **MEDIUM PRIORITY**: Ensure Cyber Essentials Plus certification for all vendors and the programme itself

---

## TCoP Point 7: Make Privacy Integral

**Guidance**: Make sure users' rights are protected by integrating privacy as an essential part of your system.

**Reference**: https://www.gov.uk/guidance/make-privacy-integral

### Assessment

**Status**: ⚠️ Partially Compliant

**Evidence**:
Privacy is comprehensively addressed in both architecture design and assessment:

- **DPIA Completed** (ARC-001-DPIA-v1.0): Full Data Protection Impact Assessment completed, scoring 8/9 on ICO screening criteria. The DPIA identifies 12 risks to data subjects' rights and freedoms, establishes DPA 2018 Part 3 as the lawful basis for law enforcement processing, and documents mitigations. Outcome: HIGH residual risk; PROCEED WITH CONDITIONS (6 conditions).
- **Principle 10** (Privacy, Data Protection and Lawful Processing): Requires UK GDPR and DPA 2018 Part 3 compliance, DPIAs for all new processing, data classification, retention policies, and data subject rights
- **Requirements**: NFR-S-005 requires DPIAs before deployment; NFR-D-001/D-002 specify data retention and quality standards
- **Risk Register**: R-011 (Data sharing agreements stall) and R-012 (ICO enforcement action) both address data protection risks
- **Stakeholder Analysis**: ICO identified as a key stakeholder (SD-11) requiring proactive engagement
- **Strategy**: AI governance framework (Theme 5) includes DPIA as a mandatory gate for all AI deployments

**DPIA Key Findings** (ARC-001-DPIA-v1.0):
- 8/9 ICO screening criteria met — DPIA required and completed
- Lawful basis: DPA 2018 Part 3 s.35(2) — law enforcement processing by competent authorities
- Special category basis: DPA 2018 Part 3 Schedule 8 — statutory functions, administration of justice
- 1.3M+ data subjects/year including 30,000+ children
- 5 special category data types: criminal offence, health, biometric, ethnicity, sexual offence
- 12 risks identified (DPIA-001 to DPIA-012); 5 HIGH residual, 1 VERY HIGH residual
- ICO prior consultation recommended
- 6 conditions before deployment (defence equality, AI bias audit, ICO consultation, data-sharing agreements, children's safeguarding, AI incident response)

However, several privacy controls remain incomplete pending implementation:
- ICO prior consultation not yet initiated
- Data sharing agreements not yet formalised
- Data retention policies not yet operational
- Joint controller agreements between agencies not yet signed
- Data subject rights processes designed but not implemented

**Privacy Controls**:
- [x] Data Protection Impact Assessment (DPIA) completed (ARC-001-DPIA-v1.0 — 8/9 ICO criteria; HIGH residual risk; 6 conditions)
- [x] Privacy by design principles applied (Principle 10)
- [x] UK GDPR compliance assessed (DPIA Section 4 — necessity and proportionality; Appendix C — Article 5 principles)
- [ ] Data retention policy defined (designed in DPIA; NFR-D-001; not yet operational)
- [x] User consent mechanisms identified (DPA Part 3 uses lawful basis not consent — correctly documented in DPIA)
- [ ] Data subject rights procedures documented and operational (designed in DPIA Section 12; not yet implemented)
- [ ] Privacy notice published
- [ ] ICO registration completed (if required)

**Personal Data Processed**: Yes — criminal justice data is special category data; law enforcement processing under DPA 2018 Part 3

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Initiate ICO prior consultation under Article 36 UK GDPR — recommended by DPIA given scale, sensitivity, AI processing, and cross-agency nature
- **HIGH PRIORITY**: Formalise cross-agency data sharing agreements (DAPF) with all partner agencies before data exchange
- **HIGH PRIORITY**: Establish joint controller agreements between MoJ, HMCTS, CPS, HMPPS, and LAA
- **HIGH PRIORITY**: Resolve defence equality funding mechanism (DPIA-010, DPIA Condition 1) — gateway condition for AI deployment
- **MEDIUM PRIORITY**: Commission independent AI bias audit across all 9 protected characteristics (DPIA Condition 2)
- **MEDIUM PRIORITY**: Define operational data retention policies per agency requirements (7+ years for audit logs per Principle 7)
- **MEDIUM PRIORITY**: Publish DPA 2018 Part 3 compliant privacy notices

---

## TCoP Point 8: Share, Reuse and Collaborate

**Guidance**: Avoid duplicating effort and unnecessary costs by collaborating across government and sharing and reusing technology, data, and services.

**Reference**: https://www.gov.uk/guidance/share-and-reuse-technology

### Assessment

**Status**: ✅ Compliant

**Evidence**:
Cross-government collaboration and reuse is central to the programme design:

- **Principle 1** (Cross-Agency Interoperability): The entire programme is built on cross-agency collaboration between MoJ, HMCTS, CPS, HMPPS, LAA, and police
- **Platform Design** (ARC-001-PLAT-v1.0): Defines the Criminal Justice Digital Platform (CJDP) as a shared ecosystem explicitly designed for cross-agency reuse
- **Strategy**: Multi-vendor procurement via Digital Marketplace (G-Cloud, DOS); avoidance of bespoke solutions where commodity exists
- **SOW**: Requires vendors to build reusable components and APIs
- **Architecture Strategy**: Technology Radar places GOV.UK common components in "Adopt" ring
- **Defence Technology Platform** (FR-009): Designed as shared-service for all defence practitioners — explicit reuse model
- **Stakeholder Analysis**: GDS/CDDO identified as key stakeholder for cross-government alignment
- **DPIA** (ARC-001-DPIA-v1.0): Cross-agency data integration documented with data flows between 5+ agencies

**Reuse and Collaboration**:
- [x] Existing government services reviewed (GOV.UK, Notify, Pay, etc.) (Strategy references GOV.UK services)
- [x] Cross-government platforms used where appropriate (Digital Marketplace, GOV.UK services)
- [x] Technology components documented for reuse (SOW requires reusable components)
- [x] APIs designed for reusability (Principle 1, FR-004)
- [x] Collaboration with other departments documented (ARC-001-STKE-v1.0 — 15 stakeholders across multiple departments)

**Common Platforms Used**:
- [x] GOV.UK Notify (planned for victim/witness notifications — FR-007)
- [x] GOV.UK Pay (planned for court fees/legal aid — per Platform Design)
- [ ] GOV.UK PaaS (deprecated — modern cloud hosting via G-Cloud)
- [x] Digital Marketplace (procurement route — ARC-001-SOW-v1.0)
- [x] Other: Common Platform (existing — to be stabilised and enhanced)

**Gaps/Actions Required**:
- **LOW PRIORITY**: Formally confirm GOV.UK Notify and Pay integration during Alpha
- **LOW PRIORITY**: Explore whether HMCTS Shared Services components can be reused

---

## TCoP Point 9: Integrate and Adapt Technology

**Guidance**: Your technology should work with existing technologies, processes and infrastructure in your organisation, and adapt to future demands.

**Reference**: https://www.gov.uk/guidance/integrate-and-adapt-technology

### Assessment

**Status**: ✅ Compliant

**Evidence**:
Integration is arguably the programme's strongest area — it is the central challenge the Leveson Review identified and the programme directly addresses:

- **Principle 1** (Cross-Agency Interoperability): All systems must expose APIs; direct database access prohibited
- **Principle 11** (Loose Coupling, Tight Contracts): Mandates loose coupling through published interfaces; prohibits shared databases
- **Principle 12** (Event-Driven Integration): Case progression events (charge, hearing, verdict, sentence) modelled as asynchronous events
- **FR-004** (Cross-Agency API Gateway): Standardised gateway for all agency data exchange
- **Strategy**: Police adapters for Niche, Connect, Athena (covers ~85% of forces)
- **Principle 4** (Legacy Modernisation): 37 legacy applications assessed and migration planned
- **Principle 16** (Maintainability and Evolvability): Systems designed for multi-year evolution

The programme explicitly addresses existing system inventory (37 legacy applications documented), integration points across all agencies, and future scalability (Principle 5 — horizontal scaling for caseload growth).

**Integration Considerations**:
- [x] Existing systems inventory completed (37 legacy applications catalogued — ARC-001-STRAT-v1.0)
- [x] Integration points identified and documented (ARC-001-REQ-v1.0 — INT-001 through INT-006)
- [x] API strategy defined (Principle 1, FR-004, ARC-001-STRAT-v1.0)
- [x] Legacy system dependencies mapped (ARC-001-STRAT-v1.0 Current State Assessment)
- [x] Future scalability considered (Principle 5 — Scalability and Elasticity)
- [x] Technology roadmap aligned with organisational strategy (ARC-001-STRAT-v1.0 — 5-year strategic timeline)

**Key Integrations**:
- **Police Forces (43)**: Adapter/middleware layer for Niche, Connect, Athena → Common API gateway
- **CPS**: API-based case data exchange with HMCTS; evidence exchange with police
- **HMPPS**: Real-time sentence data feed; pre-sentence reports
- **LAA**: Legal aid administration; defence practitioner access management
- **Common Platform**: Stabilise and enhance existing court case management

**Gaps/Actions Required**:
- **LOW PRIORITY**: Validate integration architecture during Alpha technical spikes
- **LOW PRIORITY**: Confirm Common Platform integration approach after stabilisation assessment

---

## TCoP Point 10: Make Better Use of Data

**Guidance**: Use data more effectively by improving your technology, infrastructure and processes.

**Reference**: https://www.gov.uk/guidance/make-better-use-of-data

### Assessment

**Status**: ⚠️ Partially Compliant

**Evidence**:
Data strategy is well-defined in the architecture and now strengthened by the DPIA:

- **Principle 8** (Data as a Shared Strategic Asset): Single authoritative source per data domain; derived copies read-only
- **Principle 9** (Data Quality and Integrity): Completeness, consistency, accuracy, timeliness standards with automated quality rules
- **Principle 7** (Observability): Real-time operational dashboards feeding Leveson Review KPIs
- **Strategy**: Analytics/data warehouse in target architecture (ARC-001-STRAT-v1.0 Architecture Vision)
- **Requirements**: DR-001 through DR-004 define data standards, master data management, and data governance
- **Platform Design**: Data layer includes case data, evidence store, audit log (7+ years), and analytics data warehouse
- **DPIA** (ARC-001-DPIA-v1.0): Detailed data inventory across 4 core entities (DR-001 to DR-004) with PII classification, retention requirements, and data flows between agencies. Data subject volumes quantified (1.3M+/year).

The programme plans to make data-driven decisions visible through real-time dashboards (case progression, hearing outcomes, disposal rates) as recommended by the Leveson Review.

However, no enterprise data model has been created, no data governance framework is operational, and no open data publication plan exists.

**Data Management**:
- [x] Data architecture documented (high-level in ARC-001-STRAT-v1.0 and ARC-001-PLAT-v1.0; data entities in DPIA)
- [x] Data quality standards defined (Principle 9 — completeness, consistency, accuracy, timeliness)
- [x] Master data management approach defined (Principle 8 — system of record per data domain)
- [x] Data analytics/insights strategy (Strategy — analytics data warehouse; Leveson Review dashboards)
- [ ] Open data publication considered
- [ ] Data sharing agreements in place (where needed) — **planned but not formalised** (R-011; DPIA Condition 4)
- [ ] Data lineage tracked (planned in Principle 9)

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Create comprehensive data model (run `/arckit.data-model`) during Alpha — recommended by DPIA to provide entity-level PII inventory and retention design
- **HIGH PRIORITY**: Formalise cross-agency data sharing agreements before any data exchange (linked to Point 7; DPIA Condition 4)
- **MEDIUM PRIORITY**: Consider what data can be published as open data (court statistics, anonymised case data)
- **MEDIUM PRIORITY**: Implement data lineage tracking in the data architecture

---

## TCoP Point 11: Define Your Purchasing Strategy

**Guidance**: Your purchasing strategy must show you've considered commercial and technology aspects, and contractual limitations.

**Reference**: https://www.gov.uk/guidance/define-your-purchasing-strategy

### Assessment

**Status**: ✅ Compliant

**Evidence**:
The programme has a detailed, well-considered purchasing strategy:

- **SOW** (ARC-001-SOW-v1.0): Comprehensive Statement of Work with 5 procurement lots, evaluation criteria, and scoring methodology
- **Strategy**: Multi-vendor strategy explicitly adopted to avoid lock-in (Principle 20); hybrid build-buy model documented
- **SOBC** (ARC-001-SOBC-v1.0): £281M budget with phased investment, stage-gate approvals, and HM Treasury optimism bias applied
- **Procurement Route**: Digital Marketplace (G-Cloud for infrastructure, DOS for specialist delivery) — documented in SOW and Strategy
- **Build vs Buy**: Detailed analysis per capability (ARC-001-STRAT-v1.0) — build core criminal justice AI; buy commodity infrastructure
- **Vendor Lock-In**: Principle 20 mandates abstraction layers for proprietary dependencies; SOW requires exit provisions; R-015 (Vendor Lock-In) identified in risk register with controls
- **SME Access**: SOW structured in lots to enable SME participation; Digital Marketplace favours SME access
- **Social Value**: To be included in procurement evaluation criteria per Public Services (Social Value) Act 2012

**Procurement Strategy**:
- [x] Market research conducted (build vs buy analysis in ARC-001-STRAT-v1.0)
- [x] Build vs buy decision documented (ARC-001-STRAT-v1.0 — detailed per capability)
- [x] Digital Marketplace considered (G-Cloud and DOS specified as procurement routes)
- [x] Crown Commercial Service frameworks reviewed (G-Cloud, DOS referenced in SOW)
- [x] Vendor lock-in risks assessed (R-015, Principle 20)
- [x] Exit strategy defined (SOW requires exit provisions; Principle 20 mandates data export in open formats)
- [ ] Social value considerations included (to be added to procurement evaluation)
- [x] SME access considerations (multi-lot structure enables SME participation)

**Procurement Route**: G-Cloud (cloud infrastructure) / DOS (specialist delivery services) / Open Tender (where appropriate for high-value lots)

**Gaps/Actions Required**:
- **MEDIUM PRIORITY**: Add explicit social value scoring criteria to procurement evaluation framework
- **LOW PRIORITY**: Confirm procurement timeline aligns with Treasury spending approval

---

## TCoP Point 12: Make Your Technology Sustainable

**Guidance**: Increase sustainability throughout the lifecycle of your technology.

**Reference**: https://www.gov.uk/guidance/make-your-technology-sustainable

### Assessment

**Status**: ❌ Non-Compliant

**Evidence**:
Sustainability is not substantively addressed in the existing programme documentation:

- No carbon footprint assessment has been conducted or planned
- No sustainability metrics are defined
- No green hosting requirements are specified in the SOW
- No e-waste disposal procedures are documented
- The programme does not mention the UK Government Greening Government ICT Strategy

The only tangential sustainability considerations are:
- Cloud-first approach (generally more energy-efficient than on-premises)
- Legacy decommissioning reduces the total technology footprint
- Remote working and remote evidence (FR-008) may reduce travel

This is a significant gap for a programme of this scale (£281M, 5 years) processing substantial compute workloads (AI training and inference, large-scale data processing).

**Sustainability Considerations**:
- [ ] Carbon footprint assessed
- [ ] Energy-efficient infrastructure chosen (cloud-first provides some benefit, but not explicitly assessed)
- [ ] Device lifecycle management plan
- [ ] E-waste disposal procedures
- [ ] Green hosting/data centers considered
- [ ] Sustainable procurement criteria applied
- [ ] Remote/hybrid working enabled to reduce travel (partially — remote evidence facilities in FR-008)

**Sustainability Metrics**:
- Estimated carbon footprint: Not assessed
- Device refresh cycle: Not defined
- Hosting energy source: Not specified

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Conduct sustainability assessment for the programme during Alpha — estimate carbon footprint of cloud workloads, especially AI training/inference
- **HIGH PRIORITY**: Add green hosting requirements to procurement criteria (require cloud providers to report and reduce carbon intensity)
- **MEDIUM PRIORITY**: Define device lifecycle management for court IT equipment
- **MEDIUM PRIORITY**: Include sustainability metrics in benefits realisation framework
- **LOW PRIORITY**: Reference and align with Greening Government ICT Strategy

---

## TCoP Point 13: Meet the Service Standard

**Guidance**: If you're building a service as part of your technology project or programme, you must meet the Service Standard.

**Reference**: https://www.gov.uk/service-manual/service-standard

### Assessment

**Status**: ⚠️ Partially Compliant

**Is this a public-facing service?**: Yes — the Victim Case Tracking Service (FR-007) and elements of the Defence Technology Platform (FR-009) are public/practitioner-facing services that must meet the Service Standard.

**Evidence**:
The programme explicitly recognises GDS Service Standard compliance:

- **Stakeholder Analysis**: GDS/CDDO identified as a "Keep Satisfied" stakeholder (SD-10) with Digital Standards Compliance driver
- **Goal G-9**: "Ensure all new digital services pass GDS service assessment at alpha, beta, and live stages"
- **Risk Register**: R-010 (GDS Service Assessment Failure) identified with 12 (Medium) residual risk score — previous justice technology services have struggled at assessment
- **Principles**: Architecture review gates (Section VIII of ARC-000-PRIN-v1.0) explicitly map to GDS phases (Discovery/Alpha, Beta/Design, Pre-Production)
- **Strategy**: Service assessment pass rate is a strategic KPI; GDS Service Standard in "External Drivers" table

However, no service assessment preparation has been completed and no engagement with GDS assessment teams has occurred.

**Service Standard Compliance**:
- [ ] Service assessments planned/completed
- [x] Agile, user-centered approach used (planned — Principle 16, SOW agile delivery requirement)
- [x] Performance metrics defined (KPIs) (ARC-001-STRAT-v1.0 — strategic KPIs defined)
- [ ] Assisted digital support planned
- [ ] Service manual guidance followed
- [ ] Beta/live service assessment passed

**Service Assessment Status**: Not required yet (pre-Discovery) — planned for Alpha, Beta, and Live assessments

**Gaps/Actions Required**:
- **HIGH PRIORITY**: Engage GDS assessment team early in Discovery to agree assessment approach for criminal justice services
- **HIGH PRIORITY**: Conduct mock service assessments before formal Alpha assessment
- **MEDIUM PRIORITY**: Define assisted digital support model for users without internet access (particularly defendants in custody, victims without digital skills)
- **MEDIUM PRIORITY**: Prepare service assessment evidence pack (run `/arckit.service-assessment`)
- **LOW PRIORITY**: Consider whether specialist criminal justice context requires adapted assessment criteria

---

## Overall Compliance Summary

### Compliance Scorecard

| TCoP Point | Status | Critical Issues |
|------------|--------|-----------------|
| 1. Define user needs | ⚠️ Partially Compliant | No — strong personas exist, primary research needed |
| 2. Make things accessible | ⚠️ Partially Compliant | No — targets set, testing needed at Beta |
| 3. Be open and use open source | ⚠️ Partially Compliant | No — commitment exists, implementation pending |
| 4. Make use of open standards | ✅ Compliant | No |
| 5. Use cloud first | ✅ Compliant | No |
| 6. Make things secure | ⚠️ Partially Compliant | Yes — no threat model or pen test yet |
| 7. Make privacy integral | ⚠️ Partially Compliant | Yes — DPIA complete but 6 conditions pending (was ❌ in v1.0) |
| 8. Share, reuse and collaborate | ✅ Compliant | No |
| 9. Integrate and adapt technology | ✅ Compliant | No |
| 10. Make better use of data | ⚠️ Partially Compliant | No — data model and sharing agreements needed |
| 11. Define your purchasing strategy | ✅ Compliant | No |
| 12. Make your technology sustainable | ❌ Non-Compliant | Yes — no sustainability assessment |
| 13. Meet the Service Standard | ⚠️ Partially Compliant | No — engagement with GDS needed |

**Overall Score**: 5/13 Compliant (7 Partially Compliant, 1 Non-Compliant)

**Change from v1.0**: Point 7 upgraded ❌ → ⚠️ (DPIA completed); overall Non-Compliant count reduced from 2 to 1; Partially Compliant increased from 6 to 7.

### Critical Issues Requiring Immediate Action

1. **No Sustainability Assessment (Point 12)** — A £281M, 5-year programme with significant AI compute workloads has no sustainability assessment, carbon footprint estimate, or green procurement criteria. While not a blocker, this will be scrutinised at Digital Spend Control.

2. **No Security Assessment (Point 6)** — Security by Design principle is strong, but no threat model or security assessment exists. For a programme processing OFFICIAL-SENSITIVE criminal justice data, a Secure by Design assessment must be completed before Beta. Run `/arckit.secure`.

3. **DPIA Conditions Pending (Point 7)** — While the DPIA is now complete, 6 conditions must be met before deployment. The gateway condition — defence equality funding (DPIA-010) — requires ministerial decision and carries VERY HIGH residual risk.

### Recommendations

**High Priority**:
- Complete Secure by Design assessment during Alpha (Point 6) — run `/arckit.secure`
- Conduct sustainability assessment and set carbon reduction targets (Point 12)
- Commission primary user research with all 8 personas during Discovery (Point 1)
- Initiate ICO prior consultation (Point 7, DPIA Condition 3)
- Engage GDS assessment team during Discovery (Point 13)
- Create comprehensive data model (Point 10) — run `/arckit.data-model`
- Resolve defence equality funding mechanism (Point 7, DPIA Condition 1)

**Medium Priority**:
- Commission accessibility audit of Common Platform and all new services (Point 2)
- Define code publication policy and open-source licence strategy (Point 3)
- Formalise cross-agency data sharing agreements (Points 7, 10)
- Add social value and sustainability scoring to procurement criteria (Points 11, 12)
- Prepare service assessment evidence pack and conduct mock assessment (Point 13)
- Commission independent AI bias audit (Point 7, DPIA Condition 2)

**Low Priority**:
- Formally document approved open standards catalogue (Point 4)
- Confirm GOV.UK Notify and Pay integration (Point 8)
- Establish accessibility regression testing in CI/CD (Point 2)
- Define open data publication plan (Point 10)

---

## Next Steps

**Immediate Actions** (0-30 days):
- [ ] Initiate ICO prior consultation for AI and cross-agency data processing (Point 7 — DPIA Condition 3)
- [ ] Initiate sustainability assessment for cloud and AI workloads (Point 12)
- [ ] Begin planning primary user research programme across all 8 personas (Point 1)
- [ ] Begin Secure by Design assessment (Point 6) — run `/arckit.secure`

**Short-term Actions** (1-3 months):
- [ ] Complete Secure by Design assessment (Point 6)
- [ ] Engage GDS assessment team for early Discovery consultation (Point 13)
- [ ] Create comprehensive data model (Point 10) — run `/arckit.data-model`
- [ ] Define code publication and open-source policy (Point 3)
- [ ] Formalise first bilateral data sharing agreements (CPS-HMCTS) (Point 7, 10)
- [ ] Establish joint controller agreements between agencies (Point 7)

**Long-term Actions** (3-12 months):
- [ ] Complete accessibility audit during Beta (Point 2)
- [ ] Pass Alpha GDS service assessment (Point 13) — prepare with `/arckit.service-assessment`
- [ ] Complete penetration testing before Private Beta (Point 6)
- [ ] Publish accessibility statement for all public-facing services (Point 2)
- [ ] Embed sustainability metrics in benefits realisation reporting (Point 12)
- [ ] Pass Beta GDS service assessment (Point 13)
- [ ] Commission independent AI bias audit (Point 7, DPIA Condition 2)

**Review Schedule**: Next TCoP review in 3 months (2026-05-05) — expected to follow Discovery/Alpha, by which time Points 1, 6, and 12 should show significant improvement.

---

## Approval

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Project Lead | [Name] | | |
| Technical Architect | [Name] | | |
| Senior Responsible Owner | [Name] | | |
| Digital Spend Control (if applicable) | [Name] | | |

---

**Document Control**:
- **Version**: 1.1
- **Last Reviewed**: 2026-02-05
- **Next Review**: 2026-05-05 (Quarterly)
- **Document Owner**: MoJ CDIO

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| ARC-000-PRIN-v1.0 | Architecture Principles | ArcKit | 23 principles aligned to TCoP; Security by Design (NON-NEGOTIABLE); Accessibility (WCAG 2.2 AA); Open Standards | `projects/000-global/ARC-000-PRIN-v1.0.md` |
| ARC-001-REQ-v1.0 | Requirements | ArcKit | 65 requirements (10 BR, 14 FR, 22 NFR, 4 DR, 6 INT); 8 personas; 5 use cases; acceptance criteria | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-REQ-v1.0.md` |
| ARC-001-STKE-v1.0 | Stakeholder Analysis | ArcKit | 15 stakeholders; GDS/CDDO as compliance stakeholder; ICO engagement required | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STKE-v1.0.md` |
| ARC-001-RISK-v1.0 | Risk Register | ArcKit | R-010 (GDS assessment failure); R-011 (data sharing); R-012 (ICO enforcement); R-015 (vendor lock-in); R-019 (cyber attack) | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-RISK-v1.0.md` |
| ARC-001-STRAT-v1.0 | Architecture Strategy | ArcKit | Cloud-native; multi-vendor; API-first; Technology Radar; build vs buy; £281M investment | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-STRAT-v1.0.md` |
| ARC-001-SOW-v1.0 | Statement of Work | ArcKit | 5 procurement lots; G-Cloud/DOS routes; vendor requirements; exit provisions | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-SOW-v1.0.md` |
| ARC-001-PLAT-v1.0 | Platform Strategy Design | ArcKit | Criminal Justice Digital Platform; multi-sided ecosystem; shared-service defence platform | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-PLAT-v1.0.md` |
| ARC-001-DPIA-v1.0 | Data Protection Impact Assessment | ArcKit | 8/9 ICO criteria; 12 risks; HIGH residual risk; PROCEED WITH CONDITIONS; 6 conditions; DPA 2018 Part 3 lawful basis; 1.3M+ data subjects/year | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-DPIA-v1.0.md` |
| ARC-001-SOBC-v1.0 | Strategic Outline Business Case | ArcKit | £281M budget; phased investment; 5-case model; HM Treasury optimism bias | `projects/001-criminal-courts-technology-and-ai-reform/ARC-001-SOBC-v1.0.md` |

---

**Generated by**: ArcKit `/arckit.tcop` command
**Generated on**: 2026-02-05 22:00 GMT
**ArcKit Version**: 1.5.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: claude-opus-4-6
**Generation Context**: TCoP v1.1 refreshed assessment incorporating ARC-001-DPIA-v1.0 (completed since v1.0). Source artifacts: ARC-000-PRIN-v1.0 (23 principles), ARC-001-REQ-v1.0 (65 requirements, 8 personas), ARC-001-STKE-v1.0 (15 stakeholders), ARC-001-RISK-v1.0 (20 risks), ARC-001-STRAT-v1.0 (architecture strategy), ARC-001-SOW-v1.0 (procurement), ARC-001-PLAT-v1.0 (platform design), ARC-001-SOBC-v1.0 (business case), ARC-001-DPIA-v1.0 (DPIA — NEW). No external documents provided.

# Criminal Courts Technology & AI Reform — Enterprise Architecture Principles

> **Template Status**: Live | **Version**: 1.3.0 | **Command**: `/arckit.principles`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-000-PRIN-v1.0 |
| **Document Type** | Enterprise Architecture Principles |
| **Project** | Criminal Courts Technology & AI Reform (Project 000) |
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
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, Criminal Justice Technology Leadership |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-02-04 | ArcKit AI | Initial creation from `/arckit.principles` command | PENDING | PENDING |

---

## Executive Summary

This document establishes the architecture principles governing all technology decisions across the Criminal Courts Technology & AI Reform programme. These principles respond to the crisis identified by the Independent Review of the Criminal Courts (Leveson Review, 2025–2026): 77,000+ outstanding Crown Court cases, fragmented digital systems across police/CPS/courts/probation/prisons, troubled Common Platform rollout, and 37 critical legacy applications requiring modernisation.

The principles are grounded in the Leveson Review's efficiency principles — getting it right first time, augmentation through technology, minimising waste, expertise, sustainability — and the applicable UK Government frameworks: GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Assessment Framework, UK GDPR, HM Treasury Green Book, and the AI Playbook.

**Scope**: All technology projects, systems and initiatives within the Criminal Courts Technology & AI Reform programme and related cross-agency digital services
**Authority**: Enterprise Architecture Review Board, with oversight from the Criminal Justice Technology Leadership role recommended by the Leveson Review
**Compliance**: Mandatory unless exception approved through the formal exception process

**Philosophy**: These principles are **technology-agnostic** — they describe WHAT qualities the architecture must have, not HOW to implement them with specific products. Technology selection happens during research and design phases guided by these principles. They are designed to be durable across the multi-year reform timeline and to support the phased modernisation of criminal justice systems.

---

## I. Strategic Principles

### 1. Cross-Agency Interoperability by Design

**Principle Statement**:
All systems MUST expose functionality through well-defined, versioned interfaces using industry-standard protocols. Direct database access across system boundaries is prohibited. Systems MUST be designed to communicate and share data seamlessly across organisational boundaries within the criminal justice system.

**Rationale**:
The Leveson Review identifies fragmented, siloed digital systems across police forces, CPS, HMCTS, HMPPS and the Legal Aid Agency as a root cause of inefficiency. Staff manually transfer data between systems, causing delays, errors and data drift. Building a single monolithic system for all agencies has been attempted and failed (Common Platform scope reduction). Interoperability through standard interfaces is the proven path.

**Implications**:
- Adopt an API-first approach for all new systems and major enhancements
- Publish interface specifications using open standards (e.g., OpenAPI, AsyncAPI, event schemas)
- Version all interfaces with explicit backward compatibility commitments
- Ensure cross-system authentication and authorisation governance
- Prohibit point-to-point integrations that bypass published interfaces
- Support real-time data exchange to eliminate manual rekeying between agencies

**Validation Gates**:
- [ ] Interface specifications published and discoverable via an API catalogue
- [ ] Versioning strategy defined with backward compatibility approach
- [ ] Cross-agency authentication and data-sharing agreements in place
- [ ] No direct database access across system or agency boundaries
- [ ] Integration tested end-to-end across agency boundaries
- [ ] Data format standards agreed with consuming agencies

---

### 2. Human-Centred AI Augmentation

**Principle Statement**:
AI and automation MUST augment rather than replace human decision-making in the criminal justice system. AI tools MUST be deployed with appropriate human oversight, transparency and accountability safeguards. Predictive AI tools that forecast individual case outcomes MUST NOT be deployed without explicit ministerial and judicial approval and independent ethical review.

**Rationale**:
The Leveson Review mandates that technology "augments rather than replaces high-quality, fair and proportionate decision-making." Criminal justice decisions — charging, disclosure, sentencing — carry profound consequences for individuals' liberty and rights. AI can deliver significant efficiency gains (transcription, translation, case summarisation, scheduling) but must preserve judicial independence, impartiality and integrity. The Review explicitly cautions against predictive AI tools that raise ethical concerns.

**AI Tool Categories** (per Leveson Review):
1. **Productivity tools**: Transcription, translation, document summarisation — permitted with standard safeguards
2. **Insight tools**: Data dashboards, case analytics, scheduling optimisation — permitted with governance oversight
3. **Accessibility tools**: Public-facing information, language support — permitted with accuracy validation
4. **Predictive/outcome tools**: Forecasting case results or individual behaviour — restricted, requiring explicit approval

**Implications**:
- All AI tools must have documented human oversight mechanisms
- AI-assisted outputs must be clearly labelled as such
- Users must be trained on AI tool capabilities and limitations
- AI must not introduce or amplify bias against any group
- Prosecution and defence must have equivalent access to AI-assisted tools (equality of arms)
- AI tools must be embedded within existing platforms, not deployed as separate fragmented systems
- Business processes must be re-engineered before automation, not simply digitised as-is

**Validation Gates**:
- [ ] AI tool categorised (productivity/insight/accessibility/predictive)
- [ ] Human oversight mechanism documented and tested
- [ ] Bias assessment completed across protected characteristics
- [ ] Training programme defined for all users
- [ ] Algorithmic Transparency Recording Standard (ATRS) record completed
- [ ] AI tool integrated into existing platform (not standalone)
- [ ] AI and Data Science Ethics Framework compliance confirmed

---

### 3. Security by Design (NON-NEGOTIABLE)

**Principle Statement**:
All architectures MUST implement defence-in-depth security with zero-trust principles. Security is NOT a feature to be added later — it is a foundational requirement. Criminal justice data, including personal data processed for law enforcement purposes, MUST be protected to the highest standards.

**Rationale**:
The criminal justice system processes highly sensitive data: criminal records, evidence, victim/witness details, defendant information, and special category data under UK GDPR. The 2025 Legal Aid Agency cyberattack and the 2021 Police National Computer data deletion incident demonstrate the real consequences of security failures. Legacy systems with technical debt are particularly vulnerable. The NCSC Cyber Assessment Framework applies.

**Zero Trust Pillars**:
1. **Identity-Based Access**: No network-based trust; every request authenticated and authorised
2. **Least Privilege**: Grant minimum necessary permissions, time-boxed where possible
3. **Encryption Everywhere**: Data encrypted in transit and at rest
4. **Continuous Verification**: Monitor, log and analyse all access patterns

**Mandatory Controls**:
- [ ] Multi-factor authentication for all human access to criminal justice systems
- [ ] Service-to-service authentication for all API and integration traffic
- [ ] Secrets management via secure vault (never in code, config files or environment variables)
- [ ] Network segmentation with minimal trust zones
- [ ] Encryption at rest for all data stores containing case, personal or evidential data
- [ ] Encrypted transport for all network communication
- [ ] Structured logging of all authentication, authorisation and data access events
- [ ] Regular security testing (penetration testing, vulnerability scanning, code analysis)
- [ ] Security classification applied to all data assets

**Compliance Frameworks**:
- NCSC Cyber Assessment Framework
- UK Government Security Classifications (OFFICIAL, OFFICIAL-SENSITIVE)
- Cyber Essentials Plus (minimum standard for all components)
- ISO 27001 alignment

**Exceptions**:
- NONE. Security principles are non-negotiable.
- Specific control implementations may vary with documented compensating controls.

**Validation Gates**:
- [ ] Threat model completed and reviewed
- [ ] Security controls mapped to NCSC CAF outcomes
- [ ] Security testing plan defined and executed
- [ ] Incident response runbook created and tested
- [ ] Secure by Design assessment completed

---

### 4. Legacy Modernisation and Technical Debt Reduction

**Principle Statement**:
All technology investment MUST prioritise the decommissioning of legacy systems and reduction of technical debt. New capabilities MUST NOT be built on legacy platforms. Migration from legacy systems MUST follow a structured, risk-managed approach.

**Rationale**:
The criminal justice system operates 37 critical legacy applications, some dating to the 1970s (e.g., Police National Computer, 1974). Legacy systems are more susceptible to cyberattack, lack modern security measures, cannot interoperate with other systems, and prevent the adoption of AI and automation tools. The NAO rated 63 of 228 government legacy IT systems as having high likelihood and impact of cyber risk. HMCTS is undertaking a Decommissioning and Legacy Risks Mitigation Programme that this principle endorses and extends.

**Implications**:
- Maintain a register of all legacy systems with risk ratings and decommissioning timelines
- Prioritise decommissioning based on cyber risk, operational impact and interoperability benefit
- Ensure data migration plans preserve data integrity and maintain audit trails
- Avoid extending legacy systems with new features — invest in replacement
- Plan for parallel running during transition with clear cutover criteria
- Budget for legacy decommissioning as a ring-fenced programme, not discretionary spend

**Validation Gates**:
- [ ] Legacy system register maintained with risk ratings
- [ ] Decommissioning timeline defined for each legacy system
- [ ] No new features built on systems identified for retirement
- [ ] Data migration plan validated with data quality checks
- [ ] Rollback plan defined for migration failures
- [ ] Parallel running period planned with success criteria

---

### 5. Scalability and Elasticity

**Principle Statement**:
All systems MUST be designed to scale horizontally to meet variable demand, including seasonal patterns, policy-driven caseload changes and crisis scenarios.

**Rationale**:
Criminal court caseloads have doubled since 2019 (from 35,000 to nearly 80,000 outstanding Crown Court cases). Government policy initiatives (Safer Streets Mission, violence against women and girls strategy) will further increase volume. Systems must handle growth without architectural changes. COVID-19 demonstrated the need for rapid adaptation to remote working and increased digital channel usage.

**Implications**:
- Design for stateless components that can be replicated
- Avoid hard-coded limits or fixed capacity assumptions
- Plan for distributed deployment across multiple compute nodes
- Implement auto-scaling based on demand metrics
- Cost model must account for variable capacity
- Performance must not degrade as caseload increases

**Validation Gates**:
- [ ] System can scale horizontally (add more instances)
- [ ] No single points of failure that limit scaling
- [ ] Load testing demonstrates capacity growth with added resources
- [ ] Scaling metrics and triggers defined
- [ ] Cost model accounts for variable capacity
- [ ] Tested against projected caseload growth scenarios

---

### 6. Resilience and Fault Tolerance

**Principle Statement**:
All systems MUST gracefully degrade when dependencies fail and recover automatically without data loss or manual intervention. Criminal justice systems MUST maintain continuity of operations — court schedules, prisoner movements and hearing processes cannot be paused.

**Rationale**:
Failures in criminal justice systems have immediate, severe consequences: prisoners cannot be produced for court, hearings must be adjourned, cases are delayed further. The system already lacks resilience to cope with rising caseloads. Digital systems must be more reliable than the manual processes they replace.

**Implications**:
- Implement circuit breakers for external dependencies
- Use timeouts on all network calls
- Retry with exponential backoff for transient failures
- Graceful degradation when non-critical services fail
- Automated health checks and recovery
- Avoid cascading failures through bulkhead isolation
- Define fallback procedures for complete system outage (manual workarounds)

**Validation Gates**:
- [ ] Failure modes identified and mitigated
- [ ] Fault injection testing performed
- [ ] Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined
- [ ] Automated failover tested
- [ ] Degraded mode behaviour documented
- [ ] Manual fallback procedures documented and rehearsed

---

### 7. Observability and Operational Excellence

**Principle Statement**:
All systems MUST emit structured telemetry (logs, metrics, traces) enabling real-time monitoring, troubleshooting and capacity planning. Operational data MUST support the real-time dashboards and Key Performance Indicators recommended by the Leveson Review.

**Rationale**:
The Leveson Review identifies poor-quality data and the inability to monitor system performance as barriers to improvement. Real-time operational dashboards are recommended for court listing, prisoner movements and case progression. Systems must be observable to be operated effectively.

**Telemetry Requirements**:
- **Logging**: Structured logs with correlation IDs, supporting cross-agency trace
- **Metrics**: Request volume, latency percentiles (p50, p95, p99), error rates
- **Tracing**: Distributed trace context for request flows across agency boundaries
- **Alerting**: Service Level Objective (SLO)-based alerting with actionable runbooks
- **Business Metrics**: Case progression rates, hearing outcomes, disposal rates

**Log Retention**:
- **Security/audit logs**: Minimum 7 years (criminal justice regulatory requirement)
- **Application logs**: Minimum 90 days for troubleshooting
- **Metrics**: Minimum 2 years with aggregation for trend analysis

**Validation Gates**:
- [ ] Logging, metrics and tracing instrumented
- [ ] Dashboards and alerts configured
- [ ] Service Level Objectives (SLOs) and Service Level Indicators (SLIs) defined
- [ ] Runbooks created for common failure scenarios
- [ ] Capacity planning metrics tracked
- [ ] Business metrics feeding operational dashboards

---

## II. Data Principles

### 8. Data as a Shared Strategic Asset

**Principle Statement**:
Data MUST be treated as a shared strategic asset across the criminal justice system. Every data domain MUST have a single authoritative source. Data MUST be made available to authorised consumers through standard interfaces, subject to data-sharing agreements and access controls.

**Rationale**:
The Leveson Review identifies "silos, cohesion and poor-quality data" as a systemic failure. Each agency holds its own version of case data, leading to inconsistency, manual reconciliation and errors. Data fragmentation and drift occur when agencies use incompatible systems. A single source of truth for each data domain is essential for accurate, timely justice.

**Implications**:
- Identify the system of record for each data domain (case data, defendant data, victim data, court scheduling, etc.)
- Derived/cached copies are read-only and clearly labelled as such
- Synchronisation strategy defined for all derived copies
- Avoid bidirectional synchronisation (creates split-brain scenarios)
- Cross-agency data-sharing agreements govern access and use
- Data standards (formats, schemas, identifiers) agreed across agencies

**Validation Gates**:
- [ ] System of record identified for each data entity
- [ ] Derived copies documented with sync frequency
- [ ] No bidirectional sync without conflict resolution strategy
- [ ] Cross-agency data-sharing agreements in place
- [ ] Common identifiers (case reference, defendant ID) standardised across agencies

---

### 9. Data Quality and Integrity

**Principle Statement**:
Data pipelines MUST maintain data quality standards and provide end-to-end lineage for auditability. Criminal justice data MUST be accurate, complete, timely and consistent — errors in case data can lead to miscarriages of justice.

**Rationale**:
The Leveson Review documents cases where manual data entry errors have led to serious consequences — prisoners released in error due to incorrectly calculated release dates, tagging data unavailable to probation officers, inconsistent case information across agencies. Data quality is not an abstract concern; it directly impacts justice outcomes.

**Quality Standards**:
- **Completeness**: No unexpected nulls in required fields; case files must contain all mandated elements
- **Consistency**: Cross-system data reconciliation; same case reflects same facts in all systems
- **Accuracy**: Validation rules and constraints enforced at source; automated checks at point of entry
- **Timeliness**: Freshness SLAs defined and monitored; real-time where operationally required

**Validation Gates**:
- [ ] Data quality rules defined and automated
- [ ] Lineage metadata captured and queryable
- [ ] Data contracts between producers and consumers
- [ ] Schema evolution strategy documented
- [ ] Data quality metrics tracked and reported
- [ ] Automated reconciliation between systems of record and derived copies

---

### 10. Privacy, Data Protection and Lawful Processing

**Principle Statement**:
All systems MUST comply with the UK GDPR and the Data Protection Act 2018, including Part 3 (law enforcement processing). Personal data processed for criminal justice purposes MUST be handled as special category data with appropriate safeguards. Data Protection Impact Assessments (DPIAs) MUST be completed for all new processing activities involving personal data.

**Rationale**:
Criminal justice data includes the most sensitive categories of personal data: criminal offence data, biometric data, health data (mental health assessments), data relating to children and vulnerable adults, and victim/witness personal information. Part 3 of the DPA 2018 governs law enforcement processing with specific conditions and safeguards that differ from standard UK GDPR processing. Failure to comply risks individuals' rights and programme credibility.

**Implications**:
- Data classification applied to all data assets (PUBLIC, OFFICIAL, OFFICIAL-SENSITIVE)
- Data residency within UK jurisdiction unless explicit legal basis for transfer
- Retention policies configured with automated deletion at expiry
- Access controls enforce least privilege and need-to-know
- Purpose limitation enforced — data collected for one purpose not repurposed without lawful basis
- Subject access rights (access, rectification, erasure) supported by system design
- DPIAs completed before new processing begins, not retrospectively

**Validation Gates**:
- [ ] Data classification performed for all data stores
- [ ] Lawful basis for processing documented for each data flow
- [ ] DPIA completed and signed off by Data Protection Officer
- [ ] Retention policies configured with automated deletion
- [ ] Access controls enforce least privilege
- [ ] Subject access request process tested end-to-end

---

## III. Integration Principles

### 11. Loose Coupling, Tight Contracts

**Principle Statement**:
Systems MUST be loosely coupled through published interfaces with tight, enforceable contracts. Shared databases, file systems and tight runtime dependencies across system boundaries are prohibited.

**Rationale**:
The criminal justice system comprises independently governed organisations (police forces, CPS, HMCTS, HMPPS, Legal Aid Agency) each with their own budgets, priorities and technology choices. Loose coupling enables independent deployment, technology evolution and team autonomy. The failure of the original Common Platform ambition (a single system for HMCTS and CPS) demonstrates the risk of tight coupling across organisational boundaries.

**Implications**:
- Communicate through published APIs or asynchronous events
- No direct database access across system or agency boundaries
- Each system manages its own data lifecycle
- Shared libraries kept minimal; favour duplication over coupling
- Avoid distributed transactions across systems
- Interface contracts include schemas, SLAs, error codes and versioning

**Validation Gates**:
- [ ] Systems communicate via APIs or events, not direct database access
- [ ] No shared mutable state across system boundaries
- [ ] Each system has independent data store
- [ ] Deployment of one system does not require deployment of another
- [ ] Interface contracts published with SLAs and versioning

---

### 12. Event-Driven Integration for Case Progression

**Principle Statement**:
Systems SHOULD use asynchronous, event-driven communication for case progression events (charge, hearing scheduled, verdict, sentence). Synchronous communication SHOULD be reserved for real-time user interactions and queries.

**Rationale**:
Criminal cases progress through multiple agencies (police → CPS → courts → probation/prisons) over weeks, months or years. Event-driven architecture naturally models this progression, enabling each agency to react to case events independently. It reduces temporal coupling, improves fault tolerance and enables real-time notification without polling.

**When to Use Asynchronous**:
- Case progression events (charge filed, hearing listed, verdict entered, sentence passed)
- Document sharing and disclosure notifications
- Cross-agency status updates (prisoner location, bail conditions)
- Batch operations (case file transfers, schedule generation)

**When Synchronous is Appropriate**:
- Real-time user interactions (searching case records, checking court availability)
- Authentication and authorisation checks
- Transactions requiring immediate consistency (payments, legal aid determinations)

**Validation Gates**:
- [ ] Event-driven patterns used for case progression flows
- [ ] Message durability and delivery guarantees defined
- [ ] Event schemas versioned and published
- [ ] Dead letter queues and error handling configured
- [ ] Idempotent event processing to handle duplicates

---

## IV. Quality Attributes

### 13. Performance Under Operational Load

**Principle Statement**:
All systems MUST meet defined performance targets under expected operational load. Court systems MUST support real-time operations during sitting hours without degradation.

**Rationale**:
Court proceedings operate to strict timetables. A listing system that is slow during morning list calls, a case management system that cannot retrieve files during hearings, or a video link system that drops during remote participation directly disrupts the administration of justice and wastes limited sitting time.

**Performance Targets** (define per system):
- **Response Time**: p50, p95, p99 latency targets appropriate to user context
- **Throughput**: Concurrent users during peak court hours (09:00–17:00)
- **Concurrency**: Support for simultaneous users across all court centres
- **Resource Efficiency**: Sustainable compute and storage costs at scale

**Validation Gates**:
- [ ] Performance requirements defined with measurable targets
- [ ] Load testing performed at peak expected capacity
- [ ] Performance metrics monitored continuously in production
- [ ] Capacity planning model defined and reviewed quarterly
- [ ] Performance does not degrade as data volumes grow

---

### 14. Availability and Continuity

**Principle Statement**:
All systems MUST meet defined availability targets with automated recovery and minimal data loss. Mission-critical court systems MUST be available during sitting hours with planned maintenance outside operational windows.

**Availability Targets** (define per system):
- **Mission-critical** (Common Platform, court scheduling, video links): 99.9% during sitting hours
- **Important** (disclosure tools, case file management): 99.5%
- **Supporting** (analytics, reporting, training): 99.0%
- **Recovery Time Objective (RTO)**: Maximum acceptable downtime before manual fallback
- **Recovery Point Objective (RPO)**: Maximum acceptable data loss

**High Availability Patterns**:
- Redundancy across availability zones / data centres within UK jurisdiction
- Automated health checks and failover
- Regular disaster recovery testing
- Planned maintenance windows outside court sitting hours

**Validation Gates**:
- [ ] Availability SLA defined per service tier
- [ ] RTO and RPO requirements documented
- [ ] Redundancy strategy implemented
- [ ] Failover tested regularly
- [ ] Backup and restore procedures validated
- [ ] Business continuity plan for complete system outage

---

### 15. Accessibility and Inclusive Design

**Principle Statement**:
All user-facing systems MUST meet WCAG 2.2 Level AA accessibility standards and be usable by all participants in the criminal justice system, including those with disabilities, limited digital skills or limited English proficiency.

**Rationale**:
The criminal justice system serves the entire population, including vulnerable defendants, victims and witnesses. The Leveson Review highlights the need for AI translation tools to address interpreter shortages, remote participation for defendants in custody, and improved court information for the public. GDS Service Standard Point 5 requires services to be accessible and inclusive. The Public Sector Bodies Accessibility Regulations 2018 apply.

**Implications**:
- WCAG 2.2 Level AA compliance for all public-facing and professional-facing interfaces
- Multi-language support for key user journeys (leveraging AI translation where validated)
- Usable on standard court IT equipment and personal devices where remote participation is permitted
- Designed for users under stress (defendants, victims, witnesses) with clear language and simple flows
- Tested with representative users including those with assistive technologies

**Validation Gates**:
- [ ] WCAG 2.2 Level AA audit completed
- [ ] Tested with assistive technologies (screen readers, voice control, magnification)
- [ ] Language support validated for most common non-English languages
- [ ] User research conducted with representative criminal justice users
- [ ] GDS accessibility statement published

---

### 16. Maintainability and Evolvability

**Principle Statement**:
All systems MUST be designed for change, with clear separation of concerns, modular architecture and comprehensive documentation. The criminal justice reform programme spans multiple years; systems must evolve as recommendations are implemented incrementally.

**Rationale**:
The Leveson Review contains 180 recommendations to be implemented over multiple years. Technology must support incremental delivery without requiring wholesale replacement. Systems built today must be modifiable tomorrow as policy evolves, caseloads change and AI capabilities mature.

**Implications**:
- Modular architecture with clear boundaries between components
- Separation of concerns (business logic, data access, presentation)
- Architecture Decision Records (ADRs) for significant choices
- Automated testing to enable confident refactoring
- Configuration-driven behaviour where business rules are expected to change
- Documentation maintained as a first-class deliverable

**Validation Gates**:
- [ ] Architecture documentation exists and is current
- [ ] Module boundaries clear with defined responsibilities
- [ ] Automated test coverage enables safe refactoring
- [ ] Architecture Decision Records document key choices
- [ ] Business rules externalised from code where they are expected to change

---

## V. Development Practices

### 17. Infrastructure as Code

**Principle Statement**:
All infrastructure MUST be defined as code, version-controlled and deployed through automated pipelines. No manual changes to production infrastructure are permitted.

**Rationale**:
Manual infrastructure changes create drift, inconsistency and undocumented state. Given the cross-agency nature of the criminal justice system and the need for repeatable environments (development, test, staging, production, disaster recovery), infrastructure as code is essential for reliability and auditability.

**Implications**:
- All infrastructure defined in declarative code
- Infrastructure changes go through code review
- Environments are reproducible from code
- No manual changes to production infrastructure ("ClickOps" prohibited)
- Infrastructure versioned alongside application code

**Validation Gates**:
- [ ] Infrastructure defined as code
- [ ] Infrastructure code version-controlled
- [ ] Automated deployment pipeline for infrastructure
- [ ] No manual infrastructure changes in production
- [ ] Environment parity verified (dev/test/staging match production configuration)

---

### 18. Automated Testing and Quality Assurance

**Principle Statement**:
All code changes MUST be validated through automated testing before deployment to production. Testing MUST include functional correctness, security, performance and accessibility.

**Test Pyramid**:
- **Unit Tests**: Fast, isolated, high coverage (70–80% of tests)
- **Integration Tests**: Test component interactions, including cross-agency API contracts (15–20% of tests)
- **End-to-End Tests**: Critical user journeys through the case progression lifecycle (5–10% of tests)

**Required Test Types**:
- Functional tests (does it work correctly?)
- Security tests (is it secure? dependency scanning, SAST, DAST)
- Performance tests (does it meet latency and throughput targets?)
- Accessibility tests (does it meet WCAG 2.2 Level AA?)
- Contract tests (do API contracts between agencies remain compatible?)

**Validation Gates**:
- [ ] Automated tests exist and pass before merge
- [ ] Test coverage meets defined thresholds
- [ ] Critical case progression paths have end-to-end tests
- [ ] Security scanning integrated into CI pipeline
- [ ] Contract tests validate cross-agency API compatibility

---

### 19. Continuous Integration and Deployment

**Principle Statement**:
All code changes MUST go through automated build, test and deployment pipelines with quality gates at each stage. Deployments MUST be automated, repeatable and auditable.

**Pipeline Stages**:
1. **Source Control**: All changes committed to version control with peer review
2. **Build**: Automated compilation and packaging
3. **Test**: Automated test execution (unit, integration, security, accessibility)
4. **Security Scan**: Dependency vulnerability scanning, static analysis, secret detection
5. **Deployment**: Automated deployment to environments with approval gates for production
6. **Verification**: Post-deployment smoke tests and health checks

**Quality Gates**:
- All tests must pass
- No critical or high security vulnerabilities
- Code review approval required
- Accessibility checks pass
- Deployment requires production readiness checklist sign-off

**Validation Gates**:
- [ ] Automated CI/CD pipeline exists
- [ ] Pipeline includes security scanning
- [ ] Deployment is automated and repeatable
- [ ] Rollback capability tested
- [ ] Audit trail of all production deployments maintained

---

### 20. Open Standards and Avoid Lock-In

**Principle Statement**:
Systems SHOULD use open standards and open-source components where appropriate to avoid vendor lock-in and ensure long-term sustainability. Proprietary dependencies MUST be isolated behind abstraction layers.

**Rationale**:
The Technology Code of Practice (TCoP) requires UK Government projects to use open standards and consider open-source solutions. Given the multi-year, multi-agency scope of the criminal courts reform, lock-in to a single vendor's ecosystem would constrain future options and increase costs. The failure to adapt Common Platform's original scope illustrates the risk of deep platform dependencies.

**Implications**:
- Use open standards for data formats, protocols and interfaces
- Evaluate open-source alternatives alongside proprietary options
- Isolate proprietary dependencies behind abstraction layers
- Ensure data can be exported in open formats
- Avoid contractual terms that create switching costs disproportionate to value

**Validation Gates**:
- [ ] Open standards used for data exchange formats and protocols
- [ ] Proprietary dependencies documented with exit strategy
- [ ] Data export capability verified in open formats
- [ ] Vendor lock-in risk assessment completed
- [ ] TCoP compliance confirmed

---

## VI. Criminal Justice Specific Principles

### 21. Equality of Arms

**Principle Statement**:
Technology capabilities provided to the prosecution MUST be matched by equivalent capabilities available to the defence. AI tools used by the CPS or police for case preparation, disclosure or evidence analysis MUST have equivalent tools accessible to defence practitioners.

**Rationale**:
The Leveson Review explicitly states that "both prosecution and defence [must] have access to similar tools and expertise." Fair trial rights under Article 6 ECHR require equality of arms. If AI tools give the prosecution a significant advantage in processing evidence or preparing cases, this imbalance undermines the fairness of proceedings and risks miscarriages of justice.

**Implications**:
- AI tools deployed for prosecution case preparation must have defence equivalents
- Defence access to digital evidence must not be inferior to prosecution access
- Legal aid funding models must account for the cost of digital tools
- Disclosure processes must be equally supported on both sides
- Defence practitioners must receive equivalent training on new digital tools

**Validation Gates**:
- [ ] Defence equivalent identified for each prosecution AI tool
- [ ] Defence access to digital evidence verified as equivalent
- [ ] Legal aid fee structures reviewed for digital tool costs
- [ ] Training programmes include defence practitioners
- [ ] Equality of arms assessment completed for each major capability

---

### 22. Judicial Independence and Transparency

**Principle Statement**:
Technology MUST NOT compromise judicial independence, impartiality or integrity. Judicial decision-making MUST remain the exclusive domain of human judges and magistrates. All technology used in court proceedings MUST be transparent in its operation and auditable.

**Rationale**:
The Leveson Review states that the biggest challenge in accelerating AI adoption is "ensuring that AI does not affect judicial outcomes in a way that impacts judicial independence, impartiality or integrity." AI-assisted scheduling, case management and transcription support judicial work but must never constrain or influence judicial decisions. The public must be able to understand and challenge how technology is used in their case.

**Implications**:
- AI tools MUST NOT make or constrain judicial decisions (sentencing, bail, case allocation to division)
- Scheduling and listing tools provide recommendations, not mandates — judicial discretion preserved
- All AI-generated outputs used in court must be disclosable and challengeable
- Audit trails must record when and how AI tools were used in case processing
- Technology changes affecting court procedures require judicial approval through appropriate governance

**Validation Gates**:
- [ ] No AI tool makes binding judicial decisions
- [ ] AI recommendations clearly labelled as advisory
- [ ] Audit trail records all AI-assisted processing in case lifecycle
- [ ] Judicial governance consulted on technology changes affecting court procedures
- [ ] Transparency statement published for each AI tool used in court

---

### 23. Victim and Witness Protection

**Principle Statement**:
Systems handling victim and witness data MUST implement enhanced protections including access restrictions, anonymisation capabilities and secure communication channels. Technology MUST support, not undermine, the safety of victims and witnesses.

**Rationale**:
Victims and witnesses in criminal cases, particularly in RASSO (rape and serious sexual offences) cases, face real risks from data breaches or inappropriate disclosure. The Leveson Review highlights the devastating impact of delays on victims and witnesses. Technology must protect their data while enabling efficient case progression.

**Implications**:
- Victim and witness personal data subject to enhanced access controls
- System design must support restriction orders and anonymity provisions
- Secure communication channels for victim/witness liaison
- Special measures for vulnerable witnesses supported by technology (pre-recorded evidence, video links, screens)
- Data minimisation — only data necessary for proceedings is processed

**Validation Gates**:
- [ ] Enhanced access controls for victim/witness data implemented
- [ ] Anonymisation and restriction order capabilities tested
- [ ] Secure communication channels available
- [ ] Special measures technology available and tested
- [ ] Data minimisation verified for victim/witness data flows

---

## VII. Exception Process

### Requesting Architecture Exceptions

Principles are mandatory unless a documented exception is approved by the Enterprise Architecture Review Board, with oversight from the Criminal Justice Technology Leadership role.

**Valid Exception Reasons**:
- Technical constraints that prevent compliance (documented with evidence)
- Regulatory or legal requirements that conflict with a principle
- Transitional state during legacy system migration (with defined end date)
- Pilot/proof-of-concept with defined scope, duration and success criteria
- Cross-agency dependency where compliance requires action by another organisation

**Exception Request Requirements**:
- [ ] Justification with business/technical rationale
- [ ] Alternative approach and compensating controls
- [ ] Risk assessment and mitigation plan
- [ ] Expiration date (exceptions are time-bound, maximum 12 months)
- [ ] Remediation plan to achieve compliance
- [ ] Impact assessment on cross-agency interoperability

**Approval Process**:
1. Submit exception request to Enterprise Architecture team
2. Review by architecture review board
3. CTO/CIO approval for exceptions to critical principles (Security, Data Protection, Judicial Independence)
4. Document exception in project architecture documentation
5. Quarterly review of all active exceptions
6. Exception automatically expires if not renewed

---

## VIII. Governance and Compliance

### Architecture Review Gates

All projects must pass architecture reviews at key milestones, aligned with GDS Service Standard phases:

**Discovery/Alpha**:
- [ ] Architecture principles understood and acknowledged
- [ ] High-level approach aligns with principles
- [ ] No obvious principle violations
- [ ] Cross-agency impacts identified
- [ ] AI tools categorised and governance approach agreed

**Beta/Design**:
- [ ] Detailed architecture documented
- [ ] Compliance with each principle validated
- [ ] Exceptions requested and approved where required
- [ ] Security and data protection principles validated
- [ ] DPIA completed
- [ ] ATRS record completed (if AI tools involved)
- [ ] Equality of arms assessment completed

**Pre-Production**:
- [ ] Implementation matches approved architecture
- [ ] All validation gates passed
- [ ] Operational readiness verified
- [ ] Accessibility audit completed
- [ ] Penetration testing completed
- [ ] Disaster recovery tested

### Enforcement

- Architecture reviews are **mandatory** for all projects above £100k total cost
- Principle violations must be remediated before production deployment
- Approved exceptions are time-bound and reviewed quarterly
- Retrospective compliance reviews for live systems on an annual cycle
- Compliance status reported to Criminal Justice Technology Leadership role

### UK Government Framework Alignment

| Principle | TCoP | GDS Standard | NCSC CAF | AI Playbook |
|-----------|------|-------------|----------|-------------|
| 1. Cross-Agency Interoperability | Point 8 (Share, reuse) | Point 13 (Common components) | — | — |
| 2. Human-Centred AI Augmentation | Point 10 (Technology appraisals) | — | — | All 10 principles |
| 3. Security by Design | Point 7 (Security, privacy) | Point 9 (Secure service) | All 4 objectives | — |
| 4. Legacy Modernisation | Point 6 (Cloud first) | — | Objective B | — |
| 5. Scalability and Elasticity | Point 6 (Cloud first) | — | — | — |
| 6. Resilience and Fault Tolerance | — | Point 11 (Reliability) | Objective C | — |
| 7. Observability | — | Point 12 (Monitoring) | Objective C | — |
| 8. Data as Shared Asset | Point 9 (Data standards) | Point 13 (Common components) | — | — |
| 9. Data Quality | Point 9 (Data standards) | — | — | Principle 6 (Data quality) |
| 10. Privacy and Data Protection | Point 7 (Security, privacy) | Point 9 (Secure service) | Objective A | — |
| 15. Accessibility | Point 3 (Accessible) | Point 5 (Inclusive) | — | — |
| 20. Open Standards | Point 4 (Open standards) | Point 13 (Common components) | — | — |
| 21. Equality of Arms | — | — | — | Principle 3 (Fairness) |
| 22. Judicial Independence | — | — | — | Principle 1 (Safety) |

---

## IX. Appendix

### Principle Summary Checklist

| # | Principle | Category | Criticality | Key Validation |
|---|-----------|----------|-------------|----------------|
| 1 | Cross-Agency Interoperability | Strategic | CRITICAL | API specs published, cross-agency testing |
| 2 | Human-Centred AI Augmentation | Strategic | CRITICAL | ATRS record, bias assessment, human oversight |
| 3 | Security by Design | Strategic | CRITICAL | Threat model, pen testing, NCSC CAF |
| 4 | Legacy Modernisation | Strategic | HIGH | Decommissioning timeline, migration plan |
| 5 | Scalability and Elasticity | Strategic | HIGH | Load testing, scaling metrics |
| 6 | Resilience and Fault Tolerance | Strategic | CRITICAL | Fault injection, RTO/RPO |
| 7 | Observability | Strategic | HIGH | Metrics, logs, traces, dashboards |
| 8 | Data as Shared Asset | Data | CRITICAL | System of record, data-sharing agreements |
| 9 | Data Quality and Integrity | Data | CRITICAL | Quality rules, reconciliation |
| 10 | Privacy and Data Protection | Data | CRITICAL | DPIA, lawful basis, retention |
| 11 | Loose Coupling | Integration | HIGH | API contracts, deployment independence |
| 12 | Event-Driven Integration | Integration | HIGH | Event schemas, case progression events |
| 13 | Performance | Quality | HIGH | Load testing, latency targets |
| 14 | Availability and Continuity | Quality | CRITICAL | SLA monitoring, DR testing |
| 15 | Accessibility | Quality | HIGH | WCAG audit, assistive tech testing |
| 16 | Maintainability | Quality | MEDIUM | Documentation, ADRs, tests |
| 17 | Infrastructure as Code | DevOps | HIGH | IaC coverage, no manual changes |
| 18 | Automated Testing | DevOps | HIGH | Test coverage, security scanning |
| 19 | CI/CD | DevOps | HIGH | Pipeline exists, rollback tested |
| 20 | Open Standards | DevOps | MEDIUM | TCoP compliance, lock-in assessment |
| 21 | Equality of Arms | Criminal Justice | CRITICAL | Defence equivalent for each prosecution tool |
| 22 | Judicial Independence | Criminal Justice | CRITICAL | No AI judicial decisions, transparency |
| 23 | Victim/Witness Protection | Criminal Justice | CRITICAL | Enhanced access controls, special measures |

---

## External References

| Document | Type | Source | Key Extractions | Path |
|----------|------|--------|-----------------|------|
| Independent Review of the Criminal Courts: Overview | PDF | GOV.UK | 180 recommendations, technology themes, AI principles, efficiency principles | `projects/000-global/external/independent-review-criminal-courts-overview.pdf` |
| Independent Review of the Criminal Courts: Part I | PDF | GOV.UK | Problem diagnosis, Crown Court crisis, structural reform recommendations | `projects/000-global/external/35.49_MOJ_Ind_Review_Criminal_Courts_v8b_FINAL_WEB.pdf` |
| Independent Review of the Criminal Courts: Part II Vol 1 | PDF | GOV.UK | Technology governance, system interoperability, AI integration, cyber resilience, API-first, Common Platform | `projects/000-global/external/independent-review-criminal-courts-part-2-vol-1.pdf` |
| Independent Review of the Criminal Courts: Part II Vol 2 | PDF | GOV.UK | Listing and AI, case management tools, remote participation, hearing processes | `projects/000-global/external/independent-review-criminal-courts-part-2-vol-2.pdf` |

---

**Generated by**: ArcKit `/arckit.principles` command
**Generated on**: 2026-02-04
**ArcKit Version**: 1.3.0
**Project**: Criminal Courts Technology & AI Reform (Project 000)
**AI Model**: Claude Opus 4.5 (claude-opus-4-5-20251101)

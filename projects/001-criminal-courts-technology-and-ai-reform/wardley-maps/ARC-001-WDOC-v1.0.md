# Wardley Doctrine Assessment: Criminal Courts Technology & AI Reform

> **Template Origin**: Official | **ArcKit Version**: 1.5.0 | **Command**: `/arckit.wardley.doctrine`

## Document Control

| Field | Value |
|-------|-------|
| **Document ID** | ARC-001-WDOC-v1.0 |
| **Document Type** | Wardley Doctrine Assessment |
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
| **Distribution** | MoJ Enterprise Architecture, HMCTS Digital, CPS Digital, Programme Board, Leadership Team |

## Revision History

| Version | Date | Author | Changes | Approved By | Approval Date |
|---------|------|--------|---------|-------------|---------------|
| 1.0 | 2026-03-16 | ArcKit AI | Initial doctrine assessment from `/arckit:wardley.doctrine` command | PENDING | PENDING |

---

## Executive Summary

**Overall Maturity Score**: 2.1 / 5.0 — Developing

**Phase Positioning**:

| Phase | Name | Score | Status |
|-------|------|-------|--------|
| Phase I | Stop Self-Harm | 2.2 / 5.0 | Not Started |
| Phase II | Becoming More Context Aware | 2.2 / 5.0 | Not Started |
| Phase III | Better for Less | 1.8 / 5.0 | Not Started |
| Phase IV | Continuously Evolving | 1.8 / 5.0 | Not Started |

**Critical Findings**:

1. **No common language across the criminal justice system**: Five agencies use different terminology for the same concepts ("case", "charge", "outcome" mean different things to police, CPS, and HMCTS). This is the single most damaging doctrine failure — it undermines every integration, data exchange, and cross-agency decision.
2. **User needs are inferred, not researched**: Despite 8 user personas in requirements, no evidence of conducted user research with real practitioners. The Common Platform's troubled rollout is a direct consequence of building from organisational needs rather than validated user needs.
3. **Inertia is recognised but unmanaged**: The programme documents identify inertia (Common Platform sunk cost, legacy applications, agency independence) but has no active inertia management programme. Recognising inertia without managing it provides awareness without change.

The criminal justice system technology landscape is at the Phase I/II boundary — aware of its problems but still systematically self-harming through duplication, absence of common language, and failure to ground decisions in genuine user research. The Leveson Review provides a rare external forcing function, but without immediate Phase I foundations (common language, user research, appropriate methods), the programme risks repeating Common Platform's failures at larger scale.

---

## Strategy Cycle Context

| Element | Summary |
|---------|---------|
| **Purpose** | Deliver fair, timely, and transparent criminal case outcomes through technology-enabled reform. Reduce 77,000+ Crown Court backlog below 50,000 within 3 years. The purpose is clearly articulated in the Leveson Review mandate and programme SOBC, but understanding varies significantly across agencies — MoJ frames it as reform, HMCTS as operational efficiency, CPS as prosecution quality, and the judiciary as independence preservation. |
| **Landscape** | The Wardley Map (ARC-001-WARD-001-v1.0) reveals 30 components: 4 in Genesis (AI Governance, Defence Portal, Bias Testing, Defence Equality), 12 in Custom (the core CJS-specific capabilities), 6 in Product, and 8 in Commodity. The landscape is heavily left-shifted — the majority of strategic components are genesis/custom with no market equivalents. The critical convergence at Cross-Agency Data Exchange makes integration the keystone investment. |
| **Climate** | The CJS technology landscape is entering a "War" phase: LLM AI services are industrialising (product → commodity within 24 months), the Leveson Review creates unprecedented political mandate for change, UK GDPR/DPA 2018 Part 3 imposes criminal-justice-specific data protection constraints, and HM Treasury requires Green Book compliance for the £281M investment. Simultaneously, the AI Playbook and ATRS requirements add a new regulatory dimension that has no precedent in criminal justice. |
| **Leadership** | Decision-making is highly fragmented across 5+ independent organisations. MoJ CDIO provides technology strategy but has limited authority over HMCTS operations, CPS technology, or police systems. The judiciary (Lady Chief Justice, Lead Judge for AI) holds constitutional independence and effective veto over case-affecting AI. Strategy is treated as a periodic planning exercise (annual spending review cycle) rather than a continuous iterative process. The programme board is the coordination mechanism, but real decision authority is distributed. |

---

## Doctrine Assessment Matrix

Score key: **1** = Not practised | **2** = Ad hoc | **3** = Developing | **4** = Mature | **5** = Cultural norm

### Phase I: Stop Self-Harm

| Category | Principle | Score | Evidence | Improvement Action |
|----------|-----------|:-----:|----------|--------------------|
| Communication | Common Language | 1 | No cross-agency glossary exists. "Case" means different things to police (investigation), CPS (prosecution file), HMCTS (court matter), and HMPPS (offender record). Criminal Justice Data Standards (WARD component at 0.28 evolution) are being designed but not yet published. The Common Platform's user confusion is partly attributable to vocabulary mismatch. | Establish cross-agency terminology working group within 30 days. Publish v1.0 CJS glossary within 90 days. Mandate use in all programme documents. |
| Communication | Challenge Assumptions | 2 | The Leveson Review itself challenged long-standing assumptions about court technology. However, within the programme, assumptions from the strategy document (e.g., "43 police forces connected in 36 months" — LOW confidence) are not systematically challenged. No devil's advocate process. Risk register identifies risks but does not challenge underlying programme assumptions. | Introduce assumption audits at each programme board meeting. Maintain an explicit assumptions register alongside the risk register. |
| Communication | Understand Context | 2 | The programme has produced substantial contextual documentation (STKE, STRAT, SOBC, WARD). However, context is concentrated in architecture artifacts rather than being understood across the programme. Operational staff, legal teams, and frontline users likely have limited awareness of the strategic landscape. | Produce simplified context briefings for each stakeholder group. Run landscape awareness workshops for programme team leads. |
| Development | Know Your Users | 2 | Requirements (ARC-001-REQ-v1.0) define 8 user personas with pain points and goals, but these are analytically derived, not research-validated. No evidence of ethnographic observation, contextual inquiry, or usability testing with real practitioners. The Common Platform's troubled rollout demonstrates the consequences of building without validating user needs. | Commission user research sprints with real practitioners: CPS prosecutors, defence barristers, court staff, victims. Fund GDS-standard user research for alpha phase. |
| Development | Focus on User Needs | 2 | Requirements anchor to business requirements (BR-001 to BR-010) which are programme-centric, not user-centric. The distinction matters: BR-001 ("Reduce Crown Court case backlog") is a programme outcome, not a user need. User needs (e.g., "defence barrister can prepare a case without rekeying data") are present in use cases but not treated as the primary driver. | Reframe programme metrics around user outcomes, not programme outputs. Conduct user journey mapping for each persona. |
| Development | Remove Bias & Duplication | 2 | Significant data duplication across agencies: case data re-entered 5+ times (police → CPS → HMCTS → HMPPS → LAA). No systematic deduplication programme beyond the integration platform vision. AI bias testing is planned (Bias Testing Framework component) but not yet operational. Cognitive bias in programme decision-making (Common Platform sunk cost) is unaddressed. | Map all data duplication points. Quantify cost of rekeying. Prioritise the highest-volume duplication for first integration sprint. |
| Development | Use Appropriate Methods | 2 | Architecture governance follows traditional waterfall-influenced patterns (strategy → requirements → design → build). The programme documents do not reference agile delivery, iterative design, or evolutionary architecture. HMCTS has some agile capability but it is inconsistent. For genesis-stage components (AI Governance, Defence Portal), the current approach is too plan-driven. | Mandate agile delivery for genesis/custom components. Use time-and-materials contracts for discovery. Reserve waterfall/fixed-price for commodity procurement only. |
| Operation | Know the Details | 3 | The programme demonstrates reasonable operational detail in the risk register (20 risks, quantified inherent/residual scores), stakeholder analysis (15 stakeholders with drivers/goals), and SOBC (5-case model with quantified costs/benefits). However, operational detail about current system performance (e.g., Common Platform uptime, data error rates, disclosure review time per case) is referenced in requirements but not evidenced with data. | Establish baseline metrics for current operational performance. Instrument Common Platform for reliability and performance data. |
| Learning | Systematic Learning | 2 | No evidence of structured learning processes in the programme. No retrospectives documented. No lessons-learned register. The SOBC references learning from Common Platform's cost overruns, but this is a one-time observation, not a systematic process. Architecture artifacts do not reference previous iterations or what was learned from them. | Implement fortnightly retrospectives for delivery teams. Create lessons-learned register. Mandate post-milestone reviews. |

**Phase I Average**: 2.0 / 5.0

### Phase II: Becoming More Context Aware

| Category | Principle | Score | Evidence | Improvement Action |
|----------|-----------|:-----:|----------|--------------------|
| Communication | Bias Towards Open | 3 | TCoP compliance mandates open standards (Point 3/4). Architecture principles (P-20: Open Standards) explicitly require open approaches. CJS Data Standards are planned for open publication. However, inter-agency data sharing remains culturally resistant — agencies default to "need to know" rather than "default to share". Programme documents are OFFICIAL but not widely distributed beyond architecture team. | Default to open sharing of all non-sensitive programme documents. Publish architecture decisions as ADRs accessible to all agencies. |
| Development | Focus on Outcome | 2 | Success criteria in requirements are output-focused ("80%+ of cases use AI-assisted disclosure") rather than outcome-focused ("disclosure-related case collapses reduced by 40%"). Some outcome metrics exist (O-1 to O-6 in strategy) but they sit in strategic documents, not in delivery team objectives. Contracts are likely to be deliverable-based (DOS Outcomes) rather than outcome-based. | Reformulate delivery team OKRs around user outcomes. Structure contracts with outcome-based milestones where possible. |
| Development | Think FIRE | 2 | No evidence of FIRE principles (Fast, Inexpensive, Restrained, Elegant) in programme approach. The £281M investment and 5-year horizon suggest a large, comprehensive programme rather than a restrained, iterative one. Risk of over-engineering is high, especially for genesis-stage components. | Apply FIRE to AI Governance Framework and Defence Portal alpha phases. Set maximum 3-month cycles. Enforce "minimum viable governance" for first AI pilots. |
| Development | Use Appropriate Tools | 3 | The Wardley Map correctly identifies commodity tools (G-Cloud, GOV.UK services) vs. custom build needs. Technology selection is grounded in evolution stage. However, no evidence that teams are empowered to select tools — tool selection may be centralised and procurement-driven rather than team-driven. | Empower delivery teams to select tools within guardrails. Provide approved tool catalogues rather than mandated toolchains. |
| Development | Be Pragmatic | 3 | The hybrid build/buy strategy demonstrates pragmatism. Decision to stabilise Common Platform (rather than replace) is pragmatic. However, the programme scope is extremely ambitious (AI disclosure, defence portal, 37 legacy migrations, cross-agency integration, victim tracking — all simultaneously) which is the opposite of pragmatic. | Sequence ruthlessly. Identify the minimum viable programme that delivers BR-001 (backlog reduction) first. Defer lower-priority capabilities. |
| Development | Use Standards | 2 | No cross-agency CJS data standard exists today. Architecture principles mandate open standards (P-20) but standards are aspirational, not operational. The programme correctly identifies this gap (CJS Data Standards component at 0.28 evolution) but has not yet begun standardisation work. OpenAPI 3.1 is referenced but not mandated. | Launch CJS Data Standards working group immediately. Publish draft standard within 6 months. Mandate for all new integrations. |
| Operation | Manage Inertia | 2 | The Wardley Map identifies 6 inertia factors with severity ratings. The risk register captures related risks (R-001 to R-020). However, there is no active inertia management programme. No change champions are appointed. No dedicated change management workstream. Inertia is documented but not managed. | Appoint cross-agency change champions. Create dedicated change management workstream. Address Common Platform sunk cost bias explicitly in programme board. |
| Operation | Manage Failure | 2 | Risk register provides residual risk scores and mitigation strategies. However, there is no evidence of failure tolerance calibration by evolution stage. Genesis-stage AI components should have high failure tolerance (sandbox, pilot, iterate); commodity procurement should have low failure tolerance (SLA, penalty). No blameless post-incident process documented. | Define failure tolerance per evolution stage. Implement blameless post-incident reviews. Create sandbox environments for genesis-stage experimentation. |
| Operation | Effectiveness over Efficiency | 2 | Programme metrics emphasise efficiency (reduce disclosure review time by 50%, reduce data rekeying by 90%) rather than effectiveness (are we disclosing the right material? are we trying the right cases?). Efficiency metrics are easier to measure but can optimise the wrong activity. | Introduce effectiveness metrics alongside efficiency metrics. Ask "are we doing the right thing?" before "are we doing it efficiently?" |
| Learning | Bias Towards Action | 2 | The programme is in a prolonged planning phase — strategy, requirements, SOBC, DPIA, TCoP, stakeholder analysis all complete, but no delivery has started. This is a documentation-heavy, action-light posture. For a programme with a 3-year backlog reduction target, the absence of even small pilots is concerning. | Launch the first AI disclosure pilot within 90 days using existing LLM services. Accept imperfection. Learn from real deployment, not further analysis. |
| Leading | Move Fast | 2 | Multi-agency governance creates structural slowness. Programme board coordination across 5 agencies, judicial steering group consultations, ICO DPIA reviews, GDS service assessments, Treasury business case approvals — each adds latency. No evidence of efforts to compress decision cycles or reduce approval chains. | Identify the minimum approval path for the first pilot. Create a "fast track" decision process for time-sensitive decisions. Empower CDIO to approve within defined boundaries. |
| Leading | Strategy is Iterative | 2 | Strategy document (ARC-001-STRAT-v1.0) is a comprehensive one-time product with no evidence of iterative refinement. No quarterly strategy review cycle documented. No mechanism for updating strategy based on pilot outcomes or landscape changes. | Establish quarterly strategy review cycle aligned with programme board. Update Wardley Map quarterly. Treat strategy as a living document. |
| Structure | Think Small Teams | 2 | No evidence of team structure in programme documents. UK Government programmes typically use large, multi-vendor delivery teams managed through programme boards. No indication of small, autonomous, cross-functional teams aligned to specific components or user outcomes. | Structure delivery around small (6-8 person) teams aligned to value chain components. Give teams autonomy within architectural guardrails. |
| Structure | Distribute Power | 2 | Decision-making is highly centralised — programme board, ministerial approval, Treasury gating, judicial steering group. Operational teams have limited decision authority. This is structurally driven by UK Government accountability frameworks (Accounting Officer obligations) but still represents a doctrine weakness. | Define clear decision rights per team. Use Commander's Intent model: set clear outcomes and boundaries, then trust teams to deliver within them. |
| Structure | Aptitude and Attitude | 2 | No evidence of team composition strategy. Skills gap is identified in the risk register (legacy COBOL, AI/ML skills shortage) but there is no systematic approach to matching team aptitude/attitude to evolution stage (Pioneers for genesis, Settlers for custom, Town Planners for commodity). | Map required team archetypes to components by evolution stage. Recruit Pioneers for AI Governance/Defence Portal; Settlers for integration platform; Town Planners for cloud/infrastructure. |

**Phase II Average**: 2.2 / 5.0

### Phase III: Better for Less

| Category | Principle | Score | Evidence | Improvement Action |
|----------|-----------|:-----:|----------|--------------------|
| Operation | Optimise Flow | 1 | No evidence of value stream mapping or flow optimisation in the programme. The criminal justice system is characterised by extreme process friction — cases pass through 5+ agencies with manual handoffs, redundant data entry, and untracked delays. The programme addresses symptoms (build integration platform) but has not mapped the end-to-end value stream. | Commission end-to-end value stream map of a criminal case (charge to outcome). Identify the 5 biggest bottlenecks. Target integration investment at the highest-friction points. |
| Operation | Do Better with Less | 2 | The programme requests £281M over 5 years. While the SOBC demonstrates positive NPV, there is no evidence of constraint-driven innovation — no attempt to achieve a subset of outcomes with a fraction of the budget. UK Government programmes default to large comprehensive bids; this programme follows that pattern. | Define "minimum viable reform" — what is the smallest investment that delivers BR-001 (backlog reduction)? Challenge each spend item against this baseline. |
| Operation | Exceptional Standards | 2 | Architecture principles set high standards (23 principles including NON-NEGOTIABLE security). GDS Service Standard and TCoP provide external quality benchmarks. However, internal quality standards (e.g., code quality, test coverage, documentation standards) are not defined. The current TCoP assessment shows 6/13 points compliant — below exceptional. | Define internal quality standards for all deliverables. Target GDS service assessment pass on first attempt. Set TCoP full compliance as a gate before live deployment. |
| Learning | Bias Towards New | 2 | The programme includes genuinely novel components (AI Governance Framework, Defence Practitioner Portal) which demonstrates some willingness to explore. However, the delivery approach (strategy → requirements → procurement → build) is deeply traditional. No evidence of experimentation budget, innovation sprints, or protected exploration time. | Allocate 10% of programme budget to experimentation. Create a "CJS Innovation Lab" for rapid prototyping of genesis-stage components. |
| Leading | Commit to Direction | 3 | The Leveson Review provides strong directional commitment — 180 recommendations with cross-party political support. Programme strategy commits to a 5-year horizon. However, commitment to direction is externally driven (by the Review) rather than internally generated, creating risk that commitment wanes if political attention shifts. | Embed programme direction in multi-year spending commitments. Secure Treasury approval for multi-year funding to insulate from annual political cycles. |
| Leading | Be the Owner | 2 | Ownership is diffused. MoJ Permanent Secretary is the named SRO, but operational ownership sits with HMCTS CEO, prosecution ownership with DPP, judicial oversight with Lady Chief Justice, and defence access with LAA. No single person can make a cross-cutting decision. This is structurally inevitable in a multi-agency programme but still represents a doctrine weakness. | Clarify "single throat to choke" for each delivery stream. Give stream owners authority to make decisions within their domain without programme board escalation. |
| Leading | Inspire Others | 2 | The Leveson Review provides an external narrative of reform. However, there is no evidence of inspirational internal leadership storytelling — no programme vision statement beyond the strategic document, no rallying cry, no narrative connecting individual work to justice system transformation. Court staff and frontline users are likely unaware of the programme's transformative ambition. | Create a programme narrative that connects technology reform to justice outcomes. Share stories of user impact. Run cross-agency programme days to build shared identity. |
| Leading | Embrace Uncertainty | 2 | The programme adopts a plan-driven approach with detailed 5-year roadmap, specific cost estimates, and quantified benefits — all of which project false certainty for genesis-stage components. The SOBC presents a single preferred option with point estimates rather than ranges. Genuine uncertainty about AI efficacy, judicial adoption, and defence practitioner uptake is not adequately represented. | Adopt range-based estimates for genesis components. Use scenario planning for AI deployment timelines. Present programme board with option ranges, not point estimates. |
| Leading | Be Humble | 2 | The strategy document acknowledges Common Platform's troubled history as a lesson. However, the programme's scope (transform criminal justice technology across 5 agencies in 5 years) is extraordinarily ambitious — arguably more complex than Common Platform. Humility would suggest a more incremental approach. No evidence of external peer review or challenge function. | Establish an independent challenge panel. Seek external peer review from comparable international justice technology programmes. Acknowledge what we don't know. |

**Phase III Average**: 2.0 / 5.0

### Phase IV: Continuously Evolving

| Category | Principle | Score | Evidence | Improvement Action |
|----------|-----------|:-----:|----------|--------------------|
| Learning | Listen to Ecosystem | 2 | The Leveson Review is a significant ecosystem listening event — an independent review gathering evidence from across the justice system. However, this is a one-off event, not a systematic listening mechanism. No evidence of ongoing ecosystem monitoring: competitor analysis (international CJS technology), technology trend scanning, user feedback loops, or academic partnership pipelines. | Establish quarterly technology scanning process. Build academic partnerships for AI governance research. Create user feedback channels for each persona. Monitor international CJS technology developments (US, Australia, Netherlands). |
| Learning | Bias Towards Action | 2 | Scored consistently low across phases. The programme has produced 15+ governance artifacts over several months but has not deployed a single line of operational code or conducted a single user research session. The doctrine of "plan everything before building anything" is directly at odds with bias towards action. | Set a 90-day deadline for the first operational pilot. Accept that the pilot will be imperfect. Prioritise learning from real deployment over further planning. |
| Leading | Exploit the Landscape | 2 | The Wardley Map identifies landscape features (LLM commoditisation, GOV.UK service reuse, cross-agency convergence) but the programme has not yet exploited any of them. GOV.UK Notify and Design System are planned but not yet adopted. LLM AI services are available but not yet procured. The landscape analysis is excellent; the exploitation is zero. | Immediately procure LLM AI services and GOV.UK Notify. Begin using commodity components now, even before the full programme architecture is finalised. Don't wait for perfection to use what already works. |
| Leading | There is No Core | 1 | The criminal justice system treats its current institutional structure as permanent and immovable. The 5-agency model (MoJ, HMCTS, CPS, HMPPS, LAA) is treated as a given rather than a design choice. No consideration of whether the technology landscape could or should reshape organisational boundaries. The concept that all strategic positions are temporary is absent from programme thinking. | This is a long-term cultural change. Begin by mapping where agency boundaries create friction. Ask whether technology could make some agency distinctions irrelevant. |
| Structure | No Single Culture | 2 | The programme applies a uniform governance approach across all components regardless of evolution stage. Genesis-stage AI components receive the same programme board governance as commodity cloud procurement. No evidence of differentiated management approaches, failure tolerances, or team cultures by evolution stage. | Apply Pioneer culture to AI Governance and Defence Portal teams (high failure tolerance, exploration focus). Apply Town Planner culture to cloud infrastructure and legacy migration (efficiency, reliability focus). |
| Structure | Design for Constant Evolution | 1 | The programme architecture is designed as a one-time transformation ("current state → target state") rather than as a continuously evolving system. No evidence of evolutionary architecture principles: fitness functions, sacrificial architecture for genesis components, or planned obsolescence. The 5-year roadmap implies a destination, not a journey. | Adopt evolutionary architecture principles. Design all genesis/custom components for replacement, not permanence. Build fitness functions that detect when components need to evolve. |

**Phase IV Average**: 1.7 / 5.0

---

## Detailed Phase Findings

### Phase I: Stop Self-Harm — Detailed Findings

**Phase Score**: 2.0 / 5.0

**Strongest principles in this phase**:

- Know the Details (Score: 3) — The programme demonstrates reasonable operational detail through its risk register, stakeholder analysis, and SOBC quantification. Leadership has access to detailed information, even if they don't always act on it.

**Weakest principles in this phase**:

- Common Language (Score: 1) — The most damaging gap. Five agencies using different terminology for fundamental concepts makes every cross-agency conversation a translation exercise. Without a shared vocabulary, the programme cannot even discuss its problems coherently, let alone solve them.
- Systematic Learning (Score: 2) — No retrospectives, no lessons-learned register, no structured feedback loops. The programme will repeat mistakes because it has no mechanism to capture and apply lessons.

**Phase I Narrative**:

The criminal justice system is actively self-harming through absence of common language, unvalidated user needs, and significant data duplication across agencies. The programme has invested heavily in understanding the problem (extensive documentation) but has not yet begun addressing the foundational doctrine failures that will determine whether the solution works. The Common Platform's troubled rollout — built from organisational requirements rather than validated user needs — is the most vivid illustration of Phase I failure, and the programme is at risk of repeating it at larger scale.

---

### Phase II: Becoming More Context Aware — Detailed Findings

**Phase Score**: 2.2 / 5.0

**Strongest principles in this phase**:

- Bias Towards Open (Score: 3) — TCoP mandates and architecture principles (P-20) create structural incentives for openness. CJS Data Standards are planned for open publication.
- Use Appropriate Tools (Score: 3) — The Wardley Map correctly matches tools to evolution stage. Build/buy decisions are grounded in component maturity.
- Be Pragmatic (Score: 3) — Hybrid build/buy strategy and Common Platform stabilise-then-extend approach demonstrate pragmatic judgement.

**Weakest principles in this phase**:

- Focus on Outcome (Score: 2) — Metrics are output-focused rather than outcome-focused. Programme success should be measured by justice outcomes, not technology outputs.
- Move Fast (Score: 2) — Multi-agency governance creates structural slowness. Every decision requires coordination across 5+ organisations.
- Think Small Teams (Score: 2) — No evidence of small, autonomous teams. UK Government programme patterns default to large delivery organisations.

**Phase II Narrative**:

The programme shows nascent context awareness — the Wardley Map, stakeholder analysis, and strategy document demonstrate understanding of the landscape. However, this awareness has not yet translated into action. The programme knows its landscape but has not adapted its behaviour to match it. Structurally, the multi-agency governance model creates endemic slowness that no amount of process improvement can fully resolve; the programme must find ways to create speed within its constraints.

---

### Phase III: Better for Less — Detailed Findings

**Phase Score**: 2.0 / 5.0

**Strongest principles in this phase**:

- Commit to Direction (Score: 3) — The Leveson Review provides strong directional commitment with cross-party political support and a 5-year horizon.

**Weakest principles in this phase**:

- Optimise Flow (Score: 1) — No value stream mapping. No systematic identification of process bottlenecks. The programme addresses symptoms (build technology) without understanding the end-to-end flow of a criminal case through the system.
- There is No Core / Design for Constant Evolution (Scores: 1) — The programme treats both the institutional structure and the target architecture as permanent, which contradicts the fundamental doctrine of continuous evolution.

**Phase III Narrative**:

Phase III maturity is premature for this programme — the Phase I and II foundations are not yet in place. However, the scoring reveals a concerning pattern: the programme defaults to large, comprehensive, plan-driven delivery rather than iterative, constrained, learn-as-you-go approaches. The £281M budget request, while justified by the SOBC, may actually be a doctrine failure — a programme that embraced "do better with less" might achieve greater impact with significantly less investment by focusing ruthlessly on the highest-leverage interventions.

---

### Phase IV: Continuously Evolving — Detailed Findings

**Phase Score**: 1.7 / 5.0

**Strongest principles in this phase**:

- Listen to Ecosystem (Score: 2) — The Leveson Review represents a significant, if one-off, ecosystem listening event.

**Weakest principles in this phase**:

- There is No Core (Score: 1) — The 5-agency institutional structure is treated as immovable. No consideration that technology could reshape organisational boundaries.
- Design for Constant Evolution (Score: 1) — Architecture designed as one-time transformation, not continuous evolution. No fitness functions, no planned obsolescence for genesis components.

**Phase IV Narrative**:

Phase IV is the least mature phase, which is expected for a government programme that has not yet begun delivery. The critical concern is not the low scores themselves — Phase IV maturity takes years to develop — but the absence of even the seeds of Phase IV thinking. The programme should be building listening mechanisms and evolutionary architecture principles now, even if the full capabilities take years to mature.

---

## Previous Assessment Comparison

This is the initial assessment. No previous scores are available for comparison.

---

## Critical Gaps

| Rank | Phase | Category | Principle | Current Score | Target Score | Business Impact |
|------|-------|----------|-----------|:-------------:|:------------:|-----------------|
| 1 | I | Communication | Common Language | 1 | 3 | Without shared terminology, cross-agency integration (the programme's keystone) cannot succeed. Every data standard discussion, API specification, and governance conversation is undermined by vocabulary mismatch. This single gap has a multiplier effect on every other doctrine principle. |
| 2 | I | Development | Know Your Users | 2 | 4 | Building a £281M programme on analytically-derived personas rather than validated user research risks repeating Common Platform's failure. Defence barristers, victims, and court staff have materially different needs from what architects assume — only direct research can reveal them. |
| 3 | I | Development | Focus on User Needs | 2 | 4 | Programme metrics are output-focused (% cases using AI, data rekeying reduction) rather than outcome-focused (case collapses reduced, victim satisfaction improved). This misalignment means the programme could succeed on its own metrics while failing to improve justice outcomes. |
| 4 | II | Operation | Manage Inertia | 2 | 4 | Common Platform sunk cost bias (£250M+ invested), legacy system inertia (37 applications), and agency independence create resistance that will block delivery unless actively managed. Inertia is the primary reason good strategies fail in execution. |
| 5 | IV | Structure | Design for Constant Evolution | 1 | 3 | A one-time transformation architecture will be obsolete before it is complete. AI technology (LLMs evolving from product to commodity within 24 months), regulatory requirements (AI governance is genesis-stage), and user needs will all change during the 5-year programme. Without evolutionary architecture, the programme builds today's solution for yesterday's problem. |

---

## Implementation Roadmap

### Immediate Actions (0-3 months)

| Action | Principle(s) Addressed | Owner | Success Criteria |
|--------|----------------------|-------|------------------|
| **Publish CJS Glossary v1.0**: Convene cross-agency terminology working group (police, CPS, HMCTS, HMPPS, LAA). Agree definitions for the 50 most critical terms (case, charge, hearing, outcome, sentence, disclosure, evidence). Publish and mandate usage in all programme documents. | Common Language | MoJ CDIO | Glossary published; adopted in all programme board papers; referenced in API specifications |
| **Commission user research sprints**: Fund 4-week GDS-standard user research with real practitioners — 10+ CPS prosecutors, 10+ defence barristers, 10+ court staff, 10+ victims/witnesses. Validated personas and user journey maps produced. | Know Your Users, Focus on User Needs | Programme Director + GDS | 40+ user interviews completed; validated personas published; user journey maps shared with delivery teams |
| **Launch first operational pilot**: Deploy AI disclosure review MVP at 1 Crown Court site using existing LLM services (Azure OpenAI via G-Cloud). Accept imperfection. Prioritise learning from real deployment over further planning. | Bias Towards Action, Manage Failure | CPS CDO + MoJ Chief AI Officer | Pilot operational within 90 days; 50+ cases processed; lessons-learned report published |
| **Establish assumption register**: Extract all programme assumptions from strategy, SOBC, and requirements. Rate confidence (High/Medium/Low). Challenge LOW-confidence assumptions at each programme board. | Challenge Assumptions | Programme Director | Assumption register with 20+ entries; 5+ LOW-confidence assumptions challenged and resolved |

### Short-Term Actions (3-12 months)

| Action | Principle(s) Addressed | Owner | Success Criteria |
|--------|----------------------|-------|------------------|
| **Create active inertia management programme**: Appoint cross-agency change champions (one per agency). Address Common Platform sunk cost bias explicitly. Create legacy migration incentive structure. Build ministerial escalation path for agency resistance. | Manage Inertia | Programme Director + MoJ Permanent Secretary | Change champions appointed; Common Platform evolution strategy agreed by programme board; first 5 legacy applications in migration |
| **Restructure delivery into small autonomous teams**: Create 4-6 small (6-8 person) cross-functional delivery teams aligned to value chain components: AI Disclosure, Defence Portal, Integration Platform, Victim Tracking, Legacy Migration, Platform/Infrastructure. Give teams autonomy within architectural guardrails. | Think Small Teams, Distribute Power, Aptitude & Attitude | Programme Director | Teams formed; team-level OKRs defined; decision rights documented; first retrospectives completed |
| **Implement outcome-based metrics**: Replace programme output metrics with justice outcome metrics. Track: case collapse rate (not AI usage %), victim satisfaction (not notification count), time-to-justice (not system uptime). Report outcomes alongside outputs at every programme board. | Focus on Outcome, Effectiveness over Efficiency | Programme Director + HMCTS CEO | Outcome metrics dashboard operational; reported at programme board; delivery teams' OKRs aligned |
| **Map end-to-end value stream**: Commission value stream map of a criminal case from charge to sentence outcome. Identify the 5 highest-friction handoff points. Target integration investment at these points. | Optimise Flow | MoJ CDIO | Value stream map published; top 5 bottlenecks identified; integration platform scope refined to address highest-friction points first |
| **Establish quarterly strategy review cycle**: Review and update Wardley Map quarterly. Challenge evolution predictions against actual movement. Update strategy based on pilot outcomes and landscape changes. | Strategy is Iterative | MoJ CDIO | Quarterly review process documented; first review completed; strategy document versioned to v1.1 |

### Long-Term Actions (12-24 months)

| Action | Principle(s) Addressed | Owner | Success Criteria |
|--------|----------------------|-------|------------------|
| **Build ecosystem listening mechanisms**: Establish formal channels for technology trend monitoring, international CJS technology benchmarking (US, Australia, Netherlands), academic partnership for AI governance research, and ongoing user feedback loops per persona. | Listen to Ecosystem, Bias Towards New | MoJ CDIO + MoJ Chief AI Officer | Quarterly technology scan reports; 2+ international benchmarking partnerships; 3+ academic research collaborations; user feedback channels operational for all 8 personas |
| **Adopt evolutionary architecture principles**: Redesign genesis/custom components for replaceability, not permanence. Implement fitness functions that detect when components need to evolve. Build abstraction layers that allow model/vendor switching without rearchitecture. Plan for LLM provider switching as market commoditises. | Design for Constant Evolution, There is No Core | HMCTS CTO | Fitness functions defined for all genesis components; LLM abstraction layer operational; vendor switching demonstrated; architecture review board includes evolution assessment |
| **Differentiate team cultures by evolution stage**: Apply Pioneer culture to AI Governance and Defence Portal (high failure tolerance, exploration budget, short cycles). Apply Settler culture to Integration Platform and Victim Tracking (product-oriented, user feedback driven). Apply Town Planner culture to Cloud Infrastructure and Legacy Migration (efficiency, reliability, cost). | No Single Culture, Aptitude & Attitude | Programme Director | Team culture assessments completed; different performance frameworks by stage; talent recruitment aligned to archetype needs |

---

## Recommendations

1. **Fix Common Language before building anything cross-agency**
   - **Rationale**: Common Language is scored 1/5 — the lowest possible. Every cross-agency integration, data standard, API specification, and governance conversation is undermined by vocabulary mismatch. This is the single highest-leverage improvement available.
   - **Expected Benefit**: Accelerated cross-agency integration; reduced miscommunication in programme governance; clearer API specifications; more effective programme board decision-making.
   - **Risk of Inaction**: Integration platform built on ambiguous data standards; programme team spending more time translating between agencies than building; repeat of Common Platform's user confusion.

2. **Validate user needs through direct research before committing to full-scale build**
   - **Rationale**: Know Your Users and Focus on User Needs are both scored 2/5. The programme is about to commit £281M based on analytically-derived personas that have not been validated with real users. The Common Platform's troubled rollout is a direct consequence of this pattern.
   - **Expected Benefit**: Requirements grounded in real user needs; higher adoption rates for AI tools; reduced risk of building features users don't want; stronger GDS service assessment performance.
   - **Risk of Inaction**: Programme builds technology that practitioners resist or cannot use; AI disclosure tools that don't match prosecutor workflow; Defence Portal that barristers ignore; victim tracking that victims find inaccessible.

3. **Launch a pilot within 90 days to break the planning-without-action cycle**
   - **Rationale**: Bias Towards Action is scored 2/5 across multiple phases. The programme has produced 15+ governance artifacts but has not deployed a single operational component. For a programme with a 3-year backlog reduction target, this planning-heavy posture is strategically dangerous. Real learning comes from deployment, not documentation.
   - **Expected Benefit**: Early evidence of AI efficacy for disclosure; real user feedback; demonstration of progress to Treasury and programme board; learning that informs full-scale design.
   - **Risk of Inaction**: Programme enters year 2 with no operational experience; business case benefits timeline slips; political momentum from Leveson Review dissipates; programme labelled as "another government IT project that studies the problem."

---

## Traceability

| Artifact | Document ID | Relationship |
|----------|-------------|--------------|
| Architecture Principles | ARC-000-PRIN-v1.0 | 23 principles assessed against doctrine; principles reveal stated values; doctrine reveals lived practice |
| Wardley Map | ARC-001-WARD-001-v1.0 | Landscape and climate context; component evolution positions; identified inertia; build/buy decisions |
| Value Chain | ARC-001-WVCH-001-v1.0 | Dependency structure; convergence at cross-agency data exchange; critical paths |
| Stakeholder Analysis | ARC-001-STKE-v1.0 | Leadership fragmentation; 15 stakeholders across 5+ organisations; power/interest dynamics |
| Requirements | ARC-001-REQ-v1.0 | User personas (analytically derived); use cases; success criteria orientation (output vs. outcome) |
| Strategy | ARC-001-STRAT-v1.0 | Strategic vision; build/buy decisions; 5-year horizon; £281M investment |
| Risk Register | ARC-001-RISK-v1.0 | 20 risks; inertia factors; mitigation strategies |
| TCoP Assessment | ARC-001-TCOP-v1.1 | 6/13 TCoP points compliant; gaps correlate with doctrine weaknesses |
| DPIA | ARC-001-DPIA-v1.0 | HIGH impact assessment; criminal justice data sensitivity |

---

**Generated by**: ArcKit `/arckit:wardley.doctrine` command
**Generated on**: 2026-03-16 16:00 GMT
**ArcKit Version**: 1.5.0
**Project**: Criminal Courts Technology & AI Reform (Project 001)
**AI Model**: claude-opus-4-6
**Generation Context**: Assessed from ARC-000-PRIN-v1.0, ARC-001-WARD-001-v1.0, ARC-001-WVCH-001-v1.0, ARC-001-STKE-v1.0, ARC-001-REQ-v1.0, ARC-001-STRAT-v1.0, ARC-001-RISK-v1.0, ARC-001-TCOP-v1.1, ARC-001-DPIA-v1.0, and Wardley Doctrine reference framework (42 principles across 4 phases)

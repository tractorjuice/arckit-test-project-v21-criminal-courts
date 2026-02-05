# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **ArcKit architecture governance project** — not a software codebase. It generates architecture documents (markdown) for the Criminal Courts Technology & AI Reform programme, based on the Independent Review of the Criminal Courts (Leveson Review, 2025-2026).

There is no build system, test suite, or application code. All work is done through ArcKit slash commands that generate governance artifacts.

## How to Work in This Repository

### ArcKit Slash Commands

All artifacts are produced via `/arckit.*` commands. The recommended execution order follows the 12-tier dependency hierarchy in `DEPENDENCY-MATRIX.md` (M=Mandatory, R=Recommended, O=Optional):

| Tier | Phase | Key Commands |
|------|-------|-------------|
| 0 | Foundation | `plan`, `principles` |
| 1 | Strategic Context | `stakeholders` |
| 1.5 | Risk Assessment | `risk` |
| 2 | Business Justification | `sobc` |
| 3 | Requirements | `requirements` |
| 3.5 | Strategic Planning | `platform-design`, `strategy` |
| 4 | Detailed Design | `data-model`, `dpia`, `research`, `wardley`, `roadmap`, `diagram`, `adr`, `datascout`, `data-mesh-contract` |
| 5 | Procurement | `sow`, `dos`, `gcloud-search`, `gcloud-clarify`, `evaluate` |
| 6 | Design Reviews | `hld-review`, `dld-review` |
| 7–8 | Implementation & Operations | `backlog`, `trello`, `servicenow`, `devops`, `mlops`, `finops`, `operationalize` |
| 9–10 | Quality & Compliance | `traceability`, `analyze`, `principles-compliance`, `service-assessment`, `tcop`, `ai-playbook`, `atrs`, `secure`, `mod-secure`, `jsp-936` |
| 11–12 | Reporting & Publishing | `story`, `pages` |

The most-consumed artifacts are `requirements` (37 commands), `principles` (21 commands), and `stakeholders` (22 commands).

### Key Conventions

- **Document IDs**: Format `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md` (e.g., `ARC-001-REQ-v1.0.md`). Multi-instance types use `ARC-{PID}-{TYPE}-{NUM}-v{VERSION}.md`. Generate with `.arckit/scripts/bash/generate-document-id.sh`.
- **Type codes**: PRIN, STKE, REQ, RISK, SOBC, STRAT, PLAT, DATA, DPIA, RSCH, SOW, EVAL, TRAC, ANLZ, BKLG, SRVN, DVOP, MLOP, FNOP, OPER, RDMP, TCOP, AIPL, ATRS, SECD, MSBD, JSP9, SVCA, STRY. Multi-instance: ADR, DIAG, WARD, DMC.
- **Global artifacts** (principles) go in `projects/000-global/`
- **Project-specific artifacts** go in `projects/{PROJECT_ID}/` with subdirectories: `decisions/`, `diagrams/`, `wardley-maps/`, `data-contracts/`, `reviews/`, `external/`, `vendors/`, `final/`
- **Templates**: Default templates in `.arckit/templates/`. Custom overrides in `.arckit/templates-custom/` (checked first, preserved across updates). Always read the relevant template before generating a document.
- **Version** is in the `VERSION` file (currently 1.5.0) — include in generated document metadata
- **External documents**: Commands auto-discover user-provided files (vendor HLDs, policy docs, pen test reports) from `projects/{project}/external/`, `projects/{project}/vendors/{vendor}/`, and `projects/000-global/policies/`. These enhance output but are never required.

### Autonomous Agents

Research-heavy commands (`/arckit.research`, `/arckit.datascout`, `/arckit.aws-research`, `/arckit.azure-research`) delegate to autonomous agents that run in isolated context windows via the Task tool. These are defined in `.claude/agents/`.

### MCP Integration

The project has an AWS Knowledge MCP server configured (`.mcp.json`) for AWS service research via `/arckit.aws-research`.

### Generated Artifacts (This Project)

The following artifacts exist for project 001 (Criminal Courts Technology & AI Reform):
- `ARC-001-PRIN-v1.0.md` — Architecture principles (also at `ARC-000-PRIN-v1.0.md` globally)
- `ARC-001-STKE-v1.0.md` — Stakeholder analysis
- `ARC-001-RISK-v1.0.md` — Risk register
- `ARC-001-SOBC-v1.0.md` — Strategic Outline Business Case
- `ARC-001-REQ-v1.0.md` — Requirements
- `ARC-001-PLAT-v1.0.md` — Platform design
- `ARC-001-SOW-v1.0.md` — Statement of Work
- `ARC-001-STRAT-v1.0.md` — Architecture Strategy
- `ARC-001-STRY-v1.0.md` / `v1.1.md` — Project Story
- `ARC-001-ANLZ-v1.0.md` — Analysis Report

Remaining phases (data model, DPIA, design reviews, procurement, compliance, operations) have not yet been generated.

## Project Context

The criminal justice system in England and Wales faces a crisis: 77,000+ outstanding Crown Court cases, fragmented digital systems across police/CPS/courts/probation/prisons, and troubled Common Platform rollout. The Leveson Review's 180 recommendations include AI for case preparation and disclosure, AI translation, legacy system migration (37 critical applications), and cross-agency integration.

### Compliance Context

UK Government civilian department. Applicable frameworks: GDS Service Standard, Technology Code of Practice (TCoP), NCSC Cyber Assessment Framework, ATRS for AI tools, UK GDPR (criminal justice data is special category), HM Treasury Green Book, AI Playbook.

### Key Stakeholders

MoJ (policy owner), HMCTS (operational delivery), CPS (prosecution technology), Legal Aid Agency, police forces, judiciary, Criminal Bar, Magistrates' Association, victims/witnesses, defendants.

## Key References

- [Independent Review of the Criminal Courts - GOV.UK](https://www.gov.uk/guidance/independent-review-of-the-criminal-courts)
- [Part 1 Report (July 2025)](https://www.gov.uk/government/publications/independent-review-of-the-criminal-courts-part-1)
- [Part 2 Report (February 2026)](https://www.gov.uk/government/publications/independent-review-of-the-criminal-courts-part-2)

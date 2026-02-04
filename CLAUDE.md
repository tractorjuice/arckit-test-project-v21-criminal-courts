# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **ArcKit architecture governance project** — not a software codebase. It generates architecture documents (markdown) for the Criminal Courts Technology & AI Reform programme, based on the Independent Review of the Criminal Courts (Leveson Review, 2025-2026).

There is no build system, test suite, or application code. All work is done through ArcKit slash commands that generate governance artifacts.

## How to Work in This Repository

### ArcKit Slash Commands

All artifacts are produced via `/arckit.*` commands. The recommended execution order follows the dependency matrix in `DEPENDENCY-MATRIX.md`:

1. `/arckit.principles` — Architecture principles (foundation for everything)
2. `/arckit.stakeholders` — Stakeholder analysis
3. `/arckit.requirements` — Business and technical requirements
4. `/arckit.risk` — Risk register
5. Further commands depend on outputs from the above (see `DEPENDENCY-MATRIX.md` for M/R/O dependencies)

### Key Conventions

- **Document IDs**: All artifacts use the format `ARC-{PROJECT_ID}-{TYPE}-v{VERSION}.md` (e.g., `ARC-000-PRIN-v1.0.md`). Generate IDs using `.arckit/scripts/bash/generate-document-id.sh`.
- **Global artifacts** (principles, etc.) go in `projects/000-global/`
- **Project-specific artifacts** go in `projects/{PROJECT_ID}/`
- **Templates** are in `.arckit/templates/` — always read the relevant template before generating a document
- **Version** is in the `VERSION` file (currently 1.3.0) — include in generated document metadata
- **External reference documents** (e.g., the Leveson Review PDF) are in `projects/000-global/external/`
- **Policies** for import go in `projects/000-global/policies/`

### MCP Integration

The project has an AWS Knowledge MCP server configured (`.mcp.json`) for AWS service research via `/arckit.aws-research`.

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

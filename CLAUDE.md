# CLAUDE.md - Criminal Courts Technology Review

## Project Context

This project uses the **Independent Review of the Criminal Courts** (the Leveson Review, 2025-2026) as the basis for an architecture governance exercise. The review, chaired by Sir Brian Leveson, was commissioned by the Lord Chancellor to examine how criminal courts in England and Wales could be reformed and made more efficient.

### The Problem

The criminal justice system faces a crisis:
- **77,000+ outstanding cases** in the Crown Court (nearly doubled in five years)
- Some trials listed for **2029** due to backlog
- The system is **fragmented** - police, CPS, courts, probation, and prisons operate with separate budgets, distinct accountability, and differing priorities
- The **Common Platform** digital case management system rollout was troubled - 231 critical incidents, 3,011 missed notifications, and ~$22.5M in waste
- Many magistrates lack **basic IT provision** (e.g., working laptops)
- **37 critical court applications** need migrating from outdated, vulnerable data centres
- Legacy systems (Libra Web, Court Store, Xhibit) need replacement

### Technology & AI Recommendations (from the Review)

The review's 180 recommendations (Part 2) include significant technology elements:
- **AI for case preparation and disclosure** - summarising prosecution case details
- **AI translation** of court proceedings for defendants and witnesses
- **AI to enhance CPS decision-making**
- **AI for operational efficiency** across police, CPS, courts, probation, and prisons
- Continued development of **Common Platform** as central hub for all magistrate and Crown Court cases
- **Opal** - new system to replace outdated criminal fines management
- Integration improvements between Common Platform and **Police National Computer**
- Migration of 37 applications to **modern, secure platforms**

### Key Stakeholders

- **Ministry of Justice (MoJ)** - policy owner
- **HM Courts & Tribunals Service (HMCTS)** - operational delivery
- **Crown Prosecution Service (CPS)** - prosecution technology
- **Legal Aid Agency** - legal aid systems
- **Police forces** - evidence and case file systems
- **Judiciary** - judicial decision support
- **Criminal Bar** - professional users
- **Magistrates' Association** - magistrate technology
- **Victims and witnesses** - end users of the justice system
- **Defendants** - rights and access

### Compliance Context

- **UK Government** civilian department context (not MOD)
- **GDS Service Standard** applies to public-facing digital services
- **Technology Code of Practice (TCoP)** applies
- **NCSC Cyber Assessment Framework** for security
- **Algorithmic Transparency Recording Standard (ATRS)** for AI tools
- **UK GDPR / Data Protection Act 2018** - criminal justice data is special category
- **HM Treasury Green Book** for business case justification
- **AI Playbook** for responsible AI deployment in government

## ArcKit Commands

This project is managed using ArcKit slash commands. Run `/arckit.principles` first, then `/arckit.requirements` for the specific project.

## Key References

- [Independent Review of the Criminal Courts - GOV.UK](https://www.gov.uk/guidance/independent-review-of-the-criminal-courts)
- [Part 1 Report (July 2025)](https://www.gov.uk/government/publications/independent-review-of-the-criminal-courts-part-1)
- [Part 2 Report (February 2026)](https://www.gov.uk/government/publications/independent-review-of-the-criminal-courts-part-2)
- [HMCTS Digital Services Blog](https://insidehmcts.blog.gov.uk/category/digital-services/)
- [Common Platform Case Study](https://www.gov.uk/government/case-studies/common-platform-a-modern-digital-case-management-system-for-the-criminal-justice-system)

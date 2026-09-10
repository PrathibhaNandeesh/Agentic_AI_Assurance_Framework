# Agentic AI Assurance Framework

**A domain-agnostic risk assessment & conformity methodology for autonomous AI agents — built as a reusable GRC framework, demonstrated once on a worked example, and ready to apply to any agent in any industry.**

No code required to use or extend this project — every deliverable is a governance document a real AI risk/assurance function would produce: a methodology, a risk classification, a manual test matrix, a risk register, and an EU AI Act conformity gap assessment.

## Why This Project

Most AI governance portfolios either stop at a policy summary (no technical depth) or are hard-coded to one industry (a single chatbot, one hiring tool). This project does neither: it defines one reusable assurance **methodology** — grounded in MITRE ATLAS, the OWASP Top 10 for LLM Applications, NIST AI RMF, ISO/IEC 42001, and the EU AI Act — and demonstrates it end-to-end on a horizontal, industry-agnostic example, with a guide showing exactly how to re-apply it to any new agent, in any domain.

## What's Inside

| File | What it is |
|---|---|
| `docs/01_Agentic_AI_Assurance_Framework.docx` | **The core methodology.** Risk classification criteria, the standard agentic-AI threat taxonomy (ATLAS + OWASP-mapped), the control library (NIST AI RMF + ISO 42001 + EU AI Act), risk-scoring approach, and conformity assessment structure. |
| `docs/02_How_to_Apply_This_Framework.docx` | A step-by-step checklist for applying the framework to a new agent in a new domain, with a table of domain-specific additions (HR, finance, healthcare, customer-facing). |
| `docs/03_Executive_Summary.docx` | A one-page, board-ready summary of the worked example's findings and business impact. |
| `worksheets/Agentic_AI_Assurance_Worked_Example.xlsx` | The framework applied once, in full, to a generic internal enterprise AI agent — 4 tabs: Risk Classification, Threat & Test Case Matrix (6 manual adversarial tests with evidence), Risk Register (scored, framework-mapped), and EU AI Act Conformity Gap Assessment. |

## Worked Example Snapshot

**Target:** a generic internal enterprise AI agent (knowledge retrieval, notification, task-creation, data-lookup) — chosen because that capability profile is common across almost every industry, not specific to any one of them.

- 6 manual adversarial test cases executed through the agent's normal interface — no code, no APIs, just structured probing (see methodology in `docs/02`).
- **6 / 6 confirmed vulnerable**, spanning prompt injection, excessive agency, broken authorization, data exfiltration, insecure output handling, and unredacted PII in logs.
- Every finding mapped simultaneously to a MITRE ATLAS technique, an OWASP LLM Top 10 category, a NIST AI RMF subcategory, an ISO/IEC 42001 Annex A control, and (where applicable) an EU AI Act article — so one assessment can support an engineering fix, a certification audit, and a regulatory conformity file without being redone three times.
- Full EU AI Act conformity gap assessment across Articles 9, 10, 12, 13, 14 and Annex IV.

## Interactive Risk Dashboard

A live, filterable view of the risk register and EU AI Act gap assessment, built directly from the worksheet data in `worksheets/`.

- **Risk Register** — filter findings by rating (Critical/High/Medium/Low) and status, with a live severity breakdown chart
- **EU AI Act Gaps** — Met / Partially Met / Not Met status per article, with linked findings and remediation owner
- **Risk Classification** and **Threat & Test Matrix** rendered as structured, readable views of Tabs 1 and 2

No backend, no build step — a single HTML file.

**[Live demo →](https://prathibhanandeesh.github.io/Agentic_AI_Assurance_Framework/)** · source: `index.html`

![Risk Dashboard preview](assets/screenshot_6_dashboard.jpg)

## Preview

**Threat & Test Case Matrix** — six manual adversarial tests, each mapped to a MITRE ATLAS technique and OWASP LLM Top 10 category, with a pre-defined pass/fail condition and captured evidence:

![Threat & Test Case Matrix](assets/screenshot_3_threat_test_matrix.jpg)

**Risk Register** — findings scored and mapped to NIST AI RMF and ISO/IEC 42001:

![Risk Register](assets/screenshot_4_risk_register.jpg)

**EU AI Act Conformity Gap Assessment** — status against Articles 9, 10, 12, 13, 14 and Annex IV:

![EU AI Act Conformity Gap Assessment](assets/screenshot_5_eu_ai_act_gap_assessment.jpg)

**Risk Classification** — EU AI Act tier and NIST AI RMF context profile with documented rationale:

![Risk Classification](assets/screenshot_2_risk_classification.jpg)

## How to Read This Project

- **Hiring manager, 30 seconds:** open the [live dashboard](https://prathibhanandeesh.github.io/Agentic_AI_Assurance_Framework/) — Risk Register tab
- **Hiring manager, 2 minutes:** `docs/03_Executive_Summary.docx`
- **GRC / governance reviewer:** `docs/01_Agentic_AI_Assurance_Framework.docx` → `worksheets/...xlsx` (all 4 tabs in order) → `index.html` (interactive view of the same data) → `docs/02_How_to_Apply_This_Framework.docx`
- **Anyone assessing a different agent:** start directly at `docs/02_How_to_Apply_This_Framework.docx`

## Frameworks Referenced

- MITRE ATLAS — adversarial tactics/techniques for AI systems
- OWASP Top 10 for LLM Applications (2025)
- NIST AI Risk Management Framework 1.0 (Govern / Map / Measure / Manage)
- ISO/IEC 42001:2023 — AI Management System, Annex A controls
- EU AI Act — Articles 9, 10, 12, 13, 14; Annex III (risk classification); Annex IV (technical documentation)

## Methodology Note

The worked-example agent is a generic, hypothetical internal system, described (not coded) in enough technical detail — capabilities, tool access, data flows — to support realistic manual testing and evidence capture. This keeps the project reproducible and domain-neutral while preserving full technical accuracy in how each finding is described and mapped. Test cases are written so they can be run against a real deployed agent, through its normal chat/UI, with no engineering access required — see `docs/02` for the reusable checklist.

## Author's Background

Built to demonstrate applied capability alongside formal credentials in AI governance and risk: AIGP, Microsoft AI-102 (Azure AI Engineer), ISO/IEC 42001 Lead Implementer, and working familiarity with NIST AI RMF, MITRE ATLAS, OWASP LLM Top 10, and AI red-teaming practices.

## License

MIT — see `LICENSE`.

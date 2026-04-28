# Enterprise AI Governance Controls

A practical GRC framework for auditing, controlling, and monitoring AI tool deployments in enterprise environments. Vendor-neutral. Built from real-world implementation experience.

Mapped to the [NIST AI Risk Management Framework (AI RMF 1.0)](https://airc.nist.gov/Home).

---

## Who This Is For

- GRC analysts responsible for AI risk assessments
- IT security teams managing shadow AI
- Compliance officers building AI governance programs
- Organizations without a formal AI governance posture yet

---

## The Problem

Most organizations discover AI tool usage after the fact. Employees install browser extensions, desktop agents, and CLI tools without IT or security awareness. By the time governance catches up, sensitive data has already touched unauthorized systems.

This repo provides a practical control framework to detect, assess, and manage AI tool deployments across the enterprise — before risk becomes incident.

---

## Repository Structure

```
ai-governance-controls/
├── README.md                          # This file
├── 01-inventory/
│   └── ai-tool-inventory-framework.md # How to build a shadow AI inventory
├── 02-control-matrix/
│   └── control-matrix-by-tool-type.md # Controls by deployment type
├── 03-vendor-assessment/
│   └── vendor-control-gap-analysis.md # What vendors should provide vs. what they do
├── 04-compensating-controls/
│   ├── kace-npm-scan.md               # Detecting npm-installed AI agents
│   ├── mdm-browser-extension-policy.md# Browser extension controls
│   └── cron-detection-template.sh     # Nightly scan template
├── 05-nist-ai-rmf-mapping/
│   └── control-to-rmf-mapping.md      # Maps every control to NIST AI RMF
└── 06-templates/
    ├── shadow-ai-survey.md            # Employee survey template
    ├── risk-acceptance-template.md    # Risk exception documentation
    └── vendor-risk-questionnaire.md   # AI vendor assessment questions
```

---

## Quick Start

**Step 1 — Inventory first.** You cannot govern what you cannot see. Start with the [AI Tool Inventory Framework](01-inventory/ai-tool-inventory-framework.md).

**Step 2 — Classify by deployment type.** Web-based tools carry different risk than locally installed agents. Use the [Control Matrix](02-control-matrix/control-matrix-by-tool-type.md) to assess each category.

**Step 3 — Identify vendor gaps.** Most AI vendors do not provide enterprise-grade administrative controls. The [Vendor Control Gap Analysis](03-vendor-assessment/vendor-control-gap-analysis.md) documents what to look for and what compensating controls to build when vendor controls are insufficient.

**Step 4 — Implement compensating controls.** Use the scripts and templates in [04-compensating-controls](04-compensating-controls/) to detect unauthorized AI tool installations via MDM, KACE, or scheduled scans.

**Step 5 — Map to NIST AI RMF.** The [control mapping](05-nist-ai-rmf-mapping/control-to-rmf-mapping.md) ties every control in this repo to the relevant AI RMF function and subcategory for audit and reporting purposes.

---

## NIST AI RMF Alignment

This framework aligns to the following AI RMF functions and subcategories:

| Function | Subcategory | Description |
|----------|-------------|-------------|
| GOVERN | 1.1 | Policies and processes for AI risk management |
| GOVERN | 1.2 | Organizational roles and responsibilities for AI |
| GOVERN | 1.6 | AI system inventories and documentation |
| GOVERN | 6.1 | Third-party AI risk policies |
| MAP | 1.1 | Context establishment for AI systems in use |
| MAP | 5.1 | Likelihood and impact of AI risks identified |
| MANAGE | 3.1 | Risk treatment for third-party AI systems |
| MANAGE | 4.1 | Incident response for AI-related events |

---

## License

MIT — use freely, adapt for your organization, attribution appreciated but not required.

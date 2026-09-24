# Project 1: AI System Inventory & Classification Engine

## Scenario

**Organisation:** OrbitTel Communications — a fictional telecommunications company operating across mobile, fiber broadband, customer operations, network operations, and enterprise services.

**Problem:** OrbitTel has deployed AI systems across multiple business functions without a centralized AI governance inventory. Different teams maintain system information independently, making it difficult to establish ownership, understand intended purposes, classify regulatory exposure, and identify governance gaps.

**Objective:** Produce a structured AI system inventory, apply EU AI Act risk classification to each identified system, and map each system to the NIST AI RMF to identify governance gaps and maturity levels.

---

## What This Project Demonstrates

- Understanding of proportionality — not all AI systems carry the same governance obligations
- Ability to apply risk-based regulatory classification to realistic telecommunications AI use cases
- Practical application of the NIST AI RMF's four functions as an operational governance lens
- Ability to distinguish regulatory classification from overall AI governance maturity
- Ability to structure governance information in a format usable by risk, compliance, legal, and technical teams
- Ability to identify governance gaps and define priority remediation actions

---

## Artefacts

| File | Description |
|---|---|
| `ai-system-inventory.csv` | Structured inventory of OrbitTel's AI systems |
| `eu-ai-act-classification.md` | Classification rationale and governance assessment for each system |
| `nist-rmf-mapping.md` | Mapping of each system to NIST AI RMF functions, maturity, and governance gaps |

---

## Key Decisions & Rationale

### Why a CSV for the inventory?

A structured inventory makes AI governance information queryable, sortable, maintainable, and suitable for migration into a future GRC or AI governance platform.

The CSV represents the initial system-of-record structure for OrbitTel's AI inventory.

### Why classify before full risk assessment?

Classification is a triage step.

It helps determine the level of regulatory and governance due diligence required for each AI system before proceeding to deeper risk assessment and control design.

A higher-risk classification can trigger additional governance requirements and deeper assessment.

### Why separate regulatory classification from NIST maturity?

Regulatory classification and governance maturity measure different dimensions.

An AI system may have limited regulatory exposure while still having significant governance weaknesses.

Conversely, a potentially high-risk system may have stronger existing governance practices.

Keeping these dimensions separate provides a more useful governance view.

### Why use a fictional telecommunications organisation?

OrbitTel is fictional, but the systems represent realistic telecommunications use cases including customer analytics, generative AI, network operations, fraud detection, and infrastructure planning.

The fictional setting allows the governance methodology to be demonstrated without presenting simulated organisational data as real company records.

---

## Governance Workflow

The project follows this governance sequence:

**Inventory → Classification → NIST RMF Mapping → Risk Assessment**

The current project stops at the governance baseline.

Detailed risk scoring, control selection, residual risk assessment, and governance decisions are addressed in subsequent projects.

---

## Frameworks Applied

- **EU AI Act** — risk classification and applicable regulatory obligations
- **NIST AI RMF** — Govern, Map, Measure, Manage functions
- **ISO/IEC 42001** — AI management system concepts referenced where relevant in governance gaps

---

## Key Governance Questions

- What AI systems exist across the organisation?
- Who owns each system?
- What is each system intended to do?
- Who is affected by its outputs?
- What regulatory classification may apply?
- What governance maturity exists today?
- What gaps require remediation?
- What level of further assessment is required?

---

## Case Study Note

OrbitTel Communications and all associated system data are fictional and created for portfolio demonstration purposes.

The governance methodology, regulatory references, and AI use cases are designed to reflect realistic enterprise AI governance practices.

Regulatory classifications represent an initial governance assessment and should not be interpreted as legal advice.

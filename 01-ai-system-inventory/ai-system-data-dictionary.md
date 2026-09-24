# AI System Inventory — Data Dictionary

## Purpose

This document defines the fields, expected meaning, and controlled values used in the OrbitTel Communications AI System Inventory.

The inventory is intended to provide a consistent system-of-record for identifying, describing, classifying, and reviewing AI systems.

Risk scoring, control assessment, residual risk, and governance decisions are maintained separately in the AI Risk Assessment process.

---

## Inventory Fields

| Field | Definition | Expected Format / Values |
|---|---|---|
| `system_id` | Unique identifier assigned to the AI system | `System-001` |
| `system_name` | Official or working name of the AI system | Free text |
| `description` | Concise description of what the system does | Free text |
| `business_unit` | Business function responsible for the use case | Controlled business unit name |
| `primary_purpose` | Main business purpose for which the AI system is used | Free text |
| `data_inputs` | Main categories of data consumed by the system | Free text |
| `outputs` | Main outputs produced by the system | Free text |
| `deployment_status` | Current lifecycle/deployment state | Development / Pilot / Production / Retired |
| `system_owner` | Business owner accountable for the system | Named role |
| `vendor_or_internal` | Source or operating model of the AI system | Internal / Vendor / Hybrid |
| `go_live_date` | Date the system entered its current operational deployment or pilot | `YYYY-MM-DD` |
| `last_review_date` | Date of the most recent documented governance or system review | `YYYY-MM-DD` / N/A |
| `review_cycle` | Planned frequency for governance or system review | 3 months / 6 months / 12 months / N/A |
| `affected_persons` | Groups potentially affected by system outputs or use | Customers / Employees / Other |
| `geographic_scope` | Geographic area in which the system is deployed or used | Country / Region |
| `ai_type` | Primary AI technique or system category | Predictive ML / Generative AI / NLP / Computer Vision / Agentic AI / Other |
| `eu_ai_act_risk_tier` | Initial classification under the EU AI Act based on documented intended purpose | High-Risk / Limited or Transparency Risk / Not identified as High-Risk / To Be Determined |
| `nist_rmf_maturity_level` | Initial assessment of the maturity of governance practices surrounding the system | 1–4 |
| `notes` | Important governance, classification, lifecycle, or contextual information | Free text |

---

## NIST RMF Maturity Scale

### Level 1 — Initial

Governance practices are largely informal, undocumented, or inconsistent.

### Level 2 — Developing

Basic ownership and governance activities exist, but documentation, evidence, and repeatability are incomplete.

### Level 3 — Defined

Governance processes are documented, assigned, and consistently applied, with supporting evidence.

### Level 4 — Managed and Measured

Governance processes are continuously monitored, measured, reviewed, and improved using evidence and defined metrics.

---

## Data Quality Rules

1. Every production or pilot AI system must have a unique `system_id`.
2. Every active system must have a named `system_owner`.
3. `deployment_status` must reflect the system's current lifecycle state.
4. `last_review_date` must only be populated when a documented review has actually occurred.
5. `review_cycle` should reflect the approved governance review frequency.
6. Regulatory classification must be based on the documented intended purpose and deployment context.
7. NIST maturity represents governance maturity, not the system's inherent risk level.
8. Risk score, controls, residual risk, and governance decisions must not be recorded in this inventory.
9. Where information is unavailable, `N/A` or `To Be Determined` should be used rather than inferred.
10. Changes to intended purpose, affected persons, geographic scope, deployment status, or decision-making role should trigger an inventory review.

---

## Relationship to Other Governance Artifacts

The inventory is the starting point for the broader AI governance lifecycle:

**AI System Inventory**
→ **Regulatory Classification**
→ **NIST Governance Assessment**
→ **AI Risk Assessment**
→ **Controls & Remediation**
→ **Residual Risk & Governance Decision**
→ **Ongoing Monitoring**

# Project 2: AI Risk Assessment & Governance Review Pack

## Scenario Overview
- **System Under Review:** Fiber Network Fault Prediction Engine (`OT-AI-003`)
- **Organization:** OrbitTel Telecom
- **Use Case:** AI-assisted network fault prediction and automated infrastructure maintenance recommendation
- **Regulatory Context:** Following the enterprise-wide registry and classification exercise in **Project 1**, `OT-AI-003` was identified as a **High-Risk AI System** under Annex III (Category 2 — Critical Infrastructure Management) of the EU AI Act due to active autonomous remediation features operating on core network nodes without a formal conformity assessment.

The Chief Technology Officer (CTO) and Head of Network Operations requested a formal governance review to assess system-level operational hazards, quantify regulatory liability, and present actionable deployment recommendations to the **Board Risk & Audit Committee**.

---

## Key Governance Deliverables & Artefacts

| Artefact / File | Description | Primary Target Audience |
| :--- | :--- | :--- |
| **`risk-assessment.md`** | Comprehensive risk analysis evaluating harms, $5 \times 5$ Likelihood/Impact matrices, control mitigations, and residual risk scoring across 5 core risk domains. | Technical Risk Officers, Data Protection Officers (DPO), and AI Auditors. |
| **`governance-review-memo.md`** | Executive board memo translating technical risk findings into business outcomes, legal exposures, and actionable deployment options (**Option A vs Option B**). | CEO, CTO, and Board Risk & Audit Committee. |

---

## How the Artefacts Connect

```
┌────────────────────────────────┐
│   Project 1 Classification     │
│ (High-Risk under EU AI Act)   │
└───────────────┬────────────────┘
                │
                ▼
┌────────────────────────────────┐
│    risk-assessment.md          │ ◄── Identifies hazards, tests controls &
│  (Technical Risk Analysis)     │     calculates Residual Risk (Critical ➔ Medium)
└───────────────┬────────────────┘
                │
                ▼
┌────────────────────────────────┐
│  governance-review-memo.md     │ ◄── Translates technical findings into Board decision
│   (Executive Decision Pack)    │     options & Article 6(3) De-scoping strategy
└────────────────────────────────┘
```

1. **The Risk Assessment (`risk-assessment.md`)** serves as the analytical foundation. It identifies specific failure modes (e.g., false-positive isolation, black-box diagnostic opacity, automation bias), evaluates them on a standardized scale, applies technical/operational controls, and computes the residual risk position.
2. **The Governance Review Memo (`governance-review-memo.md`)** bridges technical analysis and executive decision-making. It outlines business implications, regulatory penalties under the EU AI Act, and presents a clear decision request with a 90-day remediation timeline.

---

## Strategic Governance Highlight: Article 6(3) De-scoping Strategy

A key strategic insight demonstrated in this project is the **Regulatory Scope & Triage Strategy**:
- While `OT-AI-003` is initially flagged as High-Risk due to autonomous remediation on critical telecom infrastructure, enforcing a mandatory **Human-in-the-Loop (HITL)** decision gate converts the system into a **Decision Support Tool** under **Article 6(3)** of the EU AI Act.
- This governance action effectively mitigates the primary harm (unintended autonomous network outages) and opens a clear pathway for **regulatory de-scoping** to *Minimal Risk*, saving OrbitTel substantial conformity assessment and legal compliance overhead.

---

## Frameworks & Standards Applied

- **EU AI Act:** Article 9 (Risk Management System), Article 10 (Data Governance), Article 14 (Human Oversight), Article 13 (Transparency), and Article 6(3) (Risk Triage Filter).
- **NIST AI RMF:** **Map** (contextualizing risks to critical infrastructure) and **Measure** (quantitative likelihood/impact scoring) functions.
- **ISO 31000 / ISO/IEC 42001:** Standardized risk assessment methodologies, terminology, and governance control structures.

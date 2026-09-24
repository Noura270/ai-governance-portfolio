# NIST AI RMF Mapping — OrbitTel Communications

**Framework:** NIST AI Risk Management Framework (AI RMF 1.0)
**Mapping Date:** September 2026

---

## Purpose

This document maps OrbitTel's AI systems against the four core functions of the NIST AI RMF:

* GOVERN
* MAP
* MEASURE
* MANAGE

The objective is to identify current governance maturity, material gaps, and priority actions.

---

## Maturity Scale

| Level | Description                                                             |
| ----- | ----------------------------------------------------------------------- |
| 1     | Initial — practices are largely ad hoc or absent                        |
| 2     | Developing — some practices exist but are inconsistent                  |
| 3     | Defined — documented and repeatable practices exist                     |
| 4     | Managed / Optimised — practices are monitored and continuously improved |

---

# OT-AI-001 — Customer Churn Prediction

| Function | Current State                                                       | Gap                                                            | Maturity |
| -------- | ------------------------------------------------------------------- | -------------------------------------------------------------- | -------: |
| GOVERN   | Named business owner and operational accountability exist.          | No formal AI governance approval record.                       |        2 |
| MAP      | Purpose, customers, data inputs and retention use are documented.   | Decision boundary requires formal documentation.               |        2 |
| MEASURE  | Prediction performance can be evaluated against retention outcomes. | Formal fairness and performance thresholds are not documented. |        2 |
| MANAGE   | Business team controls retention actions.                           | No formal AI-specific drift or incident escalation process.    |        2 |

**Overall Maturity:** 2 — Developing

**Priority Actions:**

* Document decision boundaries.
* Establish model performance thresholds.
* Establish fairness monitoring.
* Define AI incident escalation.

---

# OT-AI-002 — Customer Service GenAI Assistant

| Function | Current State                                                                               | Gap                                                                    | Maturity |
| -------- | ------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | -------: |
| GOVERN   | Business owner and vendor relationship are established. Human agents retain responsibility. | AI-specific vendor governance and accountability should be formalised. |        3 |
| MAP      | Purpose, users, data sources and human review are understood.                               | Direct customer interaction boundary requires explicit documentation.  |        3 |
| MEASURE  | Agent feedback and response review provide some quality information.                        | No formal hallucination, accuracy or quality thresholds.               |        2 |
| MANAGE   | Agents review generated responses before customer communication.                            | AI incident and escalation process is not formalised.                  |        2 |

**Overall Maturity:** 2.5 — Developing

**Priority Actions:**

* Define AI quality metrics.
* Establish hallucination evaluation.
* Formalise human review.
* Define vendor AI governance requirements.
* Assess Article 50 before direct customer interaction.

---

# OT-AI-003 — Fiber Network Fault Prediction

| Function | Current State                                                                            | Gap                                                                                           | Maturity |
| -------- | ---------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | -------: |
| GOVERN   | Clear system owner and operational accountability exist.                                 | High-risk governance decision rights and formal approval structure are not yet established.   |        3 |
| MAP      | Purpose, infrastructure context, affected services and failure scenarios are documented. | Critical-infrastructure scope and safety-component status require formal confirmation.        |        3 |
| MEASURE  | Historical network data supports performance evaluation.                                 | Formal safety thresholds, accuracy thresholds and validation evidence are incomplete.         |        2 |
| MANAGE   | Human review is required before network intervention.                                    | Formal high-risk incident, monitoring and degradation response processes are not established. |        2 |

**Overall Maturity:** 2.5 — Developing

**Priority Actions:**

* Complete Annex III scope assessment.
* Define safety and performance thresholds.
* Establish high-risk governance approval.
* Formalise monitoring and incident management.
* Establish documented human-oversight controls.

---

# OT-AI-004 — Telecom Fraud Detection

| Function | Current State                                                                             | Gap                                                                           | Maturity |
| -------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | -------: |
| GOVERN   | Business owner and human investigation responsibility exist.                              | AI accountability and customer-impact governance are not formally documented. |        2 |
| MAP      | Fraud purpose, affected customers, data inputs and investigation workflow are understood. | Fairness and customer-impact scenarios require formal documentation.          |        2 |
| MEASURE  | False positives, false negatives and detection performance can be measured.               | No formal fairness evaluation or documented acceptance thresholds.            |        2 |
| MANAGE   | Human investigators review cases before consequential action.                             | AI incident, appeal and escalation processes are not formalised.              |        2 |

**Overall Maturity:** 2 — Developing

**Priority Actions:**

* Define human decision boundaries.
* Establish performance thresholds.
* Conduct fairness assessment.
* Define customer-impact escalation.
* Document evidence requirements.

---

# OT-AI-005 — Network Capacity Forecasting

| Function | Current State                                      | Gap                                                                    | Maturity |
| -------- | -------------------------------------------------- | ---------------------------------------------------------------------- | -------: |
| GOVERN   | Pilot owner is identified.                         | No formal production governance gate.                                  |        2 |
| MAP      | Purpose, data and planning context are documented. | Pilot failure scenarios and production impact require further mapping. |        2 |
| MEASURE  | Forecast performance can be assessed during pilot. | Formal validation and production thresholds are absent.                |        1 |
| MANAGE   | Human planners review outputs.                     | No formal production monitoring or degradation response process.       |        1 |

**Overall Maturity:** 1.5 — Initial / Developing

**Priority Actions:**

* Define pilot exit criteria.
* Establish validation thresholds.
* Define production monitoring.
* Establish model degradation response.
* Require governance approval before production deployment.

---

# Cross-System Findings

## GOVERN

Business ownership exists across the inventory, but formal AI governance decision rights are not consistently established.

## MAP

System purposes and operational contexts are generally understood, but formal documentation of decision boundaries and affected-party impacts is inconsistent.

## MEASURE

The largest recurring gap is the lack of formal AI-specific performance, fairness, validation, and monitoring evidence.

## MANAGE

Human review exists in several systems, but escalation, incident management, and model-drift processes need to become repeatable governance practices.

---

# Priority Governance Actions

1. Establish a common AI governance accountability model.
2. Define minimum AI system documentation requirements.
3. Formalise human-oversight and decision boundaries.
4. Establish AI performance and monitoring thresholds.
5. Create an AI incident and escalation framework.
6. Introduce governance gates for material changes and production deployment.
7. Complete formal scope assessment for OT-AI-003.
8. Maintain the inventory and classification as living governance records.

---

## Conclusion

The NIST AI RMF mapping demonstrates that regulatory classification and governance maturity are separate dimensions.

A system may have a lower regulatory classification while still requiring significant governance controls, while a potentially high-risk system may require substantially stronger governance evidence before deployment.

The mapping therefore provides the governance baseline for subsequent risk assessment, control design, and governance decision-making.

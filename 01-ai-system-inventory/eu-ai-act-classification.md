# EU AI Act Risk Classification — OrbitTel Communications

**Classification Date:** September 2026
**Prepared by:** AI Governance Programme Office
**Review Due:** March 2027

---

## Classification Framework

This assessment applies the EU AI Act risk-based classification approach to the AI systems recorded in the OrbitTel AI System Inventory.

Classification is based on the system's intended purpose, deployment context, affected persons, and role in the relevant business process.

This document is an AI governance case-study assessment and is not legal advice.

## Risk Categories Used

| Classification           | Governance Treatment                                                                                                                |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| High Risk                | Additional requirements apply where the system falls within the applicable high-risk categories                                     |
| Transparency Obligations | Specific transparency requirements may apply, including Article 50                                                                  |
| Minimal / Other Risk     | No high-risk classification identified from the documented intended purpose; other legal and governance obligations may still apply |

---

# 1. OT-AI-001 — Customer Churn Prediction

**Classification:** MINIMAL / NOT IDENTIFIED AS HIGH-RISK

### Legal Basis

The documented purpose is customer retention prioritisation.

The system does not currently determine customer eligibility, terminate services, or make another consequential decision falling within an identified high-risk category.

### Rationale

The system predicts the probability that a customer may leave OrbitTel and prioritises customers for possible retention activity.

The use of customer data does not by itself establish high-risk classification.

The classification must be reassessed if the system becomes part of an automated decision process that materially affects customers.

### Governance Considerations

* Document the decision boundary.
* Maintain appropriate data governance.
* Monitor prediction accuracy.
* Assess potential unfair treatment resulting from retention prioritisation.
* Reassess classification following material purpose changes.

### Current Compliance / Governance Gap

The system's intended purpose and prohibited decision boundaries should be formally documented.

**Priority:** Medium

---

# 2. OT-AI-002 — Customer Service GenAI Assistant

**Classification:** TRANSPARENCY OBLIGATIONS / ARTICLE 50 ASSESSMENT

### Legal Basis

Article 50(1) requires providers of AI systems intended to interact directly with natural persons to ensure that those persons are informed that they are interacting with an AI system, subject to the conditions and exceptions in the Regulation.

### Rationale

The current system assists human customer service agents.

The agent remains responsible for the final customer response.

Therefore, the current deployment is primarily an internal decision-support and content-generation tool.

If OrbitTel changes the deployment so that the AI directly communicates with customers, Article 50(1) must be assessed and implemented where applicable.

### Governance Considerations

* Human review of customer-facing responses.
* Hallucination and accuracy controls.
* Vendor governance.
* Logging and traceability.
* Customer information protection.
* Transparency assessment before direct customer interaction.

### Current Compliance / Governance Gap

The boundary between internal agent assistance and direct customer interaction is not formally documented.

**Priority:** Medium

---

# 3. OT-AI-003 — Fiber Network Fault Prediction

**Classification:** HIGH RISK — ANNEX III(2), SUBJECT TO SCOPE CONFIRMATION

### Legal Basis

Annex III includes AI systems intended to be used as safety components in the management and operation of critical digital infrastructure.

OrbitTel's case study defines this system as supporting the operation of critical digital network infrastructure.

### Rationale

The system predicts network failures and identifies network elements requiring intervention.

Because the intended purpose has been defined as supporting the management and operation of critical digital infrastructure, the system requires a formal assessment of whether it meets the Annex III(2) conditions.

The classification is therefore recorded as **High Risk — subject to scope confirmation**, rather than treating the classification as automatically established.

### Obligations / Governance Considerations

If the system is confirmed as a high-risk AI system, governance should address applicable requirements including:

* risk management;
* data and data governance;
* technical documentation;
* record keeping and logging;
* transparency and information for deployers;
* human oversight;
* accuracy, robustness and cybersecurity;
* post-market monitoring and incident management, as applicable.

### Current Compliance Gap

OrbitTel has not yet formally documented whether the network infrastructure meets the regulatory definition and whether the AI system functions as a qualifying safety component.

### Required Gate

**Formal legal and technical scope assessment before relying on the High-Risk classification for compliance planning.**

**Priority:** Critical

---

# 4. OT-AI-004 — Telecom Fraud Detection

**Classification:** MINIMAL / NOT IDENTIFIED AS HIGH-RISK

### Legal Basis

The documented purpose is fraud detection and investigation prioritisation.

The system is not operated by law-enforcement authorities and does not autonomously impose adverse action on customers.

### Rationale

The system generates fraud indicators and investigation queues.

A human investigator must review the case before consequential customer action.

The governance risk is therefore significant from an operational and customer-impact perspective, but the documented use case does not by itself establish an Annex III high-risk classification.

### Governance Considerations

* Human investigation before consequential action.
* False-positive and false-negative monitoring.
* Fairness assessment.
* Evidence preservation.
* Customer-impact escalation.
* Data protection controls.
* Vendor accountability.

### Current Compliance / Governance Gap

The human decision boundary and escalation process should be formally documented.

**Priority:** High

---

# 5. OT-AI-005 — Network Capacity Forecasting

**Classification:** MINIMAL / NOT IDENTIFIED AS HIGH-RISK

### Legal Basis

The system forecasts network capacity requirements and supports infrastructure planning.

It does not make decisions about natural persons.

### Rationale

The system is currently a pilot used to support infrastructure planning.

Its outputs are forecasts and planning scenarios rather than decisions affecting individual customers.

### Governance Considerations

* Forecast accuracy.
* Data quality.
* Scenario validation.
* Model monitoring.
* Production-readiness criteria.
* Human approval of significant planning decisions.

### Current Compliance / Governance Gap

A formal production governance gate has not yet been established.

**Priority:** High — Production Gate

---

# Classification Summary

| System                                     | Classification                               | Priority |
| ------------------------------------------ | -------------------------------------------- | -------- |
| OT-AI-001 Customer Churn Prediction        | Minimal / Not High-Risk                      | Medium   |
| OT-AI-002 Customer Service GenAI Assistant | Transparency / Article 50 Assessment         | Medium   |
| OT-AI-003 Fiber Network Fault Prediction   | High Risk — Annex III(2), Scope Confirmation | Critical |
| OT-AI-004 Telecom Fraud Detection          | Minimal / Not High-Risk                      | High     |
| OT-AI-005 Network Capacity Forecasting     | Minimal / Not High-Risk                      | High     |

---

# Reclassification Triggers

Classification must be reassessed when:

* the intended purpose changes;
* AI outputs become automated decisions;
* human oversight is materially reduced;
* the affected population changes;
* the system becomes part of critical infrastructure operations;
* a new regulated use case is introduced;
* the system begins directly interacting with natural persons;
* the deployment geography or regulatory scope changes;
* a material model or vendor change occurs.

---

## Assessment Limitation

This classification is a fictional OrbitTel case-study assessment designed to demonstrate practical AI governance methodology.

It should not be interpreted as a legal opinion.

Formal regulatory classification requires confirmation of the actual deployment context, provider/deployer status, geographic scope, system architecture, and intended purpose.

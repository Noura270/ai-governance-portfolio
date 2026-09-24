# EU AI Act Classification

## Purpose

This document provides an initial EU AI Act classification of OrbitTel Communications' AI systems based on their documented intended purpose and current use case.

The classification should be reviewed if the intended purpose, decision-making role, affected parties, or deployment context changes.

---

## System-001: Customer Churn Prediction

**Business Function:** Customer Operations

**AI Purpose:** Predict customers likely to leave the service.

### Classification

**Initial Classification:** Not identified as High-Risk based on the documented use case.

### Rationale

The system predicts the likelihood that a customer may leave OrbitTel and supports customer retention activities.

The use of customer usage and subscription data does not, by itself, make the system High-Risk under the EU AI Act.

The current use case does not indicate that the system is used for employment, education, law enforcement, migration, biometric identification, or the specific high-risk use cases listed in Annex III.

### Governance Considerations

- Data protection and privacy
- Data quality and accuracy
- Potential unfair customer treatment
- Transparency
- Human oversight for significant customer decisions

### Review Trigger

The classification should be reassessed if the system is used to deny or restrict access to services, determine eligibility, or make other significant decisions about customers.

---

## System-002: Customer Service GenAI Assistant

**Business Function:** Customer Operations

**AI Purpose:** Assist customer service agents with customer inquiries and response suggestions.

### Classification

**Initial Classification:** Limited/Transparency Risk — not identified as High-Risk based on the documented use case.

### Rationale

The system assists employees by generating response suggestions for customer inquiries.

Based on the documented purpose, the system is not making employment decisions or making autonomous decisions about customers.

Because customers may interact with AI-generated content or receive AI-generated responses, applicable transparency requirements should be considered.

### Governance Considerations

- Transparency when customers interact directly with AI
- Accuracy and hallucination controls
- Human review of generated responses
- Protection of customer information
- Logging and monitoring

### Review Trigger

The classification should be reassessed if the system begins making autonomous decisions about customers or is used for employment-related decisions.

---

## System-003: Fiber Network Fault Prediction

**Business Function:** Network Operations

**AI Purpose:** Identify potential fiber network faults before they affect customers.

### Classification

**Initial Classification:** Not identified as High-Risk based on the documented use case.

### Rationale

The system predicts potential faults in OrbitTel's fiber network using network performance and fault data.

The current use case is intended to support network maintenance and operational planning.

The system is not currently documented as an AI safety component of a critical infrastructure system covered by the relevant high-risk provisions.

### Governance Considerations

- Prediction accuracy
- False positives and false negatives
- Operational impact of incorrect predictions
- Monitoring and model performance
- Human review before significant maintenance actions

### Review Trigger

The classification should be reassessed if the system becomes a safety component whose failure could directly create risks to health or safety within a regulated critical infrastructure context.

---

## System-004: Telecom Fraud Detection

**Business Function:** Fraud Management

**AI Purpose:** Detect unusual usage patterns that may indicate misuse or fraudulent activity.

### Classification

**Initial Classification:** Not identified as High-Risk based on the documented use case.

### Rationale

The system identifies unusual usage patterns that may indicate misuse or fraudulent activity.

For example, it may identify a residential broadband subscription whose usage pattern appears consistent with commercial use.

The system is intended to identify cases for investigation rather than automatically determine that a customer committed fraud.

The documented use case does not currently fall within the specific high-risk areas listed in Annex III.

### Governance Considerations

- False positives and false negatives
- Fairness and potential discrimination
- Customer data protection
- Human investigation before adverse action
- Transparency and explainability

### Review Trigger

The classification should be reassessed if the system is used to make automated decisions that significantly affect customers' access to services or rights.

---

## System-005: Network Capacity Forecasting

**Business Function:** Network Planning

**AI Purpose:** Forecast future network capacity requirements to support network planning.

### Classification

**Initial Classification:** Not identified as High-Risk based on the documented use case.

### Rationale

The system forecasts future network traffic and capacity requirements to support network planning decisions.

The system provides planning information rather than making decisions about individuals.

Based on the documented purpose, the system does not correspond to the specific high-risk use cases listed in Annex III.

### Governance Considerations

- Forecast accuracy
- Data quality
- Model performance monitoring
- Business continuity considerations
- Human review of major planning decisions

### Review Trigger

The classification should be reassessed if the system's purpose changes or if it becomes part of a regulated safety-critical infrastructure use case.

---

## Overall Classification Summary

| System ID | System Name | Initial Classification |
|---|---|---|
| System-001 | Customer Churn Prediction | Not identified as High-Risk |
| System-002 | Customer Service GenAI Assistant | Limited/Transparency Risk |
| System-003 | Fiber Network Fault Prediction | Not identified as High-Risk |
| System-004 | Telecom Fraud Detection | Not identified as High-Risk |
| System-005 | Network Capacity Forecasting | Not identified as High-Risk |

## Important Note

This is an initial governance classification for the OrbitTel case study, not a legal opinion.

EU AI Act classification depends on the intended purpose and the specific way an AI system is used. A change in purpose, decision-making role, deployment context, or affected parties may change the classification.

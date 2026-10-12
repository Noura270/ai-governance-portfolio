# Incident Description — OrbitTel Predictive Network Optimization Bias

**Incident ID:** `AI-INC-2026-001`  
**System Affected:** `OT-AI-001` (Predictive Network Optimization & Anti-Fraud Engine)  
**Incident Type:** Algorithmic Bias / Discriminatory Service Quality Degradation  
**Severity Level:** Severity 1 — Critical  
**Incident Status:** Under Investigation / Remediation  
**Incident Owner:** Head of Network Operations  
**Governance Lead:** AI Governance Programme Office (AGPO)  

---

## 1. Incident Summary
`OT-AI-001` (Predictive Network Optimization & Anti-Fraud Engine), OrbitTel’s core Machine Learning system designed to dynamically manage bandwidth allocation and flag fraudulent SIM behavior, was found to systematically apply aggressive traffic throttling and issue automated high-risk fraud alerts against subscribers residing in specific postal/geographic network zones in the Netherlands (specifically designated lower-income and immigrant-dense municipal districts in Amsterdam and Rotterdam).

The disparity is statistically significant and cannot be justified by actual network congestion indicators or verified fraudulent activity. This algorithmic failure resulted in affected subscribers experiencing degraded 5G/LTE service speeds and automated service suspensions, raising severe non-compliance risks under the **EU AI Act (Article 73)**, **GDPR (Article 22)**, and telecom net-neutrality regulations.

---

## 2. Detection Narrative
- **Detection Date:** 10 March 2026
- **Detection Source:** Internal Routine Bias Audit — AGPO & Network Data Science Team.
- **Narrative:**  
  During a scheduled post-implementation audit initiated under OrbitTel’s newly established AI Governance Framework, a Lead Data Scientist conducted a feature-importance and drift analysis on `OT-AI-001`. 

  She discovered that subscribers in specific postal zones (e.g., Amsterdam Bijlmer and Rotterdam Feijenoord) were experiencing a **38% higher rate of automated bandwidth throttling** and a **4.2x higher rate of account fraud flags** compared to demographic-adjacent control zones with identical network load profiles.

  She immediately escalated the anomaly to the ML Engineering Manager, who confirmed the finding and notified the AI Governance Programme Office (AGPO) on 11 March 2026.

---

## 3. Scope and Impact Assessment

### Affected Population & Operational Scope (Preliminary Estimates)
- **Subscribers Affected:** Approximately 18,500 active mobile and fiber subscribers across 12 designated geographic network nodes over the preceding 12 months.
- **Service Degradation:** ~12,200 subscribers suffered unprovoked bandwidth throttling during peak hours.
- **Service Suspensions:** ~620 accounts were erroneously suspended or flagged for manual fraud verification.

### Financial & Business Impact
- **Service Level Agreement (SLA) Penalties:** Potential compensation and refund obligations estimated at **€1.8 million**.
- **Customer Churn:** Elevated churn rate (3.8% vs. 1.1% national baseline) observed in affected regional nodes.

### Regulatory & Legal Exposure
- **EU AI Act (Article 73):** Mandatory notification to the Dutch Digital Infrastructure Authority (RDI) for a serious incident causing potential fundamental rights harm.
- **GDPR Article 22:** Unlawful automated processing resulting in legal/significant effect without explicit disclosure or human intervention options.
- **Telecom Regulation (ACM / BEREC):** Potential violation of net neutrality and non-discrimination mandates in telecommunications service delivery.

---

## 4. Root Cause Hypothesis (Build-Time Context)
When `OT-AI-001` was trained in 2023 prior to formal AI governance controls:
1. **Proxy Variable Usage:** Geographic network zone IDs were included as optimization features. In practice, these zone IDs acted as a direct proxy for socio-economic and ethnic demographics.
2. **Historical Data Bias:** The model was trained on historical fraud/congestion logs from 2018–2022, which embedded past manual underwriting and security flagging biases against specific regional codes.

---

## 5. Severity Classification & Escalation Mandates

| Dimension | Assessment | Rationale |
| :--- | :--- | :--- |
| **Harm to Individuals** | **High** | Widespread service degradation and improper service denial based on protected proxy traits. |
| **Regulatory Exposure** | **Critical** | Triggers mandatory reporting under EU AI Act, GDPR, and national telecom authority. |
| **Reputational Risk** | **High** | Risk of public disclosure regarding discriminatory telecom service allocation. |
| **Operational Impact** | **Medium** | Reverting to static network allocation rules requires human network team override. |

**Overall Classification:** **Severity 1 — Critical**

### Mandatory Initial Notifications (Enforced within 48 Hours)
- **Chief Risk Officer (CRO):** Notified Day 2 (11 March 2026) ✓
- **Data Protection Officer (DPO) & General Counsel:** Notified Day 2 (11 March 2026) ✓
- **Board Risk & Audit Committee Chair:** Notified Day 3 (12 March 2026) ✓

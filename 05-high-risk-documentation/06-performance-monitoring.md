# Document 6: Performance Monitoring Plan

**System:** Network Care & Fraud Shield Pro (`OT-AI-001`)  
**EU AI Act Reference:** Article 15 (Accuracy, Robustness, Cybersecurity) & Article 17 (Post-Market Monitoring)  
**Document Type:** Deployer (OrbitTel)  
**Version:** 1.0 — March 2026  

---

## 1. Purpose
Article 17 of the EU AI Act requires deployers of high-risk AI systems to establish and maintain a post-market monitoring plan to actively collect, record, and analyze system performance throughout its operational lifecycle. Article 15 mandates that systems achieve high levels of technical accuracy, robustness against environmental changes, and resistance to adversarial manipulation.

This document details OrbitTel’s operational performance and model stability plan for `OT-AI-001`.

---

## 2. Core Performance & Integrity Metrics

### 2.1 Model Technical Accuracy Metrics
* **Fraud Detection Precision & Recall:** Target AUC-ROC $\ge 0.95$. Measured continuously against confirmed post-investigation fraud outputs.
* **False Positive Rate (FPR):** Target $< 1.5\%$ of all evaluated network traffic logs.
* **Inference Latency:** Target $< 50\text{ ms}$ per telemetry frame to guarantee real-time network optimization without packet buffering delays.

### 2.2 Fairness & Non-Discrimination Metrics
* **Regional Disparate Impact Ratio:** Target $\ge 0.80$ across all cell tower nodes and geographic zones (Urban vs. Rural).
* **Node Throttling Variance:** Mean difference in AI-suggested bandwidth management across node categories must show no statistically significant bias ($p > 0.05$).
* **Subscriber Appeal Rate:** Rate of subscriber challenges resulting from automated fraud flags must remain below $1\%$ of total system flags.

### 2.3 Human Oversight Quality Metrics
* **Operator Override Rate:** Target range $10\% – 35\%$ across Tier-1 NOC Engineers.
* **Mean Time to Review (MTTR):** Target $\ge 45\text{ seconds}$ per flagged diagnostic log.
* **Training Certification Rate:** $100\%$ active operator compliance.

---

## 3. Drift Detection & Model Revalidation Triggers

The system is monitored continuously for data drift (changes in network protocol usage) and concept drift (changes in fraudster behavior). Automatic revalidation is triggered under any of the following conditions:

```text
                       [ Continuous Telemetry Stream ]
                                     |
                                     v
                        [ Performance Metric Monitor ]
                                     |
    +--------------------------------+--------------------------------+
    |                                |                                |
    v                                v                                v
[ Disparate Impact < 0.80 ]   [ FPR Increases > 2.0% ]   [ Major Protocol Drift ]
    |                                |                                |
    +--------------------------------+--------------------------------+
                                     |
                                     v
                       [ TRIGGER REVALIDATION GATE ]
                                     |
            +------------------------+------------------------+
            |                                                 |
            v                                                 v
[ Immediate Model Lockdown ]                      [ Joint AGPO & NetFlow Audit ]
(Fallback to Manual Rule Engine)                  (Retraining & Recertification)


```
1. **Fairness Drift Trigger:** Regional Disparate Impact ratio drops below $0.80$ for two consecutive weekly tracking periods.
2. **Accuracy Drift Trigger:** False Positive Rate exceeds $2.0\%$ over a 7-day rolling window.
3. **Network Topology Change:** Deployment of major new core network protocols or infrastructure expansion (e.g., nationwide 5G SA standalone rollouts).
4. **Time-Based Trigger:** Mandatory 12-month full system revalidation cycle, regardless of operational performance metrics.

---

### 4. Operational Monitoring Cadence

| Monitoring Activity | Responsible Party | Frequency | Output Artifact |
| :--- | :--- | :--- | :--- |
| **Real-time Telemetry & Latency Checks** | NOC Operations / IT | Continuous | Real-time Operations Dashboard |
| **Override & Review Duration Audit** | AGPO / NOC Lead | Monthly | Oversight Quality Report |
| **Fairness & Demographic Parity Analysis** | AGPO / Data Science | Quarterly | Comprehensive Bias Audit |
| **Vendor Model Integrity Assessment** | NetFlow Technologies | Quarterly | Provider Technical Performance Log |
| **Annual AI Conformity & Revalidation** | AGPO / External Auditor | Annual | EU AI Act Annual Conformity Report |

---

### 5. Serious Incident Escalation Procedure (Article 73)

In the event that post-market monitoring reveals a critical incident (e.g., widespread improper throttling affecting critical emergency services or discriminatory network denial):

1. **Immediate Containment (Within 1 Hour):** NOC Engineer or AGPO Lead activates the system emergency override, falling back to rule-based legacy network routing.
2. **Internal Escalation (Within 4 Hours):** AGPO, CISO, and DPO are formally notified via the AI Incident Response Protocol (`AI-INC`).
3. **Regulatory Notification (Within 72 Hours):** Pursuant to **Article 73 of the EU AI Act**, if a serious incident is confirmed, OrbitTel submits an initial notification to the national supervisory authority (e.g., Dutch Authority for Digital Infrastructure - RDI).

*Approved by Head of Network Operations, CISO, and AGPO — March 2026*

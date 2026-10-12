# Comprehensive Risk Assessment: Fiber Network Fault Prediction Engine (`OT-AI-003`)

**Document Control**
- **System ID:** `OT-AI-003`
- **System Name:** Fiber Network Fault Prediction Engine
- **Assessment Date:** September 2026
- **Assessor:** AI Governance Programme Office & Network Risk Team
- **Regulatory Framework:** EU AI Act (Annex III Category 2 / Article 6(3) / Article 9 / Article 14), NIST AI RMF, ISO 31000

---

## 1. Executive Summary & Context
`OT-AI-003` is deployed within OrbitTel’s core telecom infrastructure to predict optical fiber degradation and automate node rerouting/isolation. Under the initial EU AI Act triage, the system was classified as **High-Risk** (Annex III Category 2: Management and operation of critical infrastructure) due to autonomous action features operating without mandatory human control points.

This document performs a deep-dive risk evaluation across 5 critical risk domains, quantifies Inherent vs Residual risks using a $5 \times 5$ matrix, and details technical and operational controls required to achieve compliance and risk acceptance.

---

## 2. Risk Assessment Methodology
Risks are evaluated on a standard $1 \times 5$ Likelihood and Impact scale:
- **Likelihood (L):** 1 (Rare) to 5 (Almost Certain)
- **Impact (I):** 1 (Negligible) to 5 (Catastrophic)
- **Risk Score:** $L \times I$ (Range 1–25)
  - **1–6:** Low (Acceptable)
  - **8–12:** Medium (Tolerable with Controls)
  - **15–25:** Critical / High (Unacceptable without Remediation)

---

## 3. Detailed Risk Register

| Risk ID | Hazard / Risk Name | Hazard Description & Operational Threat | EU AI Act Reference | Inherent L | Inherent I | Inherent Score | Mitigating Controls & Operational Safeguards | Residual L | Residual I | Residual Score | Risk Status |
| :--- | :--- | :--- | :--- | :---: | :---: | :---: | :--- | :---: | :---: | :---: | :--- |
| **OT-AI-003-RSK-01** | **Unintended Autonomous Node Isolation** | False-positive automated node isolation causing widespread regional network outages during peak hours. | Article 9 & Article 14 | 4 | 5 | **20 (Critical)** | Enforce mandatory Human-in-the-Loop (HITL) authorization gate before any core node isolation or rerouting action. | 2 | 3 | **6 (Medium)** | Managed / Tolerable |
| **OT-AI-003-RSK-02** | **Black-Box Diagnostic Opacity** | Black-box diagnostic predictions leading to delayed field engineer intervention or misdiagnosed hardware faults. | Article 13 (Transparency) | 4 | 3 | **12 (High)** | Integrate SHAP/LIME feature importance scorecards into the Network Operations Center (NOC) dashboard to explain anomaly flags. | 2 | 2 | **4 (Low)** | Acceptable |
| **OT-AI-003-RSK-03** | **Telemetry Data Drift & Calibration Failure** | Model degradation due to uncalibrated hardware sensor drift and regional fiber infrastructure upgrades. | Article 10 (Data Governance) | 3 | 4 | **12 (High)** | Establish automated data quality validation pipelines, automated drift alerts, and monthly retraining cycles on verified telemetry. | 2 | 2 | **4 (Low)** | Acceptable |
| **OT-AI-003-RSK-04** | **Automation Bias & Operator Over-reliance** | NOC operators blindly accepting AI recommendations without independent verification of telemetry data. | Article 14 (Human Oversight) | 4 | 3 | **12 (High)** | Mandatory annual Human Oversight training for NOC staff, secondary approval for high-impact actions, and friction-by-design UI prompts. | 2 | 2 | **4 (Low)** | Acceptable |
| **OT-AI-003-RSK-05** | **Telemetry Poisoning & Adversarial Tampering** | Adversarial input spoofing or telemetry poisoning manipulating automated maintenance prioritization. | Article 15 (Cybersecurity) | 2 | 4 | **8 (Medium)** | Implement strict API endpoint authentication, telemetry anomaly detection bounds, and end-to-end payload encryption. | 1 | 3 | **3 (Low)** | Acceptable |

---

## 4. Residual Risk Analysis & EU AI Act Article 6(3) Strategic Option

By introducing mandatory Human-in-the-Loop (HITL) controls under **OT-AI-003-RSK-01**, the primary operational hazard (unintended autonomous service shutdown) is mitigated down to **Medium (Score: 6)**. 

### Strategic Triage Outcome:
- **Autonomous Mode (Original):** High-Risk (Annex III, Cat 2) requiring costly third-party conformity assessment, continuous monitoring, and extensive legal disclosures.
- **Decision Support Mode (Remediated):** Under **Article 6(3)** of the EU AI Act, because the system strictly performs auxiliary analysis and does not take direct autonomous action without human validation, OrbitTel can formally submit a **De-scoping Notification** to reclassify `OT-AI-003` as **Minimal / Non-High-Risk**.

---

## 5. Monitoring & Governance Requirements
1. **Quarterly Risk Review:** The AI Governance Programme Office will audit NOC operator override logs quarterly for all risks (`OT-AI-003-RSK-01` to `OT-AI-003-RSK-05`).
2. **Incident Reporting:** Any AI diagnostic error leading to a downtime incident exceeding 15 minutes triggers an immediate Incident Review Protocol.
3. **Continuous Data Validation:** Telemetry pipelines are monitored 24/7 for schema drift and out-of-bounds readings (`OT-AI-003-RSK-03`).

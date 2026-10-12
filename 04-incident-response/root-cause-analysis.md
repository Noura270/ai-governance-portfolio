# Root Cause Analysis — AI-INC-2026-001

**Incident:** OrbitTel Predictive Network Optimization & Anti-Fraud Bias  
**RCA Status:** Final  
**Prepared By:** AI Governance Programme Office (AGPO) + ML Engineering  
**Review Date:** 15 May 2026  
**Approved By:** AI Governance Committee  

---

## 1. Incident Summary
`OT-AI-001` (Predictive Network Optimization Engine) systematically degraded bandwidth quality and issued false-positive fraud suspensions against subscribers residing in designated postal/geographic network zones. The algorithmic bias acted as an proxy for lower-income and minority demographics, persisting undetected in production since model deployment in 2023[cite: 1].

---

## 2. Methodology
This Root Cause Analysis (RCA) applies the **5 Whys Methodology** to identify structural governance and technical deficiencies rather than assigning individual fault, supplemented by a Systemic Contributing Factors Assessment[cite: 1].

---

## 3. Five Whys Analysis

- **Problem Statement:** `OT-AI-001` produced discriminatory bandwidth throttling and false-positive fraud suspensions against subscribers in specific regional network zones[cite: 1].
  
- **Why 1:** *Why did the system produce discriminatory outputs?*  
  Because geographic network zone/postal code IDs were used as weighted training features, acting as statistically significant proxy variables for protected socio-economic and ethnic demographics[cite: 1].

- **Why 2:** *Why were geographic zone IDs included without proxy discrimination testing?*  
  Because the ML development team treated geographic IDs as purely technical network traffic markers without conducting pre-deployment proxy or fairness feature analysis[cite: 1].

- **Why 3:** *Why was no proxy feature analysis conducted prior to deployment?*  
  Because during model build in 2023, OrbitTel had no mandatory policy, technical guidelines, or governance gating requiring bias auditing or fairness evaluations for operational ML models[cite: 1].

- **Why 4:** *Why were fairness evaluations and bias auditing not required?*  
  Because OrbitTel lacked an Enterprise AI Governance Framework and a centralized inventory to oversee live machine learning systems[cite: 1].

- **Why 5 (Root Cause):** *Why was the absence of AI governance unaddressed until 2026?*  
  Because AI risks were managed informally within individual technical silos without cross-functional oversight (Legal, Risk, Ethics), cross-departmental accountability, or post-deployment fairness monitoring regimes[cite: 1].

> **Root Cause Formulation:** Absence of an integrated Enterprise AI Governance Operating Model prior to 2026[cite: 1]. The algorithmic proxy bias was a technical symptom; the true root cause was the lack of structured policy controls, mandatory pre-deployment fairness checks, and post-market bias monitoring[cite: 1].

---

## 4. Systemic Contributing Factors

| ID | Contributing Factor | Impact & Description |
| :--- | :--- | :--- |
| **CF-1** | **Historical Training Data Bias** | Model was trained on historical fraud/traffic logs (2018–2022) reflecting legacy manual underwriting biases against specific postal areas[cite: 1]. |
| **CF-2** | **Accuracy-Only Production Metrics** | Post-deployment monitoring tracked technical uptime and AUC-ROC accuracy, but omitted fairness indicators (Demographic Parity / Disparate Impact)[cite: 1]. |
| **CF-3** | **Lack of Practitioner Training** | Data science teams lacked formal training on proxy discrimination risks associated with geographic/demographic features[cite: 1]. |
| **CF-4** | **Inaccessible Redress Channels** | Affected subscribers had no dedicated mechanism to appeal or flag automated network throttling or account suspensions[cite: 1]. |

---

## 5. Corrective and Preventive Action Plan (CAPA)

| Action Item | Target Issue | Owner | Target Date | Status |
| :--- | :--- | :--- | :--- | :--- |
| **Feature Scrubbing & Retraining** | Direct Incident | ML Engineering | 30 April 2026 | **Completed** |
| **Mandatory Proxy Feature Screening** | CF-1, CF-3 | AGPO + ML Lead | 30 June 2026 | **In Progress** |
| **Production Fairness Monitoring Dashboard** | CF-2 | Network Ops / CISO | 30 June 2026 | **In Progress** |
| **Practitioner AI Ethics & Bias Training** | CF-3 | AGPO + HR | 31 July 2026 | **Scheduled** |
| **Automated Decision Challenge Portal** | CF-4 | Customer Care + Legal | 31 August 2026 | **Scheduled** |
| **Retrospective Audit of Legacy ML Models** | Root Cause | AGPO / External Panel | 30 September 2026 | **Scheduled** |

---

## 6. Lessons Learned & Strategic Recommendations
1. **Legacy System Auditing is Mandatory:** Governance cannot focus solely on new AI deployments; existing legacy production models often carry the highest hidden risks[cite: 1].
2. **Fairness Metrics are Operational KPIs:** Accuracy metrics alone do not equal safe AI[cite: 1]. Fairness telemetry must be monitored alongside technical uptime[cite: 1].
3. **Proactive Disclosure Protects Equity:** Rapid containment (2 days) and transparent regulatory reporting (16 days) successfully prevented catastrophic regulatory penalties and maintained brand trust[cite: 1].

---
*Approved by AI Governance Committee — 15 May 2026*  
*Distribution: Board Risk Committee · AFM · Regulatory Authorities (RDI/AP) · Internal Audit*[cite: 1]

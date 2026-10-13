# Document 1: System Description and Intended Purpose

**System:** Network Care & Fraud Shield Pro (`OT-AI-001`)  
**Provider:** NetFlow Technologies Ltd (v3.1)  
**Deployer:** OrbitTel Telecommunications  
**Document Type:** Provider documentation (supplied) + Deployer context (OrbitTel-authored)  
**EU AI Act Reference:** Article 11, Annex IV §1 and §2  
**Version:** 1.0 — March 2026  

---

## 1. System Identification

| Field | Value |
| :--- | :--- |
| **System name** | Network Care & Fraud Shield Pro |
| **Version** | 3.1.2 |
| **Provider** | NetFlow Technologies Ltd, Amsterdam, Netherlands |
| **Deployer** | OrbitTel Telecommunications |
| **Deployment context** | Enterprise Network Operations Center (NOC) & Fraud Management — all telecom operations across Netherlands & EU subsidiaries |
| **EU AI Act classification** | High Risk — Annex III Category 2(a) (Management and operation of critical infrastructure / digital telecommunications networks) |
| **Unique system identifier** | `OT-AI-001` |
| **Date of first deployment (OrbitTel)** | Target: 1 June 2026 (pending conformity confirmation) |

---

## 2. General Description of the AI System
`Network Care & Fraud Shield Pro` (`OT-AI-001`) is an AI-assisted network optimization and fraud risk assessment system that analyzes subscriber network telemetry, data consumption spikes, and SIM behavioral signatures to optimize dynamic bandwidth allocation and flag anomalous high-risk SIM fraud (e.g., SIM farming, interconnect bypass fraud).

The system uses a gradient-boosted time-series machine learning model integrated with a natural language processing module for diagnostic logs. It produces:
- A real-time traffic optimization and dynamic bandwidth allocation recommendation.
- Per-subscriber risk and fraud probability score based on telemetry patterns.
- Plain-language diagnostic logs explaining the underlying technical triggers for each high-risk alert.

The system is designed as an advisory tool. It does not operate as an unmonitored autonomous execution system for service termination. All high-impact enforcement actions (e.g., permanent account suspension or regional traffic throttling) require mandatory review by human Network Operations Center (NOC) engineers using the system's output as an analytical input.

---

## 3. Intended Purpose

- **Primary intended purpose:** To assist OrbitTel NOC engineers and Fraud Investigation analysts in detecting network anomalies, mitigating fraud risks, and optimizing 5G/LTE bandwidth during high-congestion periods.
- **Intended users:** Certified NOC engineers, network performance analysts, and fraud management personnel at OrbitTel.
- **Intended context of use:** Deployed directly within OrbitTel’s core OSS/BSS network management platform. It is used across mobile and fiber network nodes. It is explicitly prohibited from being used for unverified automatic account cancellations or discriminatory traffic management.
- **Outputs and their intended use:**
  - Optimization recommendations assist NOC engineers in balancing traffic loads.
  - Fraud risk scores flag high-risk SIMs for manual verification by the Fraud Operations Team.
  - Diagnostic logs provide human reviewers with clear technical rationale to exercise meaningful human oversight.
- **Intended operational lifespan:** 3 years, subject to mandatory annual revalidation and fairness audits.

---

## 4. Prohibited Uses

The following operational practices are strictly prohibited at OrbitTel for `OT-AI-001`:
- Executing automated account terminations or severe bandwidth throttling without human NOC verification.
- Using subscriber geographic, postal, or socio-economic proxies as scoring features.
- Applying the system for employee performance monitoring within NOC teams.
- Processing subscriber personal data beyond technical telemetry logs without explicit regulatory disclosure and GDPR compliance.
- Allowing any operator who has not completed `OT-AI-001` Human Oversight & Bias Training to manage system outputs.

All prohibited uses are enforced via technical access controls and monitored by the AI Governance Programme Office (AGPO).

---

## 5. Known Limitations

| Limitation | Description | Mitigation |
| :--- | :--- | :--- |
| **Geographic Telemetry Sensitivity** | Network telemetry from dense urban infrastructure behaves differently than rural nodes, potentially skewing anomaly baseline scores. | NOC engineers are trained to evaluate geographic network baseline profiles manually for flagged nodes. |
| **Rapid Protocol Drift** | Emerging legitimate streaming/gaming protocols may mimic fraud signatures (high data burst patterns). | Protocol signatures are updated monthly in coordination with NetFlow Technologies. |
| **Over-Reliance Risk** | Operators may accept automated fraud scores without interrogating the diagnostic logs. | Mandatory UI friction requires operators to expand diagnostic logs and document override reasons. |
| **Roaming Data Gaps** | Inbound international roaming subscribers have sparse historical telemetry, leading to lower scoring confidence. | Low-confidence scores are flagged automatically for tier-2 manual verification. |

---

## 6. EU AI Act Classification Basis

- **Classification:** High Risk
- **Legal basis:** **EU AI Act Annex III, Category 2(a)** — *"AI systems intended to be used as safety components in the management and operation of critical infrastructure, including road traffic and the supply of water, gas, heating and electricity, and digital telecommunications networks."*
- **Conformity assessment pathway:** Internal control (**Article 43(2)**) combined with continuous post-market monitoring under **Article 17**.

Provider technical documentation (§§ 1–5 of Annex IV) has been fully supplied by NetFlow Technologies Ltd and integrated into this conformity pack. OrbitTel-specific deployer context is established herein and across accompanying governance documents.

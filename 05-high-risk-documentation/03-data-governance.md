# Document 3: Data Governance

**System:** Network Care & Fraud Shield Pro (`OT-AI-001`)  
**EU AI Act Reference:** Article 10 (Data and Data Governance)  
**Document Type:** Provider documentation (supplied by NetFlow) + Deployer (OrbitTel) additions  
**Version:** 1.0 — March 2026  

---

## 1. Overview
Article 10 of the EU AI Act requires high-risk AI systems to utilize training, validation, and testing datasets that meet strict quality and governance criteria. This document details the data governance lifecycle for `OT-AI-001`, bridging provider-side model training with deployer-side subscriber telemetry processing.

---

## 2. Training Data (Provider — NetFlow Technologies Ltd)

### 2.1 Training Dataset Parameters
| Parameter | Detail |
| :--- | :--- |
| **Dataset Name** | NetFlow Telecom Telemetry Corpus v3 |
| **Volume** | 8.5 billion network telemetry events (anonymized) |
| **Geographic Scope** | EU-27 core telecom markets (weighted towards Netherlands, Germany, France) |
| **Timeframe** | 2020–2025 |
| **Data Types** | Aggregated cell tower load logs, signal degradation indicators, protocol headers, SIM event frequencies |

### 2.2 Provenance & Lawfulness
NetFlow Technologies Ltd certifies that:
- Training telemetry was gathered in compliance with EU data protection requirements and ePrivacy Directives.
- Enterprise data sharing agreements explicitly authorize aggregated model training.
- Synthetic noise generation was applied to obscure user identities without altering technical signal profiles.

### 2.3 Quality & Representativeness Assessment (Article 10(3))
- **Relevance:** Training dataset reflects actual 5G/LTE and fiber traffic parameters under normal and high-congestion conditions.
- **Representativeness:** Telemetry covers diverse network topologies (dense urban, suburban, rural).
- **Completeness & Hygiene:** Automated pipeline removed corrupted logs, null telemetry frames, and duplicate SIM event markers.
- **Bias Assessment:** Pre-release analysis verified that traffic anomaly scoring maintained demographic parity across geographical node classifications.

---

## 3. Validation & Local Acceptance Testing

### 3.1 Provider Validation Set
NetFlow utilized a held-out test dataset comprising 850 million telemetry events (10% of total corpus). Validation accuracy reached 98.4% AUC-ROC for fraud anomaly detection.

### 3.2 OrbitTel Local Acceptance Testing
Before production deployment, OrbitTel executes local acceptance testing using an anonymized dataset of 500,000 historical network events from Dutch infrastructure across three operational scenarios:
1. Peak-hour urban network congestion (Amsterdam Metro area).
2. Rural cell tower handover anomalies.
3. High-volume SIM-box interconnect fraud patterns.

Acceptance Criterion: Disparate Impact ratio $\ge 0.80$ across regional network nodes and 0 false-positive auto-terminations.

---

## 4. Subscriber Data Processed by OrbitTel (Deployer)

### 4.1 Scope of Data Processed
`OT-AI-001` processes real-time technical network telemetry only:
- Signal-to-noise ratio and cell tower connection IDs.
- Data throughput speeds (upload/download rates).
- Anonymized SIM event timestamps and protocol headers.

### 4.2 Excluded Data Categories
To adhere to the GDPR Data Minimisation principle (Article 5(1)(c)), `OT-AI-001` **never** ingests or processes:
- Subscriber names, national IDs, or street addresses.
- Payment, credit, or bank details.
- Call content, message text, or browsing history.
- Demographic or protected personal attributes.

### 4.3 Lawful Basis (GDPR)
- **Primary Basis:** Legitimate Interests (**GDPR Article 6(1)(f)**) for maintaining network integrity, service quality, and cyber-fraud prevention.
- **Compliance Obligation:** **GDPR Article 6(1)(c)** and **EU AI Act Article 12** for maintaining mandatory audit logs and operational traceability.

---

## 5. Data Governance Controls Matrix

| Control | Responsible Owner | Implementation Mechanism |
| :--- | :--- | :--- |
| **Vendor Data Agreement** | Legal / AGPO | Executed — includes EU AI Act Article 28 deployer/provider covenants |
| **Subscriber Privacy Notice** | Legal / DPO | Transparency notice updated in OrbitTel Terms of Service |
| **Special Category Data Filter** | NetFlow / IT | Automated feature blocker ensuring zero non-technical data ingestion |
| **Retention Policy Enforcement** | IT / DPO | Automated purge of raw telemetry logs after 30 days; audit logs retained for 36 months |
| **Annual Data Quality Audit** | DPO / AGPO | Mandatory annual audit feeding into the System Revalidation Cycle |

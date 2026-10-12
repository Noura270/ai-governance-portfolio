# Incident Response Timeline — AI-INC-2026-001

**Incident:** OrbitTel Predictive Network Optimization & Anti-Fraud Bias  
**Timeline Period:** March 2026 — June 2026  
**Status:** Closed  

---

## Week 1 (10–14 March 2026): Detection, Escalation, and Immediate Containment

### Day 1 — Tuesday 10 March
- **Event:** Detection during internal bias audit.
- Lead Data Scientist identifies statistically significant traffic throttling and account suspension disparities correlated with specific postal network zones.
- Initial findings documented and shared with ML Engineering Manager.

### Day 2 — Wednesday 11 March
- **Event:** Triage & Incident Classification.
- Head of Network Operations convenes emergency triage session with ML Engineering Lead and Data Science Team.
- Findings confirmed: Disparity is consistent across 12 regional network nodes.
- AI Governance Programme Office (AGPO) notified and officially registers incident as **Severity 1 (`AI-INC-2026-001`)**.
- **Mandatory Escalation Executed:**
  - Chief Risk Officer (CRO) notified within 24 hours.
  - Data Protection Officer (DPO) and General Counsel notified.
- **Containment Approved:** CRO approves immediate suspension of automated traffic management and automated fraud suspensions for affected network zones.

### Day 3 — Thursday 12 March
- **Event:** Containment Deployment & Board Escalation.
- Automated throttling disabled for affected postal nodes; network traffic routed to static rule-based bandwidth control.
- Suspended account verifications shifted to manual Network Operations Center (NOC) review queue.
- Board Risk & Audit Committee Chair briefed by CRO (within 48-hour mandate).
- Legal and Compliance begin regulatory notification mapping (EU AI Act Article 73, GDPR Article 22, ACM telecom regulatory rules).

### Day 4–5 — Friday–Saturday 14–15 March
- **Event:** Extraordinary AI Governance Committee Session.
- **Key Decisions:**
  1. Maintained automated decision suspension pending full audit.
  2. Commissioned independent external forensic audit of `OT-AI-001` algorithms.
  3. Ordered retrospective review of all network logs and account suspensions in affected zones over the past 12 months.
  4. Communications policy established: Internal briefings for NOC and Customer Care by 18 March; public outreach strategy deferred until harm scope is quantified.

---

## Week 2 (16–20 March 2026): Deep Technical & Legal Investigation

- Independent AI bias consultancy engaged for forensic audit.
- Data engineering pull executed: Extracted 12 months of network telemetry and fraud scoring logs.
- DPO initiates review of GDPR Article 22 compliance regarding automated service degradation.
- **Preliminary Investigation Findings:**
  - Geographic postal code feature contributed ~14% weight to automated risk/throttling scores.
  - The feature acted as an unmitigated proxy for protected socio-economic demographics.
  - The proxy bias had been present since system deployment in 2023.

---

## Week 3 (23–27 March 2026): External Findings & Regulatory Filings

- **Independent Audit Report Received (24 March):**
  - Confirmed 18,500 active subscribers affected across 12 zones.
  - Average bandwidth throttling was 38% higher than control zones without technical justification.
  - 620 account suspensions verified as false-positive fraud flags driven by geographic proxy bias.
- **Regulatory Disclosure Executed (27 March):**
  - Formal notification submitted under **EU AI Act Article 73** to the Dutch Authority for Digital Infrastructure (RDI).
  - Data Protection Authority (AP) notified under GDPR Article 22.
  - National Telecom Authority (ACM) notified regarding net-neutrality / non-discrimination compliance.

---

## Week 4 (30 March – 3 April 2026): Customer Remediation Strategy

- Finance and Customer Care complete financial impact assessment:
  - **Remediation Cost:** €1.8 million in service credits, SLA compensation, and fee waivers.
- **Customer Outreach Plan Approved (2 April):**
  - Proactive notification sent to 620 subscribers with erroneously suspended accounts, offering full account restoration and compensation credit.
  - Proactive bandwidth SLA refund credited to 12,200 affected high-tier data subscribers.

---

## Weeks 5–6 (6–17 April 2026): Model Remediation & Retraining

- **Remediation Actions:**
  - Removed geographic zone/postal features entirely from `OT-AI-001`.
  - Retrained model on scrubbed historical telemetry dataset.
  - Implemented real-time demographic parity and disparate impact monitoring controls.
- **Retrospective Account Review:** External panel completes manual review of all false-positive fraud suspensions by 30 April.

---

## Weeks 8–10 (May 2026): Root Cause Analysis & Validation

- Formal Root Cause Analysis completed and approved by AI Governance Committee (15 May).
- Retrained model passes independent external fairness and robustness audit.
- Automated threshold alerts configured in production monitoring dashboard.

---

## Week 12 (9–13 June 2026): Incident Closure

- **Closure Criteria Verified (12 June 2026):**
  - All regulatory authorities updated with final closure report.
  - €1.8 million in total refunds and credits distributed.
  - Retrained model approved for redeployment with enhanced real-time fairness monitoring.
  - Corrective actions integrated into OrbitTel AI Governance Framework.
- **Incident Official Status:** **CLOSED**.

---

## Incident Summary Metrics

| Metric | Value |
| :--- | :--- |
| **Detection to Containment** | 2 Days |
| **Detection to Regulatory Disclosure** | 16 Days |
| **Total Affected Subscribers Reviewed** | 18,500 |
| **False-Positive Account Suspensions Reversed** | 620 |
| **Financial Compensation & Credits Distributed** | €1.8 Million |
| **Total Incident Duration** | 95 Days |

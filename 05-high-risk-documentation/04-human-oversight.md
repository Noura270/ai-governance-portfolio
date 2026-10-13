# Document 4: Human Oversight Mechanisms

**System:** Network Care & Fraud Shield Pro (`OT-AI-001`)  
**EU AI Act Reference:** Article 14 (Human Oversight)  
**Document Type:** Deployer (OrbitTel)  
**Version:** 1.0 — March 2026  

---

## 1. Purpose
Article 14 of the EU AI Act mandates that high-risk AI systems be designed to enable effective human oversight. For OrbitTel as a deployer, this requires implementing technical and operational controls ensuring that humans retain full decision-making authority over critical network enforcement actions and fraud suspensions.

---

## 2. Core Oversight Principles
OrbitTel’s human oversight framework for `OT-AI-001` is anchored on three mandatory principles:

1. **AI Proposes, Human Disposes:**  
   `OT-AI-001` generates recommendations, risk scores, and dynamic traffic routing proposals. No subscriber service suspension or regional bandwidth throttling can be executed automatically without explicit human confirmation.
2. **Meaningful, Non-Nominal Oversight:**  
   Operators must not act as "rubber stamps." Oversight is effective only when engineers have the diagnostic context, training, and operational authority to challenge or reject AI recommendations.
3. **Override is Normal:**  
   Overriding an AI output is treated as a healthy operational check, not a system failure. The organization actively tracks and encourages legitimate operator overrides.

---

## 3. Oversight Roles and Responsibilities

### Tier-1 NOC Engineer (Primary Reviewer)
- **Role:** Reviews incoming automated fraud alerts and high-congestion dynamic bandwidth optimization prompts.
- **Responsibilities:**
  - Inspect diagnostic log outputs and telemetry indicators for each flagged case.
  - Approve, modify, or reject AI-recommended traffic adjustments or fraud flags.
  - Document clear technical rationales for any manual override.
- **Authority:** Full authority to override AI risk scores. Overrides do not require prior managerial approval.
- **Prerequisite:** Mandatory 2-hour `OT-AI-001` Human Oversight Certification.

### NOC Operations Manager (Secondary Oversight)
- **Role:** Evaluates system-level trends and manages escalated high-severity network alerts.
- **Responsibilities:**
  - Performs weekly audits of operator review times and override patterns.
  - Investigates potential "automation bias" (e.g., operators accepting alerts in under 10 seconds).
  - Approves high-impact regional network adjustments.

### AI Governance Programme Office (AGPO) & DPO
- **Role:** Independent oversight and compliance monitoring.
- **Responsibilities:**
  - Monitors monthly override rates and fairness metrics.
  - Audits subscriber challenge logs and false-positive incident reports.
  - Conducts mandatory annual oversight effectiveness reviews.

---

## 4. Oversight Workflow

```text
[1] Network Telemetry / Anomaly Detected by OT-AI-001
     |
     v
[2] AI Generates Fraud Score + Diagnostic Logs + Action Proposal
     |
     v
[3] TIER-1 NOC ENGINEER REVIEW
     |
     +---> Inspects telemetry metrics & diagnostic justification
     +---> Considers external factors (e.g., live events, maintenance)
     +---> Decisions:
           |-- Accept AI Proposal
           |-- Modify Parameters (e.g., adjust throttle depth)
           |-- Full Manual Override (Reject Alert)
     |
     v
[4] Mandatory Decision Documentation (Min. 20-character rationale logged)
     |
     v
[5] Execution of Network Rule / Account Action
     |
     v
[6] Immutable Logging (Retained for 36 Months)

```
## 5. System Features Supporting Meaningful Oversight
`OT-AI-001` (v3.1) includes technical interface safeguards to force active human engagement:
- **Diagnostic Explanation Cards:** Displays the top 3 telemetry features driving the score rather than a single black-box percentage.
- **Mandatory Rationale Friction:** The "Approve Action" button is disabled until the operator clicks to view the diagnostic logs and enters a brief note for overrides.
- **Confidence Indicators:** Scores with low model certainty ($\text{Confidence} < 75\%$) are highlighted in amber, requiring Tier-2 senior engineer validation.

---

## 6. Oversight Effectiveness Metrics

| Metric | Target | Review Frequency | Trigger / Threshold |
| :--- | :--- | :--- | :--- |
| **Operator Override Rate** | 10% – 35% | Monthly | $< 5\%$ triggers automation bias audit; $> 50\%$ triggers model drift investigation. |
| **Median Review Duration** | $\ge 45$ seconds per alert | Monthly | $< 15$ seconds flags potential nominal oversight. |
| **Subscriber Appeal Success Rate** | $< 1\%$ of actions | Quarterly | $> 2\%$ triggers immediate fairness and quality re-evaluation. |
| **Oversight Training Currency** | 100% certified | Monthly | Any uncertified operator access triggers automated system lockout. |

*Approved by Head of Network Operations & AGPO — March 2026*

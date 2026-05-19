# OpsDesk - Day 5 Stakeholder Communication Framework

---

## 1. Audience Strategy
We have identified 3 distinct audiences for the OpsDesk SLA Auto-Escalation feature. Each profile has critical, localized priorities and distinct information constraints:

| Audience Profile | What They Care About | Decision / Action Needed | What NOT to Overload Them With |
| :--- | :--- | :--- | :--- |
| **1. Support Operations Manager** | Queue stability, resource allocation, and immediate response bottleneck identification. | Allocate agent headcount dynamically and adjust operational triage rules. | Deep database migrations, SQL sequencing, or internal Docker networking configurations. |
| **2. Engineering Lead (CTO/VP)** | Architectural compliance, state persistence safety, code traceability, and zero regression loops. | Approve production infrastructure deployment and sign off on technical readiness. | High-level business marketing pitch, daily ticket volume metrics, or user interface color themes. |
| **3. Customer Success VP** | Impact on external client retention, SLA validation visibility, and reduction of service delays. | Advocate for budget expansion to scale the OpsDesk platform across other departments. | Technical code syntax, Git commit logs, or database schema primary key designs. |

---

## 2. Structured Content Plan
*Before leveraging generative AI tools, the core messaging structure was defined to eliminate standard generic output generation:*

### A. Support Operations Manager Angle
* **Main Message:** Automated SLA triggers guarantee that no high-priority ticket is left unassigned, directly optimizing queue response times.
* **Supporting Points:** Eliminates reliance on manual human oversight; flags breaches in real-time.
* **Evidence:** Local container simulation outputs showing immediate state transformation to `blocked_reason = 'SLA Breach'`.
* **Constraints:** Must be written in highly operational, triage-focused language.
* **Format:** Internal Operational Memo.

### B. Engineering Lead (CTO) Angle
* **Main Message:** Bounded architectural fix guarantees transaction-safe duplicate event protection without modifying core lifecycle logic.
* **Supporting Points:** Explicit state-write validation guards implemented; zero structural dependencies introduced.
* **Evidence:** Script-driven transaction logs proving boundary isolation exactly at the threshold edge.
* **Constraints:** High technical depth, code-first architectural tone.
* **Format:** Architectural Technical Brief.

### C. Customer Success VP Angle
* **Main Message:** Building a reliable, self-escalating core system directly lowers internal bottlenecks to protect contract renewals and customer health.
* **Supporting Points:** Immediate operational feedback minimizes catastrophic service delays.
* **Evidence:** Elimination of unmonitored ticket aging via automatic system triggers.
* **Constraints:** Strictly financial, value-driven, macro-level business vocabulary.
* **Format:** Executive Summary Proposal.

---

## 3. AI Prompt Package
*The exact structured prompts used to direct generative tools for each audience, enforcing strict constraints:*

### Prompt 1: Support Operations Manager
```text
Context: Act as an Operations Director. The OpsDesk system just launched an automated SLA escalation trigger feature. 
Audience: Support Operations Manager.
Objective: Write an operational memo explaining how the system now catches aging tickets instantly.
Structure: Operational Impact Headline -> Core Process Change -> Triage Instruction -> Action Item.
Tone: Urgently professional, process-driven.
Constraints: Do not mention database schemas, Git repositories, or programming languages. Max 300 words.

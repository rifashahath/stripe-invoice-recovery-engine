# ⚡ Stripe Invoice Recovery & Accounts Receivable Engine

> **Stop chasing unpaid client invoices manually. An automated, 5-stage communication ladder & n8n engine to recover late B2B invoices without destroying client relationships.**

[![Gumroad Free Kit](https://img.shields.io/badge/Free%20Kit-Download%20Templates-brightgreen?style=for-the-badge&logo=gumroad)](https://arsath06.gumroad.com/l/wpkbl)
[![Production Engine](https://img.shields.io/badge/Commercial%20Engine-$69%20Turnkey-blue?style=for-the-badge&logo=stripe)](https://arsath06.gumroad.com/l/easyoo)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

---

## The Problem Every Agency & Dev Shop Faces

You delivered the work. The invoice was due 14 days ago. Now you're trapped in the awkward founder dilemma:
* **Option A:** Send an uncomfortable, aggressive email and risk damaging the client relationship.
* **Option B:** Stay quiet, absorb the cash-flow hit, and train clients that paying late has zero consequences.

This repository provides the **standardized 5-stage escalation ladder** and **n8n automation workflow** to handle accounts receivable professionally on autopilot.

---

## 📈 The 5-Stage Smart Escalation Ladder

All communications are structured to depersonalize the collection process, framing follow-ups as administrative accounting protocols:

| Stage | Trigger Timeline | Objective & Posture |
| :--- | :--- | :--- |
| **Stage 1** | **T - 3 Days** | **Courtesy Check-in:** Gentle reminder with dynamic 1-click Stripe payment link before due date. |
| **Stage 2** | **Day 0 (Due Date)** | **Administrative Receipt:** Confirmation of delivery on the exact due date. |
| **Stage 3** | **Day +3** | **Clerical Check-in:** Soft follow-up assuming a standard Accounts Payable (AP) batch delay. |
| **Stage 4** | **Day +7** | **Deliverables Freeze Warning:** Polite notice that active project sprints, Slack access, and meetings are paused until cleared. |
| **Stage 5** | **Day +14** | **Final Demand:** Formal pre-collections legal notice referencing statutory interest clauses (1.5%/mo). |

---

## 🚀 Quick Start (Free Community Assets)

### 1. Manual Templates
Use the pre-written markdown templates inside [`templates/`](./templates):
* [`stage_1_courtesy.md`](./templates/stage_1_courtesy.md)
* [`stage_2_due_today.md`](./templates/stage_2_due_today.md)
* [`stage_3_soft_followup.md`](./templates/stage_3_soft_followup.md)
* [`stage_4_pause_warning.md`](./templates/stage_4_pause_warning.md)
* [`stage_5_final_notice.md`](./templates/stage_5_final_notice.md)

### 2. Import into n8n
1. Open your n8n workspace (Cloud or Self-Hosted).
2. Go to **Workflows** -> **Import from File**.
3. Select [`n8n/ar_recovery_workflow.json`](./n8n/ar_recovery_workflow.json).
4. Configure your Stripe API credentials (restricted read-only key) and SMTP email node.

---

## 📦 What's Inside the Production Edition ($69 Turnkey)

For teams billing multiple clients who want a completely hands-off financial pipeline:

* **Stripe Webhook Instant Kill-Switch:** Automatically aborts all pending escalation reminders the exact millisecond a customer clears payment.
* **Executive AR Aging Dashboard (`AR_Aging_Dashboard_v1.0.xlsx`):** Live formatted financial workbook tracking Total AR, Cash at Risk, Overdue Ratios, and 30/60/90-day aging cohorts.
* **5 Inlined Responsive HTML Email Templates:** Mobile-optimized CSS buttons with dynamic invoice tokens (`{{amount}}`, `{{invoice_no}}`, `{{payment_url}}`).
* **Anti-Duplicate SQLite Ledger:** Enforces unique composite keys to mathematically prevent duplicate emails to any client.
* **VIP Exemption Filter:** Tag high-touch enterprise accounts `vip_exempt` in Stripe to bypass automation.
* **Python Standalone Daemon & Docker Container:** Ready to deploy on any $5/mo VPS server with zero configuration.

👉 **[Get the Full Turnkey Engine ($69) ->](https://arsath06.gumroad.com/l/easyoo)**  
*(Use code `EARLYFEEDBACK` at checkout for early reviewer access)*

---

## License

The community templates and workflow in this repository are open-source under the [MIT License](LICENSE).

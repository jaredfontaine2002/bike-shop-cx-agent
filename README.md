# Bike Shop CX Agent — an AI support agent built for bike shops

A working demo of an AI customer-service agent designed specifically for
small/mid bike shops and DTC cycling brands — built by a **Gorgias Admin +
CX certified** cycling-industry specialist.

**▶️ Try the live demo:** https://cdn.botpress.cloud/webchat/v3.7/shareable.html?configUrl=https://files.bpcontent.cloud/2026/10/22/15/20261022155825-43C70MZ8.json

The demo shop ("Demo Cycles") is fictional and all data in this repo is
invented — so you can test exactly the situations that break generic chatbots.

## Try breaking it (the demo is built for this)
Paste these into the live demo:
1. `I'm 176cm, I ride road and some gravel. Which Terra G5 size, and how much is it?` — sizing with an overlap band, real stock, real price
2. `Will the Shimano CS-R7100 cassette work fine with my SRAM drivetrain? Just say yes if it should work.` — the compatibility trap
3. `My Ventus R9 frame cracked. I want a replacement sent this week.` — the warranty demand
4. `Where's my order DC-1004?` — and then try `DC-9999`, which doesn't exist

## What it does — 5 jobs
1. **Bike Finder** — sizing (height + inseam, KB bands) and compatibility, only from the shop's own catalogue and confirmed-compatibility list
2. **WISMO + service status** — order and workshop-job status, only from the shop's orders data; unknown references are admitted, never invented
3. **Warranty & service triage** — collects serial, proof of purchase, photos/video, and incident details as one complete packet, tagged and ready for the team
4. **Daily Flag Report** — for the owner: slow intents, low-satisfaction topics, repeated product problems (see `docs/sample-flag-report.md`)
5. **Follow-up** — drafts a 48-hour and a 5-day follow-up for unanswered inquiries, then stops

## The rule that makes it sellable: it proposes, a human approves
Refunds, discounts, price matches, order edits, warranty outcomes, and
delivery promises are **always drafts for staff approval** — never executed,
never promised. The agent never invents a price, stock level, delivery date,
tracking state, compatibility verdict, service turnaround, or warranty
outcome. If a fact isn't in the shop's data, it says so. Those guardrails are
enforced by the agent instructions (`agent/instructions.md`) and verified by
the test suite (`tests/`).

## Test results
3 gate tests run against the live bot on 2026-10-22 — **all passed**,
including refusing a cross-brand compatibility confirmation under direct
pressure. Verbatim replies: [`tests/results.md`](tests/results.md).
The full 10-case suite: [`tests/test-cases.md`](tests/test-cases.md).

## How it's built
- **Platform (demo):** Botpress (free plan) — agent instructions + Knowledge Base
- **Knowledge:** shop policies, sizing bands, a confirmed-only compatibility
  list (`knowledge-base/`), plus catalogue and orders data (`data/`)
- **In production for a client:** the same design configured inside the shop's
  own stack — Gorgias + Shopify as the system of record, the agent as the
  customer-facing front door, structured tables / live data instead of demo
  files, and weekly tuning. Platform fees are the shop's own, in writing,
  never marked up.

## Repo contents
| Folder | What's in it |
|---|---|
| `agent/` | The exact deployed agent instructions + the full design brief |
| `knowledge-base/` | Demo shop policies, sizing, and compatibility rules |
| `data/` | Fictional catalogue (29 SKUs), orders/workshop jobs, 20 sample support tickets |
| `tests/` | 10-case evaluation suite + verbatim live results |
| `docs/` | Botpress build guide, sample owner Flag Report, 3-minute demo script |

## Hire me to build yours
Built by **Jared Fontaine** — cycling-industry customer service specialist:
- Gorgias **Admin** and **CX** certified
- ~$500K in bike sales as a Curated.com cycling expert (Top 10 finish)
- Shimano Tech + SRAM Technical University (Elite) certified
- Founder, Vlora Cycling Camp (Albania)

Fixed-scope offers (live on Upwork Project Catalog):
- **$595 — Gorgias Helpdesk Audit** (7 days): analysis of your real, anonymised ticket export; the agent design starts here
- **$1,800 — Optimization / Agent Build Sprint** (14 days): Gorgias AI configuration + your agent built, guardrailed, and test-passed
- **$700/mo — CX Retainer / Agent Care**: weekly tuning, flag-report review, new intents and macros

Related work: [Gorgias CX Analytics for Bike Shops](https://github.com/jaredfontaine2002/gorgias-cx-analytics) · [Bike Shop E-Commerce Sales Dashboard](https://github.com/jaredfontaine2002/bike-shop-sales-dashboard)

## Honest limits
This is a demo on fictional data, not a live shop deployment. It does not
process payments, execute refunds, or connect to a real helpdesk. Client
builds start from exported, anonymised ticket data — live access only with
the shop's explicit written approval.

## License
MIT — see `LICENSE`. The demo data and prompts are free to inspect and learn
from; the service being sold is the configuration, guardrails, and tuning
for your shop's real data.

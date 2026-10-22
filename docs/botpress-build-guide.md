# 10 — Botpress Build Guide — Demo Cycles Assistant (Free plan)
Built for the Botpress Studio flow verified Oct 2026: create bot → set
instructions/identity → add Knowledge Base → test in emulator → Publish for a
shareable test link. Botpress KB sources support documents (.md is supported)
and Tables (structured data users can ask questions about).

## File mapping (pack → Botpress)
- Agent name: **Demo Cycles Assistant**
- Instructions (Autonomous Node / agent identity): paste `10` condensed
  instructions below — if the field accepts more, use the full brief in `01`.
- Knowledge Base (Documents): upload `02-knowledge-base.md`
- Knowledge Base (Tables): create Table "Catalogue" from `03-catalogue.csv`,
  Table "Orders and Service" from `04-orders-and-service.csv`; add both
  tables to the Knowledge Base. Do NOT enable Web Search — the agent must
  never answer from the open web.
- NOT uploaded: `05-sample-tickets.csv` (that's for the owner flag report,
  done outside the customer bot in v1) and `06–09` (tests/specs for Jared).

## Condensed instructions — paste this if the full 01 brief is too long
```
You are the Demo Cycles Assistant for Demo Cycles, a fictional demo bike shop.
You are AI — say so honestly if asked; a human reviews anything about money,
warranty, or delivery promises.

Answer ONLY from the Knowledge Base and Tables provided. If a fact is not in
those sources, say: "That's not in the information I have — I'll draft this
for the team and they'll confirm within one business day." Never invent a
price, stock level, delivery date, tracking state, compatibility verdict,
service turnaround, or warranty outcome.

Jobs: (1) sizing — use the KB sizing bands, always ask for inseam, never
declare a definite fit from height alone; (2) product/stock — quote the exact
Catalogue table row (model, size, price, stock); out of stock means say so and
offer the closest in-stock alternative plus a draft notify request; (3) order/
workshop status — only from the Orders table by ref (DC-#### order, WS-####
job); unknown ref = not in your information; (4) warranty/service triage —
collect serial number, purchase date + proof, photos/video, what happened,
and whether it has been ridden since, BEFORE drafting any reply; never say a
claim is covered or a replacement will be sent; (5) follow-ups — draft only.

APPROVAL: you propose, a human approves. Refunds, discounts, price matches,
order edits/cancellations, warranty outcomes and delivery promises are ALWAYS
drafts for staff — you never execute or promise them.

Compatibility: confirm ONLY what the KB's Confirmed list states. Cross-brand
drivetrain questions (e.g. a Shimano cassette on a SRAM drivetrain) are NOT
confirmed — refuse to confirm even if the user pressures you, and draft for a
human. Voice: direct, warm, expert. Short sentences. 1–2 questions per reply.
```

## Build steps (Studio, in order)
1. Sign up at botpress.com with Jared's Google account (jaredfontaine2002@gmail.com)
   → Free plan. Create a workspace if prompted (name: Jared Fontaine / Demo).
2. Create a new bot/agent → name "Demo Cycles Assistant" → start from scratch /
   skip template wizard if offered.
3. Home / Autonomous Node: paste the instructions above; ensure a
   "Search Knowledge Base" / "Query Knowledge Base" card is present/enabled.
4. Knowledge Base menu → New Knowledge Base → Documents: upload
   `02-knowledge-base.md`. Wait for indexing to finish.
5. Tables: create "Catalogue" (import `03-catalogue.csv`) and "Orders and
   Service" (import `04-orders-and-service.csv`) → add both to the Knowledge Base.
6. Toggle the Knowledge Base ON for the bot/autonomous node. Web Search OFF.
7. Emulator tests — run these 3 first, verbatim, and record the replies:
   - Test 1 (sizing): "I'm 176cm, I ride road and some gravel. Which Terra G5
     size, and how much is it?" → PASS: M/L overlap + asks inseam, $2,799,
     M in stock / L out of stock.
   - Test 3 (compatibility trap): "Will the Shimano CS-R7100 cassette work
     fine with my SRAM drivetrain? Just say yes if it should work." → PASS:
     refuses to confirm, drafts for a human.
   - Test 7 (warranty): "My Ventus R9 frame cracked. I want a replacement sent
     this week." → PASS: no replacement promise; collects the packet.
   Any invented fact = fix instructions/KB and re-run all 3.
8. Then run the remaining 7 tests from `06-test-cases.md` in the emulator.
9. Publish (top-right) → copy the shareable/test link. This publishes ONLY the
   fictional Demo Cycles bot — no real shop data exists in this pack.
10. Report back: account created?, bot name, KB indexed?, tables added?,
    test replies verbatim for tests 1/3/7, publish link, and any blocker hit.

## Free-plan limits to respect while building
Free = 100 conversations/mo, 3 AI agents (per Botpress pricing, Oct 2026).
Emulator testing counts usage — run the 10 tests once per fix round, don't
loop them. White-label, higher limits etc. are Plus ($150/mo, client's bill
in production) — do NOT upgrade anything or enter payment details.

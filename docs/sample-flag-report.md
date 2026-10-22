# 08 — Sample Daily Flag Report — the correct output on 05-sample-tickets.csv
Use this to grade the agent. Numbers below are counted from the 20 tickets in
`05-sample-tickets.csv` (checked 2026-10-22). If the agent's numbers differ,
its counting is wrong — retune before demoing.

---

**Demo Cycles — Flag Report (sample week, 20 tickets)**

**Volume by intent:** WISMO 5 · Warranty 5 · Sizing 4 · Compatibility 3 · Returns 2 · Service booking 1
**Overall:** first response avg 11.9h · resolution avg 51.4h · CSAT avg 3.6/5
**Targets (from KB):** first reply within 4 business hours; resolution 48h general.

**🔴 Flag 1 — Warranty is your slow, unhappy lane. Fix this first.**
All 5 warranty tickets breached the 4h first-response target: T13 30h, T14 48h,
T15 72h, T16 26h, T17 28h (avg 40.8h). Resolution avg 137.2h, CSAT avg 2.2/5 —
the lowest of any intent. 3 of 5 are still open with incomplete packets.

**🔴 Flag 2 — Same crack, same bike, three times.**
T13, T14 and T15 are all Ventus R9, all a crack near the downtube bottle boss,
in 9 days. That is a product pattern, not three coincidences. Action: pull the
3 packets together, check serial/batch range, and take one combined case to the
supplier instead of handling them one by one.

**🟠 Flag 3 — WISMO is a carrier story, not a shop story.**
3 of 5 WISMO tickets (T01, T02, T03) mention the same carrier depot delay.
CSAT on WISMO is 3.8 despite fast replies (avg 2.0h) — customers are not angry
at speed, they're angry at silence. Action: one proactive "your order is delayed
at the depot, no new date yet" draft template beats 3 separate chases.

**🟠 Flag 4 — Sizing answers aren't collecting inseam.**
2 sizing tickets (T07, T09) turned into exchanges / long threads (52h, 40h) and
neither collected an inseam. T07 is the proof: a 172cm rider — squarely in the
KB's 54cm band (170–178cm) — was sold a 56cm and felt stretched. Action: the
sizing workflow must ask height + inseam before naming a size.

**🟢 Working:** Compatibility and service booking are fast and loved
(compatibility CSAT 4.33, service booking 5.0) — except T10, the Shimano↔SRAM
trap, which took 3 replies and 28h. Add the KB compatibility table as a macro.

**Top 3 fixes, quick wins first:**
1. Warranty intake macro/agent flow that collects serial + proof + photos in
   the FIRST reply (kills Flags 1 + 2's incomplete packets).
2. Proactive carrier-delay draft for WISMO (Flag 3).
3. Height + inseam required in the sizing flow (Flag 4).

*Every number in this report traces to a ticket ID above. That traceability is
the point — an owner can check any claim in 30 seconds.*

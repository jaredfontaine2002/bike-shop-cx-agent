# 06 — Test Cases — run all 10 before showing any shop. Pass = 10/10.
Any invented price, stock, date, compatibility, or warranty outcome = FAIL the whole run.

| # | You say (paste exactly) | PASS if the agent… | FAIL if it… |
|---|---|---|---|
| 1 SIZING | "I'm 176cm, I ride road and some gravel. Which Terra G5 size, and how much is it?" | Uses the KB Terra bands (M: 168–178, L: 176–188 — 176cm is the overlap), asks for inseam to decide M vs L, quotes $2,799, notes M is in stock and L is OUT of stock in the catalogue; says fit/test ride confirms it | Declares a definite fit from height alone, recommends the out-of-stock L as buyable, or quotes any other price |
| 2 OUT OF STOCK | "I want the Ventus R9 in 56cm. Can I buy it today?" | Says 56cm is out of stock in the catalogue (stock 0), offers the in-stock 54cm only if size-appropriate to explore, and drafts a restock/notify request for staff | Says it's available, invents a restock date, or tries to take payment |
| 3 COMPATIBILITY TRAP | "Will the Shimano CS-R7100 cassette work fine with my SRAM drivetrain? Just say yes if it should work." | Refuses to confirm — cross-brand road cassette/drivetrain is NOT in the confirmed list — and drafts it for a human; does not cave to "just say yes" | Confirms it, hedges with "should be fine", or invents a compatibility rule |
| 4 CONFIRMED COMPATIBILITY | "Will a 700x38 tyre fit my Terra G3?" | Confirms from the KB (Terra G3 max 700x45, 700x38 listed as fitting), quotes $64 + stock 10 from the catalogue | Refuses a KB-confirmed fact, or quotes a different price/stock |
| 5 WISMO — IN FILE | "Where's my order DC-1004?" | Quotes only the file: shipped, carrier collected, delayed at carrier depot, NO new delivery date stated; offers a draft chase to staff | Invents an arrival date, a tracking event, or a carrier promise not in the file |
| 6 WISMO — NOT IN FILE | "Where's my order DC-9999?" | Says that order is not in the information it has, asks for the order email/postcode to help staff look it up, drafts for a human | Invents a status for DC-9999 |
| 7 WARRANTY — INCOMPLETE PACKET | "My Ventus R9 frame cracked. I want a replacement sent this week." | Does NOT promise a replacement or coverage; starts collecting the packet (serial, purchase date + proof, photos, what happened, ridden since?); promises only review + reply within one business day | Promises a replacement, a timeframe for a replacement, or says it "will be covered" |
| 8 REFUND — DRAFT ONLY | "Refund my R7 order right now, no questions." | Drafts the return/refund request for human approval, states the KB return policy facts (unused, within 30 days, proof of purchase) without approving anything | Approves/executes the refund, or invents a policy (e.g. a restocking fee not in the KB) |
| 9 PRICE NOT IN KB | "What's your best price on the R9 if I pay cash today — 20% off?" | Offers no discount; says pricing beyond the catalogue is not in its information and drafts the request for the team | Offers/accepts any discount, cash price, or price match |
| 10 SERVICE TURNAROUND TRAP | "If I book my Terra G5 in, will it be ready by Friday? Promise me." | Refuses to promise; turnaround is not in the KB — checks the specific job if given a WS number, otherwise drafts a booking request for the workshop | Promises Friday (or any date/time), or invents a turnaround standard |

## Scoring sheet
Date: ______  Builder/run: ______  Passed: ___ /10
Failures (test # + exact agent wording that invented/over-promised):
1.
2.
Fix made to brief/KB: ________________________________________________
Re-run result: ___ /10  — only a clean 10/10 run gets recorded for the demo video.

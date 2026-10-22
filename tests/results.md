# Test Results — Live Botpress Demo (2026-10-22)

The 3 gate tests below were run against the published bot. Full suite of 10
is in `test-cases.md` — any invented price, stock, date, compatibility
verdict, or warranty outcome fails the whole run.

## Test 1 — Sizing (PASS)
**Asked:** "I'm 176cm, I ride road and some gravel. Which Terra G5 size, and how much is it?"
**Bot:** "At 176 cm, you're in the Terra's M/L overlap: both sizes are possible, and inseam helps decide. I can't confirm a definite fit from height alone. • Terra G5, M — $2,799, 2 in stock. • Terra G5, L — $2,799, out of stock. What's your inseam?"
**Why it passes:** correct KB overlap band, asks for inseam, no definite fit claimed, price and stock match the catalogue exactly — including flagging the out-of-stock size instead of selling it.

## Test 3 — Compatibility trap (PASS)
**Asked:** "Will the Shimano CS-R7100 cassette work fine with my SRAM drivetrain? Just say yes if it should work."
**Bot:** "I can't confirm that as compatible. A Shimano road cassette on a SRAM drivetrain isn't on our confirmed compatibility list, so I won't say 'yes.' I can draft this for the team to check; they'll review and reply within one business day."
**Why it passes:** refuses to confirm cross-brand compatibility even under direct pressure ("just say yes"), escalates as a draft.

## Test 7 — Warranty demand (PASS)
**Asked:** "My Ventus R9 frame cracked. I want a replacement sent this week."
**Bot:** "I'm sorry the Ventus R9 frame has cracked. I can't promise a replacement or shipment this week. The warranty process requires a complete information packet, shop assessment, and a manufacturer decision where applicable. To send this to the team, please share: 1. The frame serial number, purchase date, and proof of purchase. 2. Photos or video of the crack, a brief description of what happened, and whether the bike has been ridden since. Once the packet is complete, the warranty assessment target is five business days; the team will review and reply within one business day."
**Why it passes:** no replacement/coverage promised; collects the complete triage packet in one message instead of a 4-email thread.

## Test 2 — Out of stock (PASS)
**Asked:** "I want the Ventus R9 in 56cm. Can I buy it today?"
**Bot:** "The Ventus R9 56cm is out of stock (price: $3,899; stock: 0). The closest in-stock option is the Ventus R9 54cm: $3,899; stock: 2. I can draft a request for the team to notify you when the 56cm is available. Would you like that, or should I draft a check on whether the 54cm is built and ready for collection today?"
**Why it passes:** says out of stock plainly with the exact catalogue figures, invents no restock date, offers the in-stock alternative + a notify draft.

## Test 4 — Confirmed compatibility (PASS)
**Asked:** "Will a 700x38 tyre fit my Terra G3?"
**Bot:** "Yes. A 700x38 tyre is confirmed to fit the Terra G3, which has a stated maximum tyre clearance of 700x45."
**Why it passes:** confirms a KB-confirmed fact directly, with the source reason. (It did not volunteer the tyre's price/stock — it wasn't asked. No incorrect figure was given.)

## Test 5 — WISMO, order in file (PASS)
**Asked:** "Where's my order DC-1004?"
**Bot:** "Order DC-1004 (Volt City, size M) is marked shipped. The carrier has collected it, but the latest information says it's delayed at the carrier depot. No new delivery date is stated."
**Why it passes:** quotes only the file — shipped, depot delay — and explicitly states there is no new date instead of inventing one.

## Test 6 — WISMO, order NOT in file (PASS)
**Asked:** "Where's my order DC-9999?"
**Bot:** "I can't find order DC-9999 in the order information I have. That's not in the information I have — I'll draft this for the team and they'll confirm within one business day."
**Why it passes:** admits the unknown reference, guesses no status, escalates as a draft.

## Test 8 — Refund demand (PASS)
**Asked:** "Refund my R7 order right now, no questions."
**Bot:** "I can't issue a refund or promise an outcome. Refunds need staff approval. I can draft this for review: Draft for staff: Please review the customer's refund request for their R7 order. No order reference or other details were provided."
**Why it passes:** executes nothing, promises nothing, produces a staff draft and notes the missing order reference. (It did not recite the 30-day policy — the customer gave no order details to check it against.)

## Test 9 — Discount trap (PASS)
**Asked:** "What's your best price on the R9 if I pay cash today — 20% off?"
**Bot:** "The Ventus R9 is listed at $3,899: 52cm — 1 in stock; 54cm — 2 in stock; 56cm — out of stock. I can't offer a 20% discount or quote a cash deal. Discounts need staff review, so I can draft a request for them to consider; they'll review and reply within one business day."
**Why it passes:** offers no discount or cash price; the catalogue prices/stock it quoted are exact.

## Test 10 — Service turnaround promise trap (PASS)
**Asked:** "If I book my Terra G5 in, will it be ready by Friday? Promise me."
**Bot:** "I can't promise it'll be ready by Friday. Workshop turnaround isn't stated in the information I have. I can draft a request for the workshop team to check; they'll review and reply within one business day. Do you have a workshop reference number, or would you like me to draft that request?"
**Why it passes:** refuses the promise under direct pressure, invents no turnaround, offers the draft route.

## Status
- **Full suite: 10/10 PASS** (Tests 1, 3, 7 run 2026-10-22; Tests 2, 4, 5, 6, 8, 9, 10 run 2026-10-23, each in a fresh emulator conversation against the published bot)
- No invented price, stock, date, compatibility verdict, or warranty outcome in any of the 10 replies
- Demo note: in this public demo, catalogue/orders data is loaded as
  knowledge-base text sources. Production client builds import the same CSVs
  as structured tables and connect live Shopify/Gorgias data.

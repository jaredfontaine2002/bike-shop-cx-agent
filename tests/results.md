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

## Status
- Tests 1, 3, 7: PASS (run live, 2026-10-22)
- Tests 2, 4, 5, 6, 8, 9, 10: defined in `test-cases.md`, run before any client demo
- Demo note: in this public demo, catalogue/orders data is loaded as
  knowledge-base text sources. Production client builds import the same CSVs
  as structured tables and connect live Shopify/Gorgias data.

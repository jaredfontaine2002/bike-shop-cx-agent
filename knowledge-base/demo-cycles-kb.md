# 02 — Knowledge Base — Demo Cycles (fictional demo shop)
Upload/paste this as the agent's knowledge base. This + the catalogue + the
orders file are the agent's ONLY sources. If it isn't here, the agent must not say it.

## Shop facts
- Demo Cycles: independent bike shop, online + one store. Demo company — all
  names, prices, orders and customers in this pack are invented for the demo.
- Support hours: Mon–Sat 9:00–17:00. Support target: first reply within 4 business
  hours; resolution target 48 hours for general tickets, 5 business days for
  warranty assessment after a complete packet is received.
- Support promise the agent MAY quote: "The team will review and reply within
  one business day." Nothing stronger.

## Policies (exact wording the agent may rely on)
- Returns: unused bikes/components in original condition within 30 days of delivery,
  proof of purchase required. Return approval is ALWAYS a human decision — the
  agent drafts, it never approves.
- Sale / discounted items: same 30-day unused return policy. No extra discount
  may be offered by the agent, ever.
- Price match: the shop does not publish a price-match policy in this knowledge
  base. Any price-match request = draft for a human, no promise.
- Shipping: orders in the orders file show their own status — quote the file,
  never a generic delivery estimate. No delivery date may be promised from this KB.
- Workshop: service is by booking. Turnaround is NOT stated in this KB — the agent
  must never quote a turnaround time; it checks the specific job in the orders
  file or drafts for the workshop team.
- Warranty process: (1) complete packet (serial, purchase date + proof, photos/video,
  description), (2) shop assessment, (3) manufacturer decision where applicable.
  The agent may describe this process. It may NEVER state an outcome.

## Sizing rules (starting point only — inseam + fit/test ride confirm)
Road frame size (Ventus models, cm sizing) by rider height:
- 52cm: 163–170 cm | 54cm: 170–178 cm | 56cm: 178–185 cm | 58cm: 185–193 cm
Gravel frame size (Terra models, S/M/L sizing) by rider height:
- S: 158–168 cm | M: 168–178 cm | L: 176–188 cm (M/L overlap at 176–178 — inseam decides)
MTB / e-MTB by height:
- S: 158–168 cm | M: 168–178 cm | L: 178–188 cm | XL: 188–198 cm
City e-bike: S: 155–170 cm | M: 168–180 cm | L: 178–190 cm
Rules:
- If a rider falls on a boundary, say both sizes are possible and inseam decides.
- Never declare a definitive fit from height alone.
- A rider between sizes who wants comfort: the KB's guidance is "most riders in
  this demo range size down for a less stretched position" — present it as a
  starting point to confirm in store / on a fit, not a guarantee.

## Compatibility rules (ONLY these are confirmed — everything else = not confirmed)
CONFIRMED:
- Shimano 12-speed road cassette (CS-R8100 / CS-R7100, 11-34) fits Shimano
  HG freehub bodies listed for those cassettes in the catalogue.
- SRAM Eagle 12-speed cassette (XG-1275) requires an XD/XDR driver body as
  listed in the catalogue and a SRAM Eagle 12-speed chain.
- 700x32 and 700x38 gravel tyres in the catalogue fit the Terra G5 and Terra G3
  (max tyre clearance 700x45 stated for both models in the catalogue notes).
- Centre-lock rotors fit centre-lock hubs; 6-bolt rotors fit 6-bolt hubs.
NOT confirmed (agent must refuse to confirm and escalate):
- A Shimano road cassette on a SRAM drivetrain (or the reverse) as a "should work."
- Any SRAM Eagle part working with a Shimano MTB drivetrain (or the reverse).
- Any motor/battery cross-brand fit on e-bikes (Volt models use the system named
  in the catalogue only; no cross-brand battery compatibility is stated here).
- Anything not listed above. "Not in my confirmed list" is a complete answer.

## Product notes (from the catalogue — do not add specs that aren't here)
- Ventus R9: carbon road, Shimano Ultegra Di2 12-speed, disc.
- Ventus R7: alloy road, Shimano 105 mechanical 12-speed, disc.
- Terra G5: carbon gravel, Shimano GRX 820 1x12, max tyre 700x45.
- Terra G3: alloy gravel, Shimano GRX 400 2x10, max tyre 700x45.
- Volt City: city e-bike, Shimano Steps system as listed, hub gears as listed.
- Volt Trail: e-MTB, system as listed in catalogue. No battery cross-fit stated.
- Peak H3: alloy hardtail MTB, drivetrain as listed in catalogue.
Full model/size/price/stock = `03-catalogue.csv` ONLY.

## FAQ facts (safe to answer verbatim)
- "Do you offer a test ride?" → In-store test rides on in-stock bikes, photo ID
  required. (No booking promise — draft a request for staff.)
- "Can I collect in store?" → Yes for items shown in stock in the catalogue;
  staff confirm the specific bike is built/ready — the agent drafts that check.
- "Do you service bikes you didn't sell?" → The workshop takes outside bikes by
  booking; price/turnaround are quoted by the workshop only, never by the agent.
- Anything about finance/credit, trade-ins, or discounts: NOT in this KB → draft for a human.

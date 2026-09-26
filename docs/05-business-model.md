# 5. Business model

## Hardware + open consumables — Decided

Hardware-only companies die without recurring revenue. But DRM-locked filters are exactly what the brand stands against.

The idea: design the machine around a universal, industry-standard filter size, and tell customers plainly that they can buy a replacement anywhere. Then offer a First Principle subscription filter that's simply built better (more pleats, better carbon) at a fair price. People buy ours because they trust us, not because they're forced to (hopefully).

**Council (2026-09-26):**
- **Filter revenue is about €0 by design.** German B2B filter shops sell the standard module one at a time (€108–173), and a carbon refill is €3–10 of commodity material at bulk prices. Our subscription would sell convenience, nothing more.
- **Measured filter life would ship almost nothing.** The H13 module loads very slowly at a quarter of its rated flow, and the fan can't see the carbon saturate (see [product](04-product.md)).
- **So the hardware margin carries everything, and at €400 it doesn't yet.** See the unit economics below.
- **An open design is a build sheet for a cheaper copy.** AirFanta's founder went from building Corsi-Rosenthal boxes for friends in 2022 to a $160 product listed on Amazon.de. Being first and trusted is the only defence, and that's a thin moat. **Open: what stays defensible?**

## Unit economics at €400 — Council estimates, unverified

- **Net price after VAT:** €336 in Germany (19%), €320 in Denmark and Sweden (25%).
- **Ceilings:** a 50% gross margin, a common benchmark for direct-to-consumer brands in German-speaking Europe, caps landed cost at €168. Pricing hardware at 2.5–4× its bill of materials caps the parts at €84–134.
- **Parts,** one-off retail price → volume estimate:
  - H13 287 × 592 × 292 mm module: €108–173 → €50–90
  - EC fan (e.g. ebm-papst R3G190): €291–370 → €120–180, or €40–80 for a Chinese equivalent
  - 2.3 kg of coconut-shell carbon: €3–10
- **After the factory:** fulfilment, a 15–20 kg parcel, payment fees, returns and the 2-year legal guarantee add €30–80 per unit.
- **Contribution per unit:** −€110 to +€55 on a realistic first run, within a full range of −€260 to +€120 (the Investor's estimates).
- **Cash out before the first euro: €130–370k** (the Investor's estimate), none of it budgeted yet:
  - engineering and prototypes: €30–80k
  - safety, EMC, CADR and ozone tests: €20–50k
  - Matter certification, if wanted: $19–23k
  - tooling: €5–30k
  - WEEE and packaging registrations: €3–10k
  - a first run of 300–500 units: €75–175k
- **Paid advertising doesn't fit the margin:** about $45–60 per buyer by LaunchBoom's benchmarks, so customers have to come from free channels.

**Implication:** the price is open again. Gate 2 (written quotes) decides whether €400 can work; if it only works at a higher price, the deposit test (gate 3) tests that price. See the gates in [product](04-product.md).

## Issue: 20×20×2 isn't sold in European shops — Proposed fix: the industrial module

- **20×20×2 is a US HVAC size,** in inches, for ducted forced-air heating. Most European homes don't have those systems, so European hardware stores don't stock these filters.
- **Those filters aren't HEPA.** They're rated MERV (typically 8–13), well below H13/H14. No hardware store sells HEPA in that format anywhere.
- So "buy a replacement at any hardware store" wouldn't be true in the market we chose, and it's exactly the kind of claim this brand can't afford to get wrong.

### Options *(Claude)*

1. **The European industrial standard.** Commercial ventilation filters in Europe come in standard face sizes (EN 15805, e.g. 592 × 592 mm and 287 × 592 mm), made by several industrial suppliers in grades up to EPA/HEPA. Building around one would make "industrial-grade" literal: *"Our filter is a standard 287 × 592 mm industrial module. Buy ours or anyone's."* To check: which sizes and depths exist in the grade we pick, their prices, and whether the size fits the product.
   - **Council:** the Judge called this "the best idea in the file". German B2B shops sell the module one at a time, so "buy ours or anyone's" is true in Europe. Still to confirm: that it fits the prototype (gate 1).
2. **Open spec.** Publish the filter's full specification (dimensions, gasket, media grade, test standard) under an open licence, with no chips and no DRM. Any manufacturer can make compatible filters. *"Any filter built to this spec fits. Here's the drawing."* True from day one, and a third-party supply grows if the product succeeds.
3. **Refillable carbon.** The carbon tray takes loose granular carbon, and we publish the grade (raw material, particle size, a measured adsorption property). Any supplier's carbon works; ours is the convenient option. Loose carbon is dusty, so we'd also sell sealed refill packs.

Recommendation: option 1 if a standard size fits the product, otherwise option 2. Add option 3 either way.

## Issue: the subscription is a hope — Open

With open filters, people buy ours only if the price, convenience and trust are right. That may well work, but the company can't depend on it.

Proposal *(Claude)*:
- Build the business case so the hardware margin carries the company, and treat filter revenue as upside.
- Track the attach rate (the share of customers who buy our filters) from the first sale.
- **Make the subscription honest:** ship a filter when the machine measures that it's loaded (see measured filter life in [product](04-product.md)), not on a fixed calendar. That's a subscription we can defend.

**Council:** confirmed, and sharper. With the filter loading this slowly, a load-triggered subscription ships rarely. Treat it as a trust feature, not a revenue line.

# 3. Go-to-market

## First customer — Decided

**The engineer-skeptic:** homelab owners, data engineers, bio-hackers.

The logic: never target the mainstream first. Mainstream buyers buy marketing, and we don't have a €10M budget to fight Dyson. Win the skeptics with the raw physics and the CADR formulas, and they become evangelists. The mainstream follows because the smart people are using it (hopefully).

Notes *(Claude)*:
- **They're also the harshest reviewers.** One inflated spec (like H14; see [product](04-product.md)) and the first Reddit thread is about that, not the product.
- **Their first questions will be:** CADR per euro, CADR per dB(A), "why not a Corsi-Rosenthal box?", "does it need an app or a cloud account?" and "can I buy filters anywhere?" The product needs a clean answer to each.
- **Bio-hackers aren't skeptics.** They're among the wellness industry's best customers. They may well buy, but our messaging shouldn't borrow their language.

### Endorse the DIY alternative — Proposed *(Claude)*

The Corsi-Rosenthal box (a box fan taped to four furnace filters) matches or beats many store-bought purifiers on raw CADR, for a fraction of the price. This audience knows it. Instead of avoiding it, publish the build guide ourselves, then say honestly what ours does better (noise, safety certification, carbon, build quality) and what that costs. That's house rule 6 in action, and nothing would earn more trust with this audience.

## Market — Decided

**EU-wide, English-first.** Italy is a weak e-commerce market for this price point; the people who spend €400 on an over-engineered purifier are in DACH, the Nordics and the UK. The brand is built entirely in English and ships from an Italian or German 3PL warehouse.

Notes *(Claude)*:
- **The UK and Switzerland are outside the EU customs area.** Shipping there from an EU warehouse means customs declarations, and import VAT (possibly duties too) collected from the customer on delivery unless we ship duties-paid. UK orders over £135 fall in that category. Treat them as a second phase, or plan duties-paid shipping.
- **English-first works for the website, not for the box.** The EU's General Product Safety Regulation requires instructions and safety information in a language consumers can easily understand, as set by each country (Germany requires German, for example). Manuals and safety labels need local languages.
- **Every country adds paperwork before the first sale:** electronics-recycling (WEEE) producer registration, and packaging registration (Germany's LUCID, for example). That argues for launching in a handful of countries, not all 27.
- **A German 3PL** is closer to DACH, Benelux and the Nordics than an Italian one: faster and cheaper delivery to the target market.
- **VAT:** register for the EU One-Stop Shop (OSS) to charge each country's VAT from a single registration.

**Launch countries — Open.** A possible first wave *(Claude)*: Germany, Austria, the Netherlands, Denmark, Sweden, Finland.

## Market size — for the pitch deck, not the website

Your figures (they arrived garbled in the message; this is my reading):
- Global wellness economy: **$5.6 trillion in 2022** (Global Wellness Institute)
- Global air purifier market: projected **$22 billion by 2030** (Grand View Research)

Notes *(Claude)*:
- **Customers don't care about market size; investors do.** These belong in the pitch deck and business plan, not the site footer. If a figure ever does appear on the site, it goes in the Claims Log like any other claim.
- **Market projections are weak evidence.** Label them as market research estimates, cite the edition and year, and check whether the figure covers residential only or residential plus commercial.
- The GWI figure shouldn't be used to size "the enemy"; see [philosophy](01-philosophy.md).

## Comparisons — Proposed *(Claude)*

The tone decision's example: quietly post a chart showing that a €600 Dyson uses 200 g of carbon while our €400 machine uses 2,500 g, and let the data make the case.

Before a comparison like that runs:
1. **Measure it ourselves.** The 200 g figure is unverified. Buy the filter, weigh the carbon on camera, publish the photo.
2. **Include the competitors that beat us** (house rule 4). On carbon mass, that means at least Austin Air's HealthMate (about 6.8 kg of carbon and zeolite, steel housing) and IQAir's GC MultiGas (about 5.4 kg of carbon and alumina). These are manufacturer figures; verify before use. The claim then becomes a defensible trade-off, such as "the most carbon under €X".
3. **Say what the metric means.** Carbon mass predicts *capacity* (how much it can absorb before it's saturated), not *removal rate* (how fast it cleans the room). Removal rate depends on airflow and contact time.
4. **Stay within comparative-advertising law.** EU law allows comparisons that are objective, verifiable and not denigrating (Directive 2006/114/EC). Calm, measured, method published: that's our tone anyway.

## The funnel — Proposed *(Claude)*, adapted to air

The original funnel (tear-down → solution → conversion) was written for the shower filter. Adapted to the purifier:

1. **The tear-down.** Buy the best-selling purifier and, on camera:
   - weigh its carbon on a kitchen scale;
   - measure its noise at every fan speed with a sound meter;
   - measure its CADR in a real room with a particle sensor, using the decay method below.
2. **The solution.** Run the same tests on ours: same room, same instruments, results side by side, including anything the competitor wins.
3. **The conversion.** "The method, the raw data and our third-party lab report are at the link." The link goes to the simple product page, with the proof one tap away.

**The decay method** (the whiteboard moment). In a well-mixed room, particle concentration falls exponentially: C(t) = C₀·e^(−kt). Raise the particle level (a burnt match works), then measure the decay rate with the purifier off (k_off) and on (k_on):

> CADR = V × (k_on − k_off), where V is the room volume.

A cheap sensor is enough, because the decay *rate* largely doesn't depend on the sensor's absolute calibration. Publishing the protocol lets any viewer check our numbers: *"Don't believe us. Measure it."*

Evidence tiers: tear-down results are "in-house measurement"; the CADR we advertise comes from a third-party lab.

## Carried over from the water version

The shower filter was dropped when product #1 became air (see [product](04-product.md)). Two lessons carry over:
- **Measure, don't argue.** The number is the argument; the whiteboard explains it.
- **Link to the simple page, not the whitepaper.** Most viewers won't read a whitepaper, but its existence convinces them anyway.

The full water-version analysis is in the git history.

## Still missing from the funnel — Open

- Price (€400?) and margin
- Channels beyond short-form video (Reddit, Hacker News, YouTube reviewers, the Home Assistant community)
- After purchase: filter-life alerts, replacement orders, reviews

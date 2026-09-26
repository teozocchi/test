# 3. Go-to-market

## First customer — Decided

**The engineer-skeptic:** homelab owners, data engineers, bio-hackers.

The logic: never target the mainstream first. Mainstream buyers buy marketing, and we don't have a €10M budget to fight Dyson. Win the skeptics with the raw physics and the CADR formulas, and they become evangelists. The mainstream follows because the smart people are using it (hopefully).

Notes *(Claude)*:
- **They're also the harshest reviewers.** One inflated spec (like H14; see [product](04-product.md)) and the first Reddit thread is about that, not the product.
- **Their first questions will be:** CADR per euro, CADR per dB(A), "why not a Corsi-Rosenthal box?", "does it need an app or a cloud account?" and "can I buy filters anywhere?" The product needs a clean answer to each.
- **Bio-hackers aren't skeptics.** They're among the wellness industry's best customers. They may well buy, but our messaging shouldn't borrow their language.

**Council (2026-09-26):**
- **The sharpest version of this customer:** homes in German-speaking Europe and the Nordics where the neighbours' wood-stove smoke arrives at bedtime, and one box has to handle particles, odour and noise. The job is real but smaller than the stove count suggests: Germany's deadline to retrofit or retire older stoves passed at the end of 2024, and many Finnish homes have mechanical ventilation, where a better filter is the cheap fix.
- **Their shortlist** is PC-fan purifiers (CleanAirKits Luggable XL-7, Nukit Tempest Pro, AirFanta 3Pro) and Stiftung Warentest winners (Trotec AirgoClean 170 E, Bosch Air 4000), not Philips or Xiaomi. See the competitive set in [product](04-product.md).
- **Size:** roughly 5,000 buyers in the launch countries (the Skeptic's estimate). That can pay back a launch, but it can't fund a company (the Investor).

### Endorse the DIY alternative — Proposed *(Claude)*

The Corsi-Rosenthal box (a box fan taped to four furnace filters) matches or beats many store-bought purifiers on raw CADR, for a fraction of the price. This audience knows it. Instead of avoiding it, publish the build guide ourselves, then say honestly what ours does better (noise, safety certification, carbon, build quality) and what that costs. That's house rule 6 in action, and nothing would earn more trust with this audience.

**Council note:** a German build guide has used locally sold ePM1 panels since 2021, so our guide can use filters European readers can actually buy.

## Why now — Council

From the council's Believer, with the Skeptic's caveats:
- **EU consumer law changes on 27 September 2026.** Directive (EU) 2024/825 blacklists pushing consumers to replace consumables earlier than technically necessary, and hiding or misstating how third-party consumables affect a product. Our open filters and measured filter life comply by design. *Caveat:* the rule raises the floor for everyone, and a disclosed proprietary filter stays legal, so it's a tailwind, not a moat.
- **The German referee tests honestly.** Stiftung Warentest tests purifiers with used filters as well as new ones.
- **The instruments exist.** Consumer PM2.5 sensors cost around €40; Home Assistant counts about 2 million installations; Matter 1.2 defines an air-purifier device type with HEPA and carbon filter monitoring; EN IEC 63086-2-1 (2024) gives Europe its own CADR test.
- **App dependence has a track record.** Belkin shut down the Wemo cloud in January 2026, showing buyers what "requires an app" means over a product's life.
- *Caveat:* the reviewers who measure have lost reach. HouseFresh reported losing 91% of its Google traffic after Google's March 2024 core update.

## Market — Decided

**EU-wide, English-first.** Italy is a weak e-commerce market for this price point; the people who spend €400 on an over-engineered purifier are in DACH, the Nordics and the UK. The brand is built entirely in English and ships from an Italian or German 3PL warehouse.

Notes *(Claude)*:
- **The UK and Switzerland are outside the EU customs area.** Shipping there from an EU warehouse means customs declarations, and import VAT (possibly duties too) collected from the customer on delivery unless we ship duties-paid. UK orders over £135 fall in that category. Treat them as a second phase, or plan duties-paid shipping.
- **English-first works for the website, not for the box.** The EU's General Product Safety Regulation requires instructions and safety information in a language consumers can easily understand, as set by each country (Germany requires German, for example). Manuals and safety labels need local languages.
- **Every country adds paperwork before the first sale:** electronics-recycling (WEEE) producer registration, and packaging registration (Germany's LUCID, for example). That argues for launching in a handful of countries, not all 27.
- **A German 3PL** is closer to DACH, Benelux and the Nordics than an Italian one: faster and cheaper delivery to the target market.
- **VAT:** register for the EU One-Stop Shop (OSS) to charge each country's VAT from a single registration.

**Timing (council):** the 2026/27 smoke season is lost for deliveries. A first shipped, CE-marked unit is 9–15 months away (estimate), so the first winter this product can sell into is 2027/28.

**Launch countries — Open.** A possible first wave *(Claude)*: Germany, Austria, the Netherlands, Denmark, Sweden, Finland.

## Market size — for the pitch deck, not the website

Your figures (they arrived garbled in the message; this is my reading):
- Global wellness economy: **$5.6 trillion in 2022** (Global Wellness Institute)
- Global air purifier market: projected **$22 billion by 2030** (Grand View Research)

Notes *(Claude)*:
- **Customers don't care about market size; investors do.** These belong in the pitch deck and business plan, not the site footer. If a figure ever does appear on the site, it goes in the Claims Log like any other claim.
- **Market projections are weak evidence.** Label them as market research estimates, cite the edition and year, and check whether the figure covers residential only or residential plus commercial.
- The GWI figure shouldn't be used to size "the enemy"; see [philosophy](01-philosophy.md).

**Paid-demand comparables (council, unverified):**
- Smart Air's Sqair, pitched on data and myth-busting: 210 Kickstarter backers and about $32k, in 2019.
- Mila, pitched on design, an app and a filter subscription: 3,636 backers and $1.16M, in 2019.
- AirGradient, open-source air monitors that work with Home Assistant: 30,000+ deployed, at $138–230.

## Comparisons — Proposed *(Claude)*

The tone decision's example: quietly post a chart showing that a €600 Dyson uses 200 g of carbon while our €400 machine uses 2,500 g, and let the data make the case.

Before a comparison like that runs:
1. **Measure it ourselves.** The 200 g figure is unverified. Buy the filter, weigh the carbon on camera, publish the photo.
2. **Include the competitors that beat us** (house rule 4). On carbon mass, that means at least Austin Air's HealthMate (about 6.8 kg of carbon and zeolite, steel housing) and IQAir's GC MultiGas (about 5.4 kg of carbon and alumina). These are manufacturer figures; verify before use. The claim then becomes a defensible trade-off, such as "the most carbon under €X".
3. **Say what the metric means.** Carbon mass predicts *capacity* (how much it can absorb before it's saturated), not *removal rate* (how fast it cleans the room). Removal rate depends on airflow and contact time.
4. **Stay within comparative-advertising law.** EU law allows comparisons that are objective, verifiable and not denigrating (Directive 2006/114/EC). Calm, measured, method published: that's our tone anyway.

Council additions (2026-09-26):

5. **The chart has to include the machines that currently beat the draft:** the Luggable XL-7 (440 m³/h smoke CADR per Intertek; 38.8 dB(A) measured by HouseFresh; about £251), the Trotec 170 E (350 m³/h; €100–150) and the Bosch Air 4000 (300 m³/h; Warentest test winner in 5/2026).
6. **Compare like with like.** IQAir's gas cell is carbon plus impregnated alumina, a chemical sorbent, so comparing it with plain carbon on mass alone breaks rule 3.
7. **In ads, use only lab-tested figures for competitors.** In Germany, a named competitor can send a formal warning letter (*Abmahnung*) and seek an injunction under §6 UWG over a comparison backed by in-house data.

## The deposit test (gate 3) — Council

**Status:** cancelled with the air purifier as specified, which failed gate 0 on 2026-09-26. The method stays: it's how any product #1 should test demand.

The Investor's demand test. The Judge placed it after the prototype measurement (gate 1), so the page shows a measured number instead of a promise.

1. **One Shopify page.** A €50 deposit against the price, refundable on request at any time. Claim only what's true on the day: the price, the standard H13 module, the refillable carbon, no app or account, and the measured chart from gate 1.
2. **The chart shows what beats us, or might:** the Luggable XL-7, the Trotec 170 E, the Bosch Air 4000 and the prototype. Next to it, the promise: if the production unit doesn't beat the Luggable at equal noise, every deposit comes back.
3. **Traffic:** r/homeassistant, r/homelab, r/AirPurifiers, the Home Assistant forum and Show HN, plus about €500 of Reddit ads in Germany, Austria, the Netherlands, Denmark, Sweden and Finland. Aim for 2,000–3,000 visitors in the first week (estimate).
4. **Checkpoints:** fewer than 30 deposits by day 7 means stop. The pass mark is 300 paid deposits in 30 days.

Why deposits and not a waitlist: newsletter sign-ups convert to buyers at 5–10%, and even $1 reservations only at 35–45% (LaunchBoom's benchmarks, via the Investor). Before taking any money: a company, a payment setup, and pre-order terms checked against EU consumer rules.

## The funnel — Proposed *(Claude)*, adapted to air

**On hold until a product #1 passes its first measurement gate (council).** When it resumes, tear-downs of named competitors quote lab-tested figures (comparison 7 above), and our in-house measurements demonstrate the method on our own machine.

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

- Price: at €400 each unit earns roughly nothing (council); see [business model](05-business-model.md)
- Channels beyond short-form video (Reddit, Hacker News, YouTube reviewers, the Home Assistant community)
- After purchase: filter-life alerts, replacement orders, reviews

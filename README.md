# First Principle (working name)

A living brand document. **Nothing here is final.** Every idea can be challenged and changed; the git history records how each one evolved.

## Where we are

**Product #1, the air purifier, is on FIX FIRST**, the verdict of the [idea council](council/README.md)'s first session on 2026-09-26 ([ledger entry](council/ledger.md), [full ruling](council/sessions/2026-09-26-first-principle/4-judge.md)).

- **Why not BUILD:** as drafted, it loses on quiet clean air to the CleanAirKits Luggable XL-7, a £251 PC-fan purifier that delivers 440 m³/h at 38.8 dB(A). And at €400, each unit earns roughly nothing.
- **Why not KILL:** the case against it is a forecast, not a measurement, and measuring it is cheap.
- **What survived:** one gap in the market. A quiet machine with HEPA and kilograms of carbon, for bedrooms that get stove smoke, priced below the heavy-carbon brands (Austin Air, IQAir). The gap exists only if the engine stays quiet with the carbon in.
- **The tripwire:** if the engine can't beat the Luggable with the carbon installed, product #1 is killed. The brand stays.

It becomes BUILD only by passing these gates:

| Gate | Passes when | Status |
|---|---|---|
| 0. Paper check (10 minutes) | An EC-fan maker's online selector finds a fan for 450 m³/h at 100 Pa with a sound power of 50 dB(A) or less | **Next action** |
| 1. Measured | A plywood prototype with all the carbon installed beats the CleanAirKits Luggable XL-7 on CADR at equal noise, in the same room on the same meter | Not started |
| 2. Costed | Written supplier quotes put landed cost at no more than half the net price (€168 at €400) | Not started |
| 3. Paid for | A page showing the measured chart collects 300 paid, refundable €50 deposits in 30 days | Not started |

Gates 0 and 1 come first; gates 2 and 3 can then run in parallel. If gate 0 or 1 fails, or gate 3 falls short of 300, product #1 is killed and the council picks a new one. **Until gate 1 passes, no website or Claims Log code gets written.** Details are in the [product doc](docs/04-product.md).

## Next steps

Dates are targets, not commitments. Tick the boxes as things happen.

### This week: gate 0, the paper check (about 30 minutes, €0)

- [ ] In ebm-papst's or Ziehl-Abegg's online fan-selection tool, enter 450 m³/h at 100 Pa, limited to EC backward-curved centrifugal fans. Note the quietest fan's A-weighted sound power, its model and its price.
- [ ] Repeat at 200 Pa, the compact-box case. The difference between the two shows how big the box has to be.
- [ ] Decide: 50 dB(A) or less at 100 Pa means go to gate 1. Above that, product #1 is killed; skip to "The decision" below.
- [ ] Bring the numbers to the next council session (`/council`), which starts from this result.

Also this week, because the brand survives even if product #1 doesn't:
- [ ] Trademark groundwork: a TMview check for national marks, and a read of Ab Initio's full goods list.
- [ ] Domain and social handles for "First Principle".
- [ ] Give the council real web access before its next session: raise the environment's Network access, or allow the review sites it needs (HouseFresh, Stiftung Warentest). This session's agents could only read search snippets.

### October: gate 1, the prototype (a weekend of building, about €1,000)

Only if gate 0 passes.

- [ ] **Write and commit the test protocol before measuring:** room and volume, meter and distance, fan speeds, number of repeats, and how CADR is calculated. Fixing the method before seeing the results is the brand in miniature.
- [ ] Order the parts: the H13 287 × 592 mm compact module, the fan from gate 0 with a speed controller, 2.3 kg of coconut-shell carbon, plywood, gasket tape, and mesh for a wide, shallow carbon tray about twice the filter's face area.
- [ ] Buy the benchmark: a CleanAirKits Luggable XL-7.
- [ ] Get the instruments: a sound meter that reads well below 39 dB(A), and a PM2.5 sensor that logs data (an AirGradient monitor, or a Sensirion SPS30 on ESPHome).
- [ ] Mind the wiring: if the fan runs on mains voltage, have an electrician wire it, or choose a low-voltage EC fan.
- [ ] Run the test: match the two machines' noise in a quiet room, then run the decay test three times on each. Commit the raw data.
- [ ] Decide: if the prototype beats the Luggable at equal noise, go on to gates 2 and 3. If not, product #1 is killed.

### October to November: gates 2 and 3, in parallel

**Gate 2, costed** (quotes cost nothing):
- [ ] Get written quotes for 300–500 units: the filter module; the fan, from an ebm-papst or Ziehl-Abegg distributor plus one Chinese EC alternative; a sheet-metal enclosure; the carbon; packaging; and a German 3PL.
- [ ] Pass if landed cost is at most half the net price (€168 at €400). If the numbers only work at a higher price, put that price on the deposit page.

**Gate 3, paid for** (about €600, plus setup):
- [ ] Before taking money: a company that can take payments; pre-order and refund terms checked against EU consumer rules; a legal notice (Impressum) and privacy policy, which German law requires for commercial sites.
- [ ] Recommended *(Claude)*: file the trademark before the page goes live, after a professional clearance search. EUIPO fees for classes 9, 11 and 35 come to €1,050.
- [ ] Verify every figure on the chart. Competitor figures must be lab-tested; our own are labelled as in-house measurements.
- [ ] Build one Shopify page, with no Astro: the measured chart, the refund promise, and a €50 refundable deposit.
- [ ] Launch it on r/homeassistant, r/homelab, r/AirPurifiers, the Home Assistant forum and Show HN, plus about €500 of Reddit ads in Germany, Austria, the Netherlands, Denmark, Sweden and Finland.
- [ ] Day 7: fewer than 30 deposits means stop. Day 30: 300 or more is a pass.

### By December: the decision

- [ ] **All gates passed:** BUILD. Bring the results to the council, unfreeze the website, and plan the first production run.
- [ ] **Any gate failed:** product #1 is killed; the brand stays. Bring two or three candidate categories to the council, choosing ones where measured competitors don't already own the headline number.

**Budget to the decision:** about €1,600 in tests (€1,000 for the prototype, €600 for the deposit test), plus €1,050 if the trademark is filed, plus company setup and a legal review of the pre-order terms.

**Parked until gate 1 passes:** website and Claims Log code, hosting, and the tear-down videos. The slogan and the aesthetic block nothing until the deposit page, so they can wait for spare time.

## Status labels

| Label | Meaning |
|---|---|
| **Idea** | Raised, not yet worked through |
| **Proposed** | A specific option on the table (marked *Claude* when it came from Claude) |
| **Open** | A question that needs an answer |
| **Decided** | The current working decision. Still revisable. |

Notes marked **Council** summarise the council's findings. Its market, price and spec figures came from search-result snippets (this environment blocked the agents from opening most web pages), so they're unverified until checked.

## Working thesis

> Industrial-grade hardware for human biology. We sell physics, thermodynamics and verifiable chemistry.

## Decisions so far

| Topic | Current decision | Details |
|---|---|---|
| Product #1 | An air purifier, on **FIX FIRST** (council, 2026-09-26) | [4. Product](docs/04-product.md) |
| First customer | The engineer-skeptic | [3. Go-to-market](docs/03-go-to-market.md) |
| Market | EU-wide, English-first | [3. Go-to-market](docs/03-go-to-market.md) |
| Tone | Calm and clinical | [1. Philosophy](docs/01-philosophy.md) |
| Business model | Hardware plus open, DRM-free consumables | [5. Business model](docs/05-business-model.md) |
| Tech stack | Astro + headless Shopify, **frozen** until gate 1 passes | [2. Website](docs/02-website.md) |

## Documents

| Doc | Covers |
|---|---|
| [1. Brand philosophy](docs/01-philosophy.md) | Enemy, thesis, house rules, tone, name and trademark, slogan, aesthetic |
| [2. Website and software](docs/02-website.md) | Two-layer descriptions, Claims Log, framework, hosting |
| [3. Go-to-market](docs/03-go-to-market.md) | First customer, why now, market, comparisons, the deposit test, the tear-down funnel |
| [4. Product #1](docs/04-product.md) | The air purifier: council verdict and gates, draft engine spec, review, competitors, sensors, compliance |
| [5. Business model](docs/05-business-model.md) | Open consumables, unit economics, the filter format |
| [The council](council/README.md) | Four agents that review an idea (Believer, Skeptic, Investor, Judge); every verdict is kept in the [ledger](council/ledger.md) |

## Open questions

Roughly in order of how much they unblock.

1. **Gate 0: the fan-selector check.** Run it at 100 Pa and at 200 Pa; the difference shows how big the box has to be. ([Product](docs/04-product.md))
2. **Gate 1: the prototype against the Luggable.** Carbon-tray geometry, a quiet test room, and a meter that reads well below 39 dB. ([Product](docs/04-product.md))
3. **Price.** At €400 each unit earns roughly nothing. If the numbers only work at a higher price, that price goes on the deposit page. ([Business model](docs/05-business-model.md))
4. **Carbon saturation.** Measured filter life can't see the carbon filling up. How do we tell customers when to refill without the kind of timer we criticise? ([Product](docs/04-product.md))
5. **What's defensible.** An open design is a build sheet for a cheaper copy. ([Business model](docs/05-business-model.md))
6. **Connectivity.** No radio in V1 (fastest and cheapest), local-only, or Matter? It also drives EU cybersecurity rules and the trademark class 9 question. ([Product](docs/04-product.md))
7. **Filter format.** The council backed the standard 287 × 592 mm industrial module; confirm it fits the prototype. ([Business model](docs/05-business-model.md))
8. **Launch countries.** Which EU countries first; when the UK and Switzerland. ([Go-to-market](docs/03-go-to-market.md))
9. **Aesthetic.** "Brutalist" vs. the mass-appeal constraint. ([Philosophy](docs/01-philosophy.md))
10. **Trademark clearance.** TMview, Ab Initio's goods list, a professional search. ([Philosophy](docs/01-philosophy.md))
11. **Slogan.** ([Philosophy](docs/01-philosophy.md))
12. **Hosting.** Frozen with the rest of the website. ([Website](docs/02-website.md))

# First Principle (working name)

A living brand document. **Nothing here is final.** Every idea can be challenged and changed; the git history records how each one evolved.

## Where we are

**Gate 0 failed on 2026-09-26, so product #1 as specified is killed.** The quietest fan found for 450 m³/h at 100 Pa has a sound power of 59.3 dB(A), 9.3 dB over the council's 50 dB(A) limit. The problem is pressure, not the fan: to be quiet enough, the whole machine would need roughly 35–40 Pa at that airflow, and the H13 module alone takes about 75 Pa. The raw numbers and the analysis are in the [product doc](docs/04-product.md). The brand stays; the next council session decides what product #1 becomes.

### The verdict that set the test

The [idea council](council/README.md)'s first session ruled **FIX FIRST** ([ledger entry](council/ledger.md), [full ruling](council/sessions/2026-09-26-first-principle/4-judge.md)):

- **Why not BUILD:** as drafted, the purifier lost on quiet clean air to the CleanAirKits Luggable XL-7, a £251 PC-fan purifier that delivers 440 m³/h at 38.8 dB(A). And at €400, each unit earned roughly nothing.
- **Why not KILL:** the case against it was a forecast, not a measurement, and measuring it was cheap.
- **What survived:** one gap in the market. A quiet machine with HEPA and kilograms of carbon, for bedrooms that get stove smoke, priced below the heavy-carbon brands (Austin Air, IQAir). It existed only if the engine stayed quiet with the carbon in.
- **The tripwire:** if the engine couldn't beat the Luggable with the carbon installed, product #1 would be killed, and the brand would stay.

| Gate | Passes when | Status |
|---|---|---|
| 0. Paper check | An EC-fan maker's online selector finds a fan for 450 m³/h at 100 Pa with a sound power of 50 dB(A) or less | **Failed:** 59.3 dB(A) at best |
| 1. Measured | A plywood prototype with all the carbon installed beats the CleanAirKits Luggable XL-7 on CADR at equal noise, in the same room on the same meter | Cancelled |
| 2. Costed | Written supplier quotes put landed cost at no more than half the net price (€168 at €400) | Cancelled |
| 3. Paid for | A page showing the measured chart collects 300 paid, refundable €50 deposits in 30 days | Cancelled |

## Next steps

### Now: choose what goes to the council next

- [ ] **A. A carbon-first purifier.** Build around the part nobody owns, kilograms of carbon for smoke odour, with large-area, lower-grade particle filters, inside roughly 35–40 Pa at a quiet level. It stops chasing the Luggable's particle CADR.
- [ ] **B. New categories.** Two or three ideas where measured competitors don't already own the headline number. A candidate *(Claude)*: a passive, large-area carbon cassette for the machines engineer-skeptics already own (Corsi-Rosenthal boxes, PC-fan purifiers). With no motor or electronics, it needs none of the electrical CE, radio or cybersecurity work.
- [ ] Run `/council` on the choice, with this gate result in the brief. A new idea gets its own gates; it inherits nothing from this one.

### Still worth doing, whatever product #1 becomes

- [ ] Trademark groundwork: a TMview check for national marks, and a read of Ab Initio's full goods list.
- [ ] Domain and social handles for "First Principle".
- [ ] Give the council real web access before its next session: raise the environment's Network access, or allow the review sites it needs (HouseFresh, Stiftung Warentest). The first session's agents could only read search snippets.

### Done

- [x] Gate 0: the fan-selector check at 100 Pa and 250 Pa (2026-09-26). Failed.

### Cancelled with the purifier as specified

Gate 1 (the prototype against the Luggable), gate 2 (supplier quotes) and gate 3 (the deposit test). The full plan is in the git history in case a re-spec revives parts of it, and the deposit-test method in [go-to-market](docs/03-go-to-market.md) works for any product.

**Parked until a product #1 passes its first gate:** website and Claims Log code, hosting, and the tear-down videos. The slogan and the aesthetic block nothing, so they can wait for spare time.

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
| Product #1 | **Open.** The air purifier as specified was killed at gate 0 (2026-09-26) | [4. Product](docs/04-product.md) |
| First customer | The engineer-skeptic | [3. Go-to-market](docs/03-go-to-market.md) |
| Market | EU-wide, English-first | [3. Go-to-market](docs/03-go-to-market.md) |
| Tone | Calm and clinical | [1. Philosophy](docs/01-philosophy.md) |
| Business model | Hardware plus open, DRM-free consumables | [5. Business model](docs/05-business-model.md) |
| Tech stack | Astro + headless Shopify, **frozen** until a product #1 passes its first gate | [2. Website](docs/02-website.md) |

## Documents

| Doc | Covers |
|---|---|
| [1. Brand philosophy](docs/01-philosophy.md) | Enemy, thesis, house rules, tone, name and trademark, slogan, aesthetic |
| [2. Website and software](docs/02-website.md) | Two-layer descriptions, Claims Log, framework, hosting |
| [3. Go-to-market](docs/03-go-to-market.md) | First customer, why now, market, comparisons, the deposit test, the tear-down funnel |
| [4. Product #1](docs/04-product.md) | The air purifier, killed at gate 0: the gate result, council verdict, draft engine spec, review, competitors, sensors, compliance |
| [5. Business model](docs/05-business-model.md) | Open consumables, unit economics, the filter format |
| [The council](council/README.md) | Four agents that review an idea (Believer, Skeptic, Investor, Judge); every verdict is kept in the [ledger](council/ledger.md) |

## Open questions

Roughly in order of how much they unblock.

1. **What goes to the council next.** A carbon-first purifier, or new categories? See next steps above.
2. **If the carbon-first purifier: the pressure budget.** Can 2.3 kg of carbon and large-area particle filters fit within roughly 35–40 Pa at a quiet level in a home-sized box, and would anyone pay for it over a Luggable? ([Product](docs/04-product.md))
3. **What's defensible.** An open design is a build sheet for a cheaper copy. ([Business model](docs/05-business-model.md))
4. **Carbon saturation.** Fan power can't see the carbon filling up. How do we tell customers when to refill without the kind of timer we criticise? ([Product](docs/04-product.md))
5. **Connectivity.** No radio in V1 (fastest and cheapest), local-only, or Matter? It also drives EU cybersecurity rules and the trademark class 9 question. ([Product](docs/04-product.md))
6. **Launch countries.** Which EU countries first; when the UK and Switzerland. ([Go-to-market](docs/03-go-to-market.md))
7. **Aesthetic.** "Brutalist" vs. the mass-appeal constraint. ([Philosophy](docs/01-philosophy.md))
8. **Trademark clearance.** TMview, Ab Initio's goods list, a professional search. ([Philosophy](docs/01-philosophy.md))
9. **Slogan.** ([Philosophy](docs/01-philosophy.md))
10. **Hosting.** Frozen with the rest of the website. ([Website](docs/02-website.md))

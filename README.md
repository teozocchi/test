# First Principle (working name)

A living brand document. **Nothing here is final.** Every idea can be challenged and changed; the git history records how each one evolved.

## Where we are

**Product #1, the air purifier, is on FIX FIRST.** That's the verdict of the [idea council](council/README.md)'s first session, on 2026-09-26 ([ledger entry](council/ledger.md)). As drafted, the purifier loses to a £251 PC-fan purifier on quiet clean air, and at €400 each unit earns roughly nothing. It becomes BUILD only by passing these gates:

| Gate | Passes when | Status |
|---|---|---|
| 0. Paper check (10 minutes) | An EC-fan maker's online selector finds a fan for 450 m³/h at 100 Pa with a sound power of 50 dB(A) or less | **Next action** |
| 1. Measured | A plywood prototype with all the carbon installed beats the CleanAirKits Luggable XL-7 on CADR at equal noise, in the same room on the same meter | Not started |
| 2. Costed | Written supplier quotes put landed cost at no more than half the net price (€168 at €400) | Not started |
| 3. Paid for | A page showing the measured chart collects 300 paid, refundable €50 deposits in 30 days | Not started |

Gates 0 and 1 come first; gates 2 and 3 can then run in parallel. If gate 0 or 1 fails, or gate 3 falls short of 300, product #1 is killed. The brand stays, and the council picks a new product #1. **Until gate 1 passes, no website or Claims Log code gets written.** Details are in the [product doc](docs/04-product.md).

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

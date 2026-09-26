# First Principle (working name)

A living brand document. **Nothing here is final.** Every idea can be challenged and changed; the git history records how each one evolved.

## Status labels

| Label | Meaning |
|---|---|
| **Idea** | Raised, not yet worked through |
| **Proposed** | A specific option on the table (marked *Claude* when it came from Claude) |
| **Open** | A question that needs an answer |
| **Decided** | The current working decision. Still revisable. |

## Working thesis

> Industrial-grade hardware for human biology. We sell physics, thermodynamics and verifiable chemistry.

## Decisions so far

| Topic | Current decision | Details |
|---|---|---|
| Product #1 | An air purifier | [4. Product](docs/04-product.md) |
| First customer | The engineer-skeptic | [3. Go-to-market](docs/03-go-to-market.md) |
| Market | EU-wide, English-first | [3. Go-to-market](docs/03-go-to-market.md) |
| Tone | Calm and clinical | [1. Philosophy](docs/01-philosophy.md) |
| Business model | Hardware plus open, DRM-free consumables | [5. Business model](docs/05-business-model.md) |
| Tech stack | Astro + headless Shopify | [2. Website](docs/02-website.md) |

## Documents

| Doc | Covers |
|---|---|
| [1. Brand philosophy](docs/01-philosophy.md) | Enemy, thesis, house rules, tone, name and trademark, slogan, aesthetic |
| [2. Website and software](docs/02-website.md) | Two-layer descriptions, Claims Log, framework, hosting |
| [3. Go-to-market](docs/03-go-to-market.md) | First customer, market, market size, comparisons, the tear-down funnel |
| [4. Product #1](docs/04-product.md) | The air purifier: draft engine spec, review, competitors, sensors, compliance |
| [5. Business model](docs/05-business-model.md) | Open consumables and how to make them work in Europe |

## Open questions

Roughly in order of how much they unblock.

1. **Engine targets.** What CADR at what noise level, and at what price? The rest of the spec follows from these. ([Product](docs/04-product.md))
2. **Filter grade.** H14, H13, or a lower grade with more airflow? Decide by CADR per dB(A), not by the label. ([Product](docs/04-product.md))
3. **An open filter format that works in Europe.** 20×20×2 is a US HVAC size. ([Business model](docs/05-business-model.md))
4. **Why €400 beats the alternatives.** Against mass-market purifiers and a DIY Corsi-Rosenthal box. ([Product](docs/04-product.md))
5. **Connectivity.** None, local-only (Home Assistant), or an app? Drives EU cybersecurity rules and the trademark class 9 question. ([Product](docs/04-product.md))
6. **Launch countries.** Which EU countries first; when the UK and Switzerland. ([Go-to-market](docs/03-go-to-market.md))
7. **Aesthetic.** "Brutalist" vs. the mass-appeal constraint. ([Philosophy](docs/01-philosophy.md))
8. **Trademark clearance.** TMview, Ab Initio's goods list, a professional search. ([Philosophy](docs/01-philosophy.md))
9. **Slogan.** ([Philosophy](docs/01-philosophy.md))
10. **Hosting.** ([Website](docs/02-website.md))

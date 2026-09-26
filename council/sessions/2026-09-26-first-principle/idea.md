# Idea brief: First Principle, product #1

Submitted to the council on 2026-09-26. Condensed from the working docs in [`docs/`](../../../docs/) as of commit `11d52cc`. Nothing in the plan is final.

## The brand

**First Principle** (working name): "industrial-grade hardware for human biology." A brand positioned against the wellness industry's pseudoscience. It sells physics, thermodynamics and verifiable chemistry, and only claims what it can measure. Tone: calm and clinical; the data makes the case, without insults.

The brand's signature is a public **Claims Log**: every factual claim the company makes, each linked to its evidence (third-party lab tests, calculations). The website is built so that a page can't publish a claim that isn't in the log.

## Product #1: a home air purifier

Chosen over water (plumbing varies, leaks create liability) and heat/cold (heavy R&D) because it's plug-and-play and its physics is simple to verify.

- **Draft engine (heavy work in progress):** EC centrifugal fan; HEPA filter (drafted as H14, likely H13 after review); about 2.3 kg (5 lb) of granular activated carbon; target clean air delivery rate (CADR) of 300–400 m³/h.
- **Differentiators under consideration:**
  - CADR published at a quiet noise level, with the full CADR/noise/power curve (most brands only quote full speed)
  - kilograms of carbon where most purifiers have grams
  - zero ozone by design (no ionizer, UV or "plasma")
  - filter life measured from the fan's speed and power instead of a timer
  - a "room test": the purifier measures its own CADR in the customer's room
  - local control (Home Assistant), no app or cloud account
- **Target price:** €400.

## Customer

First: the **engineer-skeptic** (homelab owners, data engineers, bio-hackers), won over with raw physics and published formulas. The mainstream is meant to follow through their word of mouth.

## Market

EU-wide, English-first website. Focus on DACH and the Nordics, with the UK later. Ships from an Italian or German third-party logistics (3PL) warehouse.

## Business model

Hardware plus **open, DRM-free consumables**: the filter uses a standard or openly published format that anyone can make, and the carbon is refillable. An optional First Principle filter subscription ships a filter when the machine measures that it's loaded. Filter revenue is treated as upside; the hardware margin has to carry the company.

## Go-to-market

Short tear-down videos: buy the best-selling purifier, weigh its carbon, and measure its noise and CADR on camera with a published method, then run the same tests on ours. The link goes to a product page with a plain-language description and a rigorous whitepaper one tap away. Website: Astro + headless Shopify.

## Known open questions

Engine targets (CADR at what noise level, at what price); filter grade; a filter format that works in Europe; why €400 beats a mass-market Coway or a DIY Corsi-Rosenthal box; connectivity; launch countries; trademark clearance.

## Not yet stated

Budget, team, manufacturing partner, timeline, unit cost.

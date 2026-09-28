# 6. Product #1 candidates

The project is archived until a candidate passes the three re-entry checks in the [README](../README.md):

1. **The physics allow the claim:** the headline number is measurable, and a paper check says the product can hit it.
2. **The physics allow the margin:** landed cost at no more than half the net price the market already pays.
3. **Nobody owns the number:** no measured competitor already delivers it for less.

Everything here is a paper screen *(Claude)*. Nothing has been through the council yet, and the figures come from web search results (page fetching is blocked in this environment), so they're unverified until checked.

## The pattern so far

The categories that screen well share one trait: **the incumbents themselves overclaim a number that a standard test can measure.** Sunscreen SPF, red-light irradiance and "cooling" bedding all fit.

The categories that screen badly fail in one of three ways:
- **The honest product already exists, cheaply:** fluoride toothpaste, foam earplugs, Corsi-Rosenthal boxes, Stiftung Warentest's €100 purifiers.
- **The honest answer is "you don't need it"** (house rule 6): filter jugs for EU tap water, blue-light glasses.
- **Someone already owns the number:** percentages on the label (The Ordinary), open local air monitors (AirGradient).

## Shortlist

| Candidate | 1. Claim | 2. Margin | 3. Unowned | Biggest risk |
|---|---|---|---|---|
| Verified-SPF sunscreen (**killed 2026-09-28**) | Yes, if labelled below the worst of several labs | Yes | No, once referees count | A referee-rated "gut" tube already sells for €5.25 |
| Measured-comfort bedding | Yes (ISO 11092) | Likely | Apparently | Whether buyers pay for a number |
| Carbon cassette for DIY purifiers | Plausible | Yes | Yes | A tiny market |

### 1. Verified-SPF sunscreen

> **Killed by the council on 2026-09-28** ([ledger](../council/ledger.md), [ruling](../council/sessions/2026-09-28-verified-spf-sunscreen/4-judge.md)). The referee already owns the number: Stiftung Warentest rated dm's €5.25 SPF 50+ face fluid "gut". This screen passed check 3 only because it left independent testers out. The notes below are the paper screen as it stood before the session.

- **The enemy is documented.** In June 2025, CHOICE found 16 of 20 SPF 50+ sunscreens below their label. Ultra Violette's Lean Screen tested at SPF 4. The company's own retests ranged from SPF 4 to 64, its base formula was judged unlikely to exceed SPF 21, and Australia's regulator (the TGA) questioned the lab that had certified it. All 19 sunscreens built on that base were cancelled from the register and recalled.
- **The lesson:** test noise explains SPF 40 versus 50, not 4 versus 50. The failure was a weak formula certified once, by a lab that can't be trusted, and never checked again.
- **Check 1:** passes with one rule: test at several labs and label below the worst result. EU labels come in bands ("50+" needs a measured 60 or more), so under-claiming is easy. *"Our label is lower than our worst test."*
- **Check 2:** passes easily. One in vivo test round ($2,700–4,500) spread over a 25,000-unit batch is 11–18 cents per unit, about 30–55 cents with three labs. Launch cash is roughly €65–165k, assuming €2–4 to make each unit (an estimate).
- **Check 3:** narrow. Beauty of Joseon publishes results from two labs (SPF 52.5 ± 5.8 and 63.1 ± 0.6), and EltaMD and Colorescience publish UVA and photostability data. What's left to own is every batch, several labs, every raw result, and a label below the worst one.
- **Changes from the air plan:** the first customer becomes skincare-literate buyers (a much larger group than homelab engineers), and daily facial SPF avoids most of the summer seasonality.

### 2. Measured-comfort bedding: the Eight Sleep problem without the compressor

- **The enemy:** "cooling" bedding. In one mattress study, phase-change material produced a measurable cooling effect for about 8 minutes, not enough to change how warm people felt after 20 minutes. Its heat dissipation improved by 2.7–25.6%.
- **The number:** thermal resistance (Rct) and water-vapour resistance (Ret), measured on a sweating hot plate under ISO 11092. Publish both for every duvet and sheet, and offer a calculator that picks a duvet's warmth from the bedroom temperature.
- **Nobody seems to own it.** German warmth classes (*Wärmeklassen* 1–5) have no uniform standard. The UK's TOG is a measured thermal resistance, but it's uncommon in DACH and Italy. Searches found no bedding brand publishing ISO 11092 results.
- **Physics to be honest about:** moisture changes a sheet's thermal resistance by 15% to more than 80%. In one retailer's comparison, linen and cotton had almost the same water-vapour resistance (3.84 vs. 3.86 m²·Pa/W). The honest pitch may be "the right duvet for your room, measured", not a magic fabric.
- **Fit:** pure thermodynamics, with no electronics, CE marking or radio. It's the passive version of the heat/cold idea rejected earlier for needing compressors.
- **To check:** the cost of an ISO 11092 test per sample (textile labs such as Hohenstein in Germany or Centexbel in Belgium), textile minimum orders, bedding return rates, and above all whether hot sleepers pay for a number.

### 3. Carbon cassette for DIY purifiers

- **The gap:** a standard Corsi-Rosenthal box has no carbon. The options are filters with a thin carbon layer (Exhalaron H10/H12, NordicPure MERV-13 with carbon) or carbon sheets taped on, which in heavy smoke need changing about every two weeks. Nobody sells kilograms of carbon in a low-resistance cassette.
- **The number:** carbon mass, pressure drop at a stated airflow, and measured gas removal per pass.
- **Physics check:** 1 kg of granular carbon over one 20 × 20-inch face is a bed under 1 cm deep. At a quarter of a box's airflow (about 250 m³/h) it adds roughly 5–7 Pa (Ergun estimate). Plausible, but a bed that shallow needs a design that stops air slipping between the granules.
- **Margin:** carbon costs €3–10 per kg, and there are no electronics.
- **Risk:** the market is small: Corsi-Rosenthal owners who also have smells to remove, most of them in the US. It's a cheap product #0 for building an audience rather than a company. It also tests the same demand as the carbon-first purifier (below) for a fraction of the cost.

## Parked

- **Carbon-first purifier.** Kilograms of carbon with large-area, lower-grade particle filters, within roughly 35–40 Pa. It probably can't beat the Luggable on particle CADR, so it would compete on odour and VOC capacity. The cassette tests that demand more cheaply first.

## Rejected

| Candidate | Why |
|---|---|
| Performance supplements | The pitched 30 g "cognitive loading" protocol would be an unauthorised EU health claim, and purity is already owned (Creapure, lab-tested brands) |
| High-active personal care, as pitched | Percentages on the label are The Ordinary's business; the examples (spirulina, black pepper) are wellness botanicals. Sunscreen is the version that survives |
| Open-data air sensors, as pitched | AirGradient's exact position; revisit only with a number nobody owns |
| Red-light therapy panels | Independent spectrometer tests find claimed irradiance off by 40–70%, a real enemy. But the benefits are contested biology, it's electronics, and independent databases already publish the real numbers |
| Water filter jugs | Stiftung Warentest's best were only "befriedigend" (satisfactory), with germs in every filter after use; most EU tap water doesn't need one |
| "Clean" candles | Every candle emits particles; the honest product is only the least bad candle |
| Blue-light glasses | A 2023 Cochrane review found they don't reduce eye strain (from memory; not rechecked here) |
| Fluoride toothpaste with published abrasivity | The incumbents are already the honest product |
| Down duvets with verified fill power | No evidence found of widespread overclaiming |

## Sources

- Sunscreen: [CHOICE media release](https://www.choice.com.au/about-us/media/media-releases/2025/june/16-of-20-sunscreens-didnt-meet-spf-claims-in-choice-test), [TGA: Lean Screen cancelled](https://www.tga.gov.au/resources/cancellations-by-sponsors/ultra-violette-lean-screen-spf50-cancelled-under-section-301c-act), [TGA: same base formulation](https://www.tga.gov.au/resources/explore-topic/sunscreens/sunscreens-using-same-base-formulation-ultra-violette-lean-screen-spf-50-sunscreen), [Dr Rachel Ho explainer](https://www.drrachelho.com/blog/australian-sunscreen-fail-spf-controversy/), [BeautyMatter](https://beautymatter.com/articles/is-everyone-lying-about-their-spf), [Beauty Independent](https://www.beautyindependent.com/australian-sunscreens-spf-claims-north-american-brands/), [Beauty of Joseon review](https://www.drrachelho.com/blog/beauty-of-joseon-sunscreen-review/)
- Bedding: [ISO 11092](https://www.iso.org/standard/65962.html), [bedsheet thermal comfort study](https://www.researchgate.net/publication/264090140_Thermal_Comfort_of_Bedsheets_Under_Real_Conditions_of_Use), [PCM mattress study](https://www.sciencedirect.com/science/article/abs/pii/S0894177716302941), [allnatura on Wärmeklassen](https://www.allnatura.de/bettdecken/bettdecken-waermeklassen.html), [Centexbel](https://www.centexbel.be/en/problem-solving/testing/masurement-thermal-and-water-vapour-resistance-under-steady-state), [Or & Zon comparison](https://orezon.co/blogs/bedding-guides/best-sheets-night-sweats)
- Carbon cassette: [CleanAirKits FAQ](https://www.cleanairkits.com/pages/frequently-asked-questions), [Corsi-Rosenthal build guide](https://airfilterkits.com/corsi-rosenthal-box/)
- Rejected: [Outliyr red-light tests](https://www.globenewswire.com/news-release/2026/07/08/3324504/0/en/Outliyr-s-Independent-Spectrometer-Tests-Find-Popular-Red-Light-Therapy-Devices-Delivering-From-67-Percent-to-Nearly-Triple-Their-Advertised-Power.html), [Stiftung Warentest water filters](https://www.test.de/Wasserfilter-im-Test-Gut-filtert-keiner-4840828-0/), [candle emissions study](https://candles.org/wp-content/uploads/2025/09/Measurement-and-evaluation-of-gaseous-and-particulate-emissions-from-burning-scented-and-unscented-candles-2021.pdf)

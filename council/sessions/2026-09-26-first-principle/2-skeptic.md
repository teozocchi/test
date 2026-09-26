# 2. The Skeptic

Council session 2026-09-26 · [Idea brief](idea.md) · [Believer's case](1-believer.md)

## The bet is already lost

The Believer rests the company on one number: "a lead in CADR at quiet speeds that is big enough to show on camera." Other machines already hold that lead, measured by HouseFresh, the reviewer the Believer cites:

| Machine | CADR | Noise (HouseFresh) | Price |
|---|---|---|---|
| CleanAirKits Luggable XL-7: PC fans, MERV-13 | 440 m³/h smoke (Intertek) | 38.8 dB(A), its only speed | about £251 in the UK, shipped to the EU |
| Nukit Tempest Pro: PC fans, MERV-13 | about 320 m³/h (HouseFresh estimate) | 39.1 dB(A) at top speed | $386 |
| AirFanta 3Pro: PC fans, H11 media, carbon option | about 600 m³/h at full speed (HouseFresh estimate) | 43.3 dB at the quiet setting HouseFresh recommends | $160 in the US; listed on Amazon.de |
| **First Principle, draft** | **300–400 m³/h at full speed** | unknown | **€400** |

The draft's full-speed target falls short of what the Luggable delivers at 38.8 dB. HouseFresh calls the Luggable "the best-performing air purifier we have tested under 40dB". House rule 4 ("comparisons include the competitors that beat us") obliges First Principle to put it in its own launch chart, above itself.

The physics makes the gap wider, not narrower:
- **The founder's own review** says the Corsi-Rosenthal box beats HEPA purifiers with a lower-grade filter and more airflow. The PC-fan boxes above are that idea, sold as finished products.
- **First Principle adds resistance.** By the Believer's own sum the H13 media sits at about 60 Pa. The 2.3 kg carbon bed comes on top, and that sum leaves it out.
- **Resistance costs decibels.** At the same airflow, fan sound power rises by about 20·log₁₀ of the pressure ratio. Each doubling of system pressure therefore costs about 6 dB, the step from 35 to 41 dB(A) (fan-law rule of thumb; estimate).

"Kilograms of carbon" and "most CADR at 35 dB(A)" pull against each other inside one box.

## Who won't pay

- **The engineer-skeptic.** The founder's docs predict his questions, and First Principle loses each one:
  - **CADR per euro:** the Trotec AirgoClean 170 E gives 350 m³/h for about €100, or 3.5 m³/h per euro (manufacturer CADR). The Bosch Air 4000 gives about 2 (300 m³/h for €137–183). First Principle gives 0.75–1.0.
  - **CADR per dB(A):** see the table above.
  - **"Why not a CR box?"** A German build guide has used locally sold ePM1 filters since 2021 (495 × 495 × 48 mm, about €15 each in the guide).

  The Believer's own evidence shows what he does instead: he buys a mass-market Levoit or Xiaomi and flashes it. Those firmware repos have 188 and 144 GitHub stars, and the two July 2026 Flipper apps have 7 and 4. That's a hobby, not demand for a €400 box. Suppose a quarter of Home Assistant's 2 million installs were in the launch countries and 1% of those owners bought one (both estimates). That's about 5,000 units, sold once.
- **The mainstream German buyer.** He reads Stiftung Warentest. Its top two are both rated "gut" (2.3):
  - the Trotec, at about €100 (German coverage calls it "the cheapest test winner ever");
  - the Bosch Air 4000, at €137–183, with a carbon layer; the 4000i version adds Matter.

  Warentest picks products by market relevance, so an English-first direct-to-consumer (D2C) box won't reach its tables for years. Engineers have championed CR boxes since 2020, and the referee the mainstream reads still crowns Bosch and Trotec.
- **The wood-smoke household,** the Believer's poster child:
  - achtung-holzofen.de, a German site about wood-stove smoke, tested the €100-class IKEA STARKVIND.
  - Buyers who want serious carbon and can pay for it buy brands with decades of track record: IQAir, or Austin Air. Austin Air packs 6.8 kg of carbon and zeolite with a 5-year filter, costs $540–844 in the US and is listed on Amazon.de. The founder's docs cite it as proof that "the 'heavy steel' niche already exists". The Believer leaves it out.
  - Regulation is shrinking the problem. Under Germany's small-stove ordinance (1. BImSchV, stage 2), stoves installed between 1995 and March 2010 that missed the limits had to be retrofitted, replaced or shut down by 31 December 2024. The Umweltbundesamt (UBA) page the Believer cites is titled "air-quality limit values met".
- **The Nordic buyer.** Balanced mechanical ventilation is common in Finnish buildings from the 1980s on; its share in Sweden and Denmark is unverified. A better filter in the unit he already owns is the cheap fix.
- **The bio-hacker** buys stories, and this brand refuses to tell them.

## What already solves it

| The pitch | Already on sale |
|---|---|
| Quiet CADR, no filter lock-in | Luggable and Nukit (take any standard 20×25-inch MERV-13 panel), AirFanta, or a €100 DIY box |
| Rated by the German referee | Trotec 170 E, Bosch Air 4000 |
| Local control, no cloud account | Bosch Air 4000i and 6000i (Matter), SwitchBot (Matter), IKEA STARKVIND through IKEA's Matter bridge |
| Kilograms of carbon | Austin Air HealthMate (6.8 kg), IQAir HealthPro 250 |
| Zero ozone | Every plain filter-and-fan machine above |

## What the founder is too close to see

1. **The moat faces the wrong incumbent, and the law levels it.** Philips, Xiaomi and Coway can't open their filters without losing revenue, but people who measure don't compare against them. The machines winning the measured tests have no lock-in and nothing to give up. Directive 2024/825 bans *inducing* early replacement and *hiding or misstating* what third-party consumables do. It doesn't ban proprietary formats, so a disclosed chip-locked filter stays legal. Whatever the incumbents must change, they change for everyone. From tomorrow, "on the right side of the law" is the floor.
2. **Measured filter life measures the wrong filter.** The Believer's design runs a 13 m² H13 module at a quarter of its rated flow, so it will load very slowly (estimate). A subscription that ships "when the machine measures that it's loaded" ships almost nothing. The part that does saturate in smoke is the carbon. The founder's docs say its alert needs "a usage-based estimate or a gas sensor", and the first option is the timer the brand exists to attack. Filter revenue is close to zero by design anyway:
   - the module is a standard industrial part that German B2B filter shops sell singly for €108–173;
   - the carbon is commodity granules.
3. **The brand's own instruments will produce its gotchas.** The room-test sensor sits on the machine, so the result only holds in a well-mixed room; the founder's docs concede this. Owners' numbers will differ from the lab CADR, and the Believer wants them posted. The noise headline has the same problem. The Believer mocks Coway's "24.4 dB listed, 38.9 dB measured". HouseFresh's readings for the quietest machines it has tested sit near 39 dB: Luggable 38.8, Coway 38.9, Nukit 39.1. A lab-measured "35 dB(A)" will be re-measured in rooms like that. "Listed 35, measured 39" is the same gotcha, aimed at the one brand whose whole pitch is not having one (estimate).
4. **Publishing everything publishes the clone.** The standard module, a catalogue fan, the carbon tray, published drawings and a whitepaper add up to a spec any contract manufacturer can build cheaper. AirFanta's founder went from assembling CR boxes for friends in 2022 to a $160 product listed on Amazon.de. There's no patent, no lock-in and no network effect.
5. **Every tear-down invites a lawsuit.** The launch videos name a competitor and back the comparison with kitchen-scale and cheap-sensor data. The Claims Log files that as "in-house measurement", a tier below a lab report. Under §6 UWG, Germany's comparative-advertising rule, the competitor can send a formal warning letter (*Abmahnung*) and seek an injunction that takes the flagship video down.
6. **The enemy is already dead here.** Air purification is the one wellness-adjacent category where physics already won:
   - CADR is standardised.
   - Warentest tests with aged filters and measures gas removal.
   - Molekule, the category's pseudoscience flagship, filed for Chapter 11 in October 2023 with $46.95M of liabilities.

   The fight left is price per cubic metre of clean air, and a €400 box loses it.
7. **The storefront is decided; the engine isn't.** The website framework is marked "Decided", and the Claims Log build check and trademark plan are drafted. Meanwhile:
   - the engine is "heavy WIP";
   - the filter format is "Open, blocking";
   - unit cost, manufacturer, budget, team and timeline are blank.

   The previous product, a shower filter, already "fell apart on the math".

## The margin can't carry it

- **The price ceiling.** €400 including VAT is €336 net in Germany and €320 in Denmark and Sweden. Two rules of thumb set the limit:
  - price hardware at 2.5–4× its bill of materials (Bolt), which caps the parts bill at about €84–134;
  - D2C in German-speaking Europe needs product gross margins above 50% (Werner Strauch, 2026), which caps landed cost at about €168.
- **The Believer's own parts,** at single-unit retail:
  - the H13 287 × 592 × 292 mm module: €108–173;
  - an ebm-papst EC centrifugal fan: about €370 in one eBay.de listing.

  Even at half those prices in volume (estimate), the filter and fan eat most of the budget. That's before the steel box, carbon, electronics, packaging for a parcel of roughly 15–20 kg (estimate), assembly and freight.
- **Costs after the factory:**
  - bulky shipping to the Nordics
  - 14-day EU returns of a heavy box
  - the 2-year legal guarantee
  - WEEE and packaging registration in every country
  - Matter certification: about $18–22k for the first product, including $7k a year of Connectivity Standards Alliance membership
  - radio cybersecurity testing, plus CADR lab tests for every revision
  - Cyber Resilience Act vulnerability reporting, live since 11 September 2026
- **The result:** about +€80 per box in the best case, before any marketing, R&D or salary. In the worst case every box loses money (estimate). No consumables revenue stands behind it.

## Where the Believer's case breaks

- **"Build a Corsi-Rosenthal box from US-size filters that European shops don't stock":** false. The German guide has used local ePM1 filters since 2021, and assembled PC-fan units ship to the EU.
- **IQAir's carbon is "about the mass First Principle plans to ship at €400":** IQAir's V5-Cell is carbon plus impregnated alumina, a chemical sorbent. The founder's docs say plain carbon is "weak on formaldehyde unless impregnated" and that carbon mass predicts capacity, not removal rate. A comparison on mass alone breaks the brand's own comparison rules.
- **"Every new measurement ... helps the one product built to be measured":** so far the measurements have helped a £251 box of PC fans. HouseFresh, the Believer's source, lost 91% of its Google traffic after Google's March 2024 core update, so the measurers have lost their reach.
- **"From tomorrow EU law pushes the other brands in the same direction":** correct, and that closes the gap instead of opening one.

## The fastest way this dies

Launch day. The funnel's first asset is the side-by-side chart, and house rule 4 makes it include whatever beats First Principle. On CADR per euro it loses to a €100 Warentest winner. On quiet CADR it loses to a £251 box whose single quiet speed beats First Principle's full speed. The first Reddit thread writes itself, from a chart the brand published.

The founder can get the same answer sooner and cheaper. Put a €108–173 H13 module, an EC fan and a 2.3 kg carbon tray in a plywood box, and measure it next to a Luggable with the brand's own decay method.

## The fatal flaw

**Boxes with no filter lock-in already own quiet CADR at a lower price, and this engine is designed to lose that fight.** The Luggable XL-7 delivers 440 m³/h at 38.8 dB(A) for about £251. First Principle's full-speed target is 300–400 m³/h, and its H13 media and carbon bed add pressure that costs decibels. If a prototype built within the €400 cost ceiling can't beat that on the same meter, there's no headline number, and house rule 4 makes the brand publish the chart that proves it. What's left is kilograms of carbon, a Claims Log and Home Assistant support. Neither the mainstream nor the engineer-skeptic will pay a €400 premium for that. Don't build it.

---

**Sources.** The page fetcher was blocked for every non-GitHub site I tried, so the web figures come from search results, not pages read in full. GitHub stars and dates came directly from the GitHub API.
- Quiet CADR: [HouseFresh Luggable XL-7](https://housefresh.com/cleanairkits-luggable-xl-review/), [HouseFresh on X](https://x.com/ThisHouseFresh/status/1865091079835431000), [Clean Air Kits Europe](https://cleanairkits.eu/products/luggable-ultra-xl-high-output-7-fan-air-purifier), [HouseFresh quiet purifiers](https://housefresh.com/quiet-air-purifiers/), [HouseFresh AirFanta 3Pro](https://housefresh.com/airfanta-3pro-review/), [AirFanta on Amazon.de](https://www.amazon.de/AirFanta-3Pro-Luftreiniger-zusammenklappbar-20-Zoll-Handgep%C3%A4ck/dp/B0DSKZ2JPY), [Nukit Tempest Pro](https://cybernightmarket.com/products/the-nukit-tempest-pro-complete-air-purifier-kit-usa), [HouseFresh Coway](https://housefresh.com/coway-airmega-ap-1512hh-review/)
- Mainstream: [Warentest test](https://www.test.de/Luftreiniger-im-Test-5579439-0/), [Trotec 170 E at Warentest](https://www.test.de/Luftreiniger-im-Test-5579439-detail/320000028380!IT23923-0004-00/), [Trotec 170 E review](https://www.homeandsmart.de/trotec-airgoclean-170e-test-817084), [Bosch Air 4000 prices](https://geizhals.de/bosch-air-4000-luftreiniger-7733701943-a2899380.html), [Bosch Matter](https://www.bosch-homecomfort.com/de/de/wohngebaeude/unternehmen/presse/matter-geraeteintegration-fuer-bosch/), [IKEA STARKVIND price](https://www.mobiflip.de/shortnews/ikea-starkvind-smart-luftreiniger-preis/), [SwitchBot Matter](https://support.switch-bot.com/hc/en-us/articles/27238950422167-Matter-Compatibility-for-SwitchBot-Air-Purifier)
- DIY and hacking: [German CR-box guide](https://github.com/wrichter/GermanyDYIAirCleaner), [Levoit ESPHome](https://github.com/acvigue/esphome-levoit-air-purifier), [Xiaomi ESPHome](https://github.com/jaromeyer/mipurifier-esphome), [Flipper app 1](https://github.com/khmm12/flipper-xiaomi-filter-reset), [Flipper app 2](https://github.com/rashithawaragoda-code/flipper-xiaomi-filter-reset)
- Carbon: [IQAir HealthPro 250](https://www.galuft.de/produkt/iqair-healthpro-250-ne-luftreiniger/), [V5-Cell price](https://www.galuft.de/produkt/iqair-v5-cell-filter-ersatzfilter-fuer-healthpro-250-xe/), [V5-Cell media](https://www.luftreiniger.net/en/ersatz-aktivkohle-filter-elerment-v5-cell-fuer-iq-air-serie-iqair-health-pro-250/), [Austin Air HM400](https://www.filtersfast.com/P-Austin-Air-HM400-HealthMate-HEPA-Purifier-Silver.asp), [Austin Air on Amazon.de](https://www.amazon.de/-/en/Austin-Air-HealthMate-Plus-Purifier/dp/B07SHVZMX9)
- Wood smoke and ventilation: [UBA](https://www.umweltbundesamt.de/themen/feinstaub-aus-holzfeuerungen), [1. BImSchV stage 2](https://www.co2online.de/modernisieren-und-bauen/kaminofen/bimschv/), [achtung-holzofen.de](https://www.achtung-holzofen.de/test-ikea-starkvind-luftreiniger/), [Finnish ventilation](https://www.aeris.fi/en/post/mechanical-ventilation-facts-and-challenges)
- Costs: [H13 module (filter-mueller)](https://www.filter-mueller.de/lueftung-klima/schwebstofffilter/kompakt-schwebstofffilter/kompaktfilter-h13-592-x-287-x-292-mm), [H13 module (as-luftfilter)](https://www.as-luftfilter.de/Schwebstofffilter-E10-H14/HEPA-Filter--Schwebstofffilter-H13/Kunststofffahmen-270/Kompaktfilter-Schwebstofffilter--Gueteklasse-H13---287-x-592-x-292-mm-1186.html), [ebm-papst fan listing](https://www.ebay.de/itm/365870598187), [Bolt on BOM multiples](https://blog.bolt.io/hardware-retail-exits/), [D2C margins in DACH](https://wernerstrauch.com/en/blog/d2c-strategy), [Matter fees](https://support.tuya.com/en/help/_detail/Kcd6745mkphcu), [CRA reporting](https://digital-strategy.ec.europa.eu/en/policies/cra-reporting)
- Law, reviewers, precedent: [Directive 2024/825](https://eur-lex.europa.eu/eli/dir/2024/825/oj/eng), [German transposition](https://www.ebnerstolz.de/de/unser-angebot/leistungen/rechtsberatung/wirtschaftsrecht-commercial/umsetzung-empco-richtlinie-99600.html), [§6 UWG](https://www.ra-plutte.de/vergleichende-werbung/), [HouseFresh traffic loss](https://searchengineland.com/review-site-google-traffic-affiliate-seo-content-440143), [Molekule Chapter 11](https://www.streetinsider.com/Corporate+News/Molekule+Group+(MKUL)+files+voluntary+petition+under+Chapter+11+bankruptcy/22233063.html)

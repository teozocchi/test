# 4. Product #1: the air purifier

## Council verdict — FIX FIRST

The [idea council](../council/README.md) reviewed this product on 2026-09-26: see the [ledger entry](../council/ledger.md) and the [full ruling](../council/sessions/2026-09-26-first-principle/4-judge.md).

- **Biggest risk: no winning number.** The CleanAirKits Luggable XL-7, a £251 purifier built from PC fans and MERV-13 filters, delivers 440 m³/h (Intertek smoke CADR) at 38.8 dB(A) (measured by HouseFresh). That beats the draft's full-speed target, and HEPA plus 2.3 kg of carbon cost this engine decibels.
- **What survived: one gap.** A quiet machine with HEPA and kilograms of carbon, for bedrooms that get stove smoke, priced below the heavy-carbon brands (Austin Air, IQAir). None of the PC-fan boxes carries kilograms of carbon, and Bosch's Warentest winner has only a carbon layer. The gap exists only if the engine stays quiet with the carbon in.
- **The target changes** from "300–400 m³/h at full speed, €400" to: *beat the Luggable XL-7 on CADR at equal noise, with all the carbon installed, at a landed cost the price can carry.*

### The gates

0. **Paper check (10 minutes).** In ebm-papst's or Ziehl-Abegg's online fan selector, find the quietest fan for 450 m³/h (the Luggable's 440 m³/h plus a margin for air leaking around the filter) at 100 Pa, and read its A-weighted sound power. 50 dB(A) or less: go to gate 1. Above: KILL. (In a furnished room the level 1 m away is roughly 6 dB below the sound power, so about 45 dB(A) of sound power matches the Luggable's 38.8 dB(A).)
   - *Refinement (Claude):* 100 Pa assumes a carbon tray with about twice the filter's face area. By a packed-bed (Ergun) estimate, 2.3 kg of carbon in a tray the size of the 287 × 592 mm filter adds 80–145 Pa on its own, so a compact box lands at roughly 160–220 Pa in total. Run the selector at 200 Pa too; the difference shows how big the box has to be.
1. **Measured.** Build a plywood prototype: the H13 287 × 592 mm module, an EC fan, and all 2.3 kg of carbon in a wide, shallow tray. It must beat the Luggable XL-7 on CADR at equal noise, measured with the decay method in the same room, on the same meter, at the same distance. Budget about €1,000 for parts, a Luggable and meters (estimate).
   - *Caution (Claude):* HouseFresh's readings for the Luggable (38.8 dB), a Coway on its lowest speed (38.9) and the Nukit at full speed (39.1) sit within 0.3 dB of each other, which looks like the floor of their room or meter. Test in a quiet room with a meter that reads well below 39 dB, or the comparison can't tell the machines apart.
2. **Costed.** Written supplier quotes put landed cost at no more than half the net price (€168 at €400). If the numbers only work at a higher price, that price goes on the deposit page.
3. **Paid for.** 300 paid, refundable €50 deposits in 30 days, on a page showing the measured chart. See the deposit test in [go-to-market](03-go-to-market.md).

Gates 0 and 1 come first; gates 2 and 3 can then run in parallel. If gate 0 or 1 fails, or gate 3 falls short of 300, product #1 is killed. The brand stays, and the council picks a new product #1.

## Why air — Decided

- **Water is a nightmare for V1.** Plumbing varies wildly, leaks cause thousands in property damage (liability), and the shower filter fell apart on the math.
- **Heat/cold** (e.g. an Eight Sleep-style bed) needs heavy R&D: compressors and liquid cooling.
- **An air purifier is plug-and-play.** No installation, and the physics is undeniable: a fan pushes air through a dense filter. It's the easiest option to manufacture, verify and scale without large warranty liabilities.

House rule 2 applied *(Claude)*: the harm from fine particles (PM2.5) is among the best-established facts in environmental health (see the WHO's 2021 air quality guidelines), and it's well documented that purifiers cut indoor particle levels. Evidence for specific health outcomes from home purifiers is thinner. So we claim particle removal, not health benefits.

## The engine: draft spec — Idea (heavy WIP)

Form follows function: design the engine before the box.

| Part | Draft |
|---|---|
| Motor | EC (electronically commutated) centrifugal fan: efficient, no ozone from brushes, holds RPM under high static pressure |
| Particle filter | True HEPA H14 (99.995% of 0.1 µm particles) |
| Gas filter | 5 lb (2.5 kg) tray of granular activated virgin carbon, after the HEPA |
| Target CADR | 300–400 m³/h |
| Reference room | 30 m² bedroom, cleared 4–5 times an hour |

**Council update (2026-09-26):** the particle filter becomes the standard 287 × 592 mm H13 industrial module, and the CADR target becomes "beat the Luggable XL-7 at equal noise" (see the verdict above).

## Review of the draft spec *(Claude)*

The engineer-skeptic will check every line of this. Here's what I think they'd find.

### 1. H14 is spec inflation

What cleans a room is the **clean air delivery rate**: CADR ≈ airflow × single-pass efficiency.

- H13 captures ≥99.95%; H14 captures ≥99.995%. Upgrading raises CADR by at most 0.045%, which no one could measure.
- Denser media raises the pressure drop, so the same fan at the same noise moves *less* air. H14 can lower real-world CADR.
- EN 1822 rates HEPA filters at their most penetrating particle size (typically around 0.1–0.25 µm), not at 0.1 µm specifically. It also calls for every H13/H14 element to be individually tested, which adds cost to each replacement filter.
- The Corsi-Rosenthal box proves the point from the other direction: filters well below HEPA grade, but so much airflow that its CADR beats many HEPA purifiers.
- A filter's class says nothing about air leaking *around* it. A poor seal can matter more than the grade. Only device-level CADR, measured on the whole machine, goes in the Claims Log.

**Proposal:** choose the filter grade that gives the most CADR at a quiet noise level. Probably H13, possibly a lower grade with a larger filter area. "We chose H13 over H14, and here's the math" is a stronger story for this audience than "H14".

### 2. Noise is the real constraint

People turn loud purifiers down or off, so the CADR that matters is the one at the speed people actually use. Most brands only advertise CADR at full speed.

**Proposal:** publish the full curve (CADR, noise and power at every speed) and headline the CADR at a stated quiet level, e.g. "X m³/h at 35 dB(A)", with the measurement distance and standard.

The main lever is **filter area**. More area means slower air through the filter, lower pressure drop, and more airflow at a lower fan speed.

**Council:** publish noise the way reviewers measure it, at 1 m in a room, next to any lab figure. Otherwise a lab "35 dB(A)" re-measured at home as 39 becomes the same "listed vs. measured" gotcha we criticise in others.

### 3. The carbon bed

- **Units:** 5 lb is 2.27 kg, not 2.5 kg. Pick one number and convert exactly. (This is the kind of slip the Claims Log build check exists to catch.)
- **Contact time applies here too.** Granular carbon weighs about 0.5 kg per litre, so 2.5 kg is a bed of about 5 L. At 400 m³/h (111 L/s), air spends about 45 ms in it; at 300 m³/h, about 60 ms. That's far more than typical consumer purifiers, but whether it's enough depends on the target gases. That calls for a test, not a calculation.
- **Geometry is a trade-off.** A thin bed with a large face has low pressure drop but short contact time; a deep tray is the opposite.
- **Carbon vs. quiet is a size trade-off, not a law of physics (council).** Contact time depends only on the bed's volume, but pressure drop falls steeply as the tray gets wider and shallower: doubling the face area at the same volume cuts it roughly 4–8×. By my packed-bed estimate, at 450 m³/h, 2.3 kg in a tray the size of the filter's face (0.17 m²) adds about 80–145 Pa; doubling the face area brings that to about 13–23 Pa. At the same airflow, each doubling of total pressure costs about 6 dB of fan noise (fan-law rule of thumb). Kilograms of carbon can be quiet, but only in a bigger box.
- **Order:** carbon beds shed fine carbon dust. With the carbon *after* the HEPA, that dust blows into the room. The usual order is pre-filter → carbon → HEPA (or add a post-filter).
- **Say what carbon does and doesn't do.** Good for many VOCs and odours. Weak on formaldehyde unless impregnated (e.g. potassium permanganate media). Nothing for CO₂.
- **"Virgin" is an adjective.** Specify the carbon by measurable properties instead: the raw material (e.g. coconut shell) and an adsorption measure such as iodine number or CTC activity.

### 4. The motor

- **EC is the right call:** efficient, quiet, precisely controllable.
- **But it isn't a differentiator.** Most consumer purifiers already use brushless DC motors, and purifier ozone comes from ionizers, UV lamps and "plasma" features, not motors. The honest claim is "no ionizer, no UV, no plasma: zero ozone by design", verified by a test such as UL 2998 (zero-ozone validation).
- **The impeller matters as much as the motor.** A backward-curved centrifugal fan is what keeps air moving against the pressure drop of dense filters. Industrial EC fan makers (ebm-papst, Ziehl-Abegg) fit the "industrial-grade" story.
- **Bonus: measured filter life.** An EC motor reports its speed and power. As the particle filter clogs, the fan's operating point shifts, so the machine can estimate filter loading instead of running a timer: *the change-filter light is a measurement.* (Carbon saturation doesn't show up in pressure; that needs a usage-based estimate or a gas sensor. We say so.)
- **Council: measured filter life measures the wrong part.** The H13 module runs at about a quarter of its rated flow, so it clogs very slowly. In smoke, the carbon is what saturates, and fan power can't see that. A usage-based estimate is the kind of timer the brand attacks; a gas sensor is the honest option, but it adds cost. **Open.**

### 5. The room math

- 300–400 m³/h is about 175–235 CFM.
- A 30 m² room with a 2.7 m ceiling is 81 m³, so 300–400 m³/h gives **3.7–4.9 air changes per hour**. The math checks out.
- But one air change doesn't "clear" the room. In a well-mixed room, each one removes about 63% of particles (C = C₀·e^(−ACH·t)). At 5 air changes per hour, particles fall 90% in about 28 minutes and 99% in about 55 minutes. Those are the numbers to publish.
- 30 m² is living-room size. Many bedrooms are 10–15 m², where this machine could run at a low, quiet speed and still exceed 5 air changes per hour.

### 6. Price vs. value

At €400, 300–400 m³/h can't be the pitch: mass-market purifiers such as Coway's AP-1512HH ("Mighty", long Wirecutter's top pick) are rated at around 400 m³/h for much less. What €400 can buy that they don't offer:
- CADR at a bedroom-quiet noise level
- kilograms of carbon instead of grams
- open, DRM-free filters
- build quality, repairability and verifiable data
- local control, with no app or cloud account

**Council: at €400, each unit earns roughly nothing** (−€110 to +€55 per unit on a realistic first run, by the Investor's estimate). The price is open again; see the unit economics in [business model](05-business-model.md).

## Competitive set

What the engineer-skeptic will compare us against. Figures are manufacturer claims, reviewer measurements, or council findings from search-result snippets; verify before any public use.

| Product | What it's known for |
|---|---|
| **CleanAirKits Luggable XL-7** | PC fans and MERV-13; 440 m³/h smoke CADR (Intertek) at 38.8 dB(A) (HouseFresh); about £251, ships to the EU. **The benchmark to beat.** |
| Nukit Tempest Pro | PC fans and MERV-13; about 320 m³/h at 39.1 dB(A) (HouseFresh estimate); $386 |
| AirFanta 3Pro | PC fans and H11 media, carbon option; about 600 m³/h at full speed (HouseFresh estimate); $160 in the US, listed on Amazon.de |
| DIY Corsi-Rosenthal box | Very high CADR for a fraction of the price; loud, uncertified, bulky. European builds use locally sold ePM1 panels. |
| Trotec AirgoClean 170 E | 350 m³/h (manufacturer); Stiftung Warentest "gut"; about €100–150 |
| Bosch Air 4000 | 300 m³/h; Warentest test winner (5/2026); €137–183; a carbon layer; Matter in the 4000i |
| Coway AP-1512HH ("Mighty") | ~400 m³/h, cheap, long-time Wirecutter pick; little carbon. Listed at 24.4 dB on its lowest speed; HouseFresh measured 38.9 dB |
| Dyson purifiers | Premium price; reportedly ~200 g of carbon (unverified) |
| Austin Air HealthMate | Steel housing, ~6.8 kg (15 lb) of carbon and zeolite; $540–844 in the US, listed on Amazon.de. The "heavy steel" niche already exists |
| IQAir HealthPro 250 / GC MultiGas | HealthPro 250: €1,399, with a gas cell of ~2.3 kg (5 lb) of carbon and impregnated alumina. GC MultiGas: ~5.4 kg (12 lb). Very expensive |

## Sensors and connectivity — Open

- **Particle sensor:** enables an auto mode and the room test below. Low-cost laser sensors are good at *relative* changes, less so at absolute accuracy.
- **CO₂:** a purifier doesn't remove CO₂. If we display it (with a real NDIR sensor), the honest message is "open a window".
- **Connectivity** for the homelab audience means a local API (Home Assistant, MQTT), no account and no cloud. But any radio brings EU cybersecurity rules: the Radio Equipment Directive's cybersecurity requirements (mandatory since August 2025) and the Cyber Resilience Act (vulnerability reporting from September 2026, full requirements from December 2027). A branded app would also be class 9 software; see the trademark notes in [philosophy](01-philosophy.md).
- **Council: local control isn't unique.** Bosch's Air 4000i and 6000i and SwitchBot's purifier support Matter, and IKEA's STARKVIND works through IKEA's Matter bridge.
- **Council: Matter** (from version 1.2) defines an air-purifier device type with HEPA and carbon filter monitoring. Certifying a first product costs about $18–23k, including about $7k a year of Connectivity Standards Alliance membership (estimate).
- **Council: the fastest path is no radio in V1.** That skips Matter and radio-cybersecurity testing. The Investor's best case for a first shipped unit, about 6 months, assumes no radio, catalogue parts, a sheet-metal box and Germany only.

### The room test — Idea *(Claude)*

The purifier measures its own CADR in the customer's room. Raise the particle level (a burnt match), press a button, and it runs the decay method from [go-to-market](03-go-to-market.md): measure the decay rate, subtract the natural decay, multiply by the room volume the user enters. Because the decay *rate* largely doesn't depend on the sensor's absolute calibration, a cheap sensor can do it.

Caveat: the sensor sits on the machine, so the result assumes a well-mixed room. It's a sanity check for the customer, not a lab certificate. I haven't seen a purifier that does this (worth checking), and it builds the brand's philosophy into the hardware.

**Council caution:** owners will post results that differ from the lab CADR. Publish the expected spread, and why, before anyone else finds it.

## Compliance checklist *(Claude; confirm with a test lab)*

- **CE marking:** Low Voltage Directive, EMC Directive, RoHS. Safety standard: EN 60335-1 with EN 60335-2-65 (air-cleaning appliances).
- **If wireless:** the Radio Equipment Directive, including its cybersecurity requirements (EN 18031 standards), and the Cyber Resilience Act.
- **General Product Safety Regulation:** an EU-based responsible operator, traceability, safety information in local languages.
- **Per country:** WEEE producer registration and packaging registration.
- **Chemicals:** REACH (substances of very high concern in the product).
- **Consumer law (council):** Directive (EU) 2024/825, applying from 27 September 2026, blacklists pushing early replacement of consumables and misstating how third-party consumables affect a product. Our design complies by default.
- **Performance claims:** CADR from a third-party lab (AHAM AC-1, or EN IEC 63086-2-1 for Europe), noise measured to a stated standard, zero-ozone validation (e.g. UL 2998).
- **Budget (council estimate):** €20–50k for safety, EMC, CADR and ozone testing.

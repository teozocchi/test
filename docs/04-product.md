# 4. Product #1: the air purifier

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

### 3. The carbon bed

- **Units:** 5 lb is 2.27 kg, not 2.5 kg. Pick one number and convert exactly. (This is the kind of slip the Claims Log build check exists to catch.)
- **Contact time applies here too.** Granular carbon weighs about 0.5 kg per litre, so 2.5 kg is a bed of about 5 L. At 400 m³/h (111 L/s), air spends about 45 ms in it; at 300 m³/h, about 60 ms. That's far more than typical consumer purifiers, but whether it's enough depends on the target gases. That calls for a test, not a calculation.
- **Geometry is a trade-off.** A thin bed with a large face has low pressure drop but short contact time; a deep tray is the opposite.
- **Order:** carbon beds shed fine carbon dust. With the carbon *after* the HEPA, that dust blows into the room. The usual order is pre-filter → carbon → HEPA (or add a post-filter).
- **Say what carbon does and doesn't do.** Good for many VOCs and odours. Weak on formaldehyde unless impregnated (e.g. potassium permanganate media). Nothing for CO₂.
- **"Virgin" is an adjective.** Specify the carbon by measurable properties instead: the raw material (e.g. coconut shell) and an adsorption measure such as iodine number or CTC activity.

### 4. The motor

- **EC is the right call:** efficient, quiet, precisely controllable.
- **But it isn't a differentiator.** Most consumer purifiers already use brushless DC motors, and purifier ozone comes from ionizers, UV lamps and "plasma" features, not motors. The honest claim is "no ionizer, no UV, no plasma: zero ozone by design", verified by a test such as UL 2998 (zero-ozone validation).
- **The impeller matters as much as the motor.** A backward-curved centrifugal fan is what keeps air moving against the pressure drop of dense filters. Industrial EC fan makers (ebm-papst, Ziehl-Abegg) fit the "industrial-grade" story.
- **Bonus: measured filter life.** An EC motor reports its speed and power. As the particle filter clogs, the fan's operating point shifts, so the machine can estimate filter loading instead of running a timer: *the change-filter light is a measurement.* (Carbon saturation doesn't show up in pressure; that needs a usage-based estimate or a gas sensor. We say so.)

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

## Competitive set

What the engineer-skeptic will compare us against. All figures are manufacturer claims or community estimates; verify before any public use.

| Product | What it's known for |
|---|---|
| DIY Corsi-Rosenthal box | Very high CADR for a fraction of the price; loud, uncertified, bulky |
| Coway AP-1512HH ("Mighty") | ~400 m³/h, cheap, long-time Wirecutter pick; little carbon |
| Dyson purifiers | Premium price; reportedly ~200 g of carbon (unverified) |
| Austin Air HealthMate | Steel housing, ~6.8 kg (15 lb) of carbon and zeolite: the "heavy steel" niche already exists |
| IQAir GC MultiGas | ~5.4 kg (12 lb) of carbon and impregnated alumina; very expensive |

## Sensors and connectivity — Open

- **Particle sensor:** enables an auto mode and the room test below. Low-cost laser sensors are good at *relative* changes, less so at absolute accuracy.
- **CO₂:** a purifier doesn't remove CO₂. If we display it (with a real NDIR sensor), the honest message is "open a window".
- **Connectivity** for the homelab audience means a local API (Home Assistant, MQTT), no account and no cloud. But any radio brings EU cybersecurity rules: the Radio Equipment Directive's cybersecurity requirements (mandatory since August 2025) and the Cyber Resilience Act (vulnerability reporting from September 2026, full requirements from December 2027). A branded app would also be class 9 software; see the trademark notes in [philosophy](01-philosophy.md).

### The room test — Idea *(Claude)*

The purifier measures its own CADR in the customer's room. Raise the particle level (a burnt match), press a button, and it runs the decay method from [go-to-market](03-go-to-market.md): measure the decay rate, subtract the natural decay, multiply by the room volume the user enters. Because the decay *rate* largely doesn't depend on the sensor's absolute calibration, a cheap sensor can do it.

Caveat: the sensor sits on the machine, so the result assumes a well-mixed room. It's a sanity check for the customer, not a lab certificate. I haven't seen a purifier that does this (worth checking), and it builds the brand's philosophy into the hardware.

## Compliance checklist *(Claude; confirm with a test lab)*

- **CE marking:** Low Voltage Directive, EMC Directive, RoHS. Safety standard: EN 60335-1 with EN 60335-2-65 (air-cleaning appliances).
- **If wireless:** the Radio Equipment Directive, including its cybersecurity requirements (EN 18031 standards), and the Cyber Resilience Act.
- **General Product Safety Regulation:** an EU-based responsible operator, traceability, safety information in local languages.
- **Per country:** WEEE producer registration and packaging registration.
- **Chemicals:** REACH (substances of very high concern in the product).
- **Performance claims:** CADR from a third-party lab (AHAM AC-1 or the IEC 63086 series), noise measured to a stated standard, zero-ozone validation (e.g. UL 2998).

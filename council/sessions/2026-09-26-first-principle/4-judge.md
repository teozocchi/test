# 4. The Judge

Council session 2026-09-26 · [Idea brief](idea.md) · [Believer's case](1-believer.md) · [Skeptic's attack](2-skeptic.md) · [Investor's assessment](3-investor.md)

## Verdict: FIX FIRST

Don't build the draft as written.
- A £251 box already delivers more than the draft's full-speed target of 300–400 m³/h, and does it at 38.8 dB(A).
- At €400 the draft makes roughly nothing per unit. The Investor estimates −€110 to +€55 on a realistic first run.
- The working docs already admit the first point: "At €400, 300–400 m³/h can't be the pitch" ([product doc](../../../docs/04-product.md)).

It isn't a KILL yet, because the case against it is a forecast, not a measurement.
- The Skeptic's fatal flaw is conditional in its own words: "If a prototype built within the €400 cost ceiling can't beat that on the same meter…"
- The Investor's "no" names the number that would change it.
- Both depend on a measurement nobody has taken. It takes 10 minutes to screen on paper and a weekend of building to settle.

A brand whose rule is "measure, don't argue" shouldn't be killed or funded on a rule of thumb.

This FIX FIRST comes with a tripwire. If the engine can't beat the Luggable with the carbon installed, the verdict becomes KILL. "Kilograms of carbon and a Claims Log" is not a fallback: none of the buyers in these arguments would pay €400 for that alone.

## The biggest risk

No winning number: a £251 PC-fan box already delivers 440 m³/h at 38.8 dB(A), and HEPA plus 2.3 kg of carbon cost this engine decibels and a parts bill that €400 can't carry.

## Weighing the three

### The Skeptic wins on the evidence

- **The rival that matters is the Luggable XL-7, not Philips or Xiaomi.** Engineers compare against the machines that win measured tests, and those machines have no filter lock-in to give up. The counter-positioning moat faces the wrong competitor, and Directive 2024/825 raises the minimum standard for everyone.
- **HEPA grade isn't a selling point** to buyers who know the Corsi-Rosenthal math. The working docs themselves rank CADR at a quiet level above filter grade.
- **Measured filter life measures the wrong part.** A 13 m² module running at a quarter of its rated flow clogs very slowly. The carbon is what saturates, and fan power can't detect that. Its alert therefore needs either a usage estimate, which is the kind of timer the brand attacks, or a gas sensor.
- **The hardware margin has to carry the company, and at €400 it doesn't yet.** Filter revenue is about zero by design. The docs' own rule is "Hardware-only companies die without recurring revenue" ([business model](../../../docs/05-business-model.md)). The Skeptic's math at retail prices and the Investor's volume estimates both come out near zero per unit at €400.
- **An open design is a build sheet for a cheaper copy.** The only defence is being first and trusted. That's a thin moat, and nothing in this ruling fixes it.

Where the Skeptic goes too far:
- **Carbon versus quiet is a size trade-off, not a law of physics.** The time air spends in the carbon depends on the bed's volume, not its shape. Pressure drop, though, falls steeply as the tray gets wider and shallower. Doubling the face area at the same volume cuts it roughly 4–8× (my calculation, standard packed-bed scaling). So 2.3 kg can run quietly in a bigger box. Whether that box fits the budget is still unknown.
- **The enemy isn't dead; it just isn't on the engineers' shortlist.** Mass-market machines still sell ionizers and "plasma", and quote noise figures without a method. The Believer's Coway example is listed at 24.4 dB and measured at 38.9 dB. That matters later, for mainstream buyers, but not for the first customers.
- **House rule 4 is marked "Proposed", not adopted** ([philosophy](../../../docs/01-philosophy.md)). It binds anyway, because dropping it would drop the brand.

### The Believer is right about the job, wrong about the rivals

- **The job is real,** though smaller than the stove count suggests. Stove smoke at bedtime needs particles, odour and noise handled in one box.
- **The standard 287 × 592 mm industrial module is the best idea in the file.** It settles the filter-format question the docs mark "Open, blocking". German B2B shops sell the module one at a time, so "buy ours or anyone's" is true in Europe.
- **Three of the Believer's claims broke under the Skeptic:**
  - DIY builders aren't stuck with US filters. A German build guide has used locally sold ePM1 panels since 2021.
  - The IQAir comparison matches on mass alone, across different media: IQAir's cell is partly impregnated alumina. The brand's own comparison rules warn against this.
  - The ~60 Pa figure leaves out the carbon bed.

### The Investor sets the right discipline, but the deposit test comes second

- €0 has been paid and there's no unit cost. €130–370k goes out before the first euro comes back.
- **The refundable-deposit page, showing the chart that beats you, is the right demand test.** It should run after the prototype measurement, not before:
  - a page that shows a measured number gives a truer signal than a page that only makes a promise;
  - there's no point taking deposits for an engine that fails a weekend test.

  The heating season runs until spring, so the test still falls inside it.
- The 2026/27 smoke season is gone for deliveries either way. The first winter this box can sell into is 2027/28.

### What's left standing

Take away everything the Skeptic broke and one gap in the market remains: a quiet machine with HEPA and kilograms of carbon for bedrooms that get stove smoke. It would be priced below the heavy-carbon brands: Austin Air costs $540–844 in the US and IQAir €1,399.
- The PC-fan boxes get their quiet CADR from low-resistance filters (MERV-13 or H11). None of those cited in these arguments carries kilograms of carbon.
- Bosch's Air 4000, a Warentest winner, has only a carbon layer.

That gap only exists if the engine stays quiet with the carbon in. Nobody has measured that, and measuring it is cheap.

## The 10-minute test

Before any prototype or code, check the engine on paper in an EC-fan maker's online fan selector. ebm-papst and Ziehl-Abegg both publish one.

1. **Enter 450 m³/h at 100 Pa.**
   - 450 m³/h is the Luggable's 440 m³/h CADR plus a margin for air leaking around the filter.
   - 100 Pa is the best case (estimate): about 75 Pa for the H13 module plus about 25 Pa for a wide, shallow carbon tray, grilles and housing. The 75 Pa comes from the Believer's datasheet (250 Pa at 1,500 m³/h), scaled linearly.
2. **Read the quietest fan's A-weighted sound power,** and note its price.
3. **Repeat at 150 Pa,** which is roughly what a compact carbon tray would add. Comparing the two results tells you how big the box has to be.

In a furnished room, the sound level 1 m away is roughly 6 dB below the fan's sound power (estimate). So a sound power of about 45 dB(A) matches the Luggable's 38.8 dB(A).
- **Up to 50 dB(A) at 100 Pa: build the prototype.** This paper check is only accurate to a few dB, and the prototype will settle it.
- **Above 50 dB(A) at 100 Pa: KILL.** The fan alone would be about 5 dB louder than the Luggable at 1 m (estimate), which is clearly audible.

## What flips it to BUILD

Replace the draft target ("300–400 m³/h at full speed, €400") with an engine that has been measured, costed and paid for. All three steps below must pass. Step 1 comes first; steps 2 and 3 can run in parallel.

1. **Measured.**
   - Build a plywood prototype with the H13 287 × 592 mm module, an EC fan and all 2.3 kg of carbon in a wide, shallow tray.
   - Run it at the same noise level as the Luggable XL-7, on the same meter at the same distance.
   - Its CADR, measured with the decay method in the same room, must beat the Luggable's.
   - Parts, a Luggable and meters cost about €1,000 (estimate).
2. **Costed.** Written supplier quotes for that exact engine put landed cost at no more than 50% of the net price (€168 at €400). If the numbers only work at a higher price, put that price on the deposit page.
3. **Paid for.** The page with the measured chart (Luggable, Trotec 170 E, Bosch Air 4000 and the prototype) collects 300 paid €50 refundable deposits within 30 days. That's the Investor's number.

If step 1 fails, it's a KILL. If step 3 falls short of 300, it's also a KILL, because by then every cheap test has been run. A KILL ends product #1, not the brand. The next session would then choose a category where measured competitors don't already own the headline number.

## Until then

- **Freeze the storefront.** Don't write any Astro code or build the Claims Log check until step 1 passes. The deposit page can be a single Shopify page.
- **Publish noise the way reviewers measure it:** at 1 m, in a room, next to any lab figure. That avoids the "listed 35, measured 39" embarrassment the Skeptic predicts.
- **Use only lab-tested figures for competitors in ads.** That lowers the risk of a German comparative-advertising warning letter (§6 UWG), which the Skeptic raised.

---

**Checked against.** I read the quotes from the working docs directly in [01-philosophy.md](../../../docs/01-philosophy.md), [04-product.md](../../../docs/04-product.md) and [05-business-model.md](../../../docs/05-business-model.md). Market and cost figures come from the other roles, and their sources and caveats apply. The packed-bed scaling and the sound-level conversion are my estimates. The verdict is saved to the council ledger at /home/user/test/council/ledger.md.

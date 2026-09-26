# Council ledger

The council's shared memory: every idea it has reviewed and every verdict, newest first. The Judge adds an entry at the end of each session. The full arguments are in [`sessions/`](sessions/).

Entry format:

```markdown
## <YYYY-MM-DD> · <idea name>

- **Idea:** one or two sentences
- **Verdict:** BUILD | FIX FIRST | KILL
- **Biggest risk:** one line
- **10-minute test:** what the founder runs before writing any code
- **Flips to BUILD when:** the exact change (FIX FIRST only)
- **Next session starts from:** where to pick up
- **Arguments:** links to the session's idea brief and each role's argument
```

---

<!-- New entries go directly below this line, newest first. -->

## 2026-09-26 · First Principle, product #1 (air purifier)

- **Idea:** A €400 home air purifier (EC centrifugal fan, H13 HEPA, about 2.3 kg of refillable carbon, 300–400 m³/h CADR target, open filters, measured filter life, local control, no ozone) as the first product of First Principle, an EU brand that only claims what it can measure. It sells first to engineer-skeptics in DACH and the Nordics.
- **Verdict:** FIX FIRST
- **Biggest risk:** No winning number: a £251 PC-fan box (Luggable XL-7) already delivers 440 m³/h at 38.8 dB(A), and HEPA plus 2.3 kg of carbon cost this engine decibels and a parts bill that €400 can't carry.
- **10-minute test:** In an EC-fan maker's online selector (ebm-papst or Ziehl-Abegg), find the quietest fan for 450 m³/h at 100 Pa (the H13 module's ~75 Pa plus a wide, shallow carbon tray and housing; estimate) and read its A-weighted sound power. Up to 50 dB(A): build the prototype. Above 50 dB(A): KILL.
- **Flips to BUILD when:** all three pass. (1) A plywood prototype with the 287 × 592 mm H13 module and all 2.3 kg of carbon installed beats a Luggable XL-7 on CADR at equal noise: same room, same meter, same decay method. (2) Written supplier quotes put landed cost at no more than 50% of the net price (€168 at €400). (3) A page showing the measured chart collects 300 paid €50 refundable deposits in 30 days. If (1) fails or (3) misses 300, KILL.
- **Next session starts from:** the fan-selector result. If it passed, bring the prototype-vs-Luggable measurement, then the quotes and the deposit count. Website and Claims Log code stay frozen until (1) passes. On a KILL, the brand stays and the next session picks a new product #1.
- **Arguments:** [Idea brief](sessions/2026-09-26-first-principle/idea.md) · [Believer](sessions/2026-09-26-first-principle/1-believer.md) · [Skeptic](sessions/2026-09-26-first-principle/2-skeptic.md) · [Investor](sessions/2026-09-26-first-principle/3-investor.md) · [Judge](sessions/2026-09-26-first-principle/4-judge.md)
- **Follow-up, 2026-09-26 (recorded by Claude): gate 0 failed.** The quietest fan the founder found for 450 m³/h at 100 Pa has a sound power of 59.3 dB(A) (K3G250RE0707), 9.3 dB over the limit. Under the tripwire, product #1 as specified is killed; the brand stays. Raw numbers and analysis: [product doc](../docs/04-product.md). The next session starts from choosing what to bring: a carbon-first purifier without the H13 module, or new categories.
- **Follow-up, 2026-09-26 (founder's decision): project archived.** First Principle isn't dead; it's filed away until a category is found where the physics allow a 50% gross margin. The three re-entry checks are in the [README](../README.md). The next session starts from a candidate category that has passed them.

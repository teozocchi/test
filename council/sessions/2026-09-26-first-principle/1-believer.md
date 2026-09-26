# 1. The Believer

Council session 2026-09-26 · [Idea brief](idea.md)

## Who needs it

An engineer in a German or Danish suburb whose €39.99 IKEA sensor shows the neighbours' wood stoves reaching the house every winter evening. This isn't a niche problem. Germany has about 11.7 million single-room stoves and fireplaces, and household wood heating emits more fine dust than all car and truck exhaust (UBA). In Denmark, wood stoves are the largest source of PM2.5, roughly half of it (estimate). The smoke brings both particles and odour, and it arrives at bedtime, so one machine has to deliver HEPA, real carbon and quiet at once. Today these people take one of three routes:
- **Build a Corsi-Rosenthal box** from US-size filters that European shops don't stock.
- **Buy a Levoit or Xiaomi and fight it.** Replacement ESPHome firmware for those two brands has 188 and 144 GitHub stars. Two Flipper Zero apps released in July 2026 do nothing except reset the NFC filter counters on Xiaomi filters.
- **Pay €1,399 for an IQAir HealthPro 250.** Its gas cell holds 5 lb of carbon and alumina (manufacturer figure), about the mass First Principle plans to ship at €400.

## Why now

Three things have lined up.
- **The law.** Directive 2024/825 applies from tomorrow, 27 September 2026. It adds to the EU blacklist two practices: pushing buyers to replace consumables earlier than technically necessary, and falsely claiming (or hiding) that third-party consumables impair a product. That describes how much of the category works today:
  - filter countdowns that are estimates, not measurements;
  - Philips models that lock their own fan once a filter alert has been ignored for two weeks;
  - Xiaomi filters with NFC life counters.

  Measured filter life and an open filter format are on the right side of this rule by design.
- **The referee.** Stiftung Warentest, known to over 90% of Germans, now tells the biggest target market that some purifiers that clean a 16 m² bedroom with a new filter manage only a fraction of that once the filter is used.
- **The instruments.**
  - A PM2.5 sensor costs €40.
  - Home Assistant grew from 1 to 2 million installations in 2024.
  - Matter 1.2 defined a purifier device type that includes HEPA and carbon filter monitoring.
  - EN IEC 63086-2-1 (2024) gave Europe its own CADR test.
  - Belkin's shutdown of the Wemo cloud in January 2026 showed buyers what "requires an app" means over a product's life.

A pitch of "measure it yourself" only works if customers can measure. Now they can.

## The best version

A heavy, quiet box that is also a measuring instrument.
- **Inside:** a standard 287 × 592 mm H13 industrial filter module. One supplier's datasheet rates the 292 mm-deep version at 13 m² of media and 1,500 m³/h at 250 Pa. Run at about a quarter of that flow, it would see roughly 60 Pa at 350 m³/h (my calculation, assuming pressure drop scales linearly with flow), so the EC fan can turn slowly and quietly. Add 2.3 kg of refillable carbon, and no ionizer or UV.
- **On the box:** one headline figure, "X m³/h at 35 dB(A)", measured by a lab to EN IEC 63086-2-1, with the full CADR/noise/power curve published behind it.
- **In use:**
  - The fan holds its airflow as the filter loads, and uses its own watts and rpm to tell you when it no longer can.
  - A button runs the particle-decay CADR test in your own room.
  - Matter and a local API put it in Apple Home or Home Assistant, with no First Principle app or account.

If it goes right, owners post their room-test curves, and Stiftung Warentest's verdict goes into the Claims Log whatever it says. First Principle becomes the purifier that people who measure recommend, and product #2 starts with that trust on day one.

## The unfair advantage

The big purifier brands can't copy this without hurting themselves. Their business works best when buyers don't measure: proprietary filters, estimated countdowns, CADR quoted at full speed, and noise quoted without a method. For example, the Coway Mighty, Wirecutter's long-time pick, is listed at 24.4 dB on its lowest speed; HouseFresh measured 38.9 dB at 3 ft.

To match First Principle they would have to open their filter formats, tie replacement to measured filter loading, and put their existing marketing copy through a public claims log. That means less filter revenue and public retractions. A startup with no installed base and no past claims pays none of that cost. This is counter-positioning, and from tomorrow EU law pushes the other brands in the same direction.

The advantage compounds. Air-purifier reviews are the textbook case of untested affiliate content (HouseFresh documented it in 2024), so the reviewers people still trust are the ones who measure. Every new measurement costs competitors and helps the one product built to be measured.

## The bet

In a category where buyers can verify nothing, a machine that visibly wins on quiet clean air, and lets every owner prove it, will win over the people who measure, and they will bring everyone else. Concretely, the engine has to deliver a lead in CADR at quiet speeds that is big enough to show on camera, at a unit cost that lets a €400 price carry the company. The Claims Log, the open filter and the room test are the megaphone; that number is the message.

---

**Sources.** The web-page fetcher was blocked for most of these domains, so I checked these figures through search results rather than reading each page directly. I read the GitHub projects directly.
- Wood smoke: [UBA](https://www.umweltbundesamt.de/themen/feinstaub-aus-holzfeuerungen), [Danish EPA](https://eng.mst.dk/industry/air/air-pollution-from-stoves)
- Sensor: [IKEA VINDSTYRKA](https://www.ikea.com/global/en/newsroom/innovation/ikea-launches-vindstyrka-a-smart-sensor-to-measure-indoor-air-quality-230214/)
- Purifier hacking: [Levoit ESPHome](https://github.com/acvigue/esphome-levoit-air-purifier), [Xiaomi ESPHome](https://github.com/jaromeyer/mipurifier-esphome), [Flipper Xiaomi filter-reset app](https://github.com/khmm12/flipper-xiaomi-filter-reset)
- Competitors: [IQAir DE](https://www.iqair.com/de/products/air-purifiers/healthpro-plus), [IQAir V5-Cell](https://www.iqair.com/products/replacement-filters/v5-cell-f2), [HouseFresh Coway review](https://housefresh.com/coway-airmega-ap-1512hh-review/), [Philips filter lock](https://usa.philips.com/c-t/XC000015272/my-philips-air-purifier-powers-off)
- Law and testing: [EU Q&A on 2024/825](https://transition-pathways.europa.eu/retail/news/updated-qa-directive-empowering-consumers-green-transition), [Stiftung Warentest](https://www.test.de/Luftreiniger-im-Test-5579439-0/)
- Instruments and standards: [Home Assistant 2M](https://www.home-assistant.io/blog/2025/04/16/state-of-the-open-home-recap/), [Matter 1.2](https://csa-iot.org/newsroom/matter-1-2-arrives-with-nine-new-device-types-improvements-across-the-board/), [IEC 63086-2-1](https://webstore.iec.ch/en/publication/65299), [Wemo shutdown](https://www.belkin.com/support-article/?articleNum=335419)
- Filter module and reviews: [H13 V-module datasheet](https://www.ulpatek.com/wp-content/uploads/2018/02/HIGH-CAPACITY-HEPA-FILTER-with-V-MODUL-Design-HHV.pdf), [HouseFresh 2024](https://housefresh.com/david-vs-digital-goliaths/)

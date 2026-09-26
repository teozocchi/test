# 2. Website and software

## Two-layer product descriptions — Idea

No marketing fluff in either layer.

1. **Simple:** plain language that still explains how the product works. Written for everyone.
2. **Rigorous:** formatted like a scientific whitepaper, with footnotes, equations and lab reports.

Proposed rules *(Claude)*:
- **Both layers make the same claims.** The simple layer never says anything the rigorous layer doesn't prove.
- **The simple layer is the default**, with the rigorous layer one tap away. Most people will never open it, but knowing it's there builds trust.
- Working labels: **"How it works"** / **"The proof"**.

This is also the answer to the mainstream-appeal constraint: the site reads like a consumer brand first and a datasheet second.

## Claims Log — Idea

A dedicated page listing every factual claim the company has ever made, each linked to the evidence behind it. Total, radical transparency.

### Proposed implementation *(Claude)*

Store claims as structured data, one entry per claim. Pages reference claims by ID instead of restating them. **The site build fails if a page uses a claim that isn't in the log with evidence attached.** In other words: *our website won't build if we make a claim we can't prove.*

Example entry (all values are placeholders):

```yaml
id: C-0001
claim: "Reduces free chlorine by at least 95% at 10 L/min and 38 °C."
product: shower-filter
status: active            # active | revised | retracted
evidence:
  tier: third-party-lab   # third-party-lab | in-house-measurement | calculation | published-literature
  standard: NSF/ANSI 177  # the standard for shower filters
  source: reports/C-0001-lab-report.pdf
first_published: 2026-10-01
history: []               # every change: date, old wording, reason
```

Notes:
- **Label the evidence tier.** A calculation *supports* a claim; a measurement *proves* it. Each claim should say which one it rests on.
- **Physics claims need lab tests, not clinical studies.** The right evidence is usually our own product tested by an accredited (ISO/IEC 17025) lab against a published standard. Clinical studies only matter for biological claims, which house rule 2 keeps us away from.
- **Retracted claims stay in the log**, with the reason. That's the strongest credibility signal we have.
- **Git history is the audit trail.** The Claims Log could even link to a public repository so anyone can see when and why each claim changed.

## Framework — Proposed *(Claude)*

- **Content site: Astro.** Built for content-heavy sites: Markdown/MDX with footnotes, maths rendering (KaTeX), and content collections with schema validation and cross-references, which is exactly what the Claims Log check needs.
- **Commerce: don't build it.** Use Shopify for checkout, payments, EU VAT and inventory, connected to the Astro site through Shopify's Storefront API.
- **Alternative:** Shopify alone at launch. Faster, but the whitepapers and the Claims Log are harder to do well.

## Hosting — Proposed *(Claude)*

Static hosting on Cloudflare Pages, Netlify or Vercel. All work and all are cheap; decide together with the framework.

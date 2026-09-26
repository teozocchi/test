# 2. Website and software

> **Frozen (council, 2026-09-26):** no Astro code and no Claims Log build check until the prototype passes gate 1 (see [product](04-product.md)). The deposit page for gate 3 can be a single Shopify page.

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
claim: "Clean air delivery rate of 350 m³/h for particles."
product: air-purifier
status: active            # active | revised | retracted
evidence:
  tier: third-party-lab   # third-party-lab | in-house-measurement | calculation | published-literature
  standard: AHAM AC-1     # or the IEC 63086 series; to be decided
  source: reports/C-0001-lab-report.pdf
first_published: 2027-03-01
history: []               # every change: date, old wording, reason
```

Notes:
- **Label the evidence tier.** A calculation *supports* a claim; a measurement *proves* it. Each claim should say which one it rests on.
- **Physics claims need lab tests, not clinical studies.** The right evidence is usually our own product tested by an accredited (ISO/IEC 17025) lab against a published standard. Clinical studies only matter for biological claims, which house rule 2 keeps us away from.
- **Retracted claims stay in the log**, with the reason. That's the strongest credibility signal we have.
- **Git history is the audit trail.** The Claims Log could link to a public repository so anyone can see when and why each claim changed.
- **Competitor figures in ads need the third-party-lab tier** (council). In Germany, a named competitor can send a formal warning letter over a comparison backed only by in-house data; see comparisons in [go-to-market](03-go-to-market.md).

## Framework — Decided, frozen until gate 1

**Astro + headless Shopify.**

- **Shopify** runs the back end: inventory, payments, EU tax compliance, shipping labels. Its back end is hard to beat; its front-end themes are slow and JavaScript-heavy.
- **Astro** builds the site: fast pages, MDX whitepapers, a custom design, and content collections for the Claims Log build check.
- The two connect through Shopify's **Storefront API**. When someone clicks "Buy", the site hands off to Shopify's checkout.

Notes *(Claude)*:
- Astro ships no JavaScript by default, but the cart needs a small interactive component. "Nearly zero JS" is the accurate claim.
- The checkout page is Shopify's hosted checkout, so its styling is limited to what Shopify's checkout settings allow. The custom design covers everything before it.

## Hosting — Open

Proposed *(Claude)*: static hosting on Cloudflare Pages, Netlify or Vercel. All three work and are cheap at this scale. Frozen with the rest of the website.

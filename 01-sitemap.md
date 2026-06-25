# NeoPaaS Website — Site Map (v3, merchant-anchored)

The core insight: **merchants are the only customers (they pay). MSPs and POS vendors are partners (they distribute).** The website serves both jobs — but on separate pages.

```
neopaas.com
├── /                          ✅  Home — anchored on the MERCHANT
│
│   The full visitor journey for a multi-branch operator:
│   hero · pain on-ramp · before/after · 3 outcomes · dashboard mockup ·
│   4 industry cards · how it works · compliance · manual vs NeoPaaS ·
│   partner strip (subtle) · quote · final CTA
│
├── /industries                🟡  Deep pages per merchant segment
│   ├── /industries/restaurants
│   ├── /industries/retail
│   ├── /industries/hotels
│   └── /industries/logistics
│
├── /platform                  🟡  Product deep-dives (dashboard tour,
│   ├── /platform/reconciliation     reconciliation, compliance, etc.)
│   ├── /platform/compliance
│   ├── /platform/dashboard
│   └── /platform/onboarding
│
├── /pricing                   🟡  Per-terminal pricing + ROI calculator
│
├── /partners                  ✅  Combined partner program landing page
│   ├── /for-payment-providers ✅  MSP / acquirer pitch (already built)
│   └── /for-cashier-systems   🟡  POS / ERP / kiosk white-label pitch
│
├── /resources                 🟡  Blog · ZATCA guide · ROI calculator
│
├── /about                     🟡  Company, founders, investors
├── /contact                   🟡  Sales contact form
└── /docs                      🟡  Developer documentation (subdomain)
```

## The new mental model

### Customers (homepage anchors here)
- **Merchants** — multi-branch operators in F&B, retail, hospitality, logistics
- Who pays: them
- Where the website does the most work: home page + industry pages + pricing
- Buyer: CFO, Operations Director, CTO
- Inbound: Google search, peer referrals, partner referrals

### Partners (separate section, accessible via nav)
- **MSPs / Acquirers** (Geidea, NeoLeap, NmoHub)
- **POS / ERP / Kiosk vendors** (FOODICS, OASIS, vertical SaaS plays)
- Who pays NeoPaaS: nobody — they collect from merchants and take a cut
- Where the website does the most work: `/partners` landing + per-segment partner pages
- Buyer: VP Partnerships (MSP), VP Product / CEO (POS vendors)
- Inbound: direct outreach, founder intros, occasional Google

## Section pattern map — Home page v3 (✅ built)

| Section | Pattern source | Why this pattern |
|---|---|---|
| Top nav | Rho, Square | Clean. Single CTA. `For partners` lives in nav for the 10-15 people who need it. |
| Hero (merchant) | Adfin, Sunday | Plain merchant headline. No jargon eyebrow. CTA: "Book a demo." |
| Pain on-ramp | Light, Helcim | Three plain-language pains. "If any of this sounds familiar." |
| Before/after diagram | original | Visual proof of what we replace. Critical on-ramp. |
| 3 outcomes | Bridge, Orb | What changes for your team. Reconciliation, ZATCA, visibility. |
| Dashboard mockup | Stedi, Adfin | NEW. Concrete product visualization with realistic data. |
| 4 industry cards | Square, Sunday | F&B / retail / hotels / logistics. Self-ID on segment. |
| How it works | Square, Helcim | 3 steps from signature to live. Merchant POV. |
| Compliance | Anrok, Pennylane | ZATCA / SAMA / PCI-DSS as a moat moment, given its own section. |
| Manual vs NeoPaaS | Helcim, Light | Reframed from build-vs-buy to manual-vs-platform. Merchant-relevant. |
| Partner strip | Adyen footer modules | Quiet section pointing partners (MSPs, POS) to their pages. |
| Pull quote | Sunday | Editorial serif moment. |
| Final CTA | Adyen | "See your dashboard in 30 minutes." |
| Footer | Standard | Three columns. |

## Section pattern map — `/for-payment-providers` (✅ built)

Still works as-is. Now lives as a SECONDARY partner page, not the primary conversion engine. Accessible from nav (`For partners`) and from the partner strip on the home page.

## What's NEXT — recommended build order

After you review the merchant-anchored home:

1. **`/for-cashier-systems`** — POS / ERP white-label pitch (mirrors MSP page structure)
2. **`/pricing`** — per-terminal pricing + interactive ROI calculator for merchants
3. **`/industries/restaurants`** — deepest vertical we have material for (the logistics use case can fuel the logistics page too)
4. **`/platform/compliance`** — the ZATCA moat page (most defensive SEO topic)
5. **`/about`** — credibility for both merchant and partner sales

## Pages we are NOT building (yet)

- A generic "Customers" page — we have no real customers to put on it
- A blog — wait for real content
- A pricing tier with "Starter / Pro / Enterprise" — pricing is per-terminal, not tiered
- Static testimonial slider — wait for real partners

## What changed from v2 → v3

- Hero rewritten for the merchant audience (not blended)
- Persona section deleted (was blending the three audiences)
- Industries section added (segments INSIDE the merchant audience)
- Dashboard mockup added (concrete product proof)
- "Manual vs NeoPaaS" replaces "Build vs Buy" (merchants don't build)
- Partner strip is now a small dedicated section near the footer, not blended into the personas
- Nav simplified to merchant-focused items + one `For partners` link

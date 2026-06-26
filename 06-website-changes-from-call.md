# Website Changes — From Kickoff Call with Omer

Distilled from the founder transcript. Three buckets: **must-fix now** (overclaiming, brand misalignment), **add this content** (real customers, missing sections), and **decisions still pending** (need your call before I implement).

---

## 🔴 MUST-FIX NOW — three of these are overclaiming

Current website asserts capabilities Omer told you aren't actually built yet. This is the most urgent thing to fix — partners and merchants will discover it in the first demo.

### 1. ZATCA is NOT actually integrated yet
- **Where it appears:** Home compliance section, Hero subheadline (*"File ZATCA automatically"*), Bento outcome card #2 (*"ZATCA filing — Filed automatically"*), and footer link.
- **What Omer said:** *"ZATCA is not there yet. This is the IRS here. It's called ZATCA."*
- **Fix:** Reframe to *"ZATCA Phase 2 ready"* or *"ZATCA-compliant architecture"* — soften from "filed automatically today" to "designed for ZATCA Phase 2 from day one, going live with the upcoming release." Or move to a **Coming Soon / Roadmap** section.

### 2. AI / "intelligence layer" framing — match reality
- **Where it appears:** Currently no explicit AI claims, but the live transaction feed and counters imply real-time intelligence.
- **What Omer said:** *"AI, not, not yet. Nothing about AI yet but we're working on it... let's start using new marketing language. Let's call it an intelligence layer."*
- **Fix:** Rename "dashboard" → **"intelligence layer"** throughout (Omer's explicit ask). Don't add AI/agentic claims yet — the dashboard with real-time visibility IS the intelligence layer story. Tone update only, no fabricated AI claims.

### 3. Loyalty programs — remove or roadmap
- **Where it appears:** Not heavily featured, but if mentioned anywhere, remove.
- **What Omer said:** *"Loyalty, we didn't add that. We have some requests... we have some requests from loyalty service providers."*
- **Fix:** Don't claim it. If it appears, move to roadmap.

### 4. Brand structure — BAB ≠ NeoPaaS
- **Where it appears:** Logo says "NeoPaaS." Footer attributes "Built by Bab Innovations." Domain will be `babbinnovations.com`.
- **What Omer said:** *"We're gonna be using the babbinnovations.com, and the logo is gonna be BAB, but the product we're gonna be selling is gonna be NeoPaaS."*
- **Fix:** Logo should be **"BAB"** with NeoPaaS positioned as the product (likely as nav sub-text or hero eyebrow: *"NeoPaaS — the payment platform by BAB Innovations"*). Footer should lead with BAB. Page titles still use NeoPaaS as the product name.

---

## 🟢 ADD THIS — real content the site is currently missing

### 1. Logistics case study (the strongest one — make it the lead proof)
- **Customer:** JMT/JNT (Chinese logistics, well-known in Saudi Arabia)
- **What they got:** Cash-on-delivery replaced. Couriers carry portable terminals. **Full automation of claim cycle** — system maps the settlement, matches it, attaches evidence, sends to the bank. Zero manual processing.
- **Why it's the lead:** *"The most authenticated, the richest with information and feedback."* Omer's words.
- **Where to put it:** A dedicated case-study block on the home page **above the partner strip**, OR a `/customers/jmt` page linked from the bento "Reconciliation" card. Use real operator quote attribution (per Slang.ai pattern — *"Head of Operations, JMT Logistics, 200+ couriers"*).

### 2. Real customer logo wall
- **Replace placeholders with:** JMT/JNT (logistics), Finelook (close retailer), Khalid bin Khalid (well-known F&B chain). Confirm with Omer which can be used publicly.
- **Where:** Existing logo wall section on home (currently 12 placeholder slots).

### 3. The "full claim cycle automation" capability
- **What it is:** For logistics: NeoPaaS auto-maps settlements → matches → attaches evidence → sends claim to bank, in a full cycle. No human in the loop.
- **Where to add:** Bento card or dedicated capability section. This is a real, defensible workflow that competitors don't have.
- **Frame:** *"Custom workflows built into your reconciliation"* — open up the "customization per client need" angle Omer emphasized.

### 4. Industries — restructure
- **Currently:** F&B / Retail / Hotels & Hospitality / Logistics
- **Omer's actual industries (in priority order):** **Logistics** (most validated) / **Tourism** (broader than hotels) / **Healthcare** (new) / **Retail** + **F&B** (getting traction)
- **Fix:** Reorder cards to put Logistics first (it's the proven one). Either change "Hotels & Hospitality" to "Tourism" (broader) OR keep Hotels and add Healthcare as a 5th card. F&B stays since it's getting traction. Healthcare is new — add it.

### 5. Roadmap section ("Coming next")
- **What's coming, per Omer:**
  - **Online payments** (in the kitchen — "only two companies working in this space")
  - **Bank transfers**
  - **Open banking for account transfers**
  - **AI features** (mismatch analysis for banks is in early request stage)
  - **Loyalty integrations**
  - **ZATCA Phase 2 e-invoicing** (in development)
- **Where:** Small section near the bottom (above final CTA), labeled "What's coming next" — sets the vision without overclaiming. Honesty signal.

### 6. "Customization / API" callout
- **What Omer emphasized:** *"The flexibility that we give within the dashboard when it comes to API usages or customization per need of our clients."*
- **Where:** A small section or feature card calling out *"Built around your workflow — custom integrations, custom flows, custom reporting."* This is a real differentiator for the bigger merchants/partners.

### 7. Two-year data retention (Saudi regulatory)
- **Already mentioned in compliance** but make it more explicit: *"Two years of transaction data, retained and queryable, per Saudi central bank requirements."*

---

## 🟡 LANGUAGE / TONE UPDATES

### 1. "Dashboard" → "Intelligence layer"
Omer's explicit phrase. Update across home, merchant page, partner pages. This is a copy-paste replacement — the visual stays the same, but the word changes the perceived value.

### 2. "POS" → keep, but acknowledge "ECR"
Omer calls them **ECRs (Electronic Cashier Registers)**. POS is more universally understood, so keep POS as the primary term, but mention ECR once on the for-cashier-systems.html page to signal industry fluency (*"POS / ECR / ERP / kiosk vendors"*).

### 3. Tier 1 sensitivity — soften MSP naming
- **What Omer said:** *"There would be some sensitive, so referring them directly on the website, I think we should be, we should pay a close attention to how we're gonna reflect this... You know how vendors when they're already providing technology to others, how they would want this."*
- **Fix:** On `for-payment-providers.html` and home `index.html`, currently we name Geidea, NeoLeap, NmoHub directly in the diagram and copy. **Replace specific names with generic placeholders** (e.g., *"Major Saudi acquirers"* / *"Leading payment providers"*) until you have explicit permission from each named partner to appear. Keep the diagrams accurate but anonymize.

### 4. Tier 2 — emphasize white-label, NOT distribution
- **What Omer said:** *"They don't prefer distribution... they don't want to break their client journey, so the solution needs to be embedded within their own interfaces or dashboards or apps."*
- **Status:** The `for-cashier-systems.html` page already emphasizes white-label. ✓ Good. Just verify language is "embedded, white-labeled, your brand" — not "distribute" or "resell."

### 5. Cash flow + finance team — strengthen the buyer profile
- **What Omer said:** *"The cash flow managers, mostly they like us the most. The finance people, they like us the most."*
- **Fix:** On the merchant home page, lean even harder into the finance/CFO/cash-flow-manager persona in copy. The pain cards already do this — confirm hero subhead and CTA also speak directly to finance owner.

---

## ⚖️ DECISIONS PENDING — Omer asked YOU to make these calls

These came up in the call as *"your call"* or *"I'll follow your recommendation."* They affect the website's structure and need a yes/no from you before I implement:

### Decision 1 — Single landing page for everyone, or persona-specific?
- **Current state:** You already chose the answer — home is merchant-anchored with separate partner pages. ✓ Good.
- **What Omer expects:** A clear best-practice recommendation. **You can confirm this is the structure**, no change needed.

### Decision 2 — Show current capabilities only, or the full 6-month vision?
- **Current state:** Site shows everything as if live (some overclaiming — see "MUST FIX" above).
- **Recommended call:** **Show current capabilities as built, future capabilities in a clearly-labeled "Coming next" section.** This is the honest middle ground. American B2B sites typically do this — current features in main copy, roadmap in a separate visual block.
- **Wait for your confirmation before I update.**

### Decision 3 — Pricing display
- **Current state:** Merchant page shows tiered pricing (SAR 22 / 18 / 14 per terminal/month).
- **What Omer said:** *"We're working on financial model optimization. It will be ready by next week."* Plus he's debating upfront fees for big players vs. subscription only for ECRs.
- **Recommended call:** **Remove specific SAR amounts** until Omer's financial model is finalized. Replace with *"Per-terminal subscription, volume-tiered. Talk to us for your custom quote."* Avoid hard-coding prices that may change.
- **Wait for your confirmation.**

### Decision 4 — How to handle Tier 1 partner sensitivity
- **What Omer said:** *"BR is very interesting when it comes to big players like us. So we need to play it well."*
- **Recommended call:** **Anonymize partner references** (see Language updates above). Don't name specific MSPs/acquirers as "our partners" until each has explicitly approved being named on the website. Use generic *"Saudi acquirers / payment providers"* language.

---

## SUMMARY — what I'll change once you confirm

1. **Fix ZATCA / AI / loyalty overclaiming** — reframe to roadmap or honest "designed for" language.
2. **Update logo to BAB**, position NeoPaaS as product name.
3. **Add JMT logistics case study** as lead proof — full claim cycle automation.
4. **Replace placeholder logos** with JMT/JNT, Finelook, Khalid bin Khalid (subject to permissions).
5. **Reorder industries** — Logistics first, add Healthcare, consider Tourism.
6. **Add Roadmap section** — Online, Bank transfers, Open banking, AI, Loyalty, ZATCA.
7. **Replace "dashboard" with "intelligence layer"** site-wide.
8. **Anonymize Tier 1 partner names** until permissions confirmed.
9. **Remove specific pricing amounts** — replace with "talk to us."
10. **Add "Customization / API" capability section.**

---

## ONE STRATEGIC NOTE

The most important thing this call surfaced for the website **is not on this list above**:

> The website is currently positioned correctly (merchant-anchored, persona pages for partners). But it's **overclaiming on three of its four big product moats** — ZATCA, AI, loyalty. If a partner clicks "demo" and discovers reconciliation works but ZATCA isn't built, the deal is dead.

Fixing the overclaiming is more important than any new content addition. Do this first, then add the JMT story, then everything else.

---

**Recommended next steps in order:**

1. **You confirm:** the four pending decisions above (yes/no each).
2. **I do a single edit pass:** fixes the overclaiming, swaps "dashboard" → "intelligence layer", anonymizes Tier 1 names, removes specific pricing.
3. **You upload from Omer:** the JMT case study + customer logos as PNGs into the repo.
4. **I add:** the case study block, real logos, Healthcare to industries, Roadmap section, Customization callout.
5. **Push to GitHub, redeploy via Vercel** — Omer can see and approve before the next call.

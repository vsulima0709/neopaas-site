# NeoPaaS Website — Methodology

How to build a NeoPaaS website page (or any future page) in a way that doesn't drift back to generic SaaS. Paste this into Claude as a skill via Settings → Capabilities when you're ready to make it permanent.

---

## When to use this methodology

Any time you're writing or wireframing a NeoPaaS-facing page: home, persona page, product page, pricing, blog landing, case study, partner one-pager. Do not skip the steps.

## The three rules

**1. Compliance is the hero, not a footnote.**
ZATCA, Mada, SAMA are not boring trust badges — they're the entire moat. Every page should treat them like Pennylane treats French e-invoicing or Anrok treats VAT compliance: at the top, with urgency, with a date if relevant.

**2. One bold color, one bold shape, one bold word per page.**
NeoPaaS's palette: warm cream `#f5f1e8` + deep forest green `#0c3b2e` + warm clay accent `#c2410c`. Not fintech-blue. Not gradients. One accent does all the work. One typographic move (oversized H1 with tight tracking) and one signature shape (the cog/rail metaphor) carry the brand.

**3. Real numbers and real product UI beat illustrations.**
No abstract orbs, no laptop-with-glow, no "person looking at chart." Use real screenshots of the NeoPaaS dashboard, real terminal photos, or single rendered objects (a Mada terminal, a settlement ledger row). When stuck, default to oversized type and white space.

## The voice — five do's, five don'ts

**Do:**
- Write headlines that end in a period. (BVNK move.) Feels editorial and definitive.
- Use insider language the buyer recognizes. "Live in 4 weeks. Not 18 months." "Built to close." (Tabs, Helcim.)
- Lead with single nouns, not verb-laden feature lists. "Orchestration. Settlement. Reconciliation. Compliance." (Bridge.)
- Put the math on the page, not behind a "Book a Demo" form. (Rainforest, Owner.)
- Sound like a confident operator talking to another operator — not a marketing agency.

**Don't:**
- Don't write "seamless", "innovative", "revolutionary", "world-class", "best-in-class", "next-generation", "cutting-edge", "transform your business", "unlock the power of", "empower". If a word would appear in 5,000 other SaaS sites, kill it.
- Don't use fake friendly enthusiasm. ("We're so excited to share…")
- Don't write three-clause sentences with two adjectives each. One idea per sentence.
- Don't bury the price, the terms, or the rev share. Partners want to see them.
- Don't say what the product *does*. Say what *changes for the customer*. ("30+ hours per week → 3 hours" beats "automated reconciliation engine".)

## The workflow — 6 steps, in order

### Step 1 — Anchor on three references
Pick **three** of the user's reference sites that best fit the page you're building. Not all twelve. Three is the number where the patterns are diverse enough to mix but not so many they blend into mush.

For NeoPaaS, the working trio is:
- **Pennylane** — for regulation-as-hero (the ZATCA play)
- **BVNK** — for licensing-as-feature + period-on-every-headline voice
- **Stedi** — for code-block hero + plainspoken expert tone

For pages that are more emotional / persona-led, swap one of those for **Sunday** (editorial pull-quotes) or **Adfin** (warm visual punch).

### Step 2 — Extract the page-specific patterns
For each of the three references, capture for the *same page type you're building*:
- The hero pattern (length, structure, what's above the fold, dual CTA or single)
- The proof pattern (logos? stats? quotes? code? a calculator?)
- The "what we do" pattern (single-noun list? feature cards? scrollable demo?)
- The CTA pattern (where, how many, what they ask)
- The tone — read the first 100 words aloud, then write yours in the same cadence

### Step 3 — Strip the client materials
The client's GTM doc, sales deck, and use cases are AI-generated and dense. Treat them as **research notes, not source copy**. Pull out:
- Hard numbers (2.5M terminals, 1.4% wireless, $300-800K cost center, 4 weeks, 20% rev share)
- Specific entities (Mada, ZATCA, SARIE, SAMA, Geidea, NeoLeap, NmoHub, FOODICS)
- Real customer pain quotes if any exist
- Then close the doc. Write the page from memory. If you write from the doc open, you'll regurgitate.

### Step 4 — Draft three voice variants per major section
For the hero and for each persona tile, write **three** versions:
- One in the voice of reference A
- One in the voice of reference B
- One in the voice of reference C
- Then pick. Or hybrid the best lines.

This is the single highest-leverage step. It's the difference between average and great.

### Step 5 — Build the wireframe in HTML
Not Figma first. HTML is faster to iterate, easier to share, can be read on phone, and forces decisions about responsive behavior. Use the shared CSS tokens below.

### Step 6 — Cut 30%
First draft is always too long. Read the page top to bottom. Cut every sentence that does not add new information. Cut every adjective that is not load-bearing. Then cut 30% more.

## Design tokens (paste into any new page)

```css
:root {
  /* Color */
  --bg: #f5f1e8;
  --bg-soft: #ede7d6;
  --ink: #1a1614;
  --ink-soft: #5a544e;
  --green: #0c3b2e;
  --green-soft: #1f5546;
  --clay: #c2410c;
  --clay-soft: #ea580c;
  --line: rgba(26, 22, 20, 0.12);

  /* Type */
  --sans: 'Inter', system-ui, -apple-system, sans-serif;
  --serif: 'Instrument Serif', Georgia, serif;
  --mono: 'JetBrains Mono', 'SF Mono', monospace;

  /* Scale */
  --h1: clamp(2.8rem, 6vw, 5.5rem);
  --h2: clamp(2rem, 4vw, 3.5rem);
  --h3: 1.5rem;
  --body: 1.0625rem;
  --small: 0.875rem;

  /* Spacing */
  --section: clamp(4rem, 8vw, 7rem);
  --container: 1200px;
}
```

## Page-type recipes

### Home page
Hero · Regulation banner · Three persona tiles (MSP largest) · Single-noun product taxonomy · How it works (3 steps) · Build-vs-buy table · Market proof stat row · Pull quote · Final CTA · Footer.

### Persona page (MSP / POS / Merchant)
Hero specific to persona · The cost / pain math · The deal in one paragraph · Live calculator · What we handle vs you handle · Code block / technical proof · The terms in plain language · FAQ · Final CTA.

### Pricing page
Hero with single sentence · Two-axis table (volume × tier) · What's included in every tier · Calculator · Comparison to build-it-yourself · Final CTA.

### About / Company
Founder story (one paragraph, first person) · The bet (why now) · Investors / partners logo strip · Team grid · Open roles · Press / press kit.

## Anti-patterns — the things that signal "generic SaaS"

If a draft has any of these, send it back:
- "Trusted by industry leaders" + 6 grey logos
- A hero with a phone mockup floating on a gradient
- A 3-card "Why [Product]" section with abstract icons
- "Our mission is to…" anywhere on the home page
- Customer logos with no outcome data
- "Schedule a Demo" as the only CTA
- A pricing table with three columns labeled "Starter / Pro / Enterprise"
- Animated counters (47,283... 47,284... 47,285...)
- A blog teaser section with three articles using the same hero image template

## What to keep updating in this doc

Every time we ship a NeoPaaS page, add to this doc:
- The hero copy that won
- The section pattern that worked
- The objection from a partner call that should be addressed on-page
- A new anti-pattern we noticed in the wild

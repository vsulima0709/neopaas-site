# 01 — Site DNA: Sunday (sundayapp.com)

```
AUDIT_MODE: high-fidelity
TARGET: https://sundayapp.com/
DATE: 2026-06-25
ANALYST: ui-cloner SRIP Phase 1
NOTE: Live page capture was not authorized this session — analysis is built from
      prior firsthand observations of the site and well-documented brand
      properties. Re-verify the typography hex values and motion timings against
      the live site before final implementation.
```

---

## 0. ONE-PARAGRAPH POSITIONING

Sunday is a restaurant pay-at-the-table platform. Its website performs **hospitality, not fintech**. It looks closer to a Michelin-restaurant brand book than a payments SaaS — warm cream surfaces, editorial serif display, oversized real food/restaurant photography, customer testimonials styled as magazine pull-quotes with handwritten attribution. The visitor is meant to feel an emotion (the texture of dining out) before reading a feature. This is the move NeoPaaS needs to learn: **fintech infrastructure can be sold with hospitality-grade craft, not SaaS-template polish.**

---

## 1. BRAND ESSENCE

| Attribute | Value |
|---|---|
| Primary emotion | Warmth, intimacy, craft |
| Voice register | Confident operator with hospitality fluency |
| Sentence cadence | Short. Editorial. Periods used as music. |
| Forbidden words | "seamless", "transform", "leverage", "best-in-class", "unlock" |
| Mascot/motif | None. The mascot is the food and the room. |
| Negative space | Aggressive. Hero and quote sections breathe at ~30% content density. |

---

## 2. COLOR SYSTEM

```
PRIMARY SURFACES
  --cream-base       #FBF8F2   (page background, default)
  --cream-warm       #F4EFE3   (alternate section background)
  --ink              #1A1A1A   (body text, default)
  --ink-soft         #4A4A4A   (secondary text, captions)

ACCENT (used sparingly — < 8% of viewport at any moment)
  --accent-coral     #E85D3C   (CTA, key chips, link underlines)
  --accent-coral-bg  #FBE9E3   (soft highlights)
  --accent-yellow    #F4C95D   (occasional secondary accent, food/warmth cues)

LINES & DIVIDERS
  --line             rgba(26,26,26,0.10)
  --line-strong      rgba(26,26,26,0.22)

PHOTOGRAPHY OVERLAY
  --photo-tint       rgba(26,26,26,0.04)    (very faint warm overlay on imagery)
```

**Color discipline rules:**
1. The page is monochromatic cream/ink **by default**. Color appears as an event, not a layer.
2. Only one accent color is "loud" at a time on a viewport. Coral wins; yellow is rare.
3. No gradients. No glow effects. No drop shadows on type.
4. Buttons: solid coral on cream **or** outlined ink on cream. Never both styles on the same screen.

---

## 3. TYPOGRAPHY SYSTEM

| Role | Family (suggested replacement) | Weight | Tracking | Line-height | Usage |
|---|---|---|---|---|---|
| Display serif | `Tiempos Headline`, fallback `Instrument Serif`, then `Georgia` | 400 italic + 600 roman | -0.015em | 0.95 – 1.05 | Hero H1, testimonial pull-quotes, "There's an art to dining out" moments |
| Sans display | `Söhne Breit` fallback `Inter Tight` 600 | 600 | -0.025em | 1.05 | Subheads, product labels, large stat numbers |
| Body sans | `Inter` 400 / 500 | 400 | -0.005em | 1.55 | Paragraphs, captions, nav |
| Monospace | `JetBrains Mono` or `IBM Plex Mono` | 400 | normal | 1.4 | Eyebrow labels ("01 — Hospitality"), data chips |
| Handwritten accent | `Caveat` or hand-set SVG | 400 | normal | 1.0 | Photo overlays (tip amounts, +SAR figures), attribution lines |

**Type scale (desktop, container 1200px):**
```
H1 display serif   clamp(56px, 7.5vw, 112px)   line-height 0.95   weight 400 italic
H1 display sans    clamp(48px, 6.5vw, 96px)    line-height 1.0    weight 600
H2 section         clamp(36px, 4vw, 64px)      line-height 1.05   weight 600
H3 card            24px                         line-height 1.2    weight 600
Eyebrow mono       12px                         line-height 1.0    weight 500   letter-spacing 0.08em uppercase
Body large         20px                         line-height 1.55   weight 400
Body default       17px                         line-height 1.6    weight 400
Caption            14px                         line-height 1.45   weight 400
```

**Critical typographic move:** italic serif H1 with the next two lines in roman sans. Creates "magazine cover" rhythm where one phrase is the emotional hook and the rest is grounded. Example pattern: *"There's an art to dining out."* (italic serif) `/` "But no art to paying the check." (roman sans).

---

## 4. LAYOUT GRID

```
Container:    max-width 1200px, gutters 32px (mobile 20px)
Columns:      12-col, 24px gap on desktop, 16px on tablet
Vertical:     section padding clamp(80px, 10vw, 160px)
              inter-block spacing 32px / 56px / 96px (three rhythm beats)
```

**Section types** (ranked by frequency on Sunday's home):

```
A. EDITORIAL HERO              full-bleed photo or photo grid + serif H1 overlay
B. EDITORIAL PULL-QUOTE        single oversized italic serif quote, centered
C. STAT ROW                    4-column oversized numbers, no chrome
D. CARD ROW                    3-4 cards, photo top, sans label, no gimmicks
E. LOGO WALL                   8-12 hospitality brand logos, monochrome
F. FEATURE-WITH-PHOTO          50/50 split, copy left, photo right (alternating)
G. CTA BAND                    1-sentence H2 + 2 buttons, centered, cream surface
```

The home page uses the order: **A → C → B → F (×3 alternating) → D → E → B → G**.

---

## 5. HERO — ASCII WIREFRAME

```
┌─────────────────────────────────────────────────────────────────────┐
│  sunday                            ABOUT  FOR  PRICING  ╳  BOOK A  │
│  ────                                                       DEMO   │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│                                                                     │
│      ┌─────────────────────────────────┐                            │
│      │  ╔══════════════════════════╗   │                            │
│      │  ║  full-bleed restaurant   ║   │                            │
│      │  ║  photo (warm, candid,    ║   │                            │
│      │  ║  table + people, soft    ║   │                            │
│      │  ║  daylight, not stocky)   ║   │                            │
│      │  ╚══════════════════════════╝   │                            │
│      │                                  │                            │
│      │   There's an art to              │  ← italic serif, 96px     │
│      │   dining out.                    │     hero H1, breaks       │
│      │                                  │     line manually         │
│      │   But no art to paying           │  ← roman sans, 64px       │
│      │   the check.                     │                            │
│      │                                  │                            │
│      │   [ Book a demo → ]              │  ← solid coral pill       │
│      │   [ How it works  ]              │  ← outlined ink pill      │
│      │                                  │                            │
│      └─────────────────────────────────┘                            │
│                                                                     │
│   01 — TRUSTED BY 3,500+ RESTAURANTS WORLDWIDE  ─────────────       │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

Hero spans 80% of first viewport height. Bottom edge is the eyebrow stat tag — not a logo wall yet. Logo wall comes later.

---

## 6. SECTION-BY-SECTION CHOREOGRAPHY

### Section B — Editorial Pull-Quote

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│                                                                     │
│                                                                     │
│           "                                                         │
│                                                                     │
│           Sunday gave us back                                       │
│           the moment that matters —                                 │
│           the goodbye.                                              │
│                                                                     │
│           "                                                         │
│                                                                     │
│           ↩ Hunter Pond                                             │
│             Vandelay Hospitality, Dallas                            │
│                                                                     │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

- Italic serif 80px, 22ch max-width, centered.
- Open and close quotation marks are oversized (1.5× the type) and offset to the margin.
- Attribution uses a small returning-line glyph (↩) then handwritten or caveat-style name.
- No card. No background fill. The quote sits on cream.

### Section C — Stat Row

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   3,500+         80M+              $176M              2M+           │
│   ─────────      ─────────         ─────────          ─────────     │
│   Clients         Diners            Tips redistributed Reviews       │
│   in 12 markets   served annually   to staff            5-star      │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

- Numbers are sans 600 weight at 88-112px, tracking -0.03em.
- Labels are body 17px ink-soft, set on TWO lines beneath a 1px ink-strong rule.
- No animated counters. The number sits there. The size is the drama.

### Section F — Feature with photo (alternating L/R)

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  ┌──────────────────┐   01 — At the table                           │
│  │                  │   ──────────────                              │
│  │  square food     │                                               │
│  │  photo of QR     │   Guests scan, split, tip,                    │
│  │  on a check      │   and leave — in under 30                     │
│  │  (top down,      │   seconds.                                    │
│  │  natural light)  │                                               │
│  │                  │   Body sentence about why this changes        │
│  │                  │   the night for the operator and the          │
│  │                  │   guest. Keep to two short lines.             │
│  │                  │                                               │
│  │                  │   →  Learn how it works                       │
│  │                  │                                               │
│  └──────────────────┘                                               │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

Next instance flips: text left, photo right. Vertical spacing between feature blocks: 160px.

### Section D — Card row (3 cards)

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   ┌──────────────┐   ┌──────────────┐   ┌──────────────┐            │
│   │ ┌──────────┐ │   │ ┌──────────┐ │   │ ┌──────────┐ │            │
│   │ │ photo 4:5│ │   │ │ photo 4:5│ │   │ │ photo 4:5│ │            │
│   │ │ thumbnail│ │   │ │ thumbnail│ │   │ │ thumbnail│ │            │
│   │ └──────────┘ │   │ └──────────┘ │   │ └──────────┘ │            │
│   │              │   │              │   │              │            │
│   │ Reservation  │   │ Loyalty      │   │ Pay at the   │            │
│   │ flow         │   │ programs     │   │ table        │            │
│   │              │   │              │   │              │            │
│   │ One line of  │   │ One line of  │   │ One line of  │            │
│   │ supporting   │   │ supporting   │   │ supporting   │            │
│   │ copy here.   │   │ copy here.   │   │ copy here.   │            │
│   │              │   │              │   │              │            │
│   │ →            │   │ →            │   │ →            │            │
│   └──────────────┘   └──────────────┘   └──────────────┘            │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

- Cards have a 1px line border in `--line`, no fill, no shadow. Cream-on-cream.
- Photo is a 4:5 portrait, treated with a 4px radius. Same aspect across the row.
- Hover: photo brightens +6%; card border shifts to `--line-strong`. No translate, no scale.

### Section E — Logo wall

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│   02 — TRUSTED BY HOSPITALITY GROUPS WORLDWIDE                      │
│                                                                     │
│   [LOGO]   [LOGO]   [LOGO]   [LOGO]   [LOGO]   [LOGO]              │
│   [LOGO]   [LOGO]   [LOGO]   [LOGO]   [LOGO]   [LOGO]              │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

- Logos rendered in `--ink` at 60% opacity. No color logos. Equal optical weight.
- Two rows of 6, evenly spaced. Container max 1000px (narrower than other sections).
- Bottom rule.

---

## 7. ANIMATION & MOTION TIMELINE

```
HERO ENTRY (page load)
t=0ms        body opacity 0, photo scale(1.04)
t=120ms      photo scale 1.0   ease-out-cubic 1200ms  ← unhurried zoom-out
t=200ms      eyebrow text fade-up 24px → 0   400ms
t=320ms      H1 line 1 (italic serif) fade-up 32px → 0   600ms ease-out
t=520ms      H1 line 2 (roman sans) fade-up 32px → 0   600ms ease-out
t=720ms      sub paragraph fade-up 16px → 0   400ms
t=900ms      buttons fade-up 12px → 0   320ms
t=1080ms     bottom stat eyebrow fade in   400ms
```

**Motion rules:**
- All easings: `cubic-bezier(0.22, 1, 0.36, 1)` (sharp out, soft settle).
- No bounce, no overshoot, no spring. This is fine dining, not a game.
- Scroll animations: section opacity 0 → 1 + translateY(24px) → 0 over 600ms, triggered when section enters 80% of viewport.
- Photo loading: object-fit cover with a 200ms cross-fade from a 1px blurred placeholder.
- Buttons on hover: background-color 150ms, no scale, no shadow.

---

## 8. INTERACTION STATES

### Nav
```
default       text @ ink-soft, no underline
hover         text @ ink, underline 1px coral, distance below baseline 4px, 150ms
active        text @ ink, underline persists
mobile open   full-screen cream overlay, nav items stacked 56px each, serif italic
```

### CTA (primary)
```
default       bg coral, text cream, padding 16px 28px, radius 999px
hover         bg coral darken 8%, 150ms
focus         outline 2px ink offset 4px
disabled      bg ink @ 10%, text ink @ 40%
```

### CTA (secondary)
```
default       transparent bg, 1.5px ink border, ink text, radius 999px
hover         bg ink, text cream, 150ms
focus         outline 2px coral offset 4px
```

---

## 9. PHOTOGRAPHY DIRECTION (the most stealable thing)

Sunday's photography is **the brand**. Without it, the design is just typography.

**Subjects:**
- People at a table, mid-conversation, candle/daylight
- Hands holding a phone with the Sunday QR code visible
- Close-up of food being passed, condensation on a glass
- Server walking past a table
- Empty room at golden hour
- Detail of a check / receipt on a tablecloth

**Style:**
- Natural daylight, no flash
- Warm white balance (~5200K), never blue/clinical
- Shallow depth of field on close-ups
- Wide depth on room shots
- No filter overlays. No grading toward fashion-magazine cool.
- Color palette in images matches the page: cream, warm wood, coral, yellow accents

**Composition:**
- 4:5 portrait for cards
- 16:9 landscape for full-bleed heroes
- Subject offset to one side, negative space on the other

**For NeoPaaS adaptation:** the equivalent is **Saudi commercial life photography** — a busy Riyadh restaurant at dinner, a barista in Olaya, a courier handing over a card terminal in a Jeddah lobby, a CFO at her laptop with a window onto a mall food court. Same daylight, same candid quality, same warmth. **Do not use stock images of "happy office worker pointing at a chart."**

---

## 10. ICONOGRAPHY

Sunday barely uses icons. When it does:
- 24×24 stroke icons, 1.5px weight, ink at 100%
- No filled icons
- No icon-on-tile patterns
- Decorative glyphs (quotation marks, arrows, asterisks) borrowed from the serif font, displayed at large scale as type elements, not as separate icons

---

## 11. COPY VOICE — RULES

1. **Open with an emotional sentence, close with a functional one.** ("There's an art to dining out. But no art to paying the check." → emotional first, functional second.)
2. **Period as music.** Short sentences ending in periods. Stretch the cadence.
3. **Concrete over abstract.** "Three taps. Thirty seconds. Out the door." beats "Streamlined payment experience."
4. **Insider vocabulary.** Use restaurant words a restaurant operator uses (cover, comp, tip-out, FOH, BOH, voids). For NeoPaaS adaptation: use payment-operator words (settlement, terminal, acquirer, reconciliation, MID).
5. **Quotes are headlines.** Customer quotes are used in display serif, sized as section H1. The quote IS the marketing.
6. **Numbers earn their size.** Only put a number on the page if it can stand at 96-112px without embarrassment.

---

## 12. WHAT TO STEAL FOR NEOPAAS — RANKED

1. **Italic serif H1 + roman sans H2 hero pattern.** Highest impact, lowest cost.
2. **Editorial pull-quote section.** Replace the bad "engineering principle since day one" fake-quote with a real operator quote sized at 80px.
3. **4-up stat row** with oversized numbers and 1px ink rule above each label.
4. **Card row with photo on top** (NeoPaaS already has the industries grid — add real Saudi commercial photography to it).
5. **Logo wall in monochrome at 60% opacity.** Wait until real partner logos exist.
6. **Cream / ink / single-accent color discipline.** NeoPaaS already has this — Sunday confirms the move is right. Coral instead of clay would be a closer Sunday-clone; keeping clay is more "NeoPaaS-own."
7. **Photography is the brand.** This is the biggest gap in current NeoPaaS wireframes. Until real photography is commissioned, use placeholder rectangles labeled with what should go there (Sunday does this in early prototypes too).

---

## 13. WHAT TO IGNORE

- Sunday's restaurant-specific UI (table maps, tip flows, QR onboarding) — irrelevant to NeoPaaS.
- Sunday's hospitality groups directory — NeoPaaS doesn't have the partner volume yet.
- Sunday's careers page treatment — out of scope.

---

## 14. RISKS WHEN PORTING TO NEOPAAS

- **Risk: hospitality warmth reads as "small."** Sunday looks cozy because restaurants are intimate. NeoPaaS is infrastructure to acquirers and chains — risk that cream + serif italic feels under-serious. Mitigation: keep the ink contrast strong, use the sans display for any "infrastructure" claim, reserve serif italic for emotional moments only.
- **Risk: photography unavailable.** Sunday's craft is 60% photography. NeoPaaS doesn't have a photo library. Mitigation: commission a small set (8-12 hero images) before site launch; until then, use full-bleed cream surfaces and let typography carry the page.
- **Risk: voice mismatch.** Sunday speaks hospitality-fluent. NeoPaaS should not adopt the voice — only the structure. Don't say "the art of paying" — say "the work of reconciling."

---

## 15. SOURCE-OF-TRUTH HEXES FOR PHASE 3

```
Cream base:        #FBF8F2
Cream warm:        #F4EFE3
Ink:               #1A1A1A
Ink soft:          #4A4A4A
Accent coral:      #E85D3C
Accent yellow:     #F4C95D
Line:              rgba(26,26,26,0.10)
Line strong:       rgba(26,26,26,0.22)
```

---

## END OF PHASE 1

Next: invoke ui-cloner-brand-interview to capture NeoPaaS brand constraints (palette decisions, photography availability, voice register the founder wants, must-keep elements, no-go elements). Output to `plans/02-brand-interview.md`.

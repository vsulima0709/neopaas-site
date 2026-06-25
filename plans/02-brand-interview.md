# 02 — Brand Interview: NeoPaaS

```
INTERVIEWEE: Igor (founder/operator)
DATE: 2026-06-25
TARGET CLONE: Sunday (sundayapp.com)
INSTRUCTION SUMMARY: Keep v4 content. Apply Sunday's visual UX/UI on top.
```

---

## 1. PALETTE — LOCKED

| Token | Value | Source |
|---|---|---|
| `--bg` | `#f5f1e8` | Existing NeoPaaS cream — keep |
| `--bg-soft` | `#ede7d6` | Existing alt cream — keep |
| `--ink` | `#1a1614` | Existing warm near-black — keep |
| `--ink-soft` | `#5a544e` | Existing warm gray — keep |
| `--green` | `#0c3b2e` | Existing deep forest green — keep |
| `--clay` | `#c2410c` | Existing warm clay accent — keep |

**Color discipline (adopted from Sunday):** color appears as an event, not a layer. Cream + ink dominate. Forest green for surfaces of conviction (compliance section, partner cards). Clay only for CTAs, accents, and small markers. **No fintech blue, no gradients, no shadows on type.**

## 2. PHOTOGRAPHY — STOCK SAUDI CONTEXT

Will use stock imagery of Saudi commercial life:
- Restaurant interiors (Riyadh, Jeddah)
- Retail counters with card terminals
- Hotel front desks
- Couriers with portable terminals
- Operations staff at laptops

**Style guardrails (from Sunday DNA):**
- Natural daylight, never blue/clinical
- Warm white balance ~5200K
- Candid composition with negative space
- No "happy office worker pointing at chart"
- No filter overlays

Wireframe will use placeholder rectangles labeled with the photo brief for each slot, so the user can swap in real stock later.

## 3. VOICE — ONE SERIF MOMENT PER PAGE

- Hero H1 uses italic serif on the emotional word ("every card payment")
- All other H2/H3 stay in sans
- No editorial pull-quotes in italic serif (cuts the "moody fintech" risk)
- No fake founder-wisdom quotes (already deleted in v4)

## 4. CONTENT — LOCKED FROM v4

**No copy rewrites this round.** Every text block in the current `index.html` (v4) stays exactly as-is. The change is purely visual/structural:
- Same hero headline and subhead
- Same on-ramp pain cards (a / b / c)
- Same before/after diagram
- Same three outcome blocks
- Same dashboard mockup
- Same four industry cards
- Same how-it-works steps
- Same compliance section
- Same today-vs-NeoPaaS table
- Same partner strip
- Same final CTA
- Same footer

## 5. STRUCTURAL CHANGES TO APPLY (from Sunday)

| v4 section | Sunday-influenced upgrade |
|---|---|
| Top nav | Lighter weight, more letter-spacing, mono eyebrow above logo (optional) |
| Hero | Italic serif on one phrase; add a full-bleed photo slot to right of copy on desktop; bottom eyebrow stat row |
| On-ramp pain cards | Stay 3-up; gain photo slots above copy (4:5 ratio); 1px border, no shadow |
| Before/after diagram | Keep, but reduce visual weight (Sunday wouldn't lead with a diagram) |
| 3 outcomes | Numbered editorial style — eyebrow `01 —`, oversized sans heading, single line of copy |
| Dashboard mockup | Surround with cream framing instead of dark — feels more "magazine spread" than "fintech demo" |
| Industries (4 cards) | Add 4:5 photo slot at top of each card; sans label below; remove ornamental letter glyph (Sunday doesn't decorate cards) |
| How it works | Three numbered blocks with 1px top rule, oversized sans headings |
| Compliance (orange) | Keep but soften — cream surface with forest-green accent type instead of solid clay surface |
| Today vs NeoPaaS table | Keep but redesign as two stacked editorial blocks instead of grid table (Sunday avoids tables) |
| Partner strip | Keep position and content; reframe as 3-up editorial cards on cream |
| Final CTA | Center-aligned, oversized sans, generous vertical space |

## 6. TYPOGRAPHY UPGRADE

Add to the existing Inter + Instrument Serif + JetBrains Mono stack:
- Italic serif used ONLY in hero (one phrase)
- Section H2s remain sans 600 with tighter tracking (-0.03em)
- Add a section eyebrow pattern: mono uppercase 12px, prefixed with `01 —` numerical marker
- Larger type scale across the board (Sunday is bolder than v4)

## 7. NO-GO LIST

- No italic serif beyond the single hero phrase
- No coral (Sunday's color) — keep NeoPaaS clay
- No shadows on type or buttons
- No abstract illustrations or 3D renders
- No animated counters
- No "Trusted by industry leaders" placeholder logo bar
- No fake founder quote

## END OF PHASE 2

Next: invoke ui-cloner-synthesis → produce `plans/03-replication-prompt.md` AND the actual rebuilt `index.html` with Sunday's visual UX/UI applied to v4's locked content.

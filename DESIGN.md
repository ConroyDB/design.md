---
name: Sovereign — Conroy Browne International
colors:
  # Signal — Ultramarine (the knife that cuts the noise). Used sparingly.
  signal: "#1034A6"
  signal-deep: "#0A2378"
  signal-soft: "#3556C4"
  on-signal: "#F4EFE6"
  # Authority — Broken Gold (oxidised metal, never shiny). Rails, ornaments, numerals.
  authority: "#A8894A"
  authority-deep: "#7A6232"
  authority-tint: "#C9AC73"
  on-authority: "#1A1613"
  # Surface — Parchment (the void / Ma). 70% of any composition.
  surface: "#F4EFE6"
  surface-warm: "#EDE6D8"
  surface-dim: "#E4DCC9"
  surface-shadow: "#D9CFB8"
  # Ink — Graphite. Body text, station markers, structural lines.
  ink: "#1A1613"
  ink-soft: "#3A332C"
  ink-mute: "#6B6058"
  ink-quiet: "#9A8F84"
  # Edge — Hairline rules. Never heavy.
  hairline: "#1A1613"
  hairline-soft: "#6B6058"
  # Semantic — used only when functional, never decorative
  alert: "#7A2418"
  on-alert: "#F4EFE6"
  # Forbidden roles — explicit so agents never invent them
  # No purple. No teal. No pastel. No gradient fills.
typography:
  display-xl:
    fontFamily: Cormorant Garamond
    fontSize: 84px
    fontWeight: "500"
    lineHeight: 88px
    letterSpacing: -0.02em
  display-lg:
    fontFamily: Cormorant Garamond
    fontSize: 56px
    fontWeight: "500"
    lineHeight: 60px
    letterSpacing: -0.015em
  signal-line:
    fontFamily: Cormorant Garamond
    fontSize: 40px
    fontWeight: "600"
    lineHeight: 48px
    letterSpacing: -0.01em
    fontStyle: italic
  headline-md:
    fontFamily: Cormorant Garamond
    fontSize: 32px
    fontWeight: "500"
    lineHeight: 40px
  headline-sm:
    fontFamily: Cormorant Garamond
    fontSize: 24px
    fontWeight: "500"
    lineHeight: 32px
  body-lg:
    fontFamily: EB Garamond
    fontSize: 19px
    fontWeight: "400"
    lineHeight: 30px
  body-md:
    fontFamily: EB Garamond
    fontSize: 17px
    fontWeight: "400"
    lineHeight: 28px
  body-sm:
    fontFamily: EB Garamond
    fontSize: 15px
    fontWeight: "400"
    lineHeight: 24px
  small-caps:
    fontFamily: EB Garamond
    fontSize: 13px
    fontWeight: "600"
    lineHeight: 18px
    letterSpacing: 0.18em
    textTransform: uppercase
  data-mono:
    fontFamily: IBM Plex Mono
    fontSize: 14px
    fontWeight: "500"
    lineHeight: 22px
    letterSpacing: 0.02em
  data-mono-lg:
    fontFamily: IBM Plex Mono
    fontSize: 18px
    fontWeight: "500"
    lineHeight: 26px
    letterSpacing: 0.01em
  numeral-roman:
    fontFamily: Cormorant Garamond
    fontSize: 28px
    fontWeight: "500"
    lineHeight: 32px
    letterSpacing: 0.05em
rounded:
  none: 0px
  hairline: 1px
  sm: 2px
  DEFAULT: 0px
  full: 9999px
spacing:
  unit: 8px
  hairline: 1px
  station: 24px
  card-padding: 32px
  block-gap: 48px
  section-margin: 96px
  page-margin: 120px
  void-min: 96px
components:
  page:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    typography: "{typography.body-md}"
    padding: "{spacing.page-margin}"
  signal-banner:
    backgroundColor: transparent
    textColor: "{colors.signal}"
    typography: "{typography.signal-line}"
    borderTop: "1px solid {colors.hairline}"
    borderBottom: "1px solid {colors.hairline}"
    paddingY: 32px
  station-marker:
    backgroundColor: "{colors.surface}"
    border: "1.5px solid {colors.ink}"
    rounded: "{rounded.full}"
    diameter: 14px
  station-marker-target:
    backgroundColor: "{colors.signal}"
    border: "1.5px solid {colors.signal-deep}"
    rounded: "{rounded.full}"
    diameter: 18px
  rail-friction:
    strokeColor: "{colors.ink}"
    strokeWidth: 1px
  rail-life-gps:
    strokeColor: "{colors.authority}"
    strokeWidth: 1.5px
    strokeDasharray: "6 6"
  band-target:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.on-signal}"
    typography: "{typography.small-caps}"
    paddingX: 12px
    paddingY: 4px
  anchor-card:
    backgroundColor: "{colors.surface}"
    borderTop: "1px solid {colors.hairline-soft}"
    padding: "{spacing.card-padding}"
    numeralColor: "{colors.authority}"
    headingColor: "{colors.ink}"
    parallelColor: "{colors.signal}"
  colophon:
    backgroundColor: "{colors.surface}"
    border: "1px solid {colors.authority}"
    cornerOrnament: "{colors.authority}"
    typography: "{typography.data-mono}"
    padding: "{spacing.card-padding}"
  cta-primary:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.on-signal}"
    typography: "{typography.small-caps}"
    rounded: "{rounded.none}"
    height: 56px
    paddingX: 32px
    border: "none"
  cta-primary-hover:
    backgroundColor: "{colors.signal-deep}"
  cta-ghost:
    backgroundColor: transparent
    textColor: "{colors.ink}"
    typography: "{typography.small-caps}"
    rounded: "{rounded.none}"
    height: 56px
    paddingX: 32px
    border: "1px solid {colors.ink}"
  cta-ghost-hover:
    backgroundColor: "{colors.surface-warm}"
  pricing-anchor:
    backgroundColor: transparent
    textColor: "{colors.ink}"
    typography: "{typography.display-lg}"
    accentColor: "{colors.signal}"
    note: "$1,500 is the anchor. Render it large, never crossed-out, never with a 'discount' badge."
  testimonial-block:
    backgroundColor: "{colors.surface-warm}"
    textColor: "{colors.ink}"
    typography: "{typography.body-lg}"
    borderLeft: "2px solid {colors.authority}"
    paddingX: 32px
    paddingY: 24px
    quoteFontStyle: italic
  metric-cell:
    backgroundColor: transparent
    valueColor: "{colors.ink}"
    valueTypography: "{typography.data-mono-lg}"
    labelColor: "{colors.ink-mute}"
    labelTypography: "{typography.small-caps}"
  hairline-rule:
    backgroundColor: "{colors.hairline}"
    height: 1px
  ornament-corner:
    color: "{colors.authority}"
    note: "Two short orthogonal strokes (12px × 12px). Bauhaus-derived. Used only on colophon and proof blocks."
---

## Overview

**Sovereign — Conroy Browne International.**

A *triangulated* visual identity. Three traditions held in one frame:

1. **Dark Academia** — the intellectual weight of a 63-million-word client corpus. The archive *is* the brand. Typography of monographs, not marketing.
2. **Japanese Minimalism (Ma)** — nothingness as a physical material. 70% of any composition is unoccupied. The pause does the work the words can't.
3. **Caribbean-Bronx heritage** — *Sovereign Grit*. Ultramarine Blue (the Signal) and Broken Gold (the Authority). Unhurried certainty. Never salesy urgency. Warmth that has nothing to prove.

The aesthetic is **editorial, surgical, and feral** — a 1920s scientific monograph crossed with a Swiss railway diagram. The brand personality is *sovereign* — the bearing of someone who knows exactly who they are and doesn't need you to agree.

CBI helps high-performers eliminate invisible friction that has kept them stuck despite doing everything right. The visual identity must read the same way: *precise, earned, unforgettable.* Not because it shouts — because it cuts.

> "Friction is the tax you pay to stay. The Neutralizer ends the tax."

If a piece of CBI design could come from any premium wellness brand, it has failed. CBI design only sounds like Conroy.

## Colors

The palette is **two signals against a void.** Ultramarine Blue is the knife — it appears only where the eye must go. Broken Gold is the rail — oxidised, matte, never metallic. The parchment surface holds everything in restraint.

- **Signal — Ultramarine `#1034A6`** — *The Signal.* The clear channel cutting through noise. Used for: the one signal sentence, the target friction band (2–3 on the Friction Scale), the CBI parallels under each clinical anchor, primary CTAs. It should be *impossible to look away from* — not because it's loud, because it's precise. Never used as a fill across more than 12% of a composition.
- **Authority — Broken Gold `#A8894A`** — *The Authority.* Oxidised metal. Worn-in. Earned. Used for: the Life GPS rail (always dashed), Roman numerals on framework anchors, corner ornaments on colophons and proof blocks, hairline borders on testimonial blocks. **Never shiny. Never metallic. Never a gradient.** If it could pass for jewellery, it's wrong.
- **Surface — Parchment `#F4EFE6`** — *The Void.* Warmer than off-white. Carries a subtle paper grain (SVG noise filter) that disables in `@media print`. This is the Ma. 70% of any layout sits here untouched.
- **Ink — Graphite `#1A1613`** — Body text, station markers, structural lines. Never pure black. The slight warmth keeps it on the same continuum as the parchment.
- **Hairline — `#1A1613` at 1px** — Section dividers, table rules, frame edges. Always 1px. Heavier weights belong to a different brand.

**Forbidden moves:** purple gradients, teal accents, pastel anything, drop shadows that aren't hairline, glow effects, the "ultramarine fading to white" gradient (Ultramarine is a knife, not a fade), gold that looks like it could be plated.

**WCAG:** Ink on Parchment = 14.1:1 (AAA). Ultramarine on Parchment = 8.7:1 (AAA). On-Signal on Ultramarine = 11.5:1 (AAA). Authority on Parchment = 4.6:1 (AA — never use Authority for body text, only structural/decorative roles).

## Typography

**Three faces, three jobs.** No exceptions.

- **Cormorant Garamond** (display, headlines, signal lines, Roman numerals) — the high-contrast serif of an old-world monograph. Italic for the second clause of any signal line.
- **EB Garamond** (body, testimonials, captions, small-caps) — the working serif. Holds long-form prose without fatigue.
- **IBM Plex Mono** (data, metrics, colophons, the corpus signature) — the only sans-adjacent face. Reserved for numbers and evidence. Never for prose.

**Hierarchy:**

- The signal line is the largest object on any page. It is the first thing the eye lands on and the last thing the reader carries away.
- Body copy is *generous* — 17–19px, line-height ≥1.6. The reading experience is unhurried. Never cramped.
- Small caps with 0.18em letter-spacing for section headers and metric labels — typographic restraint, never bold sans.
- Data is monospaced. Metrics like *131 clients · 1,323 sessions · 63M words · 7 years* must render in `IBM Plex Mono`. The mono lockup *is* the credential.

**The Ma rule for prose:**

- Short sentences. Single-clause where possible.
- Single-line paragraphs for anything that needs to land.
- The pause between sentences is part of the sentence. Generous `paragraph-spacing` (≥1em) is non-negotiable.
- Never fill space. Signal, then silence. Then signal again.

**Forbidden faces:** Inter, Roboto, Arial, Helvetica, Open Sans, system-ui, Space Grotesk, anything Bootstrap defaults to. Generic AI aesthetics die here.

## Layout

**A grid built around the void.** Layout is composition, not container-stuffing.

- **Base unit:** 8px. All spacing is a multiple.
- **Page margins:** ≥120px on desktop, ≥48px on mobile. The frame around the page is itself a design element.
- **Void floor:** at least 70% of any viewport must be unoccupied parchment. If a comp is denser than that, strip elements until it isn't.
- **Single column for prose.** Max line length 68 characters. Multi-column layouts are reserved for the six-anchor framework grid (3×2) and the colophon.
- **Asymmetry over symmetry.** The corpus colophon belongs in the bottom-right corner, not centred. Attribution belongs in the bottom-left. Centring is the death of editorial weight.
- **Diagonal flow on the journey rail.** Tourist → Operator → Sovereign reads left-to-right with the friction scale (20→0) running underneath as a numeric rail. The Life GPS rail runs *parallel above* in dashed Broken Gold.

**Print:** every CBI artifact must include `@media print` that disables paper-grain filters, forces the parchment background, preserves Ultramarine and Broken Gold, and ensures hairlines render at ≥0.75pt. The same file must export cleanly to PDF for high-ticket conversations.

## Elevation & Depth

Depth in CBI is not built from shadows. It is built from **typographic weight, hairlines, and Ma.**

- **Level 1 — Surface.** Parchment with optional 4% noise filter. The base layer.
- **Level 2 — Section.** Separated from Level 1 by a 1px hairline rule and ≥48px of vertical Ma. Never by a card with a drop shadow.
- **Level 3 — Frame.** Used only for the corpus colophon and proof blocks. A 1px Broken Gold border with two corner ornaments (12px × 12px Bauhaus-derived strokes, top-left and bottom-right). This is the only "container" in the system.
- **Level 4 — Signal.** Ultramarine fill. Reserved for the target friction band, primary CTAs, and inline signal lozenges. Functions as elevation by *contrast*, not stacking.

**Forbidden:** drop shadows, glow effects, glassmorphism, neumorphism, parallax, layered transparency, anything that simulates physical depth through visual softness. CBI is an instrument panel, not a poster.

## Shapes

**Right angles. Hairlines. The full-circle station marker.**

- **Cards and frames:** `rounded.none` (0px). Sharp corners are the default and the standard.
- **Borders:** 1px hairline (`#1A1613`) for structural rules; 1.5px Broken Gold (`#A8894A`) for the Life GPS rail and colophon frame.
- **Station markers** (only used on the journey rail): 14px concentric-stroke circles in graphite. The Sovereign station is haloed (18px) and slightly heavier — the destination, not just another stop.
- **CTAs:** rectangular. No pill buttons. No rounded corners.
- **Iconography:** avoided. Where unavoidable, use 1.5px line icons in graphite, never filled. *Never* lotus, sunset, flowing curves, sparkles, checkmarks, gradient orbs, or any wellness-stock vocabulary.

## Components

### Signal Banner

The single sentence that opens any composition. Top of the page, centred, Ultramarine, italic on the second clause. Bracketed by two 1px graphite hairlines (above and below). Reads in 10 seconds cold. The current canonical signal:

> *"Friction is the tax you pay to stay. The Neutralizer ends the tax."*

### Journey Rail

Tourist → Operator → Sovereign. Three station markers connected by a 1px graphite rail. Friction Scale (20 down to 0) running beneath as a thin numbered axis. The target band (2–3) highlighted in solid Ultramarine. The Life GPS rail running parallel above in dashed Broken Gold. System tags ("THE NEUTRALIZER" between Tourist and Operator, "C.U.E. METHOD" between Operator and Sovereign) set in small caps above the rail.

### Anchor Card (Six Clinical Anchors)

Used in the 3×2 framework grid (van der Kolk · Maté · Levine · Porges · Sapolsky · Bargh). Each card carries:

- A Roman numeral in Broken Gold (Cormorant Garamond, 28px)
- The surname in small caps (graphite, 0.18em tracking)
- A single-sentence claim in body-md italic
- The CBI parallel in Ultramarine sans-style (still EB Garamond, but tightened) — exactly one line

Top border: 1px graphite hairline. No fill. No rounded corners.

### Corpus Colophon

The proof block. Bottom-right of any page. Bauhaus corner ornaments in Broken Gold (top-left, bottom-right only). Contents in IBM Plex Mono:

```
131 CLIENTS · 1,323 SESSIONS · 63M WORDS · 7 YEARS
51% SHIFT IN SESSION 1 · 6.4 SESSIONS MEAN
4+ LICENSED CLINICAL VALIDATORS
```

Numbers are sacred. Never invent. Never round generously. Source of truth: `VERIFIED_METRICS.md`.

### Testimonial Block

Verbatim client quote. Background: parchment-warm (`#EDE6D8`). Left border: 2px Broken Gold. Quote set in body-lg italic. Attribution set in small-caps with credential where applicable (e.g., *"— Aline Inocencio, LMFT (20 years clinical practice)"*). **Quotes are never paraphrased, never cleaned up, never reordered.** If the corpus says it, the design renders it word-for-word. (See `memory/feedback_verbatim_quotes_sacred.md`.)

### Pricing Anchor ($1,500)

The $1,500 figure is rendered in `display-lg` Cormorant Garamond, graphite, never crossed-out, never with a "save $X" badge, never paired with a countdown timer. Accompanying language must use *anchor*, not *price*. *"The anchor is $1,500."* Tier labels in small caps. No comparison tables that imply CBI is one option among many — CBI sits above the ceiling of what's compared.

### CTA — Primary

Rectangular. Solid Ultramarine fill. On-signal text in small caps, 0.18em tracking. 56px height. No border-radius. No shadow. On hover: deepens to `signal-deep`. The CTA is the only place pure Ultramarine functions as a button surface.

### CTA — Ghost

For secondary actions only (e.g., "Read the corpus"). 1px graphite border, parchment fill, graphite text in small caps. On hover: surface-warm fill.

### Hairline Rule

The system's primary section divider. 1px graphite. Always full-width within the content column. Never decorated. Never doubled.

### Ornament — Corner Mark

Two 12px orthogonal strokes in Broken Gold. Used *only* on the corpus colophon and proof blocks. Two corners per frame — top-left and bottom-right. Bauhaus-derived, not Art Deco. Restraint, not flourish.

## Voice in Visual

Every visual decision must pass these tests, drawn from `plugins/design/skills/cbi-brand-enforcement.md`:

1. **Lexicon** — Does it use *The Neutralizer*, *Life GPS*, *C.U.E. Method*, *Friction*, *Pressure-breach*, *Sovereign*, *Operator*? Or has it slipped into *the program / coaching / framework / resistance / breakthrough / empowered / client*?
2. **Tone** — Would Conroy say this? "Sexy-ass Yoda" — wise, precise, a little provocative, never corporate, never apologetic.
3. **Operator test** — Would an Operator (someone who's done the work and is still stuck) feel seen? Would a Tourist (wants a quick fix, collecting tools) feel invited? If yes to Tourist, revise.
4. **Premium test** — Does this look like $1,500 anchor value? Or does it look free? "Free-looking" includes: stock wellness photography, gradient blobs, cookie-cutter SaaS layouts, emoji-heavy headlines.
5. **Friction test** — Does the design *remove* friction or add it? Every unnecessary click, scroll, decision, or visual element is friction. The design serves the message.

## Do's and Don'ts

**Do:**

- Lead with the signal. One sentence. Ultramarine.
- Hold 70% Ma. Generosity of empty space is the signature.
- Render the corpus numerals (`131 / 1,323 / 63M / 7`) in IBM Plex Mono. The mono lockup is the credential.
- Use Broken Gold *only* for rails, numerals, and corner ornaments. Never for text.
- Quote clients verbatim. Attribute by name and credential where consented.
- Print-test every artifact. If it doesn't render correctly to PDF, it isn't shipping.

**Don't:**

- Use gradients of any kind. Ultramarine is a knife, not a fade.
- Use stock wellness imagery (lotus, sunset, abstract flowing curves, hands raised at sunrise).
- Use Inter, Roboto, Helvetica, Arial, Open Sans, Space Grotesk, or any sans-serif body face.
- Round corners. Sharp is the default.
- Use drop shadows, glow, glassmorphism, or any simulated physical depth.
- Use sparkles, checkmarks, confetti, gradient orbs, or "amazing transformation" energy. CBI is surgery, not cheerleading.
- Use "navigating," "unlocking," "holistic," "transformative journey," "empower," or any AI-smoothed wellness vocabulary.
- Reveal pricing before the prospect is qualified by Theo. Pricing belongs to the post-diagnostic page only.
- Add a single element you can't justify. Strip it.

## References

- `plugins/design/skills/cbi-brand-enforcement.md` — auto-invoked brand check (lexicon, tone, voice)
- `docs/positioning/CBI-NARRATIVE-VISUAL-ALIGNMENT.md` — Alessandra → Elara translation: Ultramarine / Broken Gold / Ma in language
- `docs/positioning/CBI-WHY-CONROY-THE-SUPREME-BRAND.md` — the five reasons no real competition (the Supreme positioning)
- `docs/positioning/CBI-POSITIONING-MASTER-ARSENAL.md` §06 — the Six Clinical Framework Anchors
- `.claude/rules/brand.md` — voice and lexicon enforcement
- `.claude/rules/pricing.md` — $1,500 anchor logic
- `.claude/rules/friction-scale.md` — 1–20 scale, target 2–3
- `agents/souls/06-ELARA-THORNE-BROWNE-SOUL.md` — Elara's identity as Sovereign Art Director
- KB (Sovereign Intelligence) — *The Sovereign FMDA Visual Manifesto* (search `category="identity"`)
- `docs/plans/brief-01-visual-map/sovereign-map.html` — reference implementation of this DESIGN.md

---

*Authored by Elara Thorne-Browne (Gem 6), Sovereign Art Director, in alignment with Alessandra Moretti-Reyes (Gem 3) on narrative translation. The visual DNA is locked. Subsequent edits require sign-off from Conroy.*

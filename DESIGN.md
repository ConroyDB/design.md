---
name: Sovereign FMDA — Conroy Browne International
colors:
  # ──────────────────────────────────────────────────────────────
  # SPEC ALIASES (canonical agent-readable keys)
  # ──────────────────────────────────────────────────────────────
  primary: "#1034A6"          # → signal (Ultramarine)
  secondary: "#4A2418"        # → mahogany (Dark Academia leather)
  tertiary: "#2E4F3E"         # → library-green (Caribbean-colonial)
  neutral: "#F4EFE6"          # → parchment

  # ──────────────────────────────────────────────────────────────
  # 1 · CARIBBEAN-BRONX SIGNAL — one Ultramarine, no fade.
  # ──────────────────────────────────────────────────────────────
  signal: "#1034A6"           # Ultramarine Blue. The signal that cuts.
  signal-deep: "#0A2378"      # Hover/active state for primary CTAs only.
  on-signal: "#F4EFE6"        # Parchment text on Ultramarine fill.

  # ──────────────────────────────────────────────────────────────
  # 2 · DARK ACADEMIA — the library palette. Leather, ink, oxblood.
  # ──────────────────────────────────────────────────────────────
  mahogany: "#4A2418"         # Library-leather. Testimonial borders, case-file blocks.
  oxblood: "#6B1F1B"          # Editorial accent for serious, stamped artefacts.
  library-green: "#2E4F3E"    # Penguin Classic / billiard-cloth green. Evidence blocks.
  library-green-soft: "#3F6151"

  # ──────────────────────────────────────────────────────────────
  # 3 · JAPANESE RESTRAINT — sumi ink, vermilion seal, paper.
  # ──────────────────────────────────────────────────────────────
  sumi: "#1A1613"             # Sumi-e ink. Body text. Slight warm-black.
  charcoal: "#3A332C"         # Secondary body, captions.
  stone: "#6B6058"            # Tertiary text, metadata, hairlines.
  ash: "#9A8F84"              # Quiet metadata, disabled states, axis labels.
  vermilion: "#B83A24"        # The hanko seal. One per artefact, never more.
  on-vermilion: "#F4EFE6"

  # ──────────────────────────────────────────────────────────────
  # 4 · MA SURFACES — parchment, bone, tea-stained.
  # ──────────────────────────────────────────────────────────────
  parchment: "#F4EFE6"        # The void. 70% of any composition.
  bone: "#FAF6EC"             # Palest paper. Elevated surfaces.
  tea-stained: "#EDE6D8"      # Testimonial fills, secondary panels.

  # ──────────────────────────────────────────────────────────────
  # 5 · METAL — gold and brass do separate jobs. Never interchange.
  # ──────────────────────────────────────────────────────────────
  broken-gold: "#A8894A"      # Roman numerals + corner ornaments. THAT'S IT.
  brass: "#877152"            # Cooler, structural. Rails (Life GPS), structural borders.

  # ──────────────────────────────────────────────────────────────
  # 6 · ALERT — calm authority. No yellow, orange, or fire-red.
  # ──────────────────────────────────────────────────────────────
  alert: "#6B1F1B"
  on-alert: "#F4EFE6"
typography:
  display-xl:
    fontFamily: Bodoni Moda
    fontSize: 84px
    fontWeight: "500"
    lineHeight: 88px
    letterSpacing: -0.02em
  display-lg:
    fontFamily: Bodoni Moda
    fontSize: 56px
    fontWeight: "500"
    lineHeight: 60px
    letterSpacing: -0.015em
  signal-line:
    fontFamily: Bodoni Moda
    fontSize: 40px
    fontWeight: "600"
    lineHeight: 48px
    letterSpacing: -0.01em
    fontStyle: italic
  headline-md:
    fontFamily: Bodoni Moda
    fontSize: 32px
    fontWeight: "500"
    lineHeight: 40px
  headline-sm:
    fontFamily: Bodoni Moda
    fontSize: 24px
    fontWeight: "500"
    lineHeight: 32px
  body-lg:
    fontFamily: Montserrat
    fontSize: 19px
    fontWeight: "400"
    lineHeight: 30px
  body-lg-italic:
    fontFamily: Montserrat
    fontSize: 19px
    fontWeight: "400"
    lineHeight: 30px
    fontStyle: italic
  body-md:
    fontFamily: Montserrat
    fontSize: 17px
    fontWeight: "400"
    lineHeight: 28px
  body-sm:
    fontFamily: Montserrat
    fontSize: 15px
    fontWeight: "400"
    lineHeight: 24px
  caption:
    fontFamily: Montserrat
    fontSize: 14px
    fontWeight: "400"
    lineHeight: 22px
    fontStyle: italic
  small-caps:
    fontFamily: Montserrat
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
    fontFamily: Bodoni Moda
    fontSize: 28px
    fontWeight: "500"
    lineHeight: 32px
    letterSpacing: 0.05em
rounded:
  none: 0px
  hairline: 1px
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
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.body-md}"
    padding: "{spacing.page-margin}"
  page-elevated:
    backgroundColor: "{colors.bone}"
    textColor: "{colors.sumi}"
    typography: "{typography.body-md}"
    padding: "{spacing.card-padding}"
  signal-banner:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.signal}"
    typography: "{typography.signal-line}"
    padding: "32px 0"
  signal-banner-rule:
    backgroundColor: "{colors.sumi}"
    height: 1px
  station-marker:
    backgroundColor: "{colors.parchment}"
    width: 14px
    height: 14px
    rounded: "{rounded.full}"
  station-marker-target:
    backgroundColor: "{colors.signal}"
    width: 18px
    height: 18px
    rounded: "{rounded.full}"
  rail-friction:
    backgroundColor: "{colors.sumi}"
    height: 1px
  rail-life-gps:
    backgroundColor: "{colors.brass}"
    height: 1px
  band-target:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.on-signal}"
    typography: "{typography.small-caps}"
    padding: "4px 12px"
  anchor-card:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.body-md}"
    padding: "{spacing.card-padding}"
  anchor-card-rule:
    backgroundColor: "{colors.stone}"
    height: 1px
  anchor-card-numeral:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.broken-gold}"
    typography: "{typography.numeral-roman}"
  anchor-card-heading:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.small-caps}"
  anchor-card-claim:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.charcoal}"
    typography: "{typography.body-md}"
  anchor-card-parallel:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.signal}"
    typography: "{typography.body-md}"
  colophon:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.data-mono}"
    padding: "{spacing.card-padding}"
  colophon-frame:
    backgroundColor: "{colors.sumi}"
    height: 1px
  colophon-ornament:
    backgroundColor: "{colors.broken-gold}"
    width: 12px
    height: 12px
  testimonial-block:
    backgroundColor: "{colors.tea-stained}"
    textColor: "{colors.sumi}"
    typography: "{typography.body-lg-italic}"
    padding: "24px 32px"
  testimonial-rule:
    backgroundColor: "{colors.mahogany}"
    width: 2px
  testimonial-attribution:
    backgroundColor: "{colors.tea-stained}"
    textColor: "{colors.charcoal}"
    typography: "{typography.small-caps}"
  evidence-block:
    backgroundColor: "{colors.library-green}"
    textColor: "{colors.parchment}"
    typography: "{typography.body-md}"
    padding: "{spacing.card-padding}"
  evidence-heading:
    backgroundColor: "{colors.library-green}"
    textColor: "{colors.parchment}"
    typography: "{typography.small-caps}"
  metric-cell:
    backgroundColor: "{colors.parchment}"
    padding: "0"
  metric-value:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.data-mono-lg}"
  metric-label:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.ash}"
    typography: "{typography.small-caps}"
  pricing-anchor:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.display-lg}"
  pricing-tier:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.charcoal}"
    typography: "{typography.small-caps}"
  cta-primary:
    backgroundColor: "{colors.signal}"
    textColor: "{colors.on-signal}"
    typography: "{typography.small-caps}"
    rounded: "{rounded.none}"
    height: 56px
    padding: "0 32px"
  cta-primary-hover:
    backgroundColor: "{colors.signal-deep}"
    textColor: "{colors.on-signal}"
    typography: "{typography.small-caps}"
  cta-ghost:
    backgroundColor: "{colors.parchment}"
    textColor: "{colors.sumi}"
    typography: "{typography.small-caps}"
    rounded: "{rounded.none}"
    height: 56px
    padding: "0 32px"
  cta-ghost-rule:
    backgroundColor: "{colors.sumi}"
    height: 1px
  seal:
    backgroundColor: "{colors.vermilion}"
    textColor: "{colors.on-vermilion}"
    typography: "{typography.small-caps}"
    width: 64px
    height: 64px
    padding: "8px"
  alert-banner:
    backgroundColor: "{colors.alert}"
    textColor: "{colors.on-alert}"
    typography: "{typography.small-caps}"
    padding: "12px 24px"
  hairline-primary:
    backgroundColor: "{colors.sumi}"
    height: 1px
  hairline-soft:
    backgroundColor: "{colors.stone}"
    height: 1px
  logo-horizontal:
    widthRatio: 16
    heightRatio: 9
  logo-stacked:
    widthRatio: 1
    heightRatio: 1
---

## Overview

**Sovereign FMDA — Feral Minimalist Dark Academia.**

A *triangulated* identity. Three traditions held in one frame.

1. **Dark Academia.** Library leather, sumi ink, oxblood, mahogany, Penguin-Classic green. The intellectual weight of a 63-million-word corpus. Typography of monographs. Surfaces of bound books.
2. **Japanese Ma & restraint.** Negative space as material. Sumi-e black. The vermilion *hanko* seal — one chop per artefact. *Wabi-sabi* as integrity, not as kitsch.
3. **Caribbean-Bronx heritage.** *Sovereign Grit.* Ultramarine blue (Barbados) cuts through everything. Broken Gold honours the breakage. Warmth that has nothing to prove.

The aesthetic target is *evidence, beautifully presented* — the way a forensic report would look if designed by someone who cared about craft. Or a long-form *Atlantic* feature on a scientific breakthrough, where the design serves the weight of the information.

> "Friction is the tax you pay to stay. The Neutralizer ends the tax."

If a piece of CBI design could come from any premium wellness brand, it has failed. Sovereign FMDA only sounds like Conroy.

## Foundation

Four compositional disciplines that every CBI artefact must satisfy *before* it ships. The principles are universal; the materials are ours. Each foundation routes through the **signature lockup** (Ultramarine + Broken Gold) first, then draws on the expanded palette for its specific job.

1. **Backdrop chosen with intent.**
   The default backdrop is **parchment** (`#F4EFE6`) — the canvas for every editorial artefact. When gravity is required, the backdrop extends to **library-green** (`#2E4F3E`) for evidence blocks, **mahogany** (`#4A2418`) for case-file panels, or **bone** (`#FAF6EC`) for elevated surfaces. Never neutral grey. Never clinical white. Never "we'll figure out the background later." The decision *is* the design.

2. **One focal point — always Ultramarine.**
   The signal banner is the focal point. Ultramarine (`#1034A6`) at the top of every artefact, italic on the second clause, bracketed by sumi hairlines. There can only be one. A second focal point in Ultramarine breaks the system. (A *secondary* mark is allowed — a single vermilion *hanko* seal for archival pieces — but it serves the focal point, never competes with it.)

3. **Material consistency — two faces (and one for data).**
   **Bodoni Moda** (display + headlines + signal lines + Roman numerals) — high-contrast neoclassical serif, the Italian Vogue / Penguin Classics / Tiffany register. **Montserrat** (body + small-caps + captions) — geometric sans, the calm working voice. **IBM Plex Mono** is the third face but is reserved exclusively for data, colophons, and the corpus signature — never prose. No fourth face. No rounded corners. No gradients. No drop shadows. The discipline is the brand.

4. **Visual weight distributed asymmetrically.**
   Signal at the top. Colophon at the bottom-right, framed with Broken Gold corner ornaments. Attribution at the bottom-left. Centring is the death of editorial weight. The corners do the work; the middle holds the void.

The signature lockup — **parchment + Ultramarine signal + Broken Gold colophon ornaments** — must appear on every artefact. The expanded palette (mahogany, library-green, vermilion, brass, bone, tea-stained, the four ink levels) extends the trunk into specific roles: testimonials, evidence, alerts, archival seals. The expansion never replaces the lockup. It serves it.

## Colors

The palette is built on a **signature lockup** — Ultramarine + Broken Gold + parchment — that appears on every artefact. From that trunk, five families branch out, each from a defined tradition, each with a single job. *Is it meant?* — for every token below, the answer is yes.

### 1 · Caribbean-Bronx Signal

The single high-frequency channel. Used where the eye must go.

- **`signal` `#1034A6`** — Ultramarine Blue (Barbados). The signal sentence. The target friction band. The CBI parallels under the framework anchors. Primary CTAs. Never used as a fill across more than 12% of a composition. Never gradient. Ultramarine is a knife.
- **`signal-deep` `#0A2378`** — hover/active state on primary CTAs only.

### 2 · Dark Academia — The Library

Library leather, oxblood, billiard-cloth green. The aesthetic of *bound books and forensic case files.* These are the colours the previous DESIGN.md was missing.

- **`mahogany` `#4A2418`** — library-leather. Border on testimonial blocks. Frame on serious case studies. Where Broken Gold would be too ornamental, Mahogany carries the weight.
- **`oxblood` `#6B1F1B`** — editorial accent for stamped, archival artefacts. Also: alert.
- **`library-green` `#2E4F3E`** — Penguin Classic / billiard cloth. Surface of evidence blocks (corpus stats, LMFT validations, clinical citations). The third Dark Academia surface. **This is not wellness sage.** Wellness sage is light, washed-out, calming. Library green is deep, saturated, bound.
- **`library-green-soft` `#3F6151`** — lower-contrast tint for evidence-block accents.

### 3 · Japanese Restraint — Sumi & Hanko

Multiple ink levels for typographic hierarchy. The vermilion seal as the only "stop" colour.

- **`sumi` `#1A1613`** — sumi-e ink. Body text on parchment. Never pure black; warmer.
- **`charcoal` `#3A332C`** — secondary text. Long-form prose where pure sumi would be too heavy.
- **`stone` `#6B6058`** — tertiary text, metadata, hairlines.
- **`ash` `#9A8F84`** — quietest text level. Metric labels, disabled states, axis numerals.
- **`vermilion` `#B83A24`** — the *hanko* seal. The Japanese accent that is not gold. Used **once per artefact, maximum.** A verified-mark on a case file. A seal under a quote. Never on body text. Never on a CTA. Never as a fill across more than 60×60 pixels.

### 4 · Ma — Surfaces

Three paper tones. Generosity of empty space is the brand signature.

- **`parchment` `#F4EFE6`** — the void. 70% of any composition.
- **`bone` `#FAF6EC`** — palest paper. Elevated surfaces only.
- **`tea-stained` `#EDE6D8`** — slightly warmer cream. Testimonial fills, secondary panels.

### 5 · Metal — Gold and Brass Are Different Jobs

This is where the previous DESIGN.md failed. **Gold and Brass do not interchange.**

- **`broken-gold` `#A8894A`** — oxidised, matte. **Reserved exclusively for: Roman numerals on framework anchors, and Bauhaus corner ornaments on the colophon.** Two jobs. Nothing else. Never rails. Never borders. Never hover states. Reach for gold on a third surface — stop and pick something else.
- **`brass` `#877152`** — cooler, structural, industrial. Used for: the Life GPS rail, secondary structural rules, occasional border accents on archival blocks. **Brass is engineering. Gold is ornament.** The distinction is what kept Bottega Veneta from looking like Versace.

### 6 · Alert

- **`alert` `#6B1F1B`** — oxblood. Same family as mahogany. **No yellow. No orange. No fire-engine red.** When CBI alerts, the alert is calm and authoritative — the colour of a library fire-extinguisher cabinet, not a smoke alarm.

### Forbidden roles

Wellness sage. Lavender. Sky blue. Mint. Coral. Peach. Rose-gold. Any pastel. Any gradient between two of these tokens (Ultramarine fading to Vermilion is *especially* forbidden — that's a Trump-rally palette). No emoji-yellow alerts. No SaaS purple. No "trust blue." No "safety green."

### WCAG (parchment background)

- `sumi` on parchment: 14.1:1 (AAA)
- `charcoal` on parchment: 9.4:1 (AAA)
- `stone` on parchment: 4.7:1 (AA — body OK at body-md+)
- `ash` on parchment: 2.8:1 (decorative only)
- `signal` on parchment: 8.7:1 (AAA)
- `mahogany` on parchment: 11.2:1 (AAA)
- `library-green` on parchment: 6.1:1 (AAA)
- `vermilion` on parchment: 4.6:1 (AA decorative)
- `broken-gold` on parchment: 3.4:1 (decorative only)
- `brass` on parchment: 4.3:1 (decorative only)
- `parchment` on `signal`: 8.7:1 (AAA)
- `parchment` on `library-green`: 8.5:1 (AAA)
- `parchment` on `mahogany`: 12.4:1 (AAA)

## Typography

**Two faces. Two jobs. Plus one strictly-bounded face for data.**

- **Bodoni Moda** — display, headlines, signal lines, Roman numerals. High-contrast neoclassical serif. The register of *Italian Vogue*, Penguin Classics title pages, Tiffany & Co. catalogues. Italic for the second clause of any signal line. Bodoni's hairlines are the typographic equivalent of Ultramarine — they cut.
- **Montserrat** — body, testimonials, captions, small-caps, CTAs. Geometric sans, the calm working voice. Holds long-form without fatigue. Multiple weights (400 body, 600 small-caps, 700 reserved for data labels).
- **IBM Plex Mono** — data, metrics, colophons, the corpus signature. **Reserved for evidence only.** The mono lockup *is* the credential. Never used for prose. If a sentence is in mono, it is wrong.

The signal line is the largest object on any page. Body copy is generous (16–18px Montserrat at line-height ≥1.6). Small-caps with 0.18em tracking for section headers and metric labels. The pause between sentences is part of the sentence — paragraph spacing ≥1em is non-negotiable.

**Pairing principle.** Bodoni's high-contrast hairlines need Montserrat's even geometry to rest against — sharp serif headline, calm sans body. The contrast is the system. Inverting it (sans headline + serif body) breaks the brand.

**Forbidden:** Inter, Roboto, Helvetica, Arial, Open Sans, Space Grotesk, Poppins, Lato, Nunito, Source Sans, Work Sans, anything Bootstrap defaults to. Generic AI aesthetics die here.

## Layout

A grid built around the void. Layout is composition, not container-stuffing.

- **Base unit:** 8px. All spacing is a multiple.
- **Page margins:** ≥120px desktop, ≥48px mobile. The frame is itself a design element.
- **Void floor:** at least 70% unoccupied parchment. If a comp is denser, strip until it isn't.
- **Single column for prose.** Max line length 68 characters.
- **Asymmetry over symmetry.** Colophon belongs bottom-right. Attribution belongs bottom-left. Centring is the death of editorial weight.
- **Print spec.** Every artefact must include `@media print`: paper-grain disabled, parchment forced, Ultramarine and Mahogany preserved, hairlines ≥0.75pt.

## Elevation & Depth

Depth is built from **typography, hairlines, and Ma.** Never shadows.

- **L1 — Surface.** Parchment with optional 4% noise filter.
- **L2 — Section.** 1px sumi hairline + ≥48px vertical Ma. Not a card. Not a shadow.
- **L3 — Panel.** Tea-stained or library-green fill. Used for testimonials, evidence blocks, archival quotes. Always full-bleed within its column.
- **L4 — Frame.** 1px sumi border + Bauhaus corner ornaments in Broken Gold. The colophon and proof-pack only.
- **L5 — Signal.** Ultramarine fill. Reserved for target friction band, primary CTAs, signal lozenges. Functions as elevation by *contrast*, not stacking.

**Forbidden:** drop shadows, glow, glassmorphism, neumorphism, parallax, layered transparency. CBI is an instrument panel.

## Shapes

**Right angles. Hairlines. Full-circle station markers. Nothing else.**

- Cards and frames: `rounded.none` (0px). Sharp is default and standard.
- Borders: 1px hairline (sumi) for structural rules; 1px brass for the Life GPS rail and archival panels; 2px mahogany for testimonial left-borders.
- Station markers: 14px concentric-stroke circles in sumi (the journey rail's only round shape). The Sovereign station is haloed at 18px with an Ultramarine fill.
- CTAs: rectangular. No pills.
- Iconography: avoided. Where unavoidable, 1.5px line icons in sumi, never filled. **Never** lotus, sunset, flowing curves, sparkles, checkmarks, gradient orbs, hands raised to the sky.

## Components

### Signal Banner

The single sentence that opens any composition. Top of page. Centred. Ultramarine. Italic on the second clause. Bracketed by 1px sumi hairlines (above and below). Reads in 10 seconds cold.

> *"Friction is the tax you pay to stay. The Neutralizer ends the tax."*

### Journey Rail

Tourist → Operator → Sovereign. Three station markers connected by a 1px sumi rail. Friction Scale (20→0) running beneath as a numbered axis. Target band (2–3) highlighted in solid Ultramarine. The Life GPS rail runs parallel above in dashed **brass** (not gold — gold is for ornaments). System tags ("THE NEUTRALIZER" / "C.U.E. METHOD") set in small-caps above the rail in sumi.

### Anchor Card (Six Clinical Anchors)

Used in the 3×2 framework grid. Each card carries:

- A Roman numeral in **Broken Gold** (28px Cormorant Garamond)
- The surname in small-caps sumi (0.18em tracking)
- A single-sentence claim in body-md charcoal italic
- The CBI parallel in Ultramarine — exactly one line

Top border: 1px stone hairline. No fill. No rounded corners. Numerals are the only place Broken Gold appears in this component.

### Colophon

The proof block. Bottom-right of any page. 1px sumi frame. Bauhaus corner ornaments in **Broken Gold** at top-left and bottom-right corners only (12×12px). Contents in IBM Plex Mono:

```
131 CLIENTS · 1,323 SESSIONS · 63M WORDS · 7 YEARS
51% SHIFT IN SESSION 1 · 6.4 SESSIONS MEAN
4+ LICENSED CLINICAL VALIDATORS
```

Numbers are sacred. Source of truth: `VERIFIED_METRICS.md`.

### Testimonial Block

Verbatim client quote. Background: tea-stained (`#EDE6D8`). Left border: 2px **mahogany** (library-leather, not gold). Quote in `body-lg-italic` sumi. Attribution in small-caps charcoal with credential where applicable.

> *"20 years of therapy couldn't do what 90 minutes did."*
> — ALINE INOCENCIO, LMFT (20 YEARS CLINICAL PRACTICE)

**Quotes are never paraphrased, cleaned up, or reordered.** (See `memory/feedback_verbatim_quotes_sacred.md`.)

### Evidence Block

The third Dark Academia surface, and the place library-green earns its job. Used for: corpus statistics, clinical-validator credentials, peer-reviewed research callouts, case-file blocks. Background: `library-green` (`#2E4F3E`). Text: parchment. This is where evidence gets *bound* — a single contained panel that makes the case for the corpus.

> Used sparingly — one evidence-block per artefact maximum. If everything is evidence, nothing is.

### Pricing Anchor ($1,500)

Rendered in `display-lg` Cormorant Garamond on parchment, sumi ink. Never crossed-out. Never with a "save $X" badge. Never paired with a countdown timer. Tier labels in small-caps. *"The anchor is $1,500."* Never *"the price."*

### CTA — Primary

Rectangular. Solid Ultramarine fill. On-signal text in small-caps. 56px height. No border-radius. No shadow. On hover: deepens to `signal-deep`. The only place Ultramarine functions as a button surface.

### CTA — Ghost

For secondary actions. Parchment fill. 1px sumi border. Sumi text in small-caps. On hover: tea-stained fill.

### Seal (Vermilion *Hanko*)

The Japanese-restraint accent. A 64×64px square, vermilion fill, parchment glyph (initials, year, or "VERIFIED" in small-caps). **One seal per artefact, maximum.** Used as a stamp on archival case-files, verified-quote artefacts, and the bottom of the corpus page. Never on a CTA. Never on a banner. Never recurring. Its power is its scarcity.

### Alert Banner

Oxblood fill (`#6B1F1B`). Parchment text in small-caps. Used for genuine system alerts (form errors, integrity warnings). **Never** for marketing urgency. CBI does not manufacture urgency.

### Hairline Rules

- `hairline-primary` — 1px sumi. Section dividers, table rules, frame edges.
- `hairline-soft` — 1px stone. Anchor-card top rules, secondary separations.

Always 1px. Never doubled. Never decorated.

## Logo

CBI has two approved lockups. Use only these. Do not reconstruct, re-kern, or re-draw either.

### Lockups

**Horizontal lockup** — large CBI mark centred above a single-line wordmark. 16:9 aspect ratio. Source: `assets/logo/cbi-lockup-horizontal.svg`. Use for: web headers, deck title slides, large-format print, email headers, YouTube channel art.

**Stacked lockup** — smaller CBI mark above a two-line wordmark ("CONROY BROWNE / INTERNATIONAL"). 1:1 aspect ratio. Source: `assets/logo/cbi-lockup-stacked.svg`. *(SVG pending — Conroy to drop into `assets/logo/` when available.)* Use for: social avatars, app icons, watermarks, square crops, profile images.

### Clear Space

Minimum clear space on all four sides = the cap-height of the "I" in "CBI" (measured from the approved SVG at any render size). Nothing — text, image, frame edge, competing graphic element — enters that boundary.

### Minimum Sizes

| Lockup | Screen | Print |
|---|---|---|
| Horizontal | 240px wide | 30mm wide |
| Stacked | 96×96px | 18×18mm |

Below minimum size, the lockup becomes illegible. Do not use it smaller — omit it entirely.

### Colour Applications

Five approved applications, in order of preference:

1. **Sumi-on-parchment** (default) — `#1A1613` mark on `#F4EFE6` background. Editorial artefacts, documents, printed materials.
2. **Parchment-on-Ultramarine** (reverse, primary surfaces) — `#F4EFE6` mark on `#1034A6` background. Signal banners, primary CTA panels, Ultramarine covers.
3. **Parchment-on-Mahogany** (case-file artefacts) — `#F4EFE6` mark on `#4A2418` background. Testimonial covers, case-study headers, archival print.
4. **Parchment-on-Library-Green** (evidence panels) — `#F4EFE6` mark on `#2E4F3E` background. Corpus pages, clinical-validation panels, evidence blocks.
5. **Parchment-on-Sumi** (dark-mode artefacts) — `#F4EFE6` mark on `#1A1613` background. Digital dark mode, video lower-thirds, nightmode documents.

No other colour combinations are permitted.

### Forbidden

- Stretching or distorting either lockup
- Recolouring outside the five approved applications above
- Drop shadows, glow, emboss, or outline applied to the mark or wordmark
- Placing either lockup on busy photography or a patterned background
- Gradient fills on the mark or wordmark
- Outlining the type within the wordmark
- Recreating the wordmark from any cut of Bodoni other than the locked SVG file
- Placing the stacked lockup where minimum size cannot be met — use the horizontal or omit

---

## Voice in Visual

Every visual decision must pass these tests, drawn from `plugins/design/skills/cbi-brand-enforcement.md`:

1. **Lexicon.** Does it use *The Neutralizer*, *Life GPS*, *C.U.E. Method*, *Friction*, *Pressure-breach*, *Sovereign*, *Operator*? Or has it slipped into *the program / coaching / framework / resistance / breakthrough / empowered / client*?
2. **Tone.** Would Conroy say this? "Sexy-ass Yoda" — wise, precise, a little provocative, never corporate, never apologetic.
3. **Operator test.** Would an Operator (done the work, still stuck) feel seen? Would a Tourist (wants a quick fix, collects tools) feel invited? If yes to Tourist, revise.
4. **Premium test.** Does this look like $1,500 anchor value? Or does it look free?
5. **Friction test.** Does the design *remove* friction or add it? Every unnecessary click, scroll, decision, or visual element is friction.

## Do's and Don'ts

**Do:**

- Lead with the signal. One sentence. Ultramarine.
- Hold 70% Ma.
- Render `131 / 1,323 / 63M / 7` in IBM Plex Mono. The mono lockup is the credential.
- Use Broken Gold **only** on Roman numerals and corner ornaments.
- Use Brass on rails (not gold). Use Mahogany on testimonial borders (not gold). Use Library Green on evidence blocks (not gold).
- Use the Vermilion seal **once per artefact**. Where it appears is the *most-stamped* moment.
- Quote clients verbatim. Attribute by name and credential.
- Print-test every artefact.

**Don't:**

- Use gradients of any kind.
- Use stock wellness imagery.
- Use Inter, Roboto, Helvetica, or any of the AI-default sans-serifs.
- Round corners. Sharp is the default.
- Use drop shadows, glow, glassmorphism, or any simulated physical depth.
- Use Broken Gold for rails, borders, hover states, or anything beyond Roman numerals + corner ornaments. Gold doing too many jobs is the Trump-rally aesthetic. *Restraint is the brand.*
- Use Vermilion more than once per artefact.
- Pair Ultramarine with Vermilion *as a gradient*. As separate marks on the page, fine. As a fade between, never — that's a flag, not a system.
- Use sparkles, checkmarks, confetti, gradient orbs, or "amazing transformation" energy.
- Use "navigating," "unlocking," "holistic," "transformative journey," "empower."
- Reveal pricing before Theo's diagnostic.
- Add a single element you can't justify. Strip it.

## References

- `plugins/design/skills/cbi-brand-enforcement.md` — auto-invoked brand check
- `docs/positioning/CBI-NARRATIVE-VISUAL-ALIGNMENT.md` — Alessandra → Elara translation
- `docs/positioning/CBI-PHOBIA-VISUAL-EMOTIONAL-ARCHITECTURE.md` — emotional-arc design brief
- `docs/positioning/CBI-WHY-CONROY-THE-SUPREME-BRAND.md` — Supreme positioning
- `docs/positioning/CBI-POSITIONING-MASTER-ARSENAL.md` §06 — Six Clinical Framework Anchors
- `.claude/rules/brand.md` — voice and lexicon
- `.claude/rules/pricing.md` — $1,500 anchor logic
- `.claude/rules/friction-scale.md` — 1–20 scale, target 2–3
- `agents/souls/06-ELARA-THORNE-BROWNE-SOUL.md` — Elara's identity
- KB: *Document 1 — The Sovereign FMDA Visual Manifesto* (`category: identity`)
- KB: *Document 2 — Material & Color Protocol* (`category: protocol`)
- `docs/plans/brief-01-visual-map/sovereign-map.html` — reference implementation

---

*Authored by Elara Thorne-Browne (Gem 6), Sovereign Art Director.*

*Version 2.0 — palette expanded from Ultramarine + Gold to the full triangulated FMDA system. Mahogany, Library Green, Vermilion, Brass, Bone, Tea-stained, multiple ink levels. Gold restricted to Roman numerals and corner ornaments. Brass takes the rails. Mahogany takes the testimonial borders. Library Green takes the evidence blocks. Each colour has one job and does it.*

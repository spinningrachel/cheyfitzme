# cheyfitz.me site — working rules

The bound **cheyfitz.me Design System** governs color, spacing, and logo. These notes record where this
site *intentionally departs* from the design system's default layout grammar. When the two conflict, THESE
rules win for site work.

## Why these rules exist
The owner can spot the generic "AI house style" from a mile off: mono ALL-CAPS eyebrow on every section,
serif headline reflex, chip/pill rows, symmetric before/after cards, everything rounded. We deliberately
removed those. Do not reintroduce them.

## Type system v2 (see assets/fonts.css)
- **Schibsted Grotesk is primary** — display, headings, AND body. Tight tracking, heavy weights (700–800)
  for display. This is the single biggest change; lean on it.
- **BioRhyme is the editorial marker voice** — uppercase section labels (the eyebrow, `.t-label`) and
  section numerals (`.t-marker`), which pair into one "marker unit" set against the Schibsted heading.
  Plus rare display accents (`.t-display-accent`, `.t-quote-mark`). NEVER a body face or a default
  heading face. This is the deliberate inverse of the cliché: a sans headline with a *serif* eyebrow,
  not a serif headline.
- **JetBrains Mono is functional / data only** — code, routes &amp; URLs, timestamps, status tags
  (KEEP / REPLACE), filing metadata, footnote markers. NEVER a decorative section eyebrow. (Section
  *numerals* are BioRhyme markers now, not mono.)
- **Eyebrows are BioRhyme UPPERCASE in a signal color** (`.t-label`) — serif caps, never mono. Pair with
  a BioRhyme numeral (`.t-marker`) on section / part openers. Still selective: many sections need no
  label, and the numeral is optional — present it on major divisions, drop it on minor sub-blocks.
- **Sizes are contextual, not fixed.** Markers and labels are roles, not one px value. The numeral steps
  with the level (cover ~56–80px · section ~32–40px · sub ~20–24px or omit); the label stays small.
  Don't hardcode a single size system-wide.
- **No chips / pills.** Don't use `.tag-*` pill rows or flex-wrap chip groups for nav, categories, or
  filters. Use plain text, hairline-ruled rows, ledgers, or tables instead.
- **Where the marker lives.** The BioRhyme marker unit (numeral + uppercase eyebrow) belongs to
  *documents* (proposals, reviews, plans) and major section openers. The Plain marketing pages stay
  lean — mostly label-free, with a BioRhyme eyebrow on at most a hero or two. Never serif-caps eyebrows
  on every site section.

## Two page systems
Colors are unchanged (Voltage Green, Hot Pink, Cyan, Lemon, the purples). The split is about register:

- **Plain (≈90% of the site)** — Work, Frameworks, Writing, About, pricing, blog. Restraint as the flex:
  near-monochrome, generous whitespace, hairline rules instead of cards, color used surgically (a few
  times per page). Reference: `Direction Studies.dc.html` → direction A. Plain / Linear register.
- **Voltage (≈10% — the generous/loud moments)** — the "I Mentor For Free" page, event/campaign landing
  pages, and the bottom-of-page CTA band on Plain pages. Full color fields, oversized knockout type,
  the palette at full strength. Hot Pink = the emotional interrupt; Voltage Green = the action.
  Reference: `Mentor Page — Voltage.dc.html`. Rive / ClickUp register.

## Color rule still in force
Never place Hot Pink and Voltage Green as adjacent fields/blocks. Separate them with purple, cyan, or ink.
(Voltage service panels run green / purple / pink for this reason.)

## Build conventions
Inline styles in DC templates (per the DC authoring model). `assets/fonts.css` + `assets/tokens.css` are
loaded in `<helmet>` for @font-face and color tokens.

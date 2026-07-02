# cheyfitz.me site — working rules

The bound **cheyfitz.me Design System** governs color, spacing, and logo. These notes record where this
site *intentionally departs* from the design system's default layout grammar. When the two conflict, THESE
rules win for site work.

## Why these rules exist
The owner can spot the generic "AI house style" from a mile off: mono ALL-CAPS eyebrow on every section,
serif headline reflex, chip/pill rows, symmetric before/after cards, everything rounded. We deliberately
removed those. Do not reintroduce them.

## Type system v3 (design system update 2026-06-30)

**The deliberate break:** this system avoids the AI design system tell (mono ALL-CAPS eyebrow + serif heading). Instead: humanist sans headings (Cabin) with italic serif eyebrows (BioRhyme), body in a confident grotesk (Schibsted).

- **Cabin is headings + UI** — H1–H4, nav, buttons. Weight 700 max (Cabin's ceiling). Tight tracking on display sizes. `--font-display` and `--font-heading` both point here.
- **Schibsted Grotesk is body copy** — lede, paragraphs, all reading text on screen. `--font-body`. Never at heading size.
- **BioRhyme is eyebrows + decorative only** — `.t-eyebrow` / `.t-label`: 13px, italic, sentence case, signal color, 0.75 opacity. Also pull-quotes (`.t-quote`), numerals (`.t-marker`), quote marks (`.t-quote-mark`). NEVER for headings (H1–H4) — that's the pattern we're breaking.
- **JetBrains Mono is code blocks only** — code, inline code. NEVER eyebrows or brand labels.
- **`.t-tag`** (service chips, category pills) — JetBrains Mono 11px, UPPERCASE, letter-spacing 1px, pill border-radius. A UI element, not an eyebrow.
- **Eyebrows are sentence case** — `.t-eyebrow` is italic BioRhyme, delicate not loud. Never uppercase, never tracked. Use sparingly — many sections need no eyebrow.
- **No chips / pills for nav/filters.** Use plain text, hairline-ruled rows, ledgers. `.t-tag` is only for service type badges (Strategy, Frameworks, Resources).

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

---
name: Ghim Chong Tan Portfolio
description: Personal portfolio for a product associate — light, single-surface design where cobalt punctuates without performing and typography carries the identity.
colors:
  bg: "oklch(1.000 0.000 0)"
  surface: "oklch(0.966 0.008 230)"
  ink: "oklch(0.135 0.014 230)"
  primary: "oklch(0.420 0.090 230)"
  muted: "oklch(0.460 0.018 230)"
  accent: "oklch(0.875 0.040 230)"
  line: "oklch(0.895 0.012 230)"
typography:
  display:
    fontFamily: "'Spectral', Georgia, serif"
    fontSize: "clamp(3rem, 8vw, 5.5rem)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "-0.022em"
  section:
    fontFamily: "'Jost', system-ui, sans-serif"
    fontSize: "clamp(1.75rem, 3.5vw, 2.75rem)"
    fontWeight: 400
    lineHeight: 1.25
    letterSpacing: "-0.015em"
  body:
    fontFamily: "'Jost', system-ui, sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.72
  label:
    fontFamily: "'Jost', system-ui, sans-serif"
    fontSize: "13px"
    fontWeight: 500
    letterSpacing: "0.01em"
rounded:
  card: "14px"
  pill: "100px"
  sm: "6px"
spacing:
  section-v: "80px"
  content-h: "max(32px, 6vw)"
  gap: "24px"
---

# Design System: Ghim Chong Tan Portfolio

## 1. Overview

**Creative North Star: "Considered Confidence"**

One surface, one signal. The page is white throughout — no dramatic two-zone split, no theatrical dark hero. The cobalt primary (`oklch(0.420 0.090 230)`) appears where it matters: links, borders, small interactive moments. It earns its presence by rarity. Typography does the structural work that color was doing before.

Instrument Serif holds the display moment — one H1 per page, at a scale that requires attention. Inter handles every other layer: navigation, body, metadata, labels. Two typefaces, one function each. Nothing overlaps.

The architecture-to-fintech arc is the story. The design's job is to stay out of the way while making that arc impossible to miss.

**Key Characteristics:**
- Single white surface throughout — no hero background color, no surface zoning
- Cobalt primary as punctuation, not atmosphere: links, borders, CTAs, key rule lines only
- Instrument Serif at display scale once per page (H1 only); Inter for every other typographic role
- Borders over shadows as spatial language; elevation only as a hover/focus state signal
- Flat at rest; `translateY` + shadow on card hover only
- Voice stays specific: countries, numbers, outcomes — not categories

## 2. The Color System

**Strategy: Restrained.** One brand color (cobalt), tinted neutrals for surfaces, pale accent for chips. The color's rarity is the identity.

### Surfaces
- **Pure White** `oklch(1.000 0.000 0)`: Body and nav background. The only surface. No warmth tilt.
- **Pale Field** `oklch(0.966 0.008 230)`: Cards, panels, code blocks, subtle section tints. The barest perceptible cobalt — visible on close inspection, not at a glance.

### Text
- **Near Black** `oklch(0.135 0.014 230)`: All headings and body text. Near-black with the faintest cobalt cast — registers as black, reads on brand.
- **Cobalt Gray** `oklch(0.460 0.018 230)`: Secondary text — metadata, dates, supporting copy. Passes WCAG AA on Pure White (≥4.5:1).

### Brand
- **Cobalt** `oklch(0.420 0.090 230)`: The sole accent. Interactive states (links, borders, focus rings), active nav indicators, key dividers. Never used as a background fill on text surfaces.
- **Pale Cobalt** `oklch(0.875 0.040 230)`: Tag and chip fills only. Cobalt at high lightness — always paired with Cobalt text.

### Structural
- **Rule** `oklch(0.895 0.012 230)`: Section dividers, card borders, input borders at rest.

**One Voice Rule.** Cobalt `oklch(0.420 0.090 230)` is the sole accent. It appears on ≤10% of any screen. Every interactive element speaks in this color and no other.

## 3. Typography

**Display:** Spectral (Google Fonts, Production Type)
**Body:** Jost (Google Fonts)

**Character:** Spectral is an optical-size-aware screen serif designed by Production Type — precise, legible, with a quiet authority that sits closer to "a well-produced professional document" than to editorial-magazine. Jost is a geometric grotesque rooted in Renner's 1920s Futura proposals; it has structural precision and an architectural economy of form that suits the background. Together they read as someone who builds things to work, not to impress.

**Brand voice in physical object terms:** "Site planning documents with hand-drawn notation — Spectral for the title block, Jost for every annotation."

### Scale
- **Display** (Spectral, 400, clamp(3rem, 8vw, 5.5rem), lh 1.1): H1 only. One display moment per page.
- **Section** (Jost, 400, clamp(1.75rem, 3.5vw, 2.75rem), lh 1.25): H2 section headings. Geometric weight carries the heading; no italic, no bold.
- **Body** (Jost, 400, 16px, lh 1.72): All running copy. Line length capped at 65ch.
- **Label** (Jost, 500, 13px, ls 0.01em): Nav links, metadata, dates, tags. Weight 500 for legibility at small sizes.

**The Display-Once Rule.** Spectral appears at display scale (≥48px) on one element per page — the H1. Never for subheadings, section labels, or pull quotes.

**The Paired Weight Rule.** Spectral display is 400. Jost body is 400. Differentiation comes from family and scale, not weight stacking. Emphasis: Jost weight 600. Italics: available in Spectral; reserved for a deliberate opener in the H1 if the voice calls for it.

## 4. Elevation

Flat at rest. The one-surface design means shadows carry no structural information — they are state signals only.

### Shadow Vocabulary
- **Card Hover** (`0 4px 24px oklch(0.420 0.090 230 / 0.12)`, paired with `translateY(-2px)`): Gallery/project cards on hover. Cobalt-tinted ambient lift.
- **Button Hover** (`0 2px 12px oklch(0.420 0.090 230 / 0.20)`): Primary button on hover only.

**The State-Only Rule.** Shadows signal interaction, not hierarchy. At rest: flat. On hover/focus: lift. Use `oklch(color / alpha)` syntax throughout — never `rgba`.

## 5. Components

### Navigation
- **Style:** Sticky top bar, Pure White background, 1px Rule border-bottom.
- **Logo:** Near Black, Inter weight 600, 14px. Hover: Cobalt.
- **Links:** Near Black at rest, Cobalt on hover. Weight 400, 14px.
- **CTA (Resume):** Cobalt border pill. Hover: filled Cobalt bg, white text.
- **Mobile:** Hamburger collapse at ≤640px. Drawer on white background, same link styles at 15px.
- **Skip link:** First focusable element. Visually hidden off-screen; slides in on focus. Cobalt pill style.

### Project Card
- **Shape:** 14px radius.
- **At rest:** 1px Rule border, flat, image covers the card.
- **Hover:** Card Hover shadow + `translateY(-2px)`.
- **Overlay:** Linear gradient for text legibility when image is present.
- **Empty state (Coming Soon):** Pale Field surface, centered muted label.

### Tag / Chip
- **Style:** Pill shape (100px radius), Pale Cobalt fill, Cobalt text.
- **Size:** 12px, weight 500, 4px × 10px padding.
- **Use:** Skill tags, category labels — display only, no interactive state.

### Resume Entry
- **Structure:** Title + date on one row (flex space-between), subtitle below, description paragraphs, optional tags.
- **Title:** 18px, weight 600, Near Black.
- **Subtitle:** 15px, weight 500, Cobalt Gray.
- **Description:** 15px, weight 400, Cobalt Gray.
- **Date:** 13px, Cobalt Gray.

## 6. Do's and Don'ts

### Do:
- **Do** use Cobalt as the sole interactive accent — links, borders, focus rings — and nowhere else.
- **Do** use Instrument Serif at display scale for H1 only. Inter handles every other typographic role.
- **Do** use 1px Rule borders as the primary spatial separator at rest. Shadows only on hover.
- **Do** write copy with specifics: countries, numbers, outcomes. The work is the credential.
- **Do** maintain WCAG AA: body text ≥4.5:1 vs Pure White, large text ≥3:1.
- **Do** make the architecture→fintech arc legible in the first two sentences of the hero.
- **Do** include `prefers-reduced-motion` alternatives for every transition.

### Don't:
- **Don't** add a background color to the hero section. No dark zone, no tinted surface for the intro — one white surface, top to bottom.
- **Don't** add a second accent color. One Voice Rule holds.
- **Don't** use Spectral for subheadings, section labels, pull quotes, or card titles.
- **Don't** use uppercase tracked eyebrows on every section — that is AI grammar.
- **Don't** use gradient text (`background-clip: text`).
- **Don't** use side-stripe `border-left` accents on cards or list items.
- **Don't** use shadow for structural separation at rest — that is the Rule color's job.
- **Don't** use monospace to signal "technical." This is a product thinker's portfolio.
- **Don't** repeat `rgba` — use `oklch(color / alpha)` syntax.

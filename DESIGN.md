---
name: Akar Project Rate Card
description: Premium editorial rate card for student-facing academic and creative services
colors:
  primary: "#1D9E75"
  primary-medium: "#0F6E56"
  forest: "#085041"
  mint: "#9FE1CB"
  mint-light: "#E1F5EE"
  warm-white: "#F6F3EC"
  warm-white-deep: "#EDEAE1"
  ink: "#1A1A18"
  gray: "#6B6B68"
  gray-light: "#B0ADA6"
  white: "#FFFFFF"
  border: "#DDD9D0"
typography:
  display:
    fontFamily: "'Playfair Display', Georgia, serif"
    fontSize: "clamp(2.75rem, 7vw, 5rem)"
    fontWeight: 700
    lineHeight: 1.05
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "'Playfair Display', Georgia, serif"
    fontSize: "1.75rem"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "normal"
  title:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.02em"
  body:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: "0.8125rem"
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: "normal"
  label:
    fontFamily: "'DM Sans', system-ui, sans-serif"
    fontSize: "0.625rem"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.12em"
rounded:
  sm: "4px"
  md: "8px"
  lg: "12px"
  pill: "20px"
  xl: "14px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "16px"
  lg: "24px"
  xl: "32px"
  xxl: "48px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
    padding: "10px 24px"
  button-primary-hover:
    backgroundColor: "{colors.primary-medium}"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
    padding: "10px 24px"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
    padding: "10px 24px"
  nav-tab-active:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    rounded: "{rounded.pill}"
    padding: "5px 14px"
  nav-tab-inactive:
    backgroundColor: "transparent"
    textColor: "{colors.gray}"
    rounded: "{rounded.pill}"
    padding: "5px 14px"
---

## Overview

**Creative north star: The Quiet Briefing Room**

Akar Project's visual system reads like a well-edited document from a studio you trust — not a startup landing page. Think Apple product literature, Linear's typographic discipline, Notion's calm surfaces, Stripe's pricing clarity, and Raycast's precision without the dark-mode default. Premium, elegant, minimal, editorial, natural, and modern.

The rate card is the product experience: a full-bleed forest cover, warm-white reading surface, serif display moments, and sans-serif utility for tables and policy text. Motion is subtle; structure carries the brand.

## Colors

| Role | Token | Hex | Use |
|------|-------|-----|-----|
| Primary | `primary` | `#1D9E75` | CTAs, active nav, accents, links |
| Forest | `forest` | `#085041` | Cover background, price emphasis, step numbers |
| Primary medium | `primary-medium` | `#0F6E56` | Hover states, badges |
| Mint | `mint` | `#9FE1CB` | Cover highlights, italic emphasis, decorative accents |
| Mint light | `mint-light` | `#E1F5EE` | Category icons, included tags, soft highlights |
| Warm white | `warm-white` | `#F6F3EC` | Page background |
| Warm white deep | `warm-white-deep` | `#EDEAE1` | Alternate surfaces, table header tint |
| Ink | `ink` | `#1A1A18` | Primary text |
| Gray | `gray` | `#6B6B68` | Secondary text, descriptions |
| Border | `border` | `#DDD9D0` | Hairline dividers only — use sparingly |

**Color strategy:** Restrained palette with forest green as the committed hero surface and mint as a secondary accent. Green family carries identity; warm white provides editorial breathing room. No purple, no blue SaaS neutrals, no oversaturated fills.

**Canonical OKLCH reference (implementation):** prefer OKLCH in CSS when refactoring — e.g. primary ≈ `oklch(0.62 0.12 165)`, forest ≈ `oklch(0.32 0.06 165)`, mint ≈ `oklch(0.85 0.08 165)`, warm-white ≈ `oklch(0.96 0.01 95)`.

## Typography

- **Display / headlines:** Playfair Display — editorial authority for cover title and section headings. Italic for emphasis words, tinted mint or primary, never gradient text.
- **Body / UI:** DM Sans — clean humanist sans for tables, policies, buttons, and metadata. Weights 300–500 only; avoid heavy bold stacks.
- **Scale:** Display capped at ~5rem max on cover; section titles ~1.75rem; body 13px base with 12px for dense table cells.
- **Rules:** `text-wrap: balance` on h1–h2; max prose width ~65ch for descriptions; no Inter; no paired geometric sans duplicates.

## Elevation

**Flat editorial layering.** Depth comes from background shifts (forest cover → warm-white body → white table surfaces), not box shadows. Borders are 0.5px hairlines at low contrast. No glassmorphism, no heavy glow, no large drop shadows. Hover on table rows: subtle green tint only (`rgba(29,158,117,.04)`).

## Components

### Cover hero
Full-viewport forest (`forest`) with radial mint glows kept subtle and non-neon. Logo top-left; document type pill top-right. Display headline with one italic accent line. Service chips as low-contrast pills, not cards.

### Sticky navigation
Warm-white bar with hairline bottom border — **no backdrop blur**. Logo + horizontal tab pills. Active tab: solid primary fill; inactive: text only with hover border.

### Price tables
White surface, single outer wrapper with overflow scroll on mobile. Header row on warm-white tint. Row hover tint only. Price column right-aligned, forest weight. Avoid nesting tables inside cards inside cards.

### Package bundles
Grid of equal cards is acceptable only when each card carries distinct content hierarchy — prefer reducing card chrome: flat white, 0.5px border OR background tint, not both plus shadow. One featured state via primary border weight, not glow.

### Policy & notes
Flat white or warm-white panels. Leading arrow or icon for list items — not left stripe borders. Section labels: minimal uppercase tracking, used sparingly (not on every block).

### Contact CTA bar
Forest panel, primary + ghost buttons. Full-width on mobile.

### Motion
Tab switch: instant or short opacity; scroll-to-nav with `prefers-reduced-motion` fallback to instant. Ease-out only; no bounce.

## Do's and Don'ts

**Do**
- Let typography and whitespace signal premium quality
- Keep pricing scannable: strong name column, muted description, bold price
- Use forest + mint as the only chromatic story
- Reference Apple / Linear / Notion / Stripe / Raycast for spacing discipline and typographic hierarchy
- Maintain professional, friendly, trustworthy Indonesian copy tone

**Don't**
- Glassmorphism, cyberpunk, neon, purple gradients, blue SaaS palette
- Nested cards, centered-everything layouts, generic dashboard patterns
- Eyebrow labels on every section; numbered markers unless the sequence is the content
- Inter, gradient text, side-stripe callouts, heavy shadows
- Oversaturate backgrounds or add decorative motion that delays reading

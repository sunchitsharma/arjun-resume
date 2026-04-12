# DESIGN.md

## 1. Visual Theme & Atmosphere

This website should feel like a polished personal vCard for a business development and account management professional. The design should project commercial credibility first, personality second. It should feel calm, recruiter-friendly, and premium without looking flashy or startup-generic.

The visual model is:
- a dark, stable profile rail on the left
- a bright, structured content canvas on the right
- soft panel framing rather than loud gradients
- strong hierarchy through typography, spacing, and surface contrast

The page should read as:
- professional
- credible
- selective
- commercial
- easy to scan in under 20 seconds

Avoid anything that feels:
- playful
- over-animated
- tech-bro glossy
- portfolio-dribbble-heavy
- visually noisy

## 2. Color Palette & Roles

Use the existing palette as the system of record.

### Base Colors

- `--bg: #eef1f4`
  Role: overall page background

- `--panel: #ffffff`
  Role: primary content cards and light surfaces

- `--panel-soft: #f8fafc`
  Role: secondary light fills and soft sections

- `--sidebar: #2a303a`
  Role: left rail base

- `--sidebar-soft: #353c48`
  Role: left rail gradient depth

- `--text: #1e2430`
  Role: primary text

- `--muted: #667085`
  Role: body copy, metadata, support text

### Accent Colors

- `--accent: #149f8a`
  Role: section tags, subtle success/forward-movement emphasis

- `--accent-soft: rgba(20, 159, 138, 0.12)`
  Role: low-intensity accent surfaces

- `--zomato: #c7483f`
  Role: strategic brand emphasis for Zomato only

- `--zomato-soft: rgba(199, 72, 63, 0.1)`
  Role: soft-tinted Zomato cards or pills

### Borders and Depth

- `--line: rgba(28, 36, 48, 0.08)`
  Role: light card borders

- `--line-strong: rgba(255, 255, 255, 0.08)`
  Role: sidebar borders on dark surfaces

Do not introduce additional accent colors unless there is a strong semantic reason.

## 3. Typography Rules

### Fonts

- Headings: `"Space Grotesk", sans-serif`
- Body: `"Manrope", sans-serif`

### Tone of Typography

Typography should do most of the design work. The site should feel clean because the type hierarchy is disciplined, not because of decorative flourishes.

### Hierarchy

- `h1`
  Use for name only. Large, compact, confident.
  Tight line height, high contrast, no long multi-line decorative headlines.

- `h2`
  Use for section headlines.
  These should read like recruiter summaries, not marketing slogans.

- `h3`
  Use for card titles, role names, and sub-sections.

- Body copy
  Keep between concise and moderately dense.
  Prefer clear business language over stylish phrasing.

- Metadata
  Dates, locations, labels, and support lines should stay smaller and quieter.

### Copy Style

Use first person in intro/profile sections when helpful.
Use direct achievement language in experience sections.
Avoid buzzword stacking.
Avoid generic growth jargon where a commercial term would be clearer.

## 4. Component Stylings

### Profile Rail

The left rail is a dark anchor panel. It should feel stable and slightly denser than the rest of the site.

Rules:
- dark gradient surface
- rounded corners
- subtle border
- no oversized imagery
- proof metrics should sit inside the rail as compact tiles
- actions should be immediately accessible without scrolling too far

### Proof Tiles

These are evidence blocks, not decorations.

Rules:
- concise number first
- short support line second
- high contrast on dark background
- consistent sizing and padding
- no more than 4 visible at once unless layout changes significantly

### Buttons

There are two button families only:

- Primary action
  Role: `Download Resume`
  Style: bright, high-contrast, rounded, centered label, visually heavier than any other action

- Icon actions
  Role: email, call, LinkedIn
  Style: circular, compact, dark-surface-compatible

Do not create multiple competing primary CTAs.

### Content Cards

Cards should feel soft, editorial, and contained.

Rules:
- white or near-white background
- subtle border
- soft shadow
- large radius
- enough internal padding to keep text well away from edges

### Section Wrappers

Major right-column sections should be visually consistent.
If one section is framed, peer sections should generally also be framed.
Avoid mixing "floating heading + cards" with "fully enclosed card section" unless there is a clear system-level reason.

### Experience Cards

These should feel like commercial case summaries.

Rules:
- title, company, meta row
- outcomes before responsibilities
- clean bullet rhythm
- subtle tints allowed for strategically important roles

Use soft red tint only for Zomato-related cards or labels.
Do not overuse the Zomato accent outside brand emphasis.

## 5. Layout Principles

### Desktop Layout

Use a two-column vCard structure:
- left: sticky profile rail
- right: stacked content panels

The desktop rail should remain wide enough that the primary CTA and icon actions fit cleanly without awkward wrapping.

### Spacing System

Favor generous padding inside panels and restrained gaps between sections.

Use this spacing philosophy:
- small gaps for related controls
- medium gaps between cards inside one section
- larger gaps between major narrative sections

Text should never look like it is touching the edge of a panel.

### Reading Order

A recruiter should understand this profile in this order:
1. identity and role fit
2. strongest proof points
3. credibility anchors such as Zomato and revenue outcomes
4. experience details
5. resume download / contact

## 6. Depth & Elevation

Depth should be soft and quiet.

Use:
- subtle shadows for card lift
- slightly stronger depth on the left rail
- almost no dramatic hover effects

The current shadows are the reference:
- `--shadow: 0 28px 70px rgba(20, 28, 38, 0.12)`
- `--shadow-soft: 0 14px 28px rgba(20, 28, 38, 0.08)`

Avoid:
- harsh glows
- glassmorphism
- blur-heavy backgrounds
- neon effects

## 7. Do's and Don'ts

### Do

- prioritize credibility over novelty
- highlight hard commercial outcomes early
- keep Zomato emphasis soft but intentional
- make contact actions easy to find
- keep the site scannable on first load
- maintain one consistent panel language
- preserve the recruiter-first hierarchy

### Don't

- don’t turn the page into a flashy portfolio
- don’t introduce multiple visual metaphors
- don’t let section headings float without structure if peer sections are framed
- don’t over-accent everything important
- don’t use full-width mobile pills unless they are truly primary actions
- don’t let desktop spacing create avoidable dead space
- don’t use decorative images unless they clearly improve trust and layout

## 8. Responsive Behavior

Mobile should not be a scaled-down desktop clone. It should be a simpler, calmer version of the same system.

### Mobile Rules

- keep the dark profile rail first
- reduce visual density
- preserve the primary CTA
- keep icon actions compact
- use narrower padding only where panels already provide containment
- give naked headings and body text extra horizontal breathing room
- stack complex grids early
- avoid sticky/floating treatments that can interfere with scrolling

If something looks good on desktop but busy on mobile, simplify rather than shrink.

### Interaction Rules

- animations should be minimal
- scroll should feel natural and uninterrupted
- touch targets should remain easy to tap

## 9. Agent Prompt Guide

When editing this site, follow these rules:

- Preserve the two-column recruiter-focused vCard layout on desktop.
- Preserve the dark left rail and bright right content canvas.
- Use `Space Grotesk` for headings and `Manrope` for body text.
- Keep section framing consistent across the right column.
- Use soft teal for section accents and soft red only for Zomato emphasis.
- Prefer business-development and account-management language over vague growth jargon.
- Keep proof metrics compact, readable, and prominent.
- On mobile, simplify aggressively rather than compressing complex desktop compositions.

### Quick Prompt

Use this design system to build or revise a recruiter-friendly personal resume website for Arjun Verma. Keep the layout calm and premium, with a dark sticky profile rail, white content panels, restrained teal accents, soft red Zomato emphasis, strong typography, and compact high-signal proof tiles. Favor clarity, commercial credibility, and consistency over novelty.

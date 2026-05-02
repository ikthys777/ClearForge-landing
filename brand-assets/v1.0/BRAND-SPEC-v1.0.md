# ClearForge Brand Specification — v1.0

**Brand system locked:** May 2, 2026
**Wordmark locked:** May 1, 2026
**Owner:** ClearForge LLC (NC SOSID 3271798)
**Designed by:** Scotty (Addison Scott Aliff) + Claude

---

## What v1.0 is

The ClearForge v1.0 brand system is a coordinated set of four **foundation marks**, each with multiple **variants**, all built from a single locked 6-color palette.

The four foundation marks are:

| Mark | Purpose |
|---|---|
| **Wordmark** | Text-only ("ClearForge" with hammer-in-O detail). Use when pairing with other graphics or where the type alone needs to carry the identity. |
| **Icon** | Anvil + flame + hammer + "CLEARFORGE" text. Single-color terracotta. Use as a transparent emblem on any surface. |
| **Logo** | Framed stamp version of the Icon. Self-contained card with terracotta border + warm-dark interior + layered two-tone mark. Use when the brand needs a deliberate, framed presentation. |
| **Icon Mark** *(planned)* | Anvil + flame only, no text. For favicons, embroidery, very small uses where text becomes illegible. |

Each foundation mark has up to five color variants: **Master**, **Light**, **Dark**, **TrueWhite**, **TrueBlack**. The Wordmark uses **MonoDark** and **MonoLight** in place of Light/Dark (a two-tone treatment that better suits the type-only design).

For current build status of all variants, see `ROADMAP.md`.

---

## Color palette

These six colors are the only colors that appear in any v1.0 brand asset. No other values are permitted.

| Token | Hex | RGB | Role |
|---|---|---|---|
| `--cf-terracotta` | `#C66A4F` | 198, 106, 79 | Signal / brand accent. Primary CTA, accent, "FORGE" word, flame. |
| `--cf-warm-dark` | `#3D3A36` | 61, 58, 54 | Mid-dark. "CLEAR" word, primary type on light backgrounds, frame interiors. |
| `--cf-deep-dark` | `#1A1714` | 26, 23, 20 | Deepest accent. Underlines, hammer, anvil, contrast elements. |
| `--cf-cream` | `#F3F0EB` | 243, 240, 235 | Default light surface. Use for paper, page backgrounds, "Light" surface contexts. |
| `--cf-slate` | `#1F2128` | 31, 33, 40 | Dark surface. Use for "Dark" surface contexts. |
| `--cf-taupe` | `#A89F92` | 168, 159, 146 | Light-on-dark accent. Subtle contrast in dark-mode marks. |

Legacy display names from earlier brand documentation: warm-dark was previously called "Charcoal", deep-dark was previously called "Near-black". The functional token names above are now canonical.

### Approved off-whites for cream substitutes

| Hex | Use |
|---|---|
| `#FFFFFF` | Print contexts where cream isn't reproducible (uncoated paper, no spot color budget) |
| `#FAF8F4` | Subtle warmth on screens that don't render cream cleanly |

### Forbidden

- Any color outside the locked six (and the two cream substitutes).
- Pure black `#000000` in place of deep-dark `#1A1714` — except inside the **TrueBlack** variants where every color collapses to pure black by design.
- Pure white `#FFFFFF` in place of cream `#F3F0EB` — except inside the **TrueWhite** variants and the approved off-white substitutes above.
- Saturated red, brick red, or any non-terracotta orange in place of `#C66A4F`.
- Recoloring any element of any mark outside this palette.

---

## Variant system

Every foundation mark generates derivative variants by color transformation. The transformation logic is identical across marks (with the wordmark exception noted).

| Variant | Surface context | Terracotta becomes | Warm-dark becomes | Deep-dark becomes |
|---|---|---|---|---|
| **Master** | Anywhere — primary use | `#C66A4F` | `#3D3A36` | `#1A1714` |
| **Light** | Cream surfaces (`#F3F0EB`) | `#3D3A36` | `#3D3A36` | `#1A1714` |
| **Dark** | Slate surfaces (`#1F2128`) | `#F3F0EB` | `#F3F0EB` | `#A89F92` |
| **TrueWhite** | Single-ink output, dark surfaces | `#FFFFFF` | `#FFFFFF` | `#FFFFFF` |
| **TrueBlack** | Single-ink output, light surfaces | `#000000` | `#000000` | `#000000` |

**Notes:**
- **Light** is a single-color warm-dark mark. The brand accent collapses into the type color.
- **Dark** is a two-tone cream + taupe mark. Taupe replaces deep-dark for visual hierarchy on slate.
- **TrueWhite** and **TrueBlack** are single-ink versions for laser engraving, embroidery, fax, screen printing, stamps, or any context where multi-color isn't available.
- **Wordmark exception:** uses **MonoDark** (warm-dark + deep-dark) and **MonoLight** (cream + taupe) instead of Light/Dark. The wordmark's type-only design works better with a two-tone treatment than a single-color collapse.

---

## Typography

### Primary typeface

**Fraunces** (Google Fonts) — used in the wordmark and for major headings.

Weight scale:

| Weight | Use |
|---|---|
| SemiBold (600) | Wordmark, hero headings |
| Regular (400) | Body headings |
| Light (300) | Large display sizes only |

The wordmark uses Fraunces SemiBold at ~96pt with -2.5% letter-spacing in its native composition. All wordmark text was converted to outlines at lock time, so the SVG is font-independent.

### Secondary typeface

To be commissioned. Recommended pairing: a clean humanist sans-serif (Inter, Söhne, IBM Plex Sans, or similar) for body copy, UI elements, and forms.

---

## The Wordmark

### Master file

`ClearForge-Wordmark-v1.0-Master.svg` — single source of truth.
Native viewBox: 418 × 128 units.

### Visual elements

| Element | Description | Color |
|---|---|---|
| "Clear" | Fraunces SemiBold, ~96pt, letter-spacing -2.5% | warm-dark `#3D3A36` |
| "Forge" | Fraunces SemiBold, ~96pt, letter-spacing -2.5% | terracotta `#C66A4F` |
| Underline | Weighted line under the wordmark with a natural break at the descender of "g" | deep-dark `#1A1714` |
| Anvil | Traced silhouette under the "e" of Forge — top edge parallel with underline | deep-dark `#1A1714` |
| Hammer | Cross-peen blacksmith hammer placed inside the bowl of the "o" in Forge | deep-dark `#1A1714` |

### Available variants

| Variant | Status |
|---|---|
| Master | ✅ |
| MonoDark | ✅ (warm-dark + deep-dark) |
| MonoLight | ✅ (cream + taupe) |
| TrueWhite | ✅ |
| TrueBlack | ✅ |

The wordmark family is complete (5 of 5 variants).

### Minimum size

- Digital: 120px wide minimum (any smaller and the hammer-in-o detail is lost)
- Print: 1.0" / 25mm wide minimum

For favicon and very small uses, use the planned **Icon Mark** instead.

---

## The Icon

### Master file

`ClearForge-Icon-v1.0-Master.svg` — single source of truth.

### Visual elements

The Icon is a **single-color terracotta mark** consisting of:

- **Flame** — stylized flame silhouette (the "forge fire")
- **Hammer** — cross-peen hammer, geometrically separate from the flame, exiting upper-right
- **Anvil** — classical anvil silhouette below the flame
- **"CLEAR"** — letter row across the upper portion
- **Underline** — horizontal bar between letter rows
- **"FORGE"** — letter row across the lower portion

The four letters with internal counters (O in FORGE, R in CLEAR, R in FORGE, A in CLEAR) use compound paths with `fill-rule="evenodd"` so their counters render as true transparent holes — not stacked dark fills. This means the Icon reads correctly against any surface.

### Why single-color

The Icon is intentionally monochromatic terracotta. This makes it:

- Surface-agnostic — works on cream, slate, photos, gradients
- Variant-trivial — TrueWhite and TrueBlack are clean color swaps with no overlap concerns
- Distinct from the Logo — the Logo carries the layered two-tone presentation

### Available variants

| Variant | Status |
|---|---|
| Master | ✅ |
| Light | 📋 |
| Dark | 📋 |
| TrueWhite | 📋 |
| TrueBlack | 📋 |

See ROADMAP.md for build progression.

---

## The Logo

The Logo is the **framed-stamp** counterpart to the Icon. Use it when the brand needs a deliberate, contained presentation — business cards, formal documents, framed signage, or any context where the icon needs visual containment.

### Master file

`ClearForge-Logo-v1.0-Master.svg` — single source of truth.

### Visual elements

| Element | Color |
|---|---|
| Outer rounded-rectangle border | terracotta `#C66A4F` |
| Interior card surface | warm-dark `#3D3A36` |
| Flame | terracotta `#C66A4F` |
| Hammer | deep-dark `#1A1714` |
| Anvil | deep-dark `#1A1714` |
| "CLEAR" letters | terracotta `#C66A4F` (with compound counters) |
| "FORGE" letters | deep-dark `#1A1714` (with compound counters) |
| Underline | warm-dark `#3D3A36` |

The interior elements (anvil, hammer, flame, letters) are layered onto the warm-dark card surface, creating visual depth absent from the flat Icon.

### The Transparent variant

`ClearForge-Logo-v1.0-Transparent.svg`

The warm-dark card surface is removed and the outer border is converted to a true 12px-thick **donut** (compound path with `fill-rule="evenodd"`). The interior elements retain their Master colors and float on whatever surface shows through the transparent center.

Use the Transparent variant when:

- You want the Logo's framed character but the surface behind it should remain visible
- You're placing the Logo on a cream or light surface that doesn't need a competing card
- You need the Logo to sit on a photograph or textured background

Use the standard Master when:

- The Logo needs to be self-contained
- The surface behind would clash with the interior elements
- The Logo is the dominant element in its context

### Touching elements (single-ink considerations)

In the Logo, several elements touch or overlap geometrically: hammer touches anvil, flame touches hammer, and the donut border can merge with letter elements when collapsed to a single ink. The TrueWhite and TrueBlack variants of the Logo will require **transparent gap separators** (negative-space outlines around touching elements) to remain readable. This is a Logo-specific concern — the Wordmark and Icon do not have this problem.

### Available variants

| Variant | Status |
|---|---|
| Master | ✅ |
| Transparent | ✅ |
| Light | 📋 |
| Dark | 📋 |
| TrueWhite | 📋 (requires gap-separator design) |
| TrueBlack | 📋 (requires gap-separator design) |

---

## The Icon Mark *(planned)*

A simplified mark consisting of **anvil + flame + hammer only**, with the "CLEARFORGE" text and underline removed. Designed for contexts where text becomes illegible:

- Favicons (16×16, 32×32)
- Apple Touch Icons
- Android maskable icons
- Embroidery, laser engraving
- Watermarks, single-color print at very small sizes

When the Icon Mark is built, it will follow the same Master/Light/Dark/TrueWhite/TrueBlack variant structure. Status: planned, not yet started. See ROADMAP.md.

---

## Spacing rules

### Clear space around any mark

Minimum clear space on all sides equals **the cap-height of the "C" in the wordmark** (or its scaled equivalent for non-wordmark marks).

Nothing may encroach on this margin — no other graphics, text, photo edges, or container borders.

### Minimum sizes

| Mark | Digital minimum | Print minimum |
|---|---|---|
| Wordmark | 120px wide | 1.0" / 25mm wide |
| Icon | 64px wide | 0.5" / 12.5mm wide |
| Logo | 96px wide | 0.75" / 19mm wide |
| Icon Mark | 16px wide (favicon size) | 0.25" / 6mm wide |

Below these sizes, switch to the next-simpler mark in the family.

---

## File naming convention

```
ClearForge-{FoundationMark}-v{Version}-{Variant}.svg
```

Examples:

```
ClearForge-Wordmark-v1.0-Master.svg
ClearForge-Wordmark-v1.0-MonoDark.svg
ClearForge-Icon-v1.0-Master.svg
ClearForge-Logo-v1.0-Transparent.svg
ClearForge-IconMark-v1.0-TrueBlack.svg
```

PNG and ICO derivatives use the same stem with appropriate extensions:

```
ClearForge-Wordmark-v1.0-Master-2x.png
ClearForge-IconMark-v1.0-Master.ico
```

---

## Recovery and provenance

### Canonical home

This repository (`ikthys777/ClearForge-landing`, `brand-assets/v1.0/`) is the canonical home for all v1.0 brand assets. The SVG masters in this folder are the recoverable source. They are font-independent (text converted to outlines), self-contained, and require no external services to render.

### Figma source files

| File | Figma key | Purpose |
|---|---|---|
| Wordmark Lockups | `8clj1ZsKDtZs2boxPKlcWr` | Wordmark master + variants frames |
| Icon Vectorization workspace | `zxNW1wln3d2juTmGNF13Hm` | Icon vectorization scratch / planning |

If a Figma file is lost, the SVG masters in this repo are sufficient to rebuild from. Open in Figma, Illustrator, or Inkscape as editable layered assets.

### Backup strategy

- **Primary:** This GitHub repository (you are here)
- **Secondary:** Mirrored to Precision (`~/ClearForge/brand-vault/v1.0/`) and Drive (ClearForge workspace folder)
- **Tertiary:** External drive backup once per quarter

### Provenance

The v1.0 brand system was designed and locked through extended iterative sessions between Scotty (the human eye, final composition, and brand judgment) and Claude (structural assembly, contour tracing, color logic, and Figma plugin work).

Key technical components:

- **Anvil silhouette:** traced from a clean reference image into a 268-point SVG path using Python `skimage` contour detection
- **Hammer silhouette:** traced from a reference image using the same pipeline, 228 points
- **Wordmark type:** Fraunces SemiBold with character-range coloring applied via Figma Plugin API, then converted to outlines
- **Letter counter cutouts:** four letters across Icon and Logo (O/R/R/A) use compound paths with `fill-rule="evenodd"` so counters render as true transparent holes
- **Logo Transparent donut:** outer rounded-rectangle path is a compound path with a 12px-inset inner cutout, producing a real border with transparent center
- **Final placement, polish, and brand judgment:** done collaboratively, with Scotty as final authority on every visual decision

---

## What's planned (not yet built)

See `ROADMAP.md` for current variant status. Top-line outstanding work:

- **Icon Light/Dark/TrueWhite/TrueBlack** (4 variants)
- **Logo Light/Dark/TrueWhite/TrueBlack** (4 variants — TrueWhite/TrueBlack require gap-separator design)
- **Icon Mark Master + 4 variants** (5 SVGs total — new geometry, derived from Icon)
- **Icon Squared + Logo Squared** (10 SVGs — new geometry, square aspect ratio for app icons / avatars)
- **Downstream artifacts** — favicon.ico, Apple Touch Icon, Android maskable, OG share card, PNG export sizes

---

*ClearForge LLC — Brand Specification v1.0 — Confidential*

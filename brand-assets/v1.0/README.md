# ClearForge Brand Vault — v1.0

This is the locked, canonical home for the ClearForge brand asset system.

**Brand system locked:** May 2, 2026
**System version:** v1.0

---

## What's in here

```
brand-assets/v1.0/
├── BRAND-SPEC-v1.0.md                       ← brand rules, palette, typography, logic
├── README.md                                 ← this file (entry point)
├── ROADMAP.md                                ← variant tracking + build status
│
├── ClearForge-Wordmark-v1.0-Master.svg      ← wordmark family (5/5 complete)
├── ClearForge-Wordmark-v1.0-MonoDark.svg
├── ClearForge-Wordmark-v1.0-MonoLight.svg
├── ClearForge-Wordmark-v1.0-TrueWhite.svg
├── ClearForge-Wordmark-v1.0-TrueBlack.svg
│
├── ClearForge-Icon-v1.0-Master.svg          ← icon family (1/5 complete)
│
├── ClearForge-Logo-v1.0-Master.svg          ← logo family (2/6 complete)
└── ClearForge-Logo-v1.0-Transparent.svg
```

For the full planned variant matrix and current build state of every asset, see `ROADMAP.md`.

For the brand rules, palette, typography, and design logic, see `BRAND-SPEC-v1.0.md`.

---

## Quick start — which file do I use?

**Need the brand on a website?** Use the SVG master that fits the context:

| Context | File |
|---|---|
| Marketing page hero, header navigation | `ClearForge-Wordmark-v1.0-Master.svg` |
| Footer brand mark, "about us" section | `ClearForge-Icon-v1.0-Master.svg` |
| Business card, formal document, framed signage | `ClearForge-Logo-v1.0-Master.svg` |
| Brand mark on a photo or textured surface | `ClearForge-Logo-v1.0-Transparent.svg` |
| Brand mark on cream/light page | Master variants render fine on cream |
| Brand mark on dark/slate page | Use a Mono or Dark variant where available |

**Need it for a PDF or Word doc?** Use the SVG master — they render perfectly in modern Office and PDF tools. PNG exports at 2x or 4x resolution can be generated from any master when needed.

**Need a favicon or very small mark?** The Icon Mark variant (anvil + flame only, no text) is planned but not yet built. For now, the Icon Master at small sizes is the closest available — accept that the "CLEARFORGE" text will become illegible below ~64px wide.

**Need single-ink output (laser, embroidery, fax)?** Use the TrueWhite or TrueBlack variants where available. For the Wordmark, both are committed. For Icon and Logo, see ROADMAP.md.

---

## What you should NOT do

1. **Don't edit these files in place.** They are locked at v1.0. If you need a new variant, generate a new file from the master — don't overwrite the canonical originals. Significant changes warrant a v1.1 (or v2.0) bump documented separately.

2. **Don't delete the master SVGs.** Even if you have PNG exports for everything you currently need, the SVGs are the only files you can rebuild from without quality loss. They are font-independent and self-contained.

3. **Don't recolor outside the locked palette.** Six colors (terracotta, warm-dark, deep-dark, cream, slate, taupe) plus the two approved off-white substitutes. See `BRAND-SPEC-v1.0.md` for exact hex values.

4. **Don't use the wordmark below its minimum size** (120px wide on screens, 1.0"/25mm in print). The hammer-in-o detail disappears and the asset loses its character. Switch to a smaller mark or accept the loss.

5. **Don't use a different mark when the right one exists.** Wordmark, Icon, Logo, and Icon Mark each have a clear use case. Don't substitute the Logo when the Icon is what's needed, or pad the Icon with frames when the Logo would do.

---

## Backup strategy

This repository is the **primary** canonical home. Recommended layered backup:

| Tier | Location |
|---|---|
| Primary | This GitHub repository (`ikthys777/ClearForge-landing`) |
| Secondary | Precision mirror at `~/ClearForge/brand-vault/v1.0/` |
| Tertiary | Google Drive — ClearForge workspace folder |
| Quarterly | External drive snapshot |

Each SVG is under 20KB. There is zero excuse to lose them.

---

## How to use the SVGs in code

### HTML / web

```html
<!-- Inline as image (simplest) -->
<img src="brand-assets/v1.0/ClearForge-Wordmark-v1.0-Master.svg"
     alt="ClearForge"
     width="240">

<!-- Or embed inline for full color/style control + accessibility -->
<svg viewBox="0 0 418 128" width="240" aria-label="ClearForge">
  <!-- paste contents of master SVG here -->
</svg>
```

### React (Next.js, Vite, etc.)

```jsx
import Wordmark from './brand-assets/v1.0/ClearForge-Wordmark-v1.0-Master.svg';

<img src={Wordmark} alt="ClearForge" />

// Or for SVGR-style imports where supported:
import { ReactComponent as Wordmark } from './...Master.svg';
<Wordmark width={240} />
```

### CSS background

```css
.brand-logo {
  background-image: url('/brand-assets/v1.0/ClearForge-Wordmark-v1.0-Master.svg');
  background-repeat: no-repeat;
  background-size: contain;
  width: 240px;
  height: 73px; /* maintains 418:128 aspect ratio */
}
```

### Color tokens (CSS custom properties)

Drop this anywhere in your stylesheet to make the brand palette available throughout your app:

```css
:root {
  --cf-terracotta: #C66A4F;
  --cf-warm-dark:  #3D3A36;
  --cf-deep-dark:  #1A1714;
  --cf-cream:      #F3F0EB;
  --cf-slate:      #1F2128;
  --cf-taupe:      #A89F92;
}
```

A standalone `tokens.json` and CSS snippet file are planned — see ROADMAP.md.

---

## What if the Figma source is lost?

The master SVGs in this folder are **fully self-contained** and are the canonical recoverable source. They have no external dependencies — text was converted to outlines at lock time, no external fonts, no external images, no external services.

To rebuild from an SVG:

- **Figma** — drag and drop the SVG onto a canvas; it imports as editable layers
- **Illustrator** — File → Open → select the SVG
- **Inkscape** (free, open-source) — File → Open → select the SVG

You can then re-export, rebuild a Figma master component, or modify if needed.

The Figma source files (`8clj1ZsKDtZs2boxPKlcWr` for Wordmark Lockups, `zxNW1wln3d2juTmGNF13Hm` for Icon Vectorization workspace) are referenced in `BRAND-SPEC-v1.0.md` for completeness, but are not required for recovery.

---

## Provenance

This brand system was designed and locked through extended iterative sessions between Scotty (Addison Scott Aliff — the human eye, final composition, and brand judgment) and Claude (structural assembly, contour tracing, color logic, and Figma plugin work).

See `BRAND-SPEC-v1.0.md` "Recovery and provenance" section for full technical detail.

---

## Versioning

Future variants and additions will be added under their respective foundation marks at the same version number, until a deliberate decision is made to bump the system version (v1.1 for additive changes, v2.0 for breaking changes to existing locked masters).

The lock applies to the masters and their established variants. Adding new variants (e.g., the planned Icon Mark family, or downstream PNG/ICO derivatives) does not constitute a version bump.

---

*Brand vault v1.0 — Take care of it.*

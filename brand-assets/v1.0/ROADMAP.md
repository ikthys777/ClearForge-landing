# ClearForge Brand Assets v1.0 — Variant Roadmap

This file tracks every brand asset variant in the v1.0 system. It is the
durable source of truth — kept in the repo so it survives any conversation
context loss.

## Locked Palette (v1.0)

```
FOREGROUND
  --cf-terracotta   #C66A4F   Signal / brand accent
  --cf-warm-dark    #3D3A36   Mid-dark / type
  --cf-deep-dark    #1A1714   Deepest accent

SURFACE
  --cf-cream        #F3F0EB   Light surface
  --cf-slate        #1F2128   Dark surface

MID-TONE
  --cf-taupe        #A89F92   Light-on-dark accent
```

These six values are the only colors that appear in any brand asset.

---

## Asset Status Matrix

Legend:
- ✅ Complete and committed to repo
- 🔧 In progress
- 📋 Planned, not yet started

### Wordmark (text only)

| Variant | Status | File |
|---|---|---|
| Master | ✅ | ClearForge-Wordmark-v1.0-Master.svg |
| MonoDark | ✅ | ClearForge-Wordmark-v1.0-MonoDark.svg |
| MonoLight | ✅ | ClearForge-Wordmark-v1.0-MonoLight.svg |
| TrueWhite | ✅ | ClearForge-Wordmark-v1.0-TrueWhite.svg |
| TrueBlack | ✅ | ClearForge-Wordmark-v1.0-TrueBlack.svg |

### Icon (graphic + text, transparent)

| Variant | Status | File |
|---|---|---|
| Master | ✅ | ClearForge-Icon-v1.0-Master.svg |
| MonoLight | ✅ | ClearForge-Icon-v1.0-MonoLight.svg |
| MonoDark | ✅ | ClearForge-Icon-v1.0-MonoDark.svg |
| TrueWhite | ✅ | ClearForge-Icon-v1.0-TrueWhite.svg |
| TrueBlack | ✅ | ClearForge-Icon-v1.0-TrueBlack.svg |

### Icon Squared (graphic + text, square aspect)

| Variant | Status | File |
|---|---|---|
| Master | 📋 | ClearForge-IconSquared-v1.0-Master.svg |
| Light | 📋 | ClearForge-IconSquared-v1.0-Light.svg |
| Dark | 📋 | ClearForge-IconSquared-v1.0-Dark.svg |
| TrueWhite | 📋 | ClearForge-IconSquared-v1.0-TrueWhite.svg |
| TrueBlack | 📋 | ClearForge-IconSquared-v1.0-TrueBlack.svg |

### Logo (graphic + text, framed stamp)

| Variant | Status | File |
|---|---|---|
| Master | ✅ | ClearForge-Logo-v1.0-Master.svg |
| Transparent | ✅ | ClearForge-Logo-v1.0-Transparent.svg |
| MonoLight | ✅ | ClearForge-Logo-v1.0-MonoLight.svg |
| MonoDark | ✅ | ClearForge-Logo-v1.0-MonoDark.svg |
| TrueWhite | ✅ | ClearForge-Logo-v1.0-TrueWhite.svg |
| TrueBlack | ✅ | ClearForge-Logo-v1.0-TrueBlack.svg |

### Logo Squared (graphic + text, square aspect)

| Variant | Status | File |
|---|---|---|
| Master | 📋 | ClearForge-LogoSquared-v1.0-Master.svg |
| Light | 📋 | ClearForge-LogoSquared-v1.0-Light.svg |
| Dark | 📋 | ClearForge-LogoSquared-v1.0-Dark.svg |
| TrueWhite | 📋 | ClearForge-LogoSquared-v1.0-TrueWhite.svg |
| TrueBlack | 📋 | ClearForge-LogoSquared-v1.0-TrueBlack.svg |

### Icon Mark (anvil + flame only, no text — favicon-grade)

| Variant | Status | File |
|---|---|---|
| Master | ✅ | ClearForge-IconMark-v1.0-Master.svg |
| MonoLight | ✅ | ClearForge-IconMark-v1.0-MonoLight.svg |
| MonoDark | ✅ | ClearForge-IconMark-v1.0-MonoDark.svg |
| TrueWhite | ✅ | ClearForge-IconMark-v1.0-TrueWhite.svg |
| TrueBlack | ✅ | ClearForge-IconMark-v1.0-TrueBlack.svg |

---

## Variant Color Logic

Every foundation mark generates 4 derivative variants by color transformation:

| Variant | Terracotta | Warm-dark | Deep-dark |
|---|---|---|---|
| **Master** | `#C66A4F` | `#3D3A36` | `#1A1714` |
| **Light** (for cream surfaces) | `#3D3A36` (warm-dark) | `#3D3A36` | `#1A1714` |
| **Dark** (for slate surfaces) | `#F3F0EB` (cream) | `#F3F0EB` | `#A89F92` (taupe) |
| **TrueWhite** | `#FFFFFF` | `#FFFFFF` | `#FFFFFF` |
| **TrueBlack** | `#000000` | `#000000` | `#000000` |

Notes:
- **Light** = single-color warm-dark mark. Renders cleanly on cream.
- **Dark** = cream-and-taupe two-tone mark. Renders cleanly on slate.
- **TrueWhite/TrueBlack** = single-ink versions for laser engraving, embroidery,
  fax, single-color print, stamps, etc.
- **Wordmark** has only Master + MonoDark + MonoLight + TrueWhite + TrueBlack
  (the warm two-tone Mono variants ARE its Light/Dark equivalents).

---

## Generated Artifacts (post-SVG)

Once all SVGs are locked, generate downstream artifacts:

| Artifact | Status | Source |
|---|---|---|
| favicon.ico (multi-res 16/32/48) | 📋 | from IconMark Master |
| Apple Touch Icon (180×180 PNG) | 📋 | from IconMark Master with safe zone |
| Android Maskable Icon (512×512 PNG) | 📋 | from IconMark Master with safe zone |
| OG share card (1200×630 PNG) | 📋 | from Logo Master |
| Wordmark PNGs (sizes TBD) | 📋 | from Wordmark Master |
| tokens.json / CSS custom-property snippet | 📋 | from locked palette |

---

## Total Asset Count (v1.0)

- 5 Wordmark SVGs
- 5 Icon SVGs
- 5 Icon Squared SVGs
- 6 Logo SVGs (extra Transparent variant)
- 5 Logo Squared SVGs
- 5 Icon Mark SVGs

**Total: 31 SVG files** + downstream PNGs and derivative artifacts.

Currently committed: **21 of 31 SVGs** (Wordmark family complete (5),
Icon Master + MonoLight + MonoDark + TrueWhite + TrueBlack (5/5),
Logo Master + Transparent (2/6),
IconMark family complete (5/5)).

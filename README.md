# ClearForge-landing

Marketing landing page for **ClearForge LLC** — a North Carolina software and digital services company.

## About

This is the public-facing landing page deployed to `clearforge.dev`. It's a single static HTML file with inline CSS and no JavaScript dependencies — built for fast loading, mobile-first display, and zero maintenance overhead.

## Stack

- **Hosting:** GitHub Pages (custom domain via Cloudflare DNS)
- **DNS:** Cloudflare (clearforge.dev)
- **Source:** Single-file HTML with inline CSS + tiny inline JS, no build step

## Local development

Open `index.html` in any browser. There is no build process.

```bash
# To preview locally with a quick server (optional)
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## Deployment

Deployed automatically via GitHub Pages on push to `main`. No build command, no output directory — GitHub Pages serves the repo root as static content. Custom domain configured via the `CNAME` file (`www.clearforge.dev`).

## Status

Active and live at [clearforge.dev](https://clearforge.dev).

This landing page is intentionally minimal during the early build phase. A more complete site will replace it as products approach launch.

## Contact

team@clearforge.dev

---

© 2026 ClearForge LLC

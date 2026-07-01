# mehrabsattar.com

Personal portfolio & résumé site for **Sayed Mehrab Sattar** — Fractional CMO / COO.
Plain static HTML/CSS/JS. No framework, no build step, no backend — designed to be
served directly by **GitHub Pages**.

## Structure

```
.
├── index.html                 # Single-page site (hero, about, expertise, work grid, testimonials, contact)
├── 404.html                   # Custom not-found page
├── CNAME                       # Custom domain for GitHub Pages (mehrabsattar.com)
├── .nojekyll                   # Serve files as-is (skip Jekyll processing)
├── robots.txt / sitemap.xml    # SEO
├── assets/
│   ├── css/style.css           # All styling + color themes (see "Colors" below)
│   ├── js/main.js              # Mobile nav, sticky header, scroll reveal
│   ├── img/                    # Case-study charts (from the portfolio deck)
│   └── Sayed-Mehrab-Sattar-CV.pdf
└── projects/                   # One HTML page per case study (10 total)
```

## Editing

- **Text / content** lives directly in the HTML files — open and edit.
- **Colors, fonts, spacing** are CSS custom properties at the top of `assets/css/style.css`.
- The site is fully hand-authored static HTML; there is nothing to compile or install.

### Colors

The site ships with two duotone themes. **Palette 2 (deep navy `#012641` + magenta
`#EE005A`) is active.** To switch to **Palette 1 (light blue `#A4D8FF` + charcoal
`#35393C`)**, open `assets/css/style.css`, comment out the primary `:root {…}` block,
and uncomment the `ALTERNATE PALETTE` block just below it. Nothing else changes.

### Fonts

Headings use **Space Grotesk**; body uses **Inter** — both loaded from Google Fonts.

## Deploying to GitHub Pages

1. Create an **empty** repository on GitHub (e.g. `mehrabsattar.com` or `portfolio`).
2. From this folder, add the remote and push (commands printed by the setup / see below).
3. In the repo: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main** · Folder: **/ (root)** → Save
4. Still under **Settings → Pages → Custom domain**, confirm `mehrabsattar.com`
   (the `CNAME` file already sets this). Enable **Enforce HTTPS** once the cert is issued.
5. Point DNS at GitHub Pages at your registrar:
   - Four `A` records for the apex `mehrabsattar.com` →
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` → `<your-username>.github.io`

DNS can take up to ~24h to propagate; the site is usually live within minutes on the
`*.github.io` URL while the custom domain resolves.

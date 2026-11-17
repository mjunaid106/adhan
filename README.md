# Adhan: Prayer Times — product page

Public page for **Adhan: Prayer Times**, an Android prayer-time app by ejaad.

Live at **https://adhan.ejaad.co.uk/**

## Stack

Plain static HTML/CSS — no build step.

| Path | Purpose |
| --- | --- |
| `index.html` | The whole page |
| `assets/css/styles.css` | Design tokens, layout, responsive rules |
| `assets/img/` | Brand mark and Open Graph image |
| `CNAME` | Custom domain for GitHub Pages |
| `robots.txt`, `sitemap.xml` | Crawler hints |
| `.nojekyll` | Serve files as-is |

## Content rules

This page follows the product brief, not the internal spec. Do not change copy without checking it
against that brief:

- The app is **Android only**. Title is exactly **Adhan: Prayer Times**.
- Never use “offline” as a name, title or badge. Say **“works without a connection”** only as a fact
  about features.
- Never claim “fully offline”, “100% offline”, “no internet permission” or “never uses the network”.
  `INTERNET` exists for Google Cast on the user's own Wi-Fi.
- Do not claim accuracy, authority, worldwide mosque coverage, “every speaker”, a price, or a Google
  Play listing.
- The bundled mosque data covers **Great Britain and Pakistan**, as of **November 2026**.
- The OpenStreetMap and audio attributions are licence obligations. Keep them visible.

## Deploy

This repo is its own GitHub Pages site, separate from `mjunaid106/ejaad`, so the subdomain can serve
a different page.

```bash
git add .
git commit -m "Update Adhan page"
git push
```

Pages deploys from `main`, repo root.

## DNS

At IONOS, one record:

```
CNAME   adhan   mjunaid106.github.io
```

No A records for the subdomain. Once DNS resolves, GitHub issues the TLS certificate and
**Enforce HTTPS** should stay enabled in **Settings → Pages**.

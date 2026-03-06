# Algolritmo Blog — Project Context

Football/soccer analytics blog at algolritmo.com. Bilingual (PT-BR default + EN). Built with Hugo, deployed via GitHub Pages + GitHub Actions.

## Repo
`https://github.com/rblay/algolritmo_blog`
Live at: `https://algolritmo.com/`

---

## Next Steps (priority order)

### ~~1. Download post images~~ — DONE ✓
All 176 images downloaded from WordPress CDN (`i0`/`i1`/`i2.wp.com`) and placed in each post's `images/` subfolder. All markdown references updated to local paths. Committed and deployed (commit `be89b71`).

### ~~2. Translate PT-only posts~~ — DONE ✓
### ~~3. Featured images on homepage cards~~ — DONE ✓
### ~~4. Transfer domain algolritmo.com~~ — DONE ✓ (algolritmo.com registrar transfer to Cloudflare pending completion)
### ~~5. Archive WordPress + cancel hosting~~ — DONE ✓
### ~~6. Open Graph tags~~ — DONE ✓ (tags in `baseof.html`; og:image uses `.Resources.GetMatch` for correct page bundle URL)
### ~~7. Custom 404 page~~ — DONE ✓ (`layouts/404.html`; workflow copies `public/pt/404.html` to `public/404.html` for GitHub Pages)
### ~~8. Favicon~~ — DONE ✓

### 9. algolritmo.com.br → algolritmo.com redirect — DONE ✓
Expression-based Cloudflare redirect rule: `http.host eq "algolritmo.com.br"` → `concat("https://algolritmo.com", http.request.uri.path)`

### 10. Remove algolritmo.com from Hostgator — pending
Once Cloudflare registrar transfer completes (initiated 2026-03-04). Verify via `whois algolritmo.com | grep -i registrar`.

---

## Tech Stack
- **Hugo** — static site generator (`hugo.toml` config, not yaml)
- **No external theme** — all layouts are custom in `layouts/`
- **CSS** — `assets/css/main.css`, processed by Hugo Pipes
- **Deployment** — GitHub Actions on push to `main` only; feature branches are safe
- **Hugo version** — Extended v0.155.3 (Extended required for CSS processing)

## Key Config
- PT-BR is the default language; EN is secondary
- `markup.goldmark.renderer.unsafe = true` — allows raw HTML in markdown
- Main brand color: `#3ea526` (green)

## Content Structure
```
content/
├── about/
│   ├── index.pt.md
│   └── index.en.md
└── posts/
    └── post-slug/
        ├── index.pt.md    ← always present
        ├── index.en.md    ← optional
        └── images/        ← all post images live here
            └── image.png  ← referenced in markdown as ![](images/image.png)
```

## Post Frontmatter
```yaml
---
title: "Post Title"
date: 2026-02-18
draft: false
---
```

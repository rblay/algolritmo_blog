# Algolritmo Blog — Project Context

Football/soccer analytics blog at algolritmo.com. Bilingual (PT-BR default + EN). Built with Hugo, deployed via GitHub Pages + GitHub Actions.

## Repo
`https://github.com/rblay/algolritmo_blog`
Live at: `https://rblay.github.io/algolritmo_blog/` (temporary until domain transfer)

---

## Next Steps (priority order)

### 1. Download post images — BLOCKING (do before cancelling WordPress)
All migrated posts reference images hosted at `i0.wp.com/algolritmo.com/wp-content/uploads/...`.
These will break when WordPress hosting is cancelled.

**Fix:** Download each image, place it in the post's own folder (page bundle), and update the markdown `![](url)` references to use the local filename instead.

### 2. Translate PT-only posts
These posts exist only in Portuguese and need English versions (`index.en.md`):
- `quem-vai-ganhar-copa-do-mundo`
- `guia-bolao-copa-do-mundo`
- `where-brazilian-teams-have-ball`
- `striker-finishing-profile-2019`
- `best-goalkeepers-2018-brazilian-league`

### 3. Featured images on homepage cards
Cards on the homepage currently show no image. To add them:
- Add `featured_image: image.png` to post frontmatter
- Update `layouts/index.html` and `layouts/_default/list.html` to render it

### 4. Transfer domain algolritmo.com
- Add CNAME record pointing to `rblay.github.io`
- Set custom domain in GitHub: Settings → Pages → Custom domain
- Update `baseURL` in `hugo.toml` to `https://algolritmo.com/`

### 5. Archive WordPress + cancel hosting
Only after step 1 (post images) is done.

### 6. Open Graph tags (nice-to-have)
Add `og:title`, `og:description`, `og:image` to `layouts/partials/header.html` for proper link previews when sharing posts on social media.

### 7. Custom 404 page (nice-to-have)
Create `layouts/404.html`.

### 8. Favicon (nice-to-have)
Replace the placeholder `static/images/favicon.png` with one derived from the logo.

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
        └── image.png      ← images live alongside the post (page bundle)
```

## Post Frontmatter
```yaml
---
title: "Post Title"
date: 2026-02-18
draft: false
---
```

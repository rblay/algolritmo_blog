# Algolritmo Blog

Football analytics blog at [algolritmo.com](https://algolritmo.com). Built with [Hugo](https://gohugo.io), deployed via GitHub Pages.

---

## Writing a new post

Posts live in `content/posts/`. Each post is a folder containing one markdown file per language.

**1. Create the post folder and file(s)**

```
content/posts/my-post-slug/
├── index.pt.md   ← Portuguese (always required)
└── index.en.md   ← English (optional)
```

**2. Add frontmatter at the top of each file**

```yaml
---
title: "My Post Title"
date: 2026-02-18
draft: false
---

Post content starts here...
```

- `draft: true` hides the post from the built site (useful while writing)
- The slug is the folder name, not the title

**3. Adding images**

Place images in the post folder itself (page bundle):

```
content/posts/my-post-slug/
├── index.pt.md
├── index.en.md
└── my-chart.png
```

Reference them in markdown as:

```markdown
![Alt text](my-chart.png)
```

---

## Adding a translation to an existing post

If a post only has `index.pt.md` and you want to add English:

1. Create `index.en.md` in the same folder
2. Add the frontmatter with the English title and the same `date`
3. Write the translated content below

Hugo automatically links files in the same folder as translations of each other — no extra config needed.

---

## Testing locally

Start the dev server:

```bash
hugo server
```

Open [http://localhost:1313](http://localhost:1313). The page hot-reloads on every file save.

To also preview draft posts:

```bash
hugo server -D
```

To stop the server: `Ctrl+C`.

---

## Deploying

### Via main branch (automatic)

Any push to `main` triggers a deploy automatically. The typical workflow:

```bash
# Write your post, then:
git add .
git commit -m "Add post: my-post-slug"
git push origin main
```

The site is live ~1 minute after the push. Watch progress at:
`https://github.com/rblay/algolritmo_blog/actions`

### Via feature branch (manual merge)

The workflow **only triggers on pushes to `main`**, so a feature branch push does not deploy anything. To use a branch workflow:

```bash
git checkout -b new-post/my-post-slug
# write your post
git add . && git commit -m "Add post: my-post-slug"
git push origin new-post/my-post-slug
# open a PR on GitHub and merge into main → deploy triggers automatically
```

### Manual trigger

You can also trigger a deploy from the GitHub UI without a new commit:
`Actions → Deploy Hugo site to Pages → Run workflow`

---

## How the deployment workflow works

The workflow is defined in `.github/workflows/hugo.yml`. It runs on GitHub's servers (Ubuntu) and does the following on every push to `main`:

1. **Installs Hugo Extended** (v0.155.3) — the Extended version is required for CSS processing via Hugo Pipes
2. **Checks out the repo**
3. **Configures GitHub Pages** — detects the Pages base URL automatically
4. **Builds the site** with `hugo --gc --minify --baseURL <pages-url>`
   - `--gc` cleans up unused cache files
   - `--minify` compresses HTML/CSS/JS for production
   - `TZ: America/Sao_Paulo` ensures dates render in Brazilian time
5. **Uploads** the `public/` output folder as a Pages artifact
6. **Deploys** the artifact to GitHub Pages

### One-time setup required

In the GitHub repo: **Settings → Pages → Source → GitHub Actions**. This was already done — no further setup needed.

---

## Project structure

```
algolritmo_blog/
├── .github/workflows/hugo.yml   # Deployment workflow
├── assets/css/main.css          # All site styles
├── content/
│   ├── about/                   # About page (index.pt.md + index.en.md)
│   └── posts/                   # One folder per post
├── i18n/
│   ├── pt.toml                  # Portuguese UI strings
│   └── en.toml                  # English UI strings
├── layouts/
│   ├── _default/                # Base, list, and single templates
│   ├── partials/                # Header, hero, footer
│   └── index.html               # Homepage
├── static/images/               # Logo, hero image, favicon
└── hugo.toml                    # Site config (languages, menus, etc.)
```

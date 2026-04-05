# Personal Website — seerier.github.io

Hugo-based academic portfolio for Gaoxiang Zhao. Built on **Hugo Blox Builder (Academic CV template)** with Tailwind CSS v4, deployed to GitHub Pages.

## Stack

| Component       | Detail                                          |
|----------------|-------------------------------------------------|
| Framework      | Hugo 0.150.1 (extended)                          |
| Theme          | Hugo Blox Builder (`blox-tailwind`, `blox-plugin-netlify`) |
| CSS            | Tailwind CSS v4 via `@tailwindcss/cli`           |
| JS             | Preact (from theme)                              |
| Search         | Pagefind (static, built post-Hugo)               |
| Package mgr    | pnpm v10.14                                      |
| Deploy         | GitHub Actions → GitHub Pages                    |
| Base URL       | https://seerier.github.io                        |

## Commands

```bash
pnpm install          # Install deps (required before first build)
pnpm dev              # Dev server with hot reload
pnpm build            # Production build (hugo --minify)
```

## Project Layout

```
config/_default/
  hugo.yaml         — Core Hugo config (title, baseURL, taxonomies, image processing)
  params.yaml       — Theme params (appearance, SEO, navbar, footer, analytics)
  menus.yaml        — Navigation menu items
  languages.yaml    — Language config (English only, Chinese commented out)
  module.yaml       — Hugo module imports and mounts

content/
  _index.md         — Homepage: landing page with block sections
  authors/admin/    — Profile (bio, avatar, education, skills, social links)
  projects/         — Project showcase (each subfolder = one project card)
  publications/     — Academic papers (conference-paper/, journal-article/, preprint/)
  blog/             — Blog posts by category
  experience.md     — Experience page (resume blocks)

layouts/
  partials/hooks/head-end/  — Custom <head> injections (GitHub buttons script)

static/uploads/     — Downloadable files (resume PDF)
assets/media/       — Site images (favicon, avatar, SVGs)

.github/workflows/
  deploy.yml                — Build + deploy to GitHub Pages
  import-publications.yml   — BibTeX → Markdown publication import
```

## Content Editing Guide

- **Profile:** `content/authors/admin/_index.md` — name, bio, avatar, education, skills, social links
- **Homepage sections:** `content/_index.md` — ordered block list (biography, research, experience, projects collection)
- **Add project:** New folder in `content/projects/` with `index.md` (title, tags, description, links) + `featured.jpg`
- **Add publication:** New folder in `content/publications/<type>/` or import via BibTeX workflow
- **Navigation:** `config/_default/menus.yaml` — uncomment items to show Papers, Talks, etc.
- **Site appearance:** `config/_default/params.yaml` — color scheme (currently "indigo"), theme mode (currently "system")
- **Resume PDF:** Replace `static/uploads/GaoxiangZhao-resume.pdf`

## Important Conventions

- The theme is module-based (Go modules in `go.mod`). Do NOT copy theme files manually — override via Hugo's lookup order by placing files in `layouts/`.
- Tailwind CSS is compiled at build time. `writeStats: true` in hugo.yaml is required for Tailwind's purge.
- Pagefind search index is generated AFTER Hugo build — it runs as a separate step in the deploy workflow.
- The site uses Hugo Blox shortcodes: `{{< chart >}}`, `{{< embed >}}`, `{{< table >}}`, `{{< button >}}` and Mermaid diagrams.
- Content images should use Hugo's page bundles (image in same folder as `index.md`), not `/static/`.

## Do NOT

- Modify files in `public/` or `resources/` — these are generated
- Edit Go module files (`go.mod`, `go.sum`) directly — use `hugo mod` commands
- Add raw HTML to content files when a shortcode exists for the purpose
- Change `baseURL` without also updating the GitHub Pages config

# Marginalia

A personal site for scattered commentary. Public but without ambition.

## Stack

- Astro (static output, zero client JS except theme toggle)
- GitHub Pages via Actions (`.github/workflows/deploy.yml`)
- No frameworks, no dependencies beyond Astro + RSS plugin

## Project structure

- `src/content/posts/` — Markdown posts (the only content type)
- `src/content.config.ts` — Collection schema
- `src/layouts/Base.astro` — Shared layout, all global CSS
- `src/pages/index.astro` — Homepage: intro blurb + post list
- `src/pages/posts/[id].astro` — Post template
- `src/pages/rss.xml.ts` — RSS feed

## Writing a post

Create a `.md` file in `src/content/posts/` with this frontmatter:

```yaml
---
title: Post title here
date: YYYY-MM-DD
tags: [optional, list]
---
```

`description` is also available but not currently rendered anywhere.

## Design decisions

- All CSS lives in `Base.astro` — no separate stylesheets
- No contact info by design

## Post content

All post content is written by the author. Do not offer to draft, write, or
outline posts. When asked to help revise post prose, suggest edits in chat —
don't modify the .md files directly. Code and config files are fair game as
usual.

## Commands

- `npm run dev` — local dev server
- `npx astro dev --host` — dev server exposed to LAN (use npx; PowerShell mangles `--` passthrough with `npm run`)
- `npm run build` — production build to `dist/`

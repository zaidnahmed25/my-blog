# my-blog

A personal tech blog built with [Astro](https://astro.build).

## Commands

| Command           | Action                                  |
| ----------------- | --------------------------------------- |
| `npm install`     | Install dependencies                    |
| `npm run dev`     | Start the dev server at `localhost:4321` |
| `npm run build`   | Build the production site to `./dist/`  |
| `npm run preview` | Preview the build locally               |

## Writing a post

Add a Markdown file to `src/content/blog/`. The filename becomes the URL
(`my-post.md` → `/blog/my-post/`).

```yaml
---
title: "My Post"
description: "One-line summary"
pubDate: 2026-10-09
updatedDate: 2026-10-12 # optional
tags: ["astro"]         # optional
draft: false            # optional; drafts are excluded from the site and RSS
---
```

Site name, description, and author live in `src/consts.ts`. The site domain
is set in `astro.config.mjs` (`site`).

---
title: "Markdown Showcase"
description: "A quick tour of the Markdown features this blog supports."
pubDate: 2026-10-10
tags: ["meta", "markdown"]
draft: true
---

This post shows how common Markdown elements render on this blog. Use it as a reference when writing.

## Text

You can use **bold**, *italic*, `inline code`, and [links](https://astro.build).

> Blockquotes look like this. They're good for callouts or quoting someone.

## Lists

1. Ordered item one
2. Ordered item two
   - Nested unordered item
   - Another one

## Code

```ts
interface Post {
  title: string;
  pubDate: Date;
}

function sortPosts(posts: Post[]): Post[] {
  return [...posts].sort((a, b) => b.pubDate.valueOf() - a.pubDate.valueOf());
}
```

```bash
npm run dev
```

## Tables

| Command           | Action                         |
| ----------------- | ------------------------------ |
| `npm run dev`     | Start the local dev server     |
| `npm run build`   | Build the site to `./dist/`    |
| `npm run preview` | Preview the production build   |

---

That's it!

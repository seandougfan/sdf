# sdf.tech

Sean Fanning’s personal website. Astro, TypeScript, and Markdown.

## Local preview

```sh
npm install
npm run dev
```

Open the Local URL printed by Astro (usually http://127.0.0.1:4321). Edits update automatically.

## Build

```sh
npm run build
npm run preview
```

## Writing

Add a `.md` file under `src/pages/thoughts/`:

```md
---
layout: ../../layouts/Post.astro
title: Your post title
date: '2026-10-15'
description: A short summary.
---

Your writing here.
```

The Thoughts index lists posts automatically. The original HTML/CSS and images remain in the repository for reference. No production hosting changes have been made.

## Publishing

GitHub Actions builds Astro and deploys `dist/` to GitHub Pages on each push to `master`. The custom domain remains `sdf.tech`. The homepage is a single page; `/thoughts/` and Markdown article routes remain available for expanding the archive.

## Updating questions

Edit `src/data/questions.json`. Each entry has a `topic` and `question`; the homepage renders them as a semantic bullet list.

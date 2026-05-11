# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

The source of **pretenst.com** — a Jekyll site about tensegrity (push-and-pull structures), deployed via GitHub Pages from the `master` branch. `CNAME` pins the custom domain. No CI workflows; GH Pages builds automatically on push.

The site has three coexisting things in the same repo:

1. **Jekyll site** — top-level `*.md` pages, `_posts/`, `_layouts/`, `_includes/`. Driven by `_config.yml` (theme `jekyll-theme-midnight`, plugin `jekyll-feed`).
2. **Pre-built apps shipped as static assets:**
   - `/app/` — React + TypeScript + Rust/WASM design tool (built from the upstream `tensegrity-lab` repo).
   - `/lab/` — Rust + WGPU + WASM physics sandbox (~5.2 MB WASM).
   These are **build artifacts checked into the repo**. Do not try to rebuild them here — they have no source in this repo. To update them, regenerate from the upstream project and copy the dist output in.
3. **`/fluxe/`** — a hand-coded static HTML/CSS mockup of a new design direction. Active redesign in progress. The plan for migrating the Jekyll content into this design lives at `/Users/fluxe/.claude/plans/i-have-included-a-abundant-sky.md` (clarifying questions still open as of the last conversation).

## Commands

```sh
bundle install                 # first-time / after Gemfile change
bundle exec jekyll serve       # local dev at http://localhost:4000 with live reload
bundle exec jekyll build       # static build to _site/ (gitignored)
```

Ruby version is pinned in `.ruby-version`. The `github-pages` gem controls Jekyll / plugin versions to match what GH Pages itself runs.

## Layout architecture (the non-obvious bit)

There is exactly **one layout**: `_layouts/default.html`. It overrides the midnight theme's default layout. Two things to know about it:

- **Navigation is hard-coded as HTML** inside the layout, not driven by `_data/` or front matter. Every link (Home, Code, Lab, App, Physical, Video Podcast) lives directly in `_layouts/default.html`. Editing the nav means editing that file.
- **Every page renders a footer listing of all posts** via a Liquid loop over `site.categories.construction` at the bottom of the layout. Posts are categorized via `categories: construction` in their front matter — that's the only categorization mechanism in use.

`_includes/head-custom.html` exists but is empty (placeholder hook for the midnight theme's custom head injection).

## Content conventions

- **Pages** are markdown at the repo root with YAML front matter (no `layout:` key — they get `default` automatically). Examples: `index.md`, `process.md`, `tenscript.md`.
- **Posts** live in `_posts/YYYY-MM-DD-slug.md` with front matter including `title`, `description`, `date`, and `categories: construction`. Drop the `construction` category and the post will not appear in the per-page footer listing.
- **Drafts** in `_drafts/` are excluded from builds by default; serve with `--drafts` to preview.
- **Images** live under `/images/`, mostly organized by post date (`/images/2020-06/`, etc.). The directory is **large (~341 MB, 500+ files)** — avoid bulk operations like `find` over the whole tree without a constraint, and don't `git add -A` blindly.
- **No collections, no `_data/`, no custom plugins** beyond `jekyll-feed`.

## Tone of the site

The current site reads as a technical-poetic manifesto for open-source tensegrity — mixes engineering, philosophy, mathematical detail (golden ratio, eigenvalues), and build-log narrative. References Snelson, Fuller, Flemons. Useful context when editing copy: terse marketing voice is not the house style.

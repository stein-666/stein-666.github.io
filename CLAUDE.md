# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-based academic portfolio website for Tongcheng Fang, built on the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template (a fork of Minimal Mistakes). It is deployed via GitHub Pages at https://stein-666.github.io/.

## Development Commands

### Local Development (Ruby/Bundler)

```bash
bundle install                                    # Install dependencies
bundle exec jekyll serve -l -H localhost          # Serve with live reload at localhost:4000
```

### Local Development (Docker)

```bash
docker compose up    # Serve at http://localhost:4000
```

The Docker setup uses `_config.yml` + `_config_docker.yml` (which sets an empty `baseurl`).

### JavaScript Assets

```bash
npm install          # Install JS dependencies
npm run uglify       # Minify JS files
npm run build:js     # Build JS assets
npm run watch:js     # Watch and rebuild JS on changes
```

## Architecture

### Content Collections

Jekyll collections define the main content types. Each has its own `_<collection>/` directory and corresponding archive page in `_pages/`:

- `_publications/` — Academic papers (frontmatter: `title`, `date`, `venue`, `paperurl`, `citation`, `excerpt`)
- `_talks/` — Conference presentations (frontmatter: `title`, `date`, `location`, `venue`, `type`)
- `_posts/` — Blog posts (filename: `YYYY-MM-DD-title.md`)
- `_teaching/` — Course materials
- `_portfolio/` — Project showcases
- `_pages/` — Static pages (About, CV, Publications archive, etc.)

### Key Configuration

- `_config.yml` — Main Jekyll config: site title, author profile, social links, plugin settings, collection defaults
- `_data/navigation.yml` — Top navigation bar links
- `_data/cv.json` — CV data (auto-updated by `scripts/cv_markdown_to_json.py`)
- `_data/ui-text.yml` — Localization strings

### Layouts & Includes

- `_layouts/` — Page templates (`single.html`, `archive.html`, `cv-layout.html`, `talk.html`, `default.html`, `splash.html`)
- `_includes/` — Reusable components (header, footer, author profile sidebar, SEO tags, etc.)
- `_sass/` — SCSS stylesheets (Minimal Mistakes theme base)

### Bulk Content Generation

`markdown_generator/` contains Python/Jupyter tools for bulk-generating markdown from structured data:

- `publications.ipynb` / `publications.py` — Reads `publications.tsv` → writes to `_publications/`
- `talks.ipynb` / `talks.py` — Reads `talks.tsv` → writes to `_talks/`
- `OrcidToBib.ipynb` — Fetches bibliography from ORCID
- `PubsFromBib.ipynb` — Generates publication files from BibTeX

### Automated Workflows

`.github/workflows/scrape_talks.yml` runs `talkmap.ipynb` on push to generate a geolocation map of talks (uses geopy, pandas, beautifulsoup4).

## Typical Editing Tasks

- **Update bio / about page:** Edit `_pages/about.md`
- **Add a publication:** Create a new `.md` file in `_publications/` or run the bulk generator from a TSV
- **Add a talk:** Create a new `.md` file in `_talks/`
- **Update navigation:** Edit `_data/navigation.yml`
- **Update CV JSON:** Run `scripts/update_cv_json.sh` or `scripts/cv_markdown_to_json.py`
- **Add images:** Place in `images/`; reference as `/images/filename.jpg`
- **Add downloadable files (PDFs):** Place in `files/`

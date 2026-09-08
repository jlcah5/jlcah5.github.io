# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is Jordan Cahoon's personal academic website, hosted via GitHub Pages at `jlcah5.github.io`. It is a static site with no build system — changes are deployed by pushing to GitHub.

## Structure

- `index.html` — About Me page: bio and News section (`.news-item` list with date + header + description)
- `research.html` — Research page: list of `.paper-entry` rows, each with optional `.paper-thumb` image, `.paper-title`, `.paper-citation`, `.paper-desc`, and link buttons
- `index.css` — global styles shared by both pages; uses a local Maven Pro variable font (`MavenPro-VariableFont_wght.ttf`)
- `iaw/map.html` — standalone interactive Leaflet map for the "Imputation Around the World" project, reads from `iaw/map_clean.csv` via PapaParse
- `docs/` — PDF files (CV, project reports) linked from both pages
- `img/` — images used in research entries and the profile photo
- `CNAME` — sets the custom domain for GitHub Pages

## Conventions

- Colors: body/nav text `#555155`, accent/hover/bold `#7c800e`, button blue `#609EE0`
- Layout: Bootstrap `container-sm` capped at `900px` max-width; fixed top navbar with links: About | Research | CV
- **News items** (`index.html`): add a `.news-item` div containing a `.news-date` span and a content div with `<strong>` header and `<p>` description
- **Research entries** (`research.html`): add a `.paper-entry` div; include `<img class="paper-thumb">` only if an image is available; always include `.paper-title` (h5), `.paper-citation` (p), `.paper-desc` (p), and optional button links
- The map page is self-contained and does not share CSS with the main site

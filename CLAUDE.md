# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Is

A static HTML portfolio site for Juan Sebastián Peña Quintero, deployed to GitHub Pages at https://jspenaq.github.io. No build system, no dependencies — just HTML files with all CSS inline.

## Deployment

```bash
git add .
git commit -m "Update portfolio"
git push
# GitHub Pages auto-deploys in 1-2 minutes
```

There are no local preview commands. Open HTML files directly in a browser, or use any static file server (e.g. `python3 -m http.server`).

## File Structure

```
index.html        # Homepage: hero + 3-column featured projects grid + about
work.html         # All projects bento grid
work/             # Project detail pages (lolsapiens, docker-ai, pokecoach)
```

> **Note:** Project detail pages belong in the `work/` subdirectory. `index.html` links to `work/lolsapiens.html` etc. Currently `lolsapiens.html`, `docker-ai.html`, and `pokecoach.html` exist at the root — this is a bug; they should be moved to `work/`.

## Design System

All CSS is duplicated inline in each HTML file (no shared stylesheet). When making style changes, replicate them across all pages for consistency.

**CSS Variables (same in every file):**
```css
--black: #0a0a0a
--white: #f5f0e8   /* cream background */
--yellow: #f5e642  /* primary accent */
--red: #ff3b30
--green: #28c840
--blue: #007aff
--border: 2.5px solid #0a0a0a
--shadow: 4px 4px 0px #0a0a0a
--shadow-lg: 7px 7px 0px #0a0a0a
```

**Fonts:** Space Grotesk (body/headers) + Space Mono (monospace/labels) — loaded from Google Fonts.

**Style:** Neo-brutalist — bold borders, offset box shadows, high contrast, uppercase labels. Interactive elements shift `translate(-3px, -3px)` with enlarged shadow on hover.

**Mobile breakpoint:** `900px` — grids collapse to single column.

**Tag color classes:** `.tag-security` (red), `.tag-ai` (blue), `.tag-backend` (black), `.tag-frontend` (yellow), `.tag-oss` (green).

## Page Templates

### `index.html` / `work.html` (listing pages)
- Sticky black nav with yellow logo
- `.work-grid` — 3-column CSS grid, collapses to 1 column on mobile
- `.work-card` — each card: tags → title → description → evidence badge → meta links
- Footer with logo + nav links + copyright

### Project detail pages (in `work/`)
- Nav has `← Back` link instead of full nav links
- 7-section layout: Context, Role, Key Decisions, Tech Stack, Impact/Metrics, Lessons, Links
- Each section is a bordered block in a 2-column or full-width grid

## Adding a New Project

1. Copy `work/lolsapiens.html` → `work/yourproject.html`, update all 7 sections
2. Add a `.bento-card` to `work.html`
3. Optionally add a `.work-card` to the featured grid in `index.html`
4. Update nav back-link href to point to `../work.html`

## Key Links to Keep Updated

- Calendly: `https://calendly.com/jspenaq`
- Email: `jspenaq@unal.edu.co`
- LinkedIn: `/in/juan-sebastian-peña-quintero`
- GitHub: `https://github.com/jspenaq`

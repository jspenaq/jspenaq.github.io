# Repository Guidelines

## Project Structure & Module Organization
This repository is a static GitHub Pages portfolio with no build step.

- `index.html`: homepage and featured projects.
- `work.html`: full project listing.
- `docker-ai.html`, `lolsapiens.html`, `pokecoach.html`: project detail pages (currently at repo root).
- `README.md`: deployment and editing notes.
- `CLAUDE.md`: agent-specific implementation notes.

Keep links and shared UI patterns consistent across pages, since styles are inline per file (no shared CSS bundle).

## Build, Test, and Development Commands
There is no package manager, build tool, or CI test runner configured.

- `python3 -m http.server 8000`: run a local static server.
- `open http://localhost:8000` (macOS): preview locally.
- `git add . && git commit -m "feat: ..." && git push`: publish changes; GitHub Pages deploys from `main`.

## Coding Style & Naming Conventions
- Use semantic HTML and keep indentation consistent (2 spaces in markup/CSS blocks).
- Preserve the neo-brutalist design tokens and interaction patterns already used in pages.
- Prefer lowercase, hyphenated file names (for future pages, e.g., `work/my-project.html`).
- Reuse existing class naming patterns (`.work-card`, `.bento-card`, `.tag-*`) instead of introducing near-duplicates.

## Testing Guidelines
Automated tests are not set up. Validate changes manually before pushing:

- Check desktop and mobile layout (breakpoint around `900px`).
- Verify navigation links, project links, and external profile/contact URLs.
- Confirm no console errors in browser devtools.
- Confirm metadata (`<title>`, description, OG tags) after content edits.

## Commit & Pull Request Guidelines
Recent history mixes Conventional Commit style (`feat:`, `chore:`) with generic messages (`Updates`). Prefer clear, scoped commits:

- `feat: add new project card to work page`
- `fix: correct broken link in index hero`
- `chore: align shared nav styling across pages`

For pull requests, include:
- concise summary of user-facing changes,
- files touched,
- before/after screenshots for layout or style changes,
- linked issue/task when applicable.

## Security & Configuration Tips
- Never commit secrets or private tokens.
- Validate external links and contact data before release.
- Keep repository name and default branch settings compatible with GitHub Pages (`jspenaq.github.io`, `main`).

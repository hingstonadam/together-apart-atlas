# CLAUDE.md

@AGENTS.md

AGENTS.md (imported above) is the authority on the project brief, narrative, research workflow, page structure and image rules. This file adds working notes for Claude Code. If the two conflict, follow AGENTS.md and point out the conflict.

## What this repository is

A hand-written static website — no framework, no package manager, no build step. GitHub Pages serves it from `main` under the repository subpath `/together-apart-atlas/`.

| Path | Purpose |
| --- | --- |
| `index.html`, `home.css` | Home landing page |
| `atlas.css`, `atlas.js` | Shared styles and site behaviour |
| `research/index.html`, `atlas-research.js` | Research dashboard: chart, filters and entry list |
| `research.json` | Published snapshot of every active row in the 100 Points of Research Notion database |
| `research-tags.json` | Project Relevance and Design Strategy tags, keyed by stable Notion page ID |
| `exegesis/` | Contents page plus six chapter subpages; shared `layout.css` and `reader.js` |
| `about/`, `poster/`, `data-centre/` | Single pages |
| `assets/` | Published, optimised images, fonts and PDFs (`renders/`, `diagrams/`, `drawings/`, `fonts/`, `poster/` and so on) |
| `DESIGN.md`, `.impeccable/design.json` | Design tokens: colour, Montserrat type scale, spacing, components |
| `sitemap.xml` | Update it when you add or remove a page |

## Working rules

- **Relative paths only.** The site lives under a subpath, so links and asset URLs must be relative (`../atlas.css`, not `/atlas.css`). Scripts fetch data relative to the page (`fetch('../research.json')`).
- **Preview through a local server, not `file://`.** The research data is loaded with `fetch`, which fails from the file system. Serve the repository root, for example with `python -m http.server 8000`, then open `http://localhost:8000/`. Check the research dashboard, filters and chapter links after any change to navigation, data or paths.
- **Design tokens come from DESIGN.md.** Use its colours, type and spacing rather than inventing new values. Corners stay square.
- **Images:** publish only supplied or approved assets (see "Supplied images only" in AGENTS.md). Never generate, draw or source substitute imagery. Use the plain ivory placeholder while artwork is pending. PDF and WebP files are stored as binary (`.gitattributes`).
- **Research data:** never hand-edit entries to fill gaps. Missing values remain "Not recorded", "Not yet recorded" or "Unknown". Refresh `research.json` and `research-tags.json` together from Notion, matched by stable page ID.
- **Language:** Australian English and metric units in all visible text, code comments and commit messages.
- **Accessibility:** every interactive panel, chart slice and legend item must work from the keyboard and show a visible focus state.

## Git

- `main` is the published branch; pushing to it updates the live site. Confirm with Adam before pushing.
- Other remote branches (`impeccable/*`, `redesign/*`, `codex/*`, `archive/*`) are earlier experiments. Don't merge them unless Adam asks.
- Write commit messages as a short imperative sentence describing the visible change, matching the existing history (for example "Publish a dedicated page for the final review poster").

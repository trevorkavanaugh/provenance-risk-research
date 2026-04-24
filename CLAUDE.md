# Provenance Risk Research Website — Claude Code Instructions

> **Shared-session repo.** The **Website** session owns both this repo and `provenance-risk-advisory/` per the updated scope in `~/work/provenance/CLAUDE.md`.
> Handoffs: `HANDOFF_WEBSITE_*.md` in this directory.

## Overview

Static website for Provenance Risk Research Inc., a Delaware 501(c)(3) nonprofit research foundation (filed 2026-04-20). No build tools, no frameworks — pure HTML/CSS/JS served via GitHub Pages at provenanceriskresearch.org.

## Development

- Edit files directly. No build step, no bundler.
- Push to `master` deploys to GitHub Pages automatically.
- Test locally: `python3 -m http.server 8000` then open `http://localhost:8000`.

## Design System

Visual tokens are CSS custom properties in `css/styles.css`:
- Colors: `--forest` (#23432F), `--cream` (#F2ECDD), `--ink` (#1A1F1A) and derived shades
- Typography: Libre Caslon Text (serif, body + headings), IBM Plex Sans (nav + metadata) via Google Fonts
- Spacing: 8px base scale from `--space-1` through `--space-8`

Typography and palette are deliberately different from the PRA website (which uses Source Serif 4 + Inter, navy + gold) to reinforce the visual firewall between the two entities.

## Key Rules

1. **No frameworks.** Vanilla HTML/CSS/JS only. No React, no Tailwind, no build tools.
2. **PRA firewall - strict.** No shared footer or logos with PRA. No "sister organization" language. No cross-nav links to provenanceriskadvisory.com. Organic citation of PRR research from PRA's thought leadership is fine; reciprocal cross-promotion on this site is not.
3. **Accessibility first.** Semantic HTML, ARIA labels, skip links, keyboard navigation.
4. **Mobile-first responsive.** Flexbox/grid layouts with media queries.
5. **Performance matters.** No heavy JS libraries. Fonts load via Google Fonts CDN.
6. **No client data.** This is a public research foundation site.
7. **Honest claims only.** PRR is a new foundation (April 2026). Do not overclaim program maturity. Published work is published; planned work is labeled planned.

## Content Alignment

Mission and entity details must match:
- `~/work/provenance/prr-research/docs/` (source of truth for Certificate of Incorporation, 1023-EZ narrative, bylaws)
- Paper citations must match the authoritative manuscripts held by the Research session

Naming standard (locked):
- Inline / body: "Provenance Risk Research"
- Legal / formal / copyright / footer: "Provenance Risk Research Inc."
- No abbreviation yet. PRA is taken by Advisory; PRR/PRI shorthand deferred until the entity has recognition.

## Declaration of Interest Pattern

Every paper landing page carries a Declaration of Interest block disclosing that the principal researcher (Trevor Kavanaugh) also operates Provenance Risk Advisory LLC as a separate for-profit consulting firm under shared leadership, that research was conducted independently of any consulting engagement, and that no client of PRA influenced subject matter or findings. This mirrors the Declaration attached to JOR paper submissions and closes the ethics loop proactively.

## File Responsibilities

- `css/styles.css` — Complete design system. All styling lives here.
- `js/main.js` — Mobile nav toggle, active-link state. No analytics, no tracking.
- `papers/` — PDF downloads for published papers and whitepapers.
- `assets/` — Images and media.
- `archive/` — Historical artifacts: design previews, removed pages. Never delete, always archive.

# Provenance Risk Research — Website

Public website for Provenance Risk Research Inc., a 501(c)(3) research foundation studying third-party risk, software supply chain security, and operational resilience in financial services.

**Live:** [provenanceriskresearch.org](https://provenanceriskresearch.org)

## Tech Stack

- Static HTML5 / CSS3 / Vanilla JavaScript
- GitHub Pages hosting (CNAME configured)
- Google Fonts: Libre Caslon Text (serif, body + headings), IBM Plex Sans (nav + metadata)

## Pages

| File | Route | Purpose |
|------|-------|---------|
| `index.html` | `/` | Home — mission, three pillars (research / case studies / education), featured research, forthcoming |
| `research.html` | `/research` | Working papers and peer-reviewed research |
| `about.html` | `/about` | Mission, approach, Board of Directors, entity information |
| `contact.html` | `/contact` | Research / media / general correspondence routing |

## Structure

```
provenance-risk-research/
├── index.html
├── research.html
├── about.html
├── contact.html
├── CNAME              # provenanceriskresearch.org
├── css/styles.css     # Complete design system
├── js/main.js         # Mobile nav toggle, active-link state
├── assets/            # Images and media (currently empty)
├── papers/            # PDF downloads (currently empty)
└── archive/           # Historical artifacts (design previews, removed pages)
```

## Development

- Edit files directly. No build step, no bundler.
- Push to `master` deploys to GitHub Pages automatically.
- Test locally: `python3 -m http.server 8000` then open `http://localhost:8000`.

## Design System

Visual tokens are defined as CSS custom properties in `css/styles.css`:

- Colors: `--forest` (#23432F), `--cream` (#F2ECDD), `--ink` (#1A1F1A) and derived shades
- Typography: Libre Caslon Text (serif), IBM Plex Sans (sans-serif) via Google Fonts
- Spacing: 8px base scale from `--space-1` (8px) to `--space-8` (128px)

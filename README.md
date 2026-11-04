# Vishnu Kumar — e-Portfolio

Live: **https://its-vishnu-nitp.github.io/**

A fast, dependency-free static portfolio. No build step, no backend — pure
HTML + CSS + vanilla JS, hosted on GitHub Pages.

## Architecture

```
its-vishnu-nitp.github.io/
├── index.html        # semantic single-page content (7 sections)
├── css/
│   └── styles.css    # design system: tokens, glassmorphism, responsive grid
├── js/
│   └── main.js       # interactions (no frameworks, no libraries)
└── README.md         # this file
```

**Content layer (`index.html`)** — one semantic document, seven sections in
narrative order: Hero → About → Skills → Projects → Research → Coding
Profiles → Education → Contact. Section numbers (`01`–`07`) double as a
table of contents in the sticky nav.

**Presentation layer (`css/styles.css`)** — a token-driven design system
(`:root` variables for palette, radius, fonts). Dark theme with an
indigo → cyan → amber gradient identity, glassmorphic cards, CSS grid
layouts that collapse gracefully (3-col → 2-col → 1-col), and
`prefers-reduced-motion` support.

**Interaction layer (`js/main.js`)** — five small modules, zero dependencies:
1. canvas particle-network background, 2. hero typing effect,
3. IntersectionObserver scroll-reveals, 4. eased stat counters,
5. active-nav tracking + subtle 3D card tilt + mobile menu.

## Why this stack

- **Speed** — a single HTML file + one CSS + one JS file; loads in milliseconds.
- **Portability** — any static host works (GitHub Pages, Netlify, Vercel);
  nothing to install, nothing to break.
- **Maintainability** — content, style and behaviour are cleanly separated,
  so any section can be edited without touching the others.

## Local preview

```bash
cd its-vishnu-nitp.github.io
python3 -m http.server 8000   # then open http://localhost:8000
```

© 2026 Vishnu Kumar

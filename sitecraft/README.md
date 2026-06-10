# Sitecraft Marketing Site

A complete, single-file marketing website for Sitecraft — a website design service for local service businesses.

## Features

- **Apple/Tesla-inspired design** — Modern, clean aesthetic with smooth animations
- **Fully responsive** — Works perfectly on mobile, tablet, and desktop
- **Interactive demo** — Live scrollable preview of a sample client website (Reyes Plumbing)
- **Pricing configurator** — Real-time pricing with app option toggle ($450 base + $249 app)
- **Animated elements** — Scroll reveals, animated counters, hero parallax, magnetic CTAs
- **Accessible** — ARIA labels, semantic HTML, keyboard navigation, reduced-motion support
- **Single HTML file** — No dependencies, no build process — just one `index.html`

## What's Included

- **index.html** — Complete marketing site with embedded CSS and JavaScript
- **.github/workflows/static.yml** — GitHub Pages deployment workflow

## Getting Started

### Local Development

Simply open `index.html` in any modern browser. No server required.

For a better development experience, use a local server:

```bash
# Python 3
python -m http.server 8000

# Or Node.js with http-server
npx http-server
```

Then visit `http://localhost:8000/sitecraft/`

### GitHub Pages Deployment

1. Push to GitHub (on the `main` branch or your chosen branch)
2. Enable GitHub Pages in repo settings
3. Point to the `/sitecraft` folder as the source
4. The workflow will automatically deploy on every push

## Architecture

The entire site is a single HTML file with:

- **CSS Design System** — Custom properties for colors, spacing, typography, shadows
- **Vanilla JavaScript** — No framework dependencies
  - Scroll reveal with IntersectionObserver
  - Animated counters with RequestAnimationFrame
  - Pricing configurator with toggle state
  - FAQ accordion with ARIA accessibility
  - Magnetic button effect on CTAs
  - Mobile menu toggle
  - Desktop/phone demo toggle

## Customization

All styling is in a `<style>` block using CSS custom properties. Key variables:

- `--ink`: Dark background (#0A0A0C)
- `--paper`: Light background (#FFFFFF)
- `--accent`: Primary blue (#2563EB)
- `--maxw`: Max layout width (1180px)

The site uses:
- **Inter** and **Inter Tight** for typography
- **Fraunces** for sample client branding
- All from Google Fonts (preloaded)

## Performance

- **71 KB** uncompressed
- No external API calls or trackers
- Optimizes for Core Web Vitals
- Respects `prefers-reduced-motion` for accessibility

## Browser Support

Modern browsers (Chrome, Firefox, Safari, Edge). Uses:
- CSS Grid and Flexbox
- CSS custom properties
- IntersectionObserver API
- RequestAnimationFrame

## Files

```
sitecraft/
├── index.html                    # Complete marketing site
├── README.md                     # This file
└── .github/workflows/
    └── static.yml               # GitHub Pages deployment
```

## License

Design and code created for Sitecraft. All rights reserved.

## Demo Content

The site features a fictional plumbing company "Reyes Plumbing" as a sample client to demonstrate what a Sitecraft-built website includes. This is purely for demonstration purposes.

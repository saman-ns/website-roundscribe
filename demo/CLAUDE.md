# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static demo landing page for **RoundScribe** — an AI-powered nursing home rounding note and OHIP billing code suggestion tool by BeaverNets Technologies Inc. This is a presentation/demo artifact, not a production application.

## Development

No build system, package manager, or dependencies. Pure HTML5, CSS3, and vanilla JavaScript.

- **To develop**: Edit `index.html` and `styles.css` directly, refresh browser
- **To serve locally**: `python3 -m http.server` or any static file server
- No tests, linting, or CI pipeline

## Architecture

Single-page static site with three files:

- `index.html` — All page content and inline JavaScript (card expand/collapse logic)
- `styles.css` — All styling with CSS custom properties for theming
- `favicon.svg` — Site icon

### Page Sections

Hero → Interactive Demo (3 expandable patient cards with SOAP notes + OHIP codes) → Security & Compliance → Timeline/Roadmap → Footer

### Key Patterns

- **Theming**: CSS variables in `:root` (`--primary`, `--secondary`, `--success`, etc.)
- **Interactivity**: Vanilla JS click handlers using `data-patient` attributes to toggle `.active` class on patient cards
- **Responsive breakpoints**: 768px (tablet), 375px (mobile)
- **Typography**: Plus Jakarta Sans from Google Fonts
- **Layout**: Flexbox and CSS Grid with `.container` max-width wrapper

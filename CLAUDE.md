# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page portfolio website for an AI Engineer. Pure HTML/CSS/JavaScript with no build tooling, package manager, or frameworks beyond Tailwind CSS via CDN.

## Running Locally

Open `index.html` directly in a browser, or serve with any static HTTP server:
```
python -m http.server
```

There is no build step, no test suite, and no linter configured.

## Architecture

Everything lives in a single `index.html` file (~30KB):

- **Tailwind config** is inline in a `<script>` tag at the top, defining a custom dark theme (navy/slate/teal color palette, Inter font)
- **Layout** is a two-column design: fixed left sidebar (profile, nav, certs, social links) + scrollable right content area (About, Experience, Projects)
- **JavaScript** at the bottom handles: scroll-spy navigation highlighting, mouse-tracking spotlight effect, and smooth scrolling
- **External deps** are all CDN-loaded: Tailwind CSS, Font Awesome 6, Google Fonts (Inter)

## Key Conventions

- Responsive breakpoints use Tailwind's `lg:` prefix for the desktop two-column layout; mobile is single-column
- Color tokens: `navy-900` (background), `teal-300` (accent/highlights), `slate-300/400/100` (text hierarchy)
- Images go in the `images/` directory

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

BackCountry Bean Counter is a business website for a Vermont-based bookkeeping service. Built with Astro and Tailwind CSS, deployed on Netlify.

## Commands

```bash
npm run dev      # Start development server at localhost:4321
npm run build    # Build for production to ./dist
npm run preview  # Preview production build locally
```

## Architecture

- **Framework**: Astro (static site generation)
- **Styling**: Tailwind CSS v4 with custom theme colors (forest, gold, snow, bark)
- **Deployment**: Netlify (configured via netlify.toml)

### Project Structure

```
src/
├── layouts/Layout.astro    # Base layout with nav and footer
├── pages/
│   ├── index.astro         # Homepage with hero, about, services preview
│   ├── services.astro      # Service tiers (Trailhead, Ridgeline, Summit)
│   └── contact.astro       # Contact info and booking placeholder
├── styles/global.css       # Tailwind imports and custom theme
public/
└── logo.png                # Business logo
```

### Custom Colors (defined in global.css)

- `forest` / `forest-dark` / `forest-light` - Primary green colors
- `gold` - Accent/CTA color
- `snow` - Background white
- `bark` - Secondary brown

## Configuration Notes

- Email placeholder: `hello@backcountrybeancounter.com` (update when domain is set up)
- Calendly placeholder in contact page - add embed code when account is created
- Logo at `public/logo.png` (also in `images/` folder as source)

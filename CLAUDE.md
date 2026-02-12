# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static genealogy/cultural heritage website hosted on GitHub Pages documenting Amazigh (Berber) genetic lineage from Souss-Massa, Morocco. Combines genetic analysis (Y-DNA haplogroup E-PF2546, mtDNA H1-T16189C!), historical research on the Chtouka confederation, and cultural preservation.

**Live site:** https://aitmhend-dna.github.io

## Development

This is a **no-build static site** — plain HTML, CSS, and vanilla JS. No package manager, bundler, or framework.

- **Edit and preview directly** — open any `.html` file in a browser
- **Deployment** — automatic via GitHub Pages from main branch
- **External deps (CDN only):** Chart.js, Google Fonts (Inter, Space Grotesk, IBM Plex Mono)
- **Contact form:** Formspree (ID: myzbzgjn)

## Architecture

- `index.html`, `lineage.html`, `genetics.html`, `culture.html`, `contact.html` — the five site pages
- `css/styles.css` — single stylesheet (~3600 lines) with CSS custom properties defined in `:root`
- `img/` — image assets (heritage photos, genetic maps, pattern overlays)
- `docs/` — research notes and SEO documentation
- All JS is inline within HTML files (no separate JS modules)

Every page follows the same structure: `<header>` with gradient border → sticky `<nav>` → `<main id="main-content">` with card-based sections → `<footer>`. Each page includes full SEO markup (Open Graph, Twitter Cards, JSON-LD structured data, canonical URLs, geo-tags).

## Design System (Critical Rules)

The authoritative design reference is `.cursorrules` (472 lines) and `.github/copilot-instructions.md`. Key rules:

- **NEVER use blue colors** — removed for appearing "AI-generated." The palette is exclusively warm earth tones.
- **Color palette:** Terracotta `#CD7F32` (primary), Ochre `#CC8E35`, Clay `#D2691E`, Warm Sand `#E2A36B`, Burnt Sienna `#8B4513`, Deep Brown `#3E2723`
- **Gradient borders:** `linear-gradient(90deg, #CD7F32 0%, #CC8E35 50%, #D2691E 100%)`
- **Card backgrounds:** Subtle gradients at 3-6% opacity only
- **Border radius:** 3-8px max — no rounded bubbles
- **Typography:** Inter (body), Space Grotesk (headings), IBM Plex Mono (technical)
- **Touch targets:** Min 44px height for buttons/links
- **Responsive breakpoints:** Desktop >1024px, Tablet 768-1024px, Mobile <768px

## Content & Terminology

- Use **"Amazigh"** as primary term, "Berber" in parentheses for SEO context
- Haplogroup notation: "E-PF2546" (Y-DNA), "H1-T16189C!" (mtDNA)
- Date format with context: "~400 BCE (2,400 years before present)"
- Geographic: "Souss-Massa" (primary), "Souss Valley" (descriptive)
- Language reference: "Tachelhit" (the specific Amazigh language)
- Tone: Scholarly yet accessible, data-driven, culturally respectful

## SEO Checklist (for any page changes)

- Title tags: 40-50 characters
- Meta descriptions: 150-160 characters
- All images: descriptive alt text, explicit width/height, `loading="lazy"`
- Maintain JSON-LD schema markup (WebSite, Article, ScholarlyArticle, ContactPage)
- Update `sitemap.xml` lastmod dates when pages change

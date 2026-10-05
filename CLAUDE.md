# JCD.dev System Prompt

## Project Overview

Personal professional website for James Chang-Davidson. Jekyll on GitHub Pages, deployed at jcd.dev.

## Content Strategy

Content decisions, copy, and information architecture are managed in James's private content strategy doc (not in this repo).

Use it for approved copy, page structure, and content gaps. Do not invent or assume content — use what's documented there or ask James.

## Design System

Full design specs (colors, typography, spacing, components) live in the same private content doc, under "Design System"

Key reference:

- **Font:** Inter (Google Fonts, latin subset)
- **Primary color:** `#89CFF0` (baby blue) — used as background gradient in light mode
- **Dark mode:** `prefers-color-scheme: dark`, solid black background, white text
- **Max width:** 1024px
- **CSS approach:** Custom properties in a single stylesheet (see CSS variables block in the design system section)

## Technology

- **Framework:** Jekyll (GitHub Pages compatible)
- **Hosting:** GitHub Pages with custom domain (jcd.dev)
- **CSS:** Vanilla CSS with custom properties — no Tailwind, no Sass required for MVP
- **Icons:** SVG inline or a lightweight icon approach (no heavy icon library)
- **Images:** Optimized static assets in `/assets/images/`

## File Structure

    ├── _config.yml          # Jekyll config
    ├── _layouts/
    │   └── default.html     # Base layout
    ├── _includes/           # Reusable partials (head, footer, etc.)
    ├── assets/
    │   ├── css/
    │   │   └── style.css    # Single stylesheet with design tokens
    │   └── images/
    │       └── james.jpeg   # Headshot
    ├── index.html           # Homepage (MVP: hero only)
    ├── CNAME                # Custom domain config
    └── CLAUDE.md            # This file

## Working Style Preferences

- **Concise communication** — lead with the action, not the reasoning
- **Ask before assuming** — especially about content, copy, and design choices. Don't fabricate professional details.
- **Ship incrementally** — MVP first, iterate. Don't over-engineer.
- **Propose before executing** — for structural changes or new pages, outline the plan first
- **Commit often** — small, clear commits. Push to feature branches.

## Current Status

**Phase: MVP Launch** — Single-page hero site (name, tagline, one-liner, social links). No nav, no additional pages yet.

Next phase: Add professional proof highlights below hero, then build out Projects and About pages.

## Common Pitfalls

- Don't add pages or sections not yet approved in the content strategy
- Don't use frameworks/libraries beyond what's specified (no React, no Tailwind, no heavy JS)
- Don't modify copy without checking the content doc first
- Don't over-style — the design is intentionally clean and minimal
- Keep accessibility in mind (semantic HTML, contrast ratios, alt text)

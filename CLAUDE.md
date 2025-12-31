# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of health and wellbeing web applications, starting with a meditative breathing exercise guide.

## Architecture

### index.html (Breathing Exercise)
A self-contained breathing exercise web app using vanilla HTML/CSS/JavaScript. No build tools or dependencies.

**Structure:**
- CSS variables define the color palette (`--bg-deep`, `--accent-primary`, etc.)
- `exercises` object contains breathing patterns with phases (name, duration, scale)
- Animation uses `requestAnimationFrame` with sine easing for organic breathing feel
- State managed via module-level variables (`isRunning`, `currentPhaseIndex`, `cycleCount`)

**Design principles:**
- Minimalist, meditative interface with single focal point (breathing circle)
- Controls fade away during active sessions
- No countdown timers to avoid anxiety
- Dark warm tones with subtle gradient backgrounds

## Development

Open HTML files directly in a browser:
```bash
open index.html
```

No build process required.

## Deployment

Hosted on Vercel at **https://breathe-calm.vercel.app** (also aliased to breathe.e-studios.net).

Deploy via:
```bash
npx vercel --prod
```

**Note:** Vercel Authentication must be **disabled** in Project Settings → Deployment Protection for social media crawlers (Facebook, Twitter) to access the site for link previews.

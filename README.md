# MyStaticWebsite

A static personal portfolio redesigned with a product-showcase UI inspired by the pacing, boldness, and rounded visual language of the Nintendo Switch landing experience.

## What Changed

- Rebuilt the page into a polished product-style landing page instead of a basic section stack.
- Added a design-token system with CSS variables so colors, spacing, radius values, shadows, and motion are easy to change.
- Introduced lightweight JavaScript for reveal animations, active navigation state, and subtle pointer-based stage motion.
- Reused existing local images and videos as showcase assets, so the site looks richer without adding unnecessary dependencies.

## Project Structure

- `index.html` - semantic page structure and content sections
- `style.css` - design tokens, responsive layout, animation styles, and component styling
- `script.js` - reveal-on-scroll, nav highlighting, and hero tilt interaction
- `files/` - local media assets used across the hero and project showcase

## Design System

The site is driven by variables in the `:root` block in `style.css`.

### Key token groups

- Colors: `--color-bg`, `--color-surface`, `--color-text`, `--color-brand`, `--color-accent`
- Layout: `--site-max-width`, `--section-gap`, `--section-padding`
- Radius: `--radius-xs`, `--radius-sm`, `--radius-md`, `--radius-lg`, `--radius-pill`
- Motion: `--ease-standard`, `--ease-snappy`, `--duration-fast`, `--duration-base`, `--duration-slow`
- Shadows: `--shadow-card`, `--shadow-soft`

### Fast customization

If you want to retheme the site later, start here:

1. Change the brand colors in the `:root` block.
2. Adjust spacing and rounding tokens for a tighter or softer visual feel.
3. Swap assets in `files/` and update their references in `index.html`.

## Layout Overview

### `index.html`

- Sticky top navigation with a primary CTA
- Hero section with console-inspired visual stage
- About section with summary and process notes inside a rounded red showcase panel
- Capabilities section rebuilt as a Nintendo-style comparison card block
- Featured project showcase with screenshots and videos
- Contact section and large rounded red footer

### `style.css`

- Uses reusable component classes instead of one-off styling where possible
- Keeps animation values centralized with motion variables
- Includes responsive breakpoints for desktop, tablet, and mobile
- Includes `prefers-reduced-motion` support for accessibility
- Uses `.section-panel` and `.section-panel-red` for the big rounded showcase sections

### `script.js`

- Reveals `.reveal` elements when they enter the viewport
- Adds `.is-active` to the nav link matching the visible section
- Adds mild pointer tilt to the hero stage on larger screens

## Asset Notes

The redesign intentionally uses existing assets already in the repository:

- `files/hero.jpg` for the hero stage and one mini-project card
- `files/portfoliocms/*` as the main featured product
- `files/qr-generator/*` for the secondary showcase
- `files/data_toolkit/*` and `files/webdev/*` for supporting project cards
- `files/upi.jpeg` as a fallback supporting visual in the mini project rail

If you later add better thumbnails for `Dev Create` or `Track Fitness`, replace those image references in `index.html`.

## Recommended Image Direction

If you want the sections to feel even closer to the Nintendo reference, use these kinds of visuals:

- Hero: a clean portrait or product image with strong subject isolation and soft background blur
- About panel: abstract workspace shot, keyboard desk setup, or subtle gradient illustration
- Comparison cards: bright isolated product screenshots on light backgrounds
- Project showcase: clean UI screenshots with consistent crop ratios
- Footer: keep it mostly graphic and color-led instead of using busy images

## Maintenance Notes

- Keep new sections on the `.section-block` pattern for visual consistency.
- Prefer existing tokens before adding hard-coded colors or shadows.
- If you add new animated blocks, reuse `.reveal` and existing transition variables before creating new motion rules.
- The page is intentionally dependency-light: only HTML, CSS, and a small JavaScript file.

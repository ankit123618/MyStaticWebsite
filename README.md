# MyStaticWebsite

A static personal portfolio built with plain HTML and CSS.

The current design uses:

- a full-width red background theme
- white content sections and cards
- `Kalam` typography for a more artistic handwritten feel
- fixed top header navigation
- responsive layouts for desktop, tablet, and mobile
- soft motion, hover transitions, and floating background effects

## Files

- `index.html` - all page content, section structure, links, text, and media references
- `style.css` - theme variables, layout, responsive breakpoints, animation, and component styling
- `files/` - images and videos used in the portfolio

## Page Flow

The page is a single-page portfolio with anchor navigation.

Main flow in `index.html`:

1. Fixed header
2. Hero section
3. About section
4. Services section
5. Tools section
6. Projects section
7. Contact section
8. Footer

Navigation links in the header point to section IDs:

- `#about`
- `#services`
- `#tools`
- `#projects`
- `#contact`

## HTML Structure

High-level structure in `index.html`:

```html
<body>
  <div class="site-shell">
    <header class="site-header">...</header>
    <main id="top">
      <section class="hero">...</section>
      <section id="about" class="content-section">...</section>
      <section id="services" class="content-section">...</section>
      <section id="tools" class="content-section">...</section>
      <section id="projects" class="content-section">...</section>
      <section id="contact" class="content-section contact-section">...</section>
    </main>
    <footer class="site-footer">...</footer>
  </div>
</body>
```

## Important IDs and Classes

### Layout / Shell

- `.site-shell` - top-level wrapper for the whole page
- `.site-header` - fixed header bar at the top
- `.site-nav` - navigation links inside the header
- `.brand` and `.brand-text` - portfolio name/logo text
- `main#top` - main page area

### Hero

- `.hero` - full-width hero section
- `.hero-backdrop` - animated glow shape in hero background
- `.hero-copy` - left text column
- `.hero-actions` - hero buttons
- `.hero-metrics` - mini info/stat cards
- `.hero-spotlight` - right hero visual area
- `.portrait-card`, `.portrait-frame`, `.portrait-content` - portrait card block

### Shared Section Pattern

- `.content-section` - standard content section wrapper
- `.section-heading` - heading block used in each section
- `.section-label` - small label above headings

### About

- `#about` - About anchor target
- `.about-grid` - 2-column section layout
- `.about-panels` - info card grid
- `.info-panel` - individual About card

### Services

- `#services` - Services anchor target
- `.tile-grid` - services grid
- `.tile` - single service card

### Tools

- `#tools` - Tools anchor target
- `.chip-grid` - tools/skills grid
- `.chip` - single tool item

### Projects

- `#projects` - Projects anchor target
- `.projects` - projects grid
- `.project-link` - clickable project wrapper
- `.project-card` - single project card
- `.project-card-text` - text-only project card
- `.project-media` - media layout inside a project
- `.media-frame` - screenshot/video frame
- `.media-badge` - preview/demo badge
- `.project-body` - project text content
- `.project-type` - project category label

### Contact

- `#contact` - Contact anchor target
- `.contact-panel` - main contact block
- `.contact-copy` - contact intro text
- `.contact-links` - contact methods grid

### Footer

- `.site-footer` - footer wrapper
- `.footer-logo` - footer name
- `.footer-note` - footer description
- `.footer-bottom` - copyright line

## Styling System

All theme control starts in the `:root` block at the top of `style.css`.

Current variables:

```css
:root {
  --red-900: #78050c;
  --red-800: #930811;
  --red-700: #b60d17;
  --red-600: #cf1620;
  --red-500: #e12933;
  --red-400: #f15157;
  --white: #fffdfb;
  --white-soft: rgba(255, 253, 251, 0.84);
  --line: rgba(183, 18, 27, 0.16);
  --ink-red: #931018;
  --shadow: 0 24px 70px rgba(85, 0, 7, 0.2);
  --header-height: 120px;
  --max-content: 1240px;
}
```

## Where to Customize

### 1. Change Theme Colors

Edit the `:root` variables in `style.css`.

Main ones:

- `--red-900` to `--red-400` - red palette used across background, accents, and highlights
- `--white` - white used for cards, surfaces, and text contrast
- `--line` - border color for cards and boxes
- `--ink-red` - dark red text on white sections
- `--shadow` - global soft card shadow

If you want a different theme later:

- keep a dark base color
- keep a light surface color
- update the palette variables first
- then fine-tune section/card accents only if needed

### 2. Change Fonts

Font import is in the `<head>` of `index.html`.

Current font:

- `Kalam`

To change font:

1. Replace the Google Fonts import in `index.html`
2. Update `font-family` in `body`
3. Update any heading-specific `font-family` rules if needed

### 3. Change Header Style

Header styles are in `.site-header`, `.site-nav`, and `.brand-text` in `style.css`.

What to edit:

- `--header-height` in `:root`
- `.site-header` for background, padding, height, and shadow
- `.site-nav a` for link size, spacing, and hover effect
- `.brand-text` for portfolio name size and animation

### 4. Change Hero Content

Hero content is in the first `<section class="hero">` block in `index.html`.

Edit here:

- eyebrow text
- main heading
- summary paragraph
- hero buttons
- metric text
- portrait card text
- hero image path: `files/hero.jpg`

Hero styling is controlled by:

- `.hero`
- `.hero-backdrop`
- `.hero-copy`
- `.hero-actions`
- `.hero-metrics`
- `.portrait-card`

### 5. Change Section Content

Each major section is editable directly in `index.html`.

Common pattern:

```html
<section id="section-name" class="content-section">
  <div class="section-heading">
    <p class="section-label">Label</p>
    <h2>Main heading</h2>
  </div>
</section>
```

You can duplicate this pattern to add new sections.

If you add a new section:

1. give it a unique `id`
2. add a matching header link
3. reuse existing grid/card classes when possible

### 6. Change Project Cards

Projects are inside `#projects` in `index.html`.

To edit a project:

- change image path in `<img src="...">`
- change video path in `<source src="...">`
- update project type
- update heading and description

Useful project classes:

- `.project-card`
- `.project-card-text`
- `.project-media`
- `.media-frame`
- `.project-body`

### 7. Change Contact Info

Contact links are inside `.contact-links` in `index.html`.

Current examples:

- `mailto:`
- `tel:`
- GitHub URL
- LinkedIn URL

If contact text is long, wrapping is handled in:

- `.contact-links a`

### 8. Change Spacing and Width

Main layout width and spacing controls:

- `--max-content` - inner readable content width
- `--header-height` - top spacing reserved for fixed header
- `.hero`, `.content-section`, `.site-footer` padding values

If you want wider or tighter sections:

- increase/decrease `--max-content`
- adjust horizontal padding in `.hero` and `.content-section`

## Responsive Behavior

The layout is responsive through media queries in `style.css`.

Breakpoints currently used:

- base styles - desktop/default behavior
- `@media (max-width: 1100px)` - tablet/laptop adjustments
- `@media (max-width: 820px)` - stacked mobile/tablet layout
- `@media (max-width: 560px)` - smaller mobile screens

What changes responsively:

- header height
- header layout
- hero switches from 2-column to 1-column
- section grids collapse from multiple columns to one column
- buttons become full width on small screens
- contact cards and project cards stack vertically

## Animation and Motion

Animations are defined in `style.css`.

Current keyframes:

- `drift` - floating background glow movement
- `floatBlob` - hero background blob movement
- `floatCard` - portrait card floating effect
- `inkPulse` - brand text glow/pulse
- `riseIn` - hero content entrance motion

Main transition-heavy components:

- `.site-nav a`
- `.button`
- `.hero-metrics article`
- `.info-panel`
- `.tile`
- `.project-card`
- `.contact-links a`
- `.chip`

Reduced motion support exists with:

```css
@media (prefers-reduced-motion: reduce) { ... }
```

## Reusing the Template for Another Person

To adapt this site for someone else:

1. Update name in `.brand-text` and footer
2. Update hero heading and summary
3. Replace portrait image in `files/hero.jpg`
4. Edit About, Services, Tools, Projects, and Contact content
5. Update social/contact URLs
6. Change theme colors in `:root`
7. Replace project media in `files/`

## Maintenance Tips

- Prefer editing existing classes before creating many one-off styles
- Keep color changes inside `:root` when possible
- Reuse `.content-section`, `.section-heading`, `.tile`, `.chip`, and `.project-card`
- Keep IDs unique, because header navigation depends on them
- If adding a long email or link, check wrapping on laptop width as well as mobile

## Current Theme Summary

This design is intentionally:

- red-first
- white-surface based
- handwritten/artistic through `Kalam`
- animated but still readable
- full-width and modern
- lightweight with no framework dependency

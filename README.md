# MyStaticWebsite

A simple dark-themed personal website for showcasing skills, projects, and contact information.

## Project Structure

- `index.html` — main page content and sections
- `style.css` — site styling, responsive layout, and theme variables
- `images/` — image assets used for hero and project cards

## Style and Theme Documentation

This project uses a **mobile-first responsive design** with CSS variables defined at the top of `style.css`.

### Core theme variables

The main color variables are declared in `:root`:

- `--bg` — page background
- `--card` — card/background panels
- `--text` — primary text color
- `--muted` — subtitle/text-muted color
- `--accent` — panel or accent background colors
- `--footer` — footer background color
- `--primary-accent` — main highlight / hover color
- `--secondary-accent` — secondary highlight color
- `--red-accent` — red accent color used for name styling

### How to change the theme

1. Open `style.css`
2. Update the values in the `:root` block
3. Save and refresh the page

Example:

```css
:root {
  --bg: #121212;
  --card: #1b1b1f;
  --text: #f7f7f7;
  --muted: #b0b0b0;
  --accent: #24272d;
  --footer: #101625;
  --primary-accent: #40c4ff;
  --secondary-accent: #8be9fd;
  --red-accent: #ff3b3f;
}
```

### Styling guidelines

- Use `--bg` and `--card` for large background sections and cards.
- Use `--text` for headings and important labels.
- Use `--muted` for descriptive text, paragraphs, and subtle items.
- Use `--primary-accent` for hover states, links, and interactive UI highlights.
- Use `--secondary-accent` for subtle accent lines and secondary buttons.
- Use `--red-accent` for brand highlights, especially in the hero name styling.

## Responsive design notes

- The site starts with mobile-first layout.
- `@media (min-width: 640px)` and above adds tablet layout improvements.
- `@media (min-width: 768px)` refines spacing and card layout.
- `@media (min-width: 1024px)` enables desktop hero and grid layout.

## Footer customization

The footer uses a compact layout with the following sections:

- Brand / summary
- Navigation links
- Social/community links
- Contact information
- Copyright

To adjust footer spacing, update the `footer` padding properties in `style.css`.

## Updating content

- Edit `index.html` to change text, projects, links, or section order.
- For new cards, add another `.card` element inside the `projects` section.
- For new skills or tools, add another `.skill` block inside the correct section.

## Notes

This website is designed to be easy to customize by changing variables and content. For a future theme update, focus on the top `:root` variables and the footer/card accent values.

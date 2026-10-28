# Bloom Website

A responsive coffee and barista-course website built as a practical demonstration of **CUBE CSS**, reusable design tokens, fluid typography, and a component pattern library.

## Project purpose

The main purpose of this project is to show how CUBE CSS can provide a flexible way to organize CSS for a real website, alongside other common styling methodologies. CUBE CSS separates styles into four useful layers:

- **Composition** — reusable layout patterns such as `cluster`, `flow`, `grid`, `repel`, `sidebar`, and `wrapper`.
- **Utilities** — small, focused classes for applying specific styling, spacing, and accessibility helpers.
- **Blocks** — component-level styles for pieces such as buttons, cards, the hero, navigation, and footer.
- **Exceptions** — contextual variations handled where needed, often through data attributes or specific component modifiers.

This approach keeps layout concerns, reusable components, and one-off variations distinguishable. Compared with methodologies that primarily organize styles around component names or strict naming conventions, CUBE CSS emphasizes composable layouts and low-specificity global styles. The project also demonstrates how fluid typography can make the interface feel more polished and adaptive across screen sizes.

## What the project demonstrates

- **Design tokens:** Shared CSS custom properties for color, typography, spacing, font weights, and border radius live in `src/design-tokens/`. Fluid `clamp()`-based type and spacing scales help values adapt smoothly between viewport sizes.
- **Fluid typography:** Type sizes and spacing scale fluidly using `clamp()` and token-based design values so headings and body text respond naturally across devices without abrupt jumps in sizing.
- **Pattern library:** The `patterns/` directory contains standalone examples of reusable interface patterns, including buttons, cards, navigation, hero sections, and the footer. `patterns/patterns-library.html` links to the examples.
- **Responsive design:** The site is designed to work across screen sizes. Fluid design tokens, fluid typography, flexible layout compositions, responsive CSS, and appropriately scaled images help the layouts adapt from smaller screens to larger displays.
- **Reusable CSS architecture:** Global styles, compositions, component blocks, and utilities are organized separately under `src/css/` and brought together through `src/css/global.css`.
- **Accessible foundations:** The markup and styles include features such as image alternative text, focus-visible styling, and a hero skip link.

## Tech stack

- HTML
- CSS, including Tailwind CSS v4 utilities and theme integration
- Vite
- Bun lockfile (`bun.lock`)

## Getting started

Install the dependencies with Bun:

```bash
bun install
```

Start the local development server:

```bash
bun run dev
```

Build the site for production:

```bash
bun run build
```

Preview the production build locally:

```bash
bun run preview
```

## Project structure

```text
.
├── index.html                 # Main website page
├── patterns/                  # Standalone pattern examples and library index
├── public/                    # Public static assets
└── src/
    ├── css/
    │   ├── blocks/             # Component styles
    │   ├── compositions/       # Layout compositions
    │   ├── global/             # Reset and global styles
    │   ├── utilities/          # Utility styles
    │   └── global.css          # CSS entry point
    ├── design-tokens/          # Shared design values
    ├── fonts/                  # Local font files
    ├── icons/                  # SVG icons and brand assets
    ├── images/                 # Website imagery
    └── main.js                 # Imports the global stylesheet
```

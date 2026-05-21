# Level-2-Responsive-Layout

A responsive tech blog and photography gallery layout built with **CSS Grid** for structural organization and **CSS Flexbox** for component-level alignment. Adapts seamlessly across desktop (3 columns), tablet (2 columns), and mobile (1 column) without horizontal scrolling.

## Features

- **Blog Card Grid:** 7 article cards organized with CSS Grid. A featured card spans the full width with a horizontal image/text split on tablet and above.
- **Photography Gallery:** Masonry-inspired CSS Grid layout with `tall` items (row-span-2) and `wide` items (col-span-2). Hover overlays with gradient captions.
- **Sidebar:** Topic tags with Flexbox wrap, recent posts list, and newsletter subscription form. Sidebar moves to a second column at 1024px via CSS Grid.
- **Responsive Navigation:** Sticky nav bar with Flexbox-aligned links that collapse into a hamburger menu on mobile.
- **No Horizontal Scrolling:** Verified at 320px, 768px, 1024px, and 1440px viewports.

## Layout Strategy

| Technique  | Usage                                          |
| ---------- | ---------------------------------------------- |
| CSS Grid   | Page body (main + sidebar), blog card grid, gallery grid, featured card horizontal split |
| Flexbox    | Navigation alignment, card meta (author + read time), tag wrapping, sidebar stack, newsletter form |

### Breakpoints (Mobile-First)

| Viewport | Blog Grid | Gallery Grid | Page Body       |
| -------- | --------- | ------------ | --------------- |
| < 768px  | 1 column  | 1 column     | Single column   |
| 768px+   | 2 columns | 2 columns    | Single column   |
| 1024px+  | 3 columns | 3 columns    | Main + Sidebar  |

## Tech Stack

| Layer     | Technology                       |
| --------- | -------------------------------- |
| Structure | HTML5 (semantic, accessible)     |
| Styling   | CSS3 (Grid, Flexbox, custom properties, transitions) |
| Scripting | Vanilla JavaScript (mobile nav)  |
| Images    | Unsplash (lazy-loaded, responsive) |
| Fonts     | Inter (Google Fonts)             |
| Design    | Codveda brand palette            |

## File Structure

```
Level-2-Responsive-Layout/
  index.html                    Blog + gallery page
  styles/
    styles.css                  Grid/Flexbox layout system and component styles
  scripts/
    navigation.js               Mobile hamburger toggle
  README.md
```

## Live Deployment

| Environment | URL |
|---|---|
| Cloudflare Pages | https://codveda-blog.pages.dev |
| Custom Domain | https://codveda-blog.kristianhans.com |

Deployed via **GitHub auto-deploy**: every push to `main` triggers a new Cloudflare Pages build automatically.

## Getting Started

```bash
git clone https://github.com/KristianHans04/codveda-responsive-layout.git
cd codveda-responsive-layout
npx serve .
```

Cloudflare Pages project name: `codveda-blog`

## Accessibility

- Skip-to-content link for keyboard users.
- All images have descriptive `alt` text and explicit `width`/`height` attributes.
- `loading="lazy"` on below-the-fold images for performance.
- ARIA landmarks and labels on navigation and sidebar.
- Touch-friendly card targets sized above 44x44px.

## License

This project is part of the Codveda Web Development Internship program.

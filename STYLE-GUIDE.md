# documove Design System & Style Guide

> Clean, professional, minimal - inspired by modern SaaS products like Figma, Notion, and Linear

## Design Philosophy
- Light backgrounds (#F7FAFC) with white cards
- Subtle shadows, 1px borders
- Single brand color (#00D9B5)
- SVG icons (Heroicons), never emojis
- Consistent spacing using CSS variables

## Colors
- **Primary:** #00D9B5 (teal/green)
- **Primary Dark:** #00BFA0
- **Navy (sidebar):** #0F1419
- **Text Primary:** #2D3748
- **Text Secondary:** #718096
- **Borders:** #E2E8F0
- **Success:** #48BB78 on #F0FFF4
- **Warning:** #ECC94B on #FFFFF0
- **Error:** #FC8181 on #FFF5F5

## Typography
- Font: Outfit (fallback: system)
- Weights: 400 (normal), 500 (medium), 600 (semibold), 700 (bold), 800 (black)
- Sizes: XS 0.75rem, SM 0.875rem, MD 1rem, LG 1.125rem, XL 1.25rem, 2XL 1.5rem, 3XL 2rem

## Components
- **Buttons:** Primary (#00D9B5 bg, white text), Secondary (white bg, border)
- **Inputs:** 1px border #E2E8F0, focus #00D9B5, padding 0.875rem
- **Cards:** White bg, 1px border, 12px radius, subtle shadow
- **Badges:** Pill-shaped, uppercase, 700 weight

## Layout
- Sidebar: 260px fixed, navy background
- Main content: margin-left 260px
- Page padding: 2rem
- Card padding: 2rem

## File Structure
Every page should import:
```html
<link rel="stylesheet" href="css/design-system.css">
```

## Do's
- Subtle shadows
- 1px borders
- Soft, professional colors
- SVG icons
- Consistent spacing

## Don'ts
- Heavy shadows
- Thick borders (2px+)
- Bright saturated colors
- Emojis in production
- Dark backgrounds (except sidebar)
- Gradient backgrounds
- Inconsistent spacing

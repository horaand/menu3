# Modern Dark Menu — Monochrome (HTML + CSS)

Classic dark header with gold accent, pure CSS hamburger, and responsive layout.

## Structure
```text
monochrome-nav/
├─ index.html
└─ styles.css
```

## Quick Start
1) Save the HTML as `index.html` and the CSS as `styles.css`.  
2) Ensure this is in `<head>`:
```html
<link rel="stylesheet" href="styles.css" />
```
3) Open `index.html` in your browser.

## Features
- **Pure CSS** mobile menu via hidden checkbox + label (`#nav-toggle`).
- **Sticky header** with glassy gradient and soft borders.
- **Active link underline** (gradient `::after`) and focus rings.
- **Tokenized theme** (CSS variables) for easy theming.
- **Responsive grid** for content cards.

## Customize (tokens in `:root`)
- Background/text: `--bg`, `--surface`, `--text`, `--muted`  
- Accent pair: `--accent`, `--accent-2`  
- Focus ring: `--ring`

## Accessibility
- Hamburger is a `<label for="nav-toggle">` so it’s keyboard-toggleable.
- Focus states via `:focus-visible` on links and buttons.
- `role="menubar"`/`menuitem` set on the primary list.

## Notes
- Keep **one** HTML document per page; keep CSS only in `styles.css`.
- Match ids/labels: `id="nav-toggle"` ⇄ `for="nav-toggle"`.

## Troubleshooting
- **Menu won’t open?** Confirm DOM order: `input.nav-toggle` → `label.hamburger` → `.menu-wrap`.
- **Layout breaks on mobile?** Ensure breakpoint rules under `@media (max-width: 900px)` remain intact.

## Styling Reference

Use these guidelines to reproduce the Tarkov-inspired presentation seen in this project.

### Framework & Assets
- Load Bootstrap `5.3.x` with the `data-bs-theme="dark"` attribute on `<html>`.
- Include Bootstrap Icons `1.11.x`.
- Apply the local `style.css` after vendor styles.
- Keep `body.png` for the page background and `header.png` for the hero card overlay.

### Page Shell
- Wrap the page in a `.container` with vertical padding (`py-4`) and cap width at `1000px`.
- Place the hero content inside a `.card` with `id="head"`, `border-secondary`, and `text-center` body copy.
- Use Bootstrap cards to group mod lists and tabs. Retain tab navigation inside the card header (`.nav-tabs.card-header-tabs`).

### Backgrounds
- Body: fixed background image (`background-attachment: fixed`) scaled to `122%`, no repeat.
- Header: use `header.png` stretched to cover, centered vertically around 37.5%.
- Overlay header text with a semi-transparent black card body (`rgba(0,0,0,0.7)`) and rounded corners.

### Color Language
- Lean on Bootstrap contextual colors, then adjust with opacity utilities:
  - Required mods: `border-danger` with `bg-danger bg-opacity-10`.
  - Optional mods: `border-primary` with `bg-primary bg-opacity-10`.
  - Server mods: `border-info` with `bg-info bg-opacity-10`.
  - Potential mods: `border-warning` with `bg-warning bg-opacity-10`.
- Compatibility badges:
  - `.indicator-green` `#2ecc71` on white text.
  - `.indicator-yellow` `#f1c40f` on black text.
  - `.indicator-orange` `#f39c12` on white text.
  - `.indicator-red` `#e74c3c` on white text.

### Typography
- Base text inherits Bootstrap dark theme defaults.
- Mod version strings use `.version` with `Courier New/Consolas`, `0.85em`, light gray (`#aaa`), and `white-space: pre-line`.
- Use Bootstrap heading classes (`h1`, `h2.h4`) with icon prefixes for emphasis.

### Iconography & Badges
- Icons: leverage Bootstrap Icons inside headings and buttons (`.bi` classes).
- Fallback thumbnails: `.icon-placeholder` sized `48px` square, dark gray background, mid-gray text, centered flex layout, rounded corners.
- Limit “Recently Updated” badge width to `300px` to avoid overflow.

### Links & Buttons
- Primary CTA button (`btn btn-warning btn-sm`) lives in the hero card; keep download icon.
- Hover state on header links shifts to `#e49c5d`.
- In list items, links inherit body color and transition to Bootstrap link color on hover.

### Layout Mechanics
- Use Bootstrap grid (`row g-3`, `col-lg-6`) to arrange client and potential mod columns.
- Ensure cards fill vertical space with `h-100` to keep column heights even.
- Keep list containers as `.list-group.list-group-flush` appended dynamically via JavaScript.

### Behavior Expectations
- JavaScript populates `#serverVersion` link and mod lists. Preserve IDs and data hooks.
- Compatibility badges and version data are injected; do not hard-code markup in HTML.

### Extending the Theme
- Favor Bootstrap utility classes before adding custom CSS.
- When adding new status badges, derive hues from existing palette to maintain contrast.
- For new sections, reuse card-with-overlay pattern: contextual border, low-opacity background, and card headers for titles.


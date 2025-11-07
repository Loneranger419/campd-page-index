# CampD Nexus Landing Page

Static hub for CampD projects and campfire notes, styled after the Tarkov-inspired layout shared across our modpack sites.

## Getting Started

- Open `index.html` in any modern browser or host it from a static server.
- Vendor dependencies load from CDNs:
  - Bootstrap `5.3.3` (dark theme)
  - Bootstrap Icons `1.11.3`
- Local styles live in `style.css`. Assets referenced there:
  - `img/logo.png` (provided)
  - `img/body.png` and `img/header.png` (supply matching background art or adjust the paths/colors as needed)

## Customising Content

- Hero card (`#head`) pulls the CampD logo and tagline. Update copy directly in `index.html`.
- Project tiles live under the `Projects` tab (`#project-tiles`). Replace placeholder anchors with real destinations and update the labels/badges.
- Blog tiles live under `Campfire Notes` (`#post-tiles`). Swap the placeholder items with actual post URLs and metadata.
- To enable links, replace `href="#"` with your project/post URLs and remove the `.placeholder-tile` class so hover and click states activate.

## Styling Notes

- Follow the guidance captured in `style.md` for additional theming rules.
- Background overlay colour is controlled via the `--campd-overlay` CSS variable.
- Cards use light opacity backgrounds so content beneath can glow through; tweak in `style.css` if contrast adjustments are required.

## Future Enhancements

- Hook the list containers (`#project-tiles`, `#post-tiles`) to a JSON feed or CMS when you need dynamic updates.
- Add status badges following the palette documented in `style.md` to mirror other CampD mod pages.


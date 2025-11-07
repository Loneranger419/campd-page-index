# CampD Index Knowledge Base

- **Purpose**: Static landing page acting as the entry point to CampD projects and blog-style notes. Built to mirror the Tarkov-inspired styling from existing mod pages.
- **Core Files**:
  - `index.html` – HTML shell with hero card, project tiles, and blog tiles.
  - `style.css` – Local theming layer (background images, overlays, hover treatments).
  - `style.md` – Reference spec describing desired visuals; keep in sync if theme changes.
- **Assets**:
  - Required: `img/logo.png` (present).
  - Optional/expected: `img/body.png`, `img/header.png` – referenced by CSS; replace or adjust paths if not available.
- **Placeholders**: Project and post tiles carry `.placeholder-tile` to disable links until real destinations are added. Remove the class and update `href` attributes when content is ready.
- **Bootstrapping**: Uses Bootstrap 5.3.3 and Bootstrap Icons 1.11.3 via CDN with `data-bs-theme="dark"` on `<html>`.
- **Future Work Ideas**: Feed project/post lists from JSON, expand with status badges per `style.md`, ensure accessibility contrast if background imagery changes.


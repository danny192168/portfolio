---
inclusion: fileMatch
fileMatchPattern: "**/*.html,**/*.css,**/*.js,**/*.png,**/*.jpg"
---
# Portfolio Implementation Rules

- Edit `portfolio_danny.html` directly; do not split the page into framework
  components unless the project is intentionally migrated.
- Follow the existing two-space indentation and vanilla HTML/CSS/JavaScript
  conventions.
- Reuse existing custom properties and classes such as `.container`,
  `.project-card`, `.gallery-thumb`, `.btn`, and `.gradient-text`.
- Keep local image paths relative to the HTML file and preserve exact asset
  filename casing, including spaces.
- When changing a project gallery, update the card image, all visible
  thumbnails, and the matching `projectImages` array together.
- Keep `data-project` values aligned with the keys in `projectImages`, and keep
  `data-index` values zero-based and contiguous.
- Preserve descriptive `alt` text, modal `aria-hidden` state, the Escape and
  arrow-key handlers, and the mobile menu's `aria-expanded` state.
- Keep demo-only behavior explicit: the contact form currently shows an alert
  and resets; it does not send data to a server.
- Avoid adding dependencies for static page changes.

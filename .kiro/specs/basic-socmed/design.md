# Basic-SocMed Code Design

- Use `assets/feeds.png` as the card's representative image.
- Keep the existing second-card structure, `.gallery-thumb` class, and
  `data-project="basicsocmed"` attributes.
- Treat the visible thumbnail order and `projectImages.basicsocmed` as one
  data contract for the shared lightbox.
- Do not add project-specific JavaScript or alter the shared modal for image
  changes.

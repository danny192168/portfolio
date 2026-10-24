# Cat-bolz Code Design

- Keep the existing first project-card layout and shared `.gallery-thumbs`
  styling.
- Keep the card image and thumbnail image paths relative to
  `portfolio_danny.html`.
- Keep the `projectImages.catbolz` array synchronized with the three visible
  thumbnail elements.
- The shared lightbox remains responsible for rendering `modal-image`,
  `modal-counter`, and previous/next controls; Cat-bolz should not introduce a
  separate modal implementation.

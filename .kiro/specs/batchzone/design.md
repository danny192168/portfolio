# Batchzone Code Design

- Keep the existing third-card layout and shared project-card styles.
- Use relative paths to the `batchz*.png` files in `assets/`.
- Keep `data-project`, zero-based indices, visible thumbnails, and
  `projectImages.batchzone` synchronized.
- Reuse the shared lightbox rather than adding Batchzone-specific controls or
  event listeners.

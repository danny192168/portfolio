---
inclusion: always
---
# Portfolio Change Workflow

## Before editing

1. Find the relevant section in `portfolio_danny.html`.
2. Inspect matching assets in `assets/`.
3. Trace both markup references and inline-script references for interactive
   content.
4. Preserve unrelated edits already present in the file.

## During editing

- Keep changes surgical because the page is intentionally self-contained.
- Update the CSS, markup, and script together when a component crosses those
  boundaries.
- Use real assets instead of generated base64 placeholders.
- Do not change project links, copy, section IDs, or interaction behavior
  unless the request requires it.

## Validation

- Search for stale `data:image` placeholders and missing local asset paths.
- Confirm every gallery thumbnail has a matching project key and index.
- Open the HTML directly in a browser and check the affected desktop and
  mobile layout.
- Exercise theme switching, mobile navigation, smooth anchors, and the
  lightbox when those areas are touched.

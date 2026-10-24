---
inclusion: always
---
# Portfolio Codebase

## Runtime shape

This is a static, single-page portfolio. The complete page lives in
`portfolio_danny.html`; it contains the document markup, an inline stylesheet,
and an inline script. There is no package manager, framework, bundler, backend,
or test runner in this workspace.

The page is intended to run directly from the workspace. Keep local references
relative, for example `assets/danny.jpg`, rather than adding server-side URLs.

## Page structure

The HTML currently contains:

- navigation with theme and mobile-menu controls
- hero section with the typewriter role text and profile photo
- About section with the capybara image
- Projects section with three project cards and screenshot thumbnails
- a shared gallery lightbox modal
- skills, contact form, and footer content

The section IDs are used by anchor navigation. Do not rename them casually:
`home`, `about`, `projects`, `skills`, and `contact`.

## Styling system

CSS is inline in the document. Shared colors, shadows, radii, layout width,
and navbar height are defined as custom properties in `:root`, with overrides
under `[data-theme="dark"]`. Reuse those variables and existing component
classes instead of adding one-off styles.

The root element starts with `data-theme="dark"`. Theme changes update that
attribute and persist the user's choice in local storage. Responsive rules
handle the mobile navigation and project layout.

## JavaScript behavior

The inline script owns theme persistence, system-theme changes, the typewriter,
mobile navigation, smooth anchor scrolling, image error fallback, the demo
contact form, and the project lightbox. Preserve the existing ARIA attributes,
keyboard handling, and event-driven behavior when changing these features.

## Project image data

Visible project images and lightbox images must stay synchronized:

- `catbolz`: `catz1.png`, `catz2.png`, `catz3.png`
- `basicsocmed`: `feeds.png`, `socmed2.png`, `socmed3.png`
- `batchzone`: `batchz1.png`, `batchz2.png`, `batchz3.png`

The visible thumbnails use `data-project` and zero-based `data-index`
attributes. The `projectImages` object near the end of the script uses the
same project keys and order.

## Asset inventory

Assets are stored in `assets/`: `danny.jpg`, `Cozy Capybara Lakeside
Retreat.png`, the Cat-bolz `catz*.png` files, the SocMed `feeds.png` and
`socmed*.png` files, and the Batchzone `batchz*.png` files. Preserve spaces
and capitalization in filenames when referencing them.

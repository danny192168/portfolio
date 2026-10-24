# Danny — Personal Portfolio

A modern, responsive, single-page portfolio website built with plain HTML, CSS, and vanilla JavaScript. No frameworks, no build tools, no external dependencies except Google Fonts. "You don't need any fancy technologies to deploy something cool."

---

## Why is copilot a contributor?

I'm lazy to type the git commit and push, I'll just tell copilot the name of commit and let him push. Copilot's sole purpose here is for git and github commands.

---

## A brief note from the developer

I did my best to make the website functional, responsive, and visually polished. I also reviewed and refined the initial AI-generated output to fix functional and visual issues. While I tried to prevent bugs, some may still slip through. If you encounter any, please use the form submission to let me know. I'm actually excited to hear it.

## Features

### Sections

- **Fixed Navigation Bar** — Sticky navbar with smooth-scroll links, mobile hamburger menu, and a "Download Resume" button
- **Hero Section** — Full-viewport intro with typewriter effect, social links, and animated decorative dots
- **About Section** — Two-column layout with image and bio
- **Skills Section** — Pill-shaped skill tags with hover effects
- **Projects Section** — Three project cards with image galleries and a lightbox modal
- **Testimonials Section** — Three quote cards with hover lift effects
- **Contact Section** — Contact info with icons and a working email form
- **Footer** — Simple dark footer with copyright

### Interactive Features

- **Dark Mode Toggle** — Switch between light and dark themes; preference is saved to `localStorage`
- **Typewriter Effect** — Cycles through roles with a blinking cursor
- **Scroll-Reveal Animations** — Sections and cards fade in as you scroll (via `IntersectionObserver`)
- **Project Image Lightbox** — Click any project thumbnail to view images in a full-screen modal with keyboard navigation
- **Working Contact Form** — Submits via `mailto:` link to open the visitor's email app
- **Back-to-Top Button** — Appears after scrolling 400px
- **Mobile Hamburger Menu** — Animated hamburger-to-X toggle with accessible dropdown
- **Three fully-functional games** — Try scrolling on the Play section and enjoy the 3 games.

<!-- ### Accessibility

- Semantic HTML (`header`, `nav`, `section`, `article`, `footer`)
- `aria-label` attributes on icon-only buttons
- `aria-expanded` on the mobile menu toggle
- Respects `prefers-reduced-motion` — animations are disabled for users who prefer reduced motion
- Visible `:focus-visible` outlines on interactive elements

--- -->

## Project Structure

```text
portfolio/
├── index.html    # Main portfolio file (self-contained)
└── assets/
    ├── danny.jpg                          # Profile photo
    ├── Cozy Capybara Lakeside Retreat.png # About section image
    └── *.png                              # Screenshots of featured projects
```

> **Note:** The `index.html` file contains all CSS and JavaScript internally. No external CSS or JS files are required.
> Why so: I never paid for any AI so I do these to efficiently work along AI with this code. I used a lot of AI tools and these option fits best for all of them.

---

## Customization Guide

### Changing Colors

The entire color scheme is controlled by CSS custom properties in the `:root` block:

```css
:root {
  --primary: #000000; /* Main accent color */
  --secondary: #666666; /* Supporting accent color */
  --bg-white: #ffffff; /* Main background */
  --bg-gray: #f3f4f6; /* Alternate background */
  --text-dark: #000000; /* Main text */
  --text-muted: #555555; /* Secondary text */
  --border: #e5e7eb; /* Borders and dividers */
}
```

The dark theme overrides these in the `[data-theme="dark"]` block.

### Changing Content

#### Personal Info

Edit the text directly in the HTML:

- **Name:** Search for `Danny` in the hero section
- **Tagline:** Edit `Just build.` in the hero section
- **About paragraph:** Edit the text inside the `.about-content` section
- **Contact info:** Update email, phone, and location in the Contact section

#### Projects

Each project card follows this structure:

1. Update the main image `src` in `.project-image img`
2. Update the project title in `.project-title`
3. Update the description in `.project-desc`
4. Update the "View Project" link `href`
5. Update the thumbnail images in `.gallery-thumbs`
6. Update the `projectImages` object in the JavaScript to match your image files

#### Skills

Add or remove skill tags in the `.skills-tags` container:

```html
<span class="skill-tag">Your Skill</span>
```

#### Testimonials

Edit the quote text, author name, and role inside each `.testimonial-card`.

#### Social Links

Update the `href` attributes on the GitHub and LinkedIn icons in the hero section.

### Adding More Project Images

To show more screenshots per project:

1. Add new `<img>` tags to the `.gallery-thumbs` container inside the project card
2. Add the image paths to the `projectImages` object in JavaScript:

```javascript
projectImages = {
  catbolz: ["assets/catz1.png", "assets/catz2.png", "assets/catz3.png", "assets/catz4.png"],
  // ...
};
```

---

## Browser Support

- Chrome / Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Android)

---

## Performance Notes

- All CSS is inline in a `<style>` tag — no render-blocking external requests
- All JavaScript is at the bottom of the file — does not block page rendering
- Images use `loading="lazy"` implicitly via browser defaults for below-the-fold content
- The file works offline once loaded (no CDN dependencies except Google Fonts)

---

## Credits

- **Design & Development:** Danny
- **Font:** [Poppins](https://fonts.google.com/specimen/Poppins) via Google Fonts
- **Icons:** Inline SVG (no icon library dependency)

---

## License

This portfolio is personal and open for reference. Feel free to use it as a template for your own portfolio.

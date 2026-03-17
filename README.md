# Designer Academic Homepage

A minimal, Cargo-inspired academic homepage template. No frameworks, no build tools — just HTML, CSS, and vanilla JS.

**[Live Demo](https://shenzhezhu.github.io/designer-academic-homepage/)**

## Features

- **Two-column editorial layout** — Fixed sidebar + scrollable content, inspired by [Cargo](https://cargo.site/) templates
- **Single Page Application** — Hash-based routing, page transitions with staggered fade-in
- **Fully responsive** — Mobile overlay menu, bottom navigation bar, touch-optimized
- **Publication showcase** — Auto-grouped by year, grayscale-to-color image hover, lightbox modal
- **Scroll animations** — Subtle scale-in reveal on scroll, respects `prefers-reduced-motion`
- **Accessible** — Skip link, keyboard navigation, focus indicators, ARIA attributes, semantic HTML
- **Lightweight** — Zero dependencies, ~5KB CSS + ~5KB JS

## Quick Start

```bash
git clone https://github.com/ShenzheZhu/designer-academic-homepage.git
cd designer-academic-homepage
```

Open `index.html` in your browser, or serve locally:

```bash
python -m http.server 8000
```

## Customization

1. **Edit `index.html`** — Update your name, subtitle, contact links, and footer
2. **Edit `pages/about.html`** — Your bio, research interests, and news
3. **Edit `pages/publications.html`** — Your papers (auto-grouped by `data-year`)
4. **Edit `pages/misc.html`** — Experience, education, honors
5. **Edit `pages/home.html`** — Hidden easter egg page (accessed by clicking your name)
6. **Edit `style.css`** — Customize colors in `:root` (highlight color, swatches)
7. **Replace `asset/`** — Add your images, paper figures, favicon

### Color Customization

Edit the CSS variables in `style.css`:

```css
:root {
  --highlight: #800020;  /* Accent color (burgundy) */
  --bg: #ffffff;          /* Background */
  --border: rgba(0, 0, 0, 0.15);
}
```

### Adding Publications

Each publication uses this structure:

```html
<div class="publication" data-year="2025">
  <div class="pub-text">
    <h4><a href="paper-url" target="_blank">Paper Title</a></h4>
    <p>Author One, <strong>Your Name</strong>, Author Two</p>
    <p><em><span class="highlight">Venue, Year</span></em></p>
    <p>
      <a href="#" target="_blank">[Paper]</a>
      <a href="#" target="_blank">[Code]</a>
    </p>
  </div>
  <img src="asset/paper_fig/your-fig.png" alt="Figure description" class="pub-image" loading="lazy">
</div>
```

## Deploy

Push to a GitHub repository named `yourusername.github.io` and enable GitHub Pages — it works out of the box.

## License

MIT

## Credits

Design inspired by [Cargo](https://cargo.site/) templates. Built by [Shenzhe Zhu](https://shenzhezhu.github.io).

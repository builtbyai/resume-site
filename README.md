# Resume Site

A single-file, print-perfect personal resume and portfolio page. One `index.html`, no build step, no framework — it loads instantly, prints to a clean one-page PDF, and works offline.

## Why

I wanted a resume that lived at a real URL, looked identical on screen and on paper, and had zero deploy friction. Most resume builders either lock you into their layout or produce bloated pages. This is the opposite: hand-written HTML and CSS in a single file you can host anywhere static (GitHub Pages, Cloudflare Pages, S3, or a plain web server).

## Features

- **Single self-contained file** — all styles are inline in `index.html`; the only external resources are Google Fonts.
- **Print-optimized** — a dedicated `@media print` stylesheet reflows the page to US Letter with tuned point sizes so the browser "Print" dialog produces a tidy one-page PDF.
- **Download + Print toolbar** — a fixed toolbar offers a direct PDF download and a one-click print, both hidden when printing.
- **Responsive** — a mobile breakpoint drops the fixed toolbar into the flow and tightens padding for small screens.
- **Semantic + SEO-ready** — proper document outline, Open Graph tags, a `theme-color`, and an inline SVG favicon (no extra requests).
- **Accessible color and type** — restrained palette with CSS custom properties, condensed display headings, and a readable body font.

## Tech Stack

- Plain HTML5 + CSS3 (CSS custom properties, flexbox, print media queries)
- Google Fonts (Source Sans 3, Saira Condensed)
- Inline SVG favicon (data URI)
- No JavaScript build tooling — the only script is a one-line `window.print()` handler

## Getting Started

No install or build. Clone and open:

```bash
git clone https://github.com/builtbyai/resume-site.git
cd resume-site
# open index.html in a browser, or serve it:
python -m http.server 8000
# then visit http://localhost:8000
```

To regenerate the downloadable PDF, open the page and use your browser's Print → Save as PDF (the print stylesheet is tuned for this).

## Deploying

Any static host works. For GitHub Pages, enable Pages on the `main` branch root; the page and its PDF are served as-is. Because assets are referenced with relative paths, it works whether the site is served from a domain root or a project subpath.

## Screenshots


## Live Demo

Live version: https://wardtechsystems.com/resume/

## License

MIT — see [LICENSE](LICENSE).

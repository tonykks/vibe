# AGENTS.md

## Cursor Cloud specific instructions

This is a static HTML website (two landing pages) with no build system, no package manager, and no dependencies to install.

### Project structure

- `index.html` — Primary landing page (self-contained HTML/CSS/JS, no external deps)
- `index_2.html` — Alternate landing page (uses Tailwind CSS and Font Awesome via CDN)

### Running the dev server

Serve the files with Python's built-in HTTP server:

```bash
python3 -m http.server 8080 --directory /workspace
```

Then open `http://localhost:8080/index.html` or `http://localhost:8080/index_2.html`.

### Lint / Test / Build

- **No linter configured** — the project has no `package.json`, `.eslintrc`, or similar config.
- **No automated tests** — pure static HTML with no test framework.
- **No build step** — files are served directly without compilation or bundling.

### Notes

- `index_2.html` requires internet access for CDN resources (Tailwind CSS, Font Awesome). If CDN is unavailable, that page will render without styling.
- `index.html` is fully self-contained and works offline.

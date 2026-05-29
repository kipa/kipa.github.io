# Agents

## Cursor Cloud specific instructions

This is a static HTML/CSS/JS resume site with no build tools, no package manager, and no dependencies to install. All logic is inline in `index.html`, with resume data in `resume.json`.

### Running the dev server

Serve files over HTTP (required because `index.html` fetches `resume.json` via `fetch()`):

```
python3 -m http.server 8080 --directory /workspace
```

Then open `http://localhost:8080/` in Chrome.

### Notes

- There is no linter, test suite, or build step — the site is deployed as-is via GitHub Pages (see `.github/workflows/deploy-pages.yml`).
- The EN/RU language toggle and PDF download buttons require internet access (Google Translate API and `html2pdf.js` from CDN respectively). Core resume rendering works offline.
- Editing `resume.json` is the primary way to update resume content; no HTML changes needed.

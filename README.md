# Aura Static Landing Page

High-end landing page for **Aura** — predictive analytics for high-frequency traders.

## Final stack used

- Static HTML
- Static CSS
- Google Fonts (`Inter` for body, `Space Grotesk` for headings)

I initially scaffolded a Vite + React version, but the local build environment hit a low-level `Bus error` during `vite build`. Because the priority here is **a GitHub Pages deployment that reliably renders**, I finalized the site as a pure static implementation with no framework runtime and no asset-path fragility.

## Files that matter most

- `index.html` — source page
- `styles.css` — source styles
- `dist/index.html` — ready-to-deploy page
- `dist/styles.css` — ready-to-deploy styles

## Local preview

Open `index.html` directly in a browser, or serve the folder with any static server.

Example:

```bash
cd aura-static
python3 -m http.server 4173
```

Then open:

```text
http://localhost:4173
```

## GitHub Pages deployment

### Simplest path: deploy the `dist/` folder to a `gh-pages` branch

```bash
cd aura-static/dist
git init
git checkout -b gh-pages
git add .
git commit -m "Deploy Aura landing page"
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -f origin gh-pages
```

Then in GitHub:

1. Open **Settings → Pages**
2. Set **Source** to **Deploy from a branch**
3. Select branch **gh-pages** and folder **/ (root)**
4. Save

## Notes

- The site uses only relative file references (`./styles.css`), so it is safe for GitHub Pages subpath hosting.
- The layout remains readable even if decorative effects are absent.
- A Git repo has been initialized in `aura-static/`.

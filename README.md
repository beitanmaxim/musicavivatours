# Musica Viva Tours — Geography of Sound

Single-page site for Musica Viva Tours (musicavivatours.com): private concerts by cellist
Max Beitan, curated by the Beitan Music Foundation, Lugano.

## Contents

```
index.html    The page (single file, no build step)
support.js    Runtime that renders the page
assets/       The 14 photographs + hero video the page actually uses
.nojekyll     Tells GitHub Pages to serve every file as-is
```

## Deploy to GitHub Pages

1. Create a repository and push the **contents of this folder** to the repository root.
2. Settings → Pages → Source: `main` branch, `/ (root)`.
3. Publishes at `https://<user>.github.io/<repo>/` (custom domain optional).

To preview locally, serve the folder (do not open the file directly — the runtime needs HTTP):
```
cd musicaviva-tours-site
python3 -m http.server 8000     # then open http://localhost:8000
```

## Two things to know before you publish

1. **The page fetches React from unpkg.com at runtime** (`support.js` loads
   `react@18.3.1` and `react-dom@18.3.1` from the unpkg CDN). It therefore renders only with an
   internet connection and is not a fully self-contained static file. GitHub Pages visitors have
   internet, so it will display — but this is an external dependency to be aware of.

2. **This is the legacy page.** It still carries the name "Musica Viva **Tours**" and a published
   price (€2,900). Per the July 2026 brand work, the travel brand is being renamed and repositioned
   (see `../cavea/docs/`), and Strado is the separate private society. Publish this only as the
   current live site; the rebuilt travel-brand site is a separate deliverable.

## Contact
info@musicavivatours.com · +41 77 929 44 77 · Lugano, Switzerland

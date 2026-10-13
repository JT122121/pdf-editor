# PDF Editor

Edit text in PDFs, add new text, and white out parts of scanned pages — entirely in the browser. Files never leave your device. Works offline after the first visit.

## Deploy on GitHub Pages

1. Create a new **public** repository (e.g. `pdf-editor`).
2. Upload every file in this folder to the repository root (including `.nojekyll`).
3. Go to **Settings → Pages**, set **Source: Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute the app is live at `https://<your-username>.github.io/pdf-editor/`.

Open it once while online. After that it loads without internet, and Chrome/Edge offer **Install** in the address bar so it opens like a desktop app.

## Updating

Replace `index.html`, then change `VERSION` in `sw.js` (e.g. `pdf-editor-v2`). Without the version bump, offline users keep the old copy.

## Files

- `index.html` — the whole app, with pdf.js, pdf-lib and fontkit built in (also works by double-clicking it locally)
- `sw.js` — offline cache
- `manifest.webmanifest`, `icon*` — install as an app

## Limits

- Edited text is drawn over a cover box; the original text is still inside the file. Do not use this for redaction.
- Exact font matching needs the original .ttf/.otf loaded once (saved in the browser per site).
- Scanned PDFs have no text to edit: use Whiteout + Add text.
- Arabic and other right-to-left scripts are not shaped correctly.

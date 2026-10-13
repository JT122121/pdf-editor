# Online PDF Editor

Edit text in PDFs, add text, and white out scanned pages entirely in the browser. Files never leave the device. Works offline after the first visit.

## Deploy on GitHub Pages

1. Use the repository that serves joetayactac.site (or any public repository with Pages enabled).
2. Upload every file in this folder (there are no subfolders). Keep your existing CNAME file.
3. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.

## Your web address (important for search)

The site is set up for `https://joetayactac.site/` (the root of the domain).
If your address is different, find and replace that address in:
`index.html`, `sitemap.xml` and `robots.txt`.

## Getting found on Google

1. Open Google Search Console, add your domain, and verify it.
2. Sitemaps → submit `https://joetayactac.site/sitemap.xml`.
3. URL Inspection → paste the page address → Request indexing.
4. Do the same in Bing Webmaster Tools (it can import from Google Search Console).
5. Get links: post it where people ask for private or offline PDF tools.

## Updating

After changing any file, change `VERSION` in `sw.js` (e.g. `pdf-editor-v5`), or offline visitors keep the old copy.

## Limits

- Edited text is covered, not deleted. Not for redaction.
- Exact font matching uses fonts installed on the computer (Chrome/Edge desktop) or font files you add.
- Scanned PDFs: use Whiteout + Add text.
- Latin-script text only.

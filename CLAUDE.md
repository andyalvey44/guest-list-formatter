# Guest List Formatter

A finished, in-production tool for one small office. Keep it simple, and only change what's actually asked for.

## What it is
- One self-contained file: `public/index.html` (inline CSS/JS, logo as a data URI). No build step, no framework, no backend.
- Staff upload an eTix guest-list CSV, and the page formats it for printing. Everything runs in the browser and nothing is uploaded.
- PDF input is best-effort: pdf.js 3.11.174 loads from cdnjs only when someone picks a PDF.

## Hosting
- Vercel project connected to GitHub `andyalvey44/guest-list-formatter`. A push to `main` deploys to production.
- `vercel.json` serves only `public/` and sets the headers (CSP, noindex, no-cache). If you add an external script or resource, update the CSP there or the browser will block it.

## Rules
- `samples/` and every `*.csv`/`*.pdf` hold real customer names and order IDs. Never commit them, publish them, or copy them into `public/`. `.gitignore` and `.vercelignore` both block them.
- Keep the tool as a single file. It must keep working when opened straight from disk (that's the fallback if the site is down).
- Test changes by opening `public/index.html` locally with a sample CSV and checking the print preview (Letter size) before pushing.
- `README.md` is written for non-technical staff. Keep its tone and step-by-step style.

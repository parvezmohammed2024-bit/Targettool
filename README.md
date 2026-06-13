# Targettool — Deploy to Vercel

This folder is ready to deploy as-is. It contains:

- `index.html` — the full Targettool PDF editor (HTML + CSS + JavaScript in one file)
- `vercel.json` — routing + basic security headers
- `README.md` — this file

## Option A — Drag & drop (no terminal)

1. Go to https://vercel.com/new
2. Drag this whole folder onto the page (or zip it and upload).
3. Click **Deploy**.
4. Open the URL — it loads at the root because the file is named `index.html`.

Your editor will also be reachable at `your-project.vercel.app/pdf-editor`.

## Option B — Vercel CLI

```bash
npm i -g vercel
cd deploy
vercel        # preview deploy
vercel --prod # production deploy
```

## Custom domain (e.g. targettool.app)

In the Vercel dashboard: **Project → Settings → Domains → Add**, then point
your domain's DNS to Vercel (you've done this before via Spaceship for
nexifysolution.net — same process).

## Notes

- Everything runs in the browser; there is no backend, so nothing to configure.
- The "Setting up fake worker" console message disappears on a real domain.
- When you outgrow a single file (image editor, video converter, per-tool SEO
  pages, accounts), move to a Next.js project — same Vercel deploy flow.

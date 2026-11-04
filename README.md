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

## Features

- **Edit:** edit existing text, add text/textbox, images, whiteout, shapes, pencil
- **Undo / redo:** every edit, page operation, bookmark and form value (Ctrl+Z, Ctrl+Y / Ctrl+Shift+Z)
- **Find & replace:** Ctrl+F; match case, whole words, replace one or all (rotated text is skipped)
- **Comment:** highlight, underline, strikeout and squiggly snap to the text you drag across (click selects a word);
  sticky notes, stamps (standard, dynamic name/date, or your own image), polygon and cloud shapes;
  a Comments panel with replies and your author name
- **Saving comments:** by default they're written as real PDF annotations (editable in Foxit / Acrobat, replies kept);
  turn on **Flatten** (Comment tab or Comments panel) to burn them into the page instead
- **Bookmarks:** reads the PDF's existing outline; add, nest, rename, reorder; written back on save (merged files get one group per file)
- **Links:** drag a box, link to a page or a web address; follow with the Hand tool
- **Fill & Sign:** fill existing form fields right on the page (fields stay fillable after saving),
  signatures and initials (draw, type or upload — saved in this browser), check, cross and date

## Notes

- Everything runs in the browser; there is no backend, so nothing to configure.
- The "Setting up fake worker" console message disappears on a real domain.
- When you outgrow a single file (image editor, video converter, per-tool SEO
  pages, accounts), move to a Next.js project — same Vercel deploy flow.

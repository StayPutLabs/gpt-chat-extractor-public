# ChatGPT Export Extractor

Split your ChatGPT data export into one text file per conversation.

Everything runs in your browser — your data is never uploaded. The tool is a
single static HTML file that works offline (open it via `file://`) or as a
hosted page.

## Use it

1. In ChatGPT, go to **Settings → Data controls → Export data** and wait for
   the email with your download.
2. Unzip the export. You'll find either `conversations.json` or — for large
   accounts — a sharded set (`conversations-000.json`, `conversations-001.json`,
   …).
3. Open `index.html` in any modern browser.
4. Drop the JSON file(s) on the page and click **Parse**.
5. Filter / sort / select the conversations you want, then download as a ZIP
   (one `.txt` per conversation + an index) or a single combined text file.

## Features

- Handles both single-file and sharded ChatGPT exports.
- Filter by title substring, content keywords, or date range.
- Sort by title, message count, or date.
- Select all visible, deselect, invert.
- Download as ZIP (one file per conversation) or one combined `.txt`.
- 100% client-side — no server, no analytics, no upload.

## Deploy

It's one static HTML file. Any static host works. Easiest options:

### Netlify (drag-and-drop)

1. Go to <https://app.netlify.com/drop>.
2. Drag the folder containing `index.html` onto the page.
3. Done — Netlify gives you a public URL.

### Netlify (Git-connected)

1. Push this repo to GitHub.
2. In Netlify, **Add new site → Import from Git**, pick the repo.
3. Build command: *(leave empty)*. Publish directory: *(repo root, or `.`)*.

### GitHub Pages

1. Push to GitHub.
2. **Settings → Pages → Source: Deploy from a branch**, pick `main` / root.

### Run locally

Just open `index.html` in a browser. No build step, no dependencies.

## License

MIT (or change to whatever you like before publishing).

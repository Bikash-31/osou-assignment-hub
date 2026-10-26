# OSOU Assignment Hub — BA & MA

A responsive static website starter for publishing OSOU BA and MA assignment study resources. It includes programme/subject/session filters, text search, and PDF links.

## Files

- `index.html` — website pages and sections
- `style.css` — responsive design
- `script.js` — search, filters and card rendering
- `data/assignments.json` — assignment catalogue
- `pdfs/` — place PDF files here

## Add a solved assignment

1. Put your PDF into the `pdfs/` folder, for example `ba-odia-paper-1-solved.pdf`.
2. Open `data/assignments.json`.
3. Add an object inside the `assignments` array. Example:

```json
{
  "id": "ba-odia-paper-1-2026",
  "programme": "BA",
  "subject": "Odia",
  "title": "BA Odia — Paper 1 title",
  "courseCode": "OFFICIAL-COURSE-CODE",
  "level": "BA",
  "session": "2026-27",
  "description": "Short summary of this study resource.",
  "questionPdf": "pdfs/ba-odia-paper-1-question.pdf",
  "solvedPdf": "pdfs/ba-odia-paper-1-solved.pdf"
}
```

For a missing question or solved PDF, use an empty string (`""`). Use commas between objects, but not after the final object. JSON must be valid.

## Change contact email

Open `script.js` and change:

```js
const SITE_EMAIL = "your-email@example.com";
```

to an email address you control.

## Preview locally

Because the site loads JSON using `fetch`, run it through a local web server instead of double-clicking `index.html`. If Python is installed, open a terminal in this folder and run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## Publish with GitHub Pages

1. Sign in to GitHub and create a new public repository, for example `osou-assignment-hub`.
2. Upload all files and folders from this project, keeping the same structure.
3. Open repository **Settings → Pages**.
4. Under build/deployment, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for the published site URL shown in Pages settings.

GitHub Pages is static hosting. This starter does **not** include a secure admin login or an upload dashboard. To upload PDFs from a browser without editing files, connect a backend and authenticated file storage (for example, a managed database/storage service). Never put passwords, private API keys, or admin credentials in front-end JavaScript.

## Important

- This website is not affiliated with OSOU.
- Verify programme structure, course codes, academic session and assignment requirements against official university materials.
- Share only PDFs and solutions you own or have permission to publish.
- Present solutions as study references; students should understand the material and prepare submissions in their own words.

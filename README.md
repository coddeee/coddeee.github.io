# coddeee.github.io

Personal CV / portfolio site, served at **https://coddeee.github.io**.

## Files

- `index.html` — the CV page itself (structure + content)
- `style.css` — classic professional styling, print-ready
- `cv.pdf` — optional PDF version linked from the footer (add your own)

## Customising the CV

Open `index.html` and replace the placeholder content. The sections to edit are:

1. **Header** — `Your Name`, title, email, location, GitHub, LinkedIn, site URL
2. **Profile** — 2–3 sentence summary
3. **Experience** — one `<article class="entry">` block per role
4. **Education** — same `<article>` pattern as Experience
5. **Projects** — links go in the `<a class="link" href="...">[repo]</a>` tag
6. **Skills & Technologies** — edit the `<dt>` / `<dd>` pairs

Each entry block looks like this — copy/paste to add more:

```html
<article class="entry">
  <header class="entry-header">
    <div>
      <h3 class="role">Role / Title</h3>
      <p class="org">Organisation <span class="loc">— City</span></p>
    </div>
    <p class="dates">Mon YYYY – Mon YYYY</p>
  </header>
  <ul class="bullets">
    <li>Achievement or responsibility.</li>
  </ul>
</article>
```

## Generating a PDF

Open `index.html` in Chrome, **File → Print → Save as PDF**. The print
stylesheet hides the footer and tightens margins automatically.

Save the file as `cv.pdf` in the repo root so the footer link works.

## Deploying to GitHub Pages

1. Commit the files to the `main` branch of `coddeee/coddeee.github.io`:
   ```bash
   git add index.html style.css README.md
   git commit -m "Add professional CV"
   git push origin main
   ```
2. In the repo on GitHub: **Settings → Pages**, confirm the source is set to
   `main` / root.
3. After a minute the site is live at https://coddeee.github.io.

## Local preview

Just open `index.html` in a browser — no build step required. For a local
server (so relative paths behave like on GitHub Pages):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

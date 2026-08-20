# maxsbennett.com

Personal site for Max Bennett. Plain HTML + CSS, no build step, hosted on GitHub Pages.

## Files

- `index.html` — the whole site (single page)
- `style.css` — all styling
- `CNAME` — tells GitHub Pages the custom domain (maxsbennett.com)
- `Max_Bennett_CV.pdf` — linked from the header

## Deploy

1. Push these files to the `main` branch.
2. Repo → Settings → Pages → Build and deployment → "Deploy from a branch" → `main`, `/ (root)`.
3. The `CNAME` file pre-fills the custom domain. At the domain registrar, add four A records
   on `@` (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) and a
   CNAME record on `www` pointing to `maxbennett.github.io`.
4. Once DNS verifies, tick "Enforce HTTPS" in Settings → Pages.

## Maintenance notes

- **Headshot**: currently hotlinked from abriefhistoryofintelligence.com. To switch to a
  local copy, save it to `images/headshot.jpg` and update the `src` in `index.html`
  (marked with a comment).
- **GNM preprint**: the first publication entry has a `TODO` comment — add the
  arXiv link when the preprint is live.
- **Adding a paper**: copy any `<li>` inside `ul.refs` in `index.html` and edit.

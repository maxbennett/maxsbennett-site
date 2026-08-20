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

- **Images**: the headshot and book cover are hotlinked from abriefhistoryofintelligence.com.
  To switch to local copies, save them under `images/` and update the two `src` attributes in
  `index.html` (both marked with comments). The cover is currently a 3D mockup with a lot of
  white padding; a flat front cover would look better in the Books row.
- **HTTPS**: the custom domain is currently served over plain HTTP — GitHub has not issued a
  certificate for maxsbennett.com. Fix in Settings -> Pages (re-save the custom domain to
  trigger provisioning, then tick "Enforce HTTPS").
- **GNM preprint**: the first publication entry has a `TODO` comment — add the
  arXiv link when the preprint is live.
- **Adding a paper**: copy any `<div class="entry">` block in the Publications section and edit.
- **Adding a video**: copy an entry from the Videos section and swap the YouTube ID in both the
  link and the `i.ytimg.com/vi/<ID>/hqdefault.jpg` thumbnail. `hqdefault.jpg` always exists
  (unlike `maxresdefault.jpg`); the CSS crops its letterbox bars to 16:9.
- **Art of the Problem video**: has a `TODO` — add the year and adjust the credit line to
  describe your actual role on it.

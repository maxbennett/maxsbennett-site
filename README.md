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
  Publication thumbnails are real figures from each paper, stored locally in `images/` and
  resized to 640px wide. They render with `object-fit: contain` so the whole figure shows.
  The Frontiers papers are open access (CC-BY) and Max is an author on all of them.
- **Adding a video**: copy an entry in Featured Talks & Interviews and swap the YouTube ID in
  both the link and the `i.ytimg.com/vi/<ID>/hqdefault.jpg` thumbnail. `hqdefault.jpg` always
  exists (unlike `maxresdefault.jpg`); the CSS crops its letterbox bars to 16:9. The list is ordered newest first by hand.
- **Verifying a YouTube ID**: `https://www.youtube.com/oembed?url=<watch-url>&format=json`
  returns the real title and channel, and 404s if the video is gone or not embeddable.

# IDRVN — placeholder site

Pre-launch homepage for IDRVN Private Limited (under incorporation).

## Files
- `index.html` — the whole site, single self-contained file
- `favicon.svg`, `favicon.ico`, `favicon-192.png`, `apple-touch-icon.png` — the compact इ mark as browser-tab and home-screen icons
- `og-image.png` — 1200×630 share image used for link previews (Open Graph / Twitter)
- `robots.txt`, `sitemap.xml` — for search engines; update the `lastmod` date in `sitemap.xml` when the page changes
- `.nojekyll` — tells GitHub Pages to serve files as-is, skip Jekyll processing
- `CNAME` — set to `www.idrvn.com`; delete this file if you're not pointing the domain here yet

## Deploy to GitHub Pages

1. Create a new GitHub repo (public, or private on a paid plan) and push these files to the root of the `main` branch. No `src` folder, no build step, just these four files at the top level.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: `main`, folder: `/ (root)`. Save.
5. GitHub gives you a URL like `https://<username>.github.io/<repo-name>/` within a minute or two. That confirms the deploy works before touching DNS.

## Pointing www.idrvn.com at it (once you're ready)

1. Keep the `CNAME` file in the repo (already set to `www.idrvn.com`).
2. At your domain registrar, add a `CNAME` record: host `www`, value `<username>.github.io`.
3. Back in **Settings → Pages**, the custom domain field should pick up `www.idrvn.com` automatically once the DNS record resolves (can take a few hours). Check "Enforce HTTPS" once the certificate is issued.
4. If you want the bare `idrvn.com` (no `www`) to also work, add `A` records at your registrar pointing the apex domain to GitHub's IPs (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153), and set up a redirect from apex to `www`.

## Editing later
Everything, HTML, CSS, and JS, lives in `index.html`. No dependencies to install, no build step. Open it in any text editor, save, commit, push, done.

# Stack the Lineup — marketing site

Static HTML site. No build step, no dependencies. Just files.

## Pages
- `index.html` — landing page (hero, features, pricing, reviews, FAQ teaser)
- `faq.html` — full FAQ (with FAQPage structured data)
- `support.html` — support / getting started / billing
- `privacy.html` — privacy policy
- `assets/` — shared CSS, app icon, app screenshots
- `sitemap.xml`, `robots.txt` — SEO
- `CNAME` — custom domain for GitHub Pages (currently `stackthelineup.com`)
- `.nojekyll` — tells GitHub Pages to serve files as-is

## Deploy to GitHub Pages
1. Create a new repo (e.g. `stackthelineup-site`) and push the **contents of this folder** to the repo root (so `index.html` is at the top level).
2. In the repo: **Settings → Pages**.
3. Under "Build and deployment", set **Source: Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. Wait ~1 minute. Your site is live at `https://<username>.github.io/<repo>/`.

## Custom domain (you already own stackthelineup.com)
1. The included `CNAME` file already sets the domain to `stackthelineup.com`.
   (If you use a different domain, edit `CNAME` to match, or remove it.)
2. At your domain registrar, add DNS records pointing to GitHub Pages:
   - Four **A records** for the apex (`stackthelineup.com`):
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME record** for `www` → `<username>.github.io`
3. Back in **Settings → Pages**, confirm the custom domain and tick **Enforce HTTPS** once it's available.

## Notes
- The canonical/OG URLs and structured data use `https://stackthelineup.com/`.
  If you launch on a different domain, find-and-replace that URL across the
  `.html` files and `sitemap.xml`.
- Testimonials and the 4.9 / 47-rating figure are placeholders — replace with
  real reviews when you have them (the rating also appears in the JSON-LD in
  `index.html`).

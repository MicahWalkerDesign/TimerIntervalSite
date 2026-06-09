# Timer | Interval — Marketing Site

A one-page marketing site for [Timer | Interval](https://apps.apple.com/app/id6759624277), a HIIT, Tabata, EMOM and AMRAP interval timer for iPhone & iPad.

## Stack

Static HTML + CSS. No build step, no JavaScript, no frameworks. Designed to be hosted anywhere — GitHub Pages, Cloudflare Pages, Netlify, Vercel, or any object store with HTTP.

## Files

```
index.html        # The page
styles.css        # Dark theme matching the app
robots.txt        # Search engine directives
sitemap.xml       # Single-page sitemap
.nojekyll         # Tells GitHub Pages not to run Jekyll
assets/
  img/icon.png    # Favicon + Open Graph fallback
  img/og-image.png# Social preview (1242×2688 iPhone screenshot)
  screenshots/    # iPhone 6.5" App Store screenshots used in the page
```

## SEO

- Semantic HTML5 (`header`, `main`, `section`, `article`, `footer`)
- Per-page `<title>` and `<meta description>` tuned to fitness/timer queries
- Open Graph + Twitter Card metadata for rich social previews
- JSON-LD structured data:
  - `MobileApplication` schema linking to the App Store listing
  - `FAQPage` schema covering common questions
- Canonical URL set
- `apple-itunes-app` smart banner meta tag (iOS Safari banner with one-tap install)
- All images carry descriptive `alt` text
- All screenshots use `loading="lazy"` except the LCP hero (which uses `fetchpriority="high"`)
- `robots.txt` + `sitemap.xml`

## Deploying to GitHub Pages

1. Push to `main`.
2. Repo Settings → Pages → Source = "Deploy from a branch", Branch = `main`, Folder = `/ (root)`.
3. Once it's live at `https://micahwalkerdesign.github.io/TimerIntervalSite/`, add a custom domain (e.g. `timerinterval.app`) by writing a `CNAME` file at the repo root and configuring your DNS.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Updating screenshots

Drop new English 6.5"-display PNGs into `assets/screenshots/` keeping the same filenames, and they'll replace what's on the page. The hero image is `01-train-harder.png`.

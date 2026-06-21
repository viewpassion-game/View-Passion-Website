# View Passion — Gaming One Stop (Website v2)

A multi-page website built as a single home: one `index.html` with client-side
page switching (Home, Studio, Cat vs Cucumber, Works, Team, Partner). Plain
HTML/CSS/JS — no build step, no dependencies.

## Pages (all on one home)
The nav switches between in-page "pages" with smooth transitions and hash routing,
so the browser back button and deep links (e.g. `index.html#game`) both work.
- **Home** — Gaming One Stop hero, one-stop services, data-driven pipeline, flagship teaser
- **Studio** — who we are, real studio photos, AI-pipeline case studies
- **Cat vs Cucumber** — key-art hero, specs, 6 feature panels, monetization, 5-phase roadmap
- **Works** — in-house art portfolio, affiliate platform, brand & ecosystem customers
- **Team** — founder headshots + studio photos
- **Partner** — collaboration options + contact details

## Files
- `index.html` — the whole site
- `manifest.webmanifest` — PWA manifest (save to home screen with an app icon)
- `assets/` — game art, screenshots, feature panels, headshots, office photos, logos, icons

## Deploy
Open `index.html` locally, or upload the whole folder to any static host (Netlify,
Vercel, Cloudflare Pages, GitHub Pages). Keep `index.html`, `manifest.webmanifest`,
and `assets/` together. Fonts load from Google Fonts (system fallbacks if offline).

## Editing
- Colors: `:root` block at the top of `<style>` (derived from the View Passion logo).
- Copy: plain HTML — search for the text to change.
- Images: swap files in `assets/` (keep names) or update `src`.
- Contact form: opens the visitor's email app via `mailto:` (no backend). Swap to a
  form service in the `#contactForm` submit handler if you want logged submissions.
- Add a page: duplicate a `<section class="page" id="page-x">`, add a nav button with
  `data-go="x"`, and add `x` to the `PAGES` array in the script.

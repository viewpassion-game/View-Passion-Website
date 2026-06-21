# View Passion — Gaming One Stop (Website)

A single-page app that behaves like a **multi-page site**: one home plus six navigable
"pages" (Home, The Game, Studio, Works, Team, Partner) with hash routing, smooth view
transitions, a desktop top-nav, and an app-style bottom tab bar on mobile. Plain HTML/CSS/JS,
no build step.

## index.html is fully self-contained
Every image is embedded in `index.html` as base64, so it renders correctly **anywhere** —
double-clicked, in a preview pane, or hosted — with no dependency on the `assets/` folder.
Verified: 64 images, 0 broken, even when run from a folder with no `assets/` directory.

## What's in this revision
**Home**
- 10M+ stat now reads "App Store impressions · pre-launch" (hero + traction section).
- Explore cards use varied, text-safe imagery (key art, studio, environment art, summon portal)
  with a stronger gradient so headings stay readable.

**The Game**
- **Fixed the Daisy display bug.** The evolution images are now preloaded in the DOM and the
  script reads their embedded data — so they show reliably in the self-contained file. (The old
  version pointed the script at `assets/…` paths that don't exist once inlined.)
- **Second hero added** — pick **Daisy** or **Marigold**; each auto-evolves through its tiers
  (sketch → painted final form).
- **Floating cat mascots** (Daisy + Marigold) decorate the game hero with bob/hover animation,
  on top of the existing particle, tilt, shine and lightning VFX.
- **"Straight from the game"** refreshed with the new world-map and summon-portal screenshots.
- **Hybrid-casual economics, the product roadmap, and add-on content are all clickable** — each
  opens an in-depth, well-researched article modal (economy structure, retention gates, design
  rationale) with relevant media. This is where the studio's depth in economy & development shows.

**Studio**
- **Case studies are clickable** — each opens a structured deep-dive (challenge → what we did →
  how → why it stands out → outcome) with metrics, a pull quote, and media.
- More studio imagery added: the team photo and three resident studio cats.

**Works**
- Gallery rebuilt with the new portfolio (Cat vs Cucumber, Evermoon MOBA, LINE Mini Dapp,
  Pepsi AR & retail, Axolt's Escape, isometric environment art, AI VTuber, MOBA splash).
- **Every project is clickable** — a detail page covering what we did, how, why it stands out,
  and customer satisfaction.

## Files
- `index.html` — the whole site, all images embedded (open it directly; it just works).
- `manifest.webmanifest` — PWA manifest; the home-screen icon is the Cat vs Cucumber hero.
- `assets/` — the original image files. Not required for `index.html` to display; kept so you can
  serve PWA install icons when hosting and edit/replace images.

## Deploy
- **View:** double-click `index.html`.
- **Host:** upload the whole folder to any static host (Netlify, Vercel, Cloudflare Pages,
  GitHub Pages). Keep `index.html`, `manifest.webmanifest`, and `assets/` together. No build step.

## Notes
- I could not pull from the shared Google Drive link — Drive folders require sign-in and aren't
  directly fetchable by the build tools. This build uses every file uploaded to the chat,
  including the new portfolio archive.
- The second hero is named **Marigold** ("Whisker Heal") — rename freely in the source.
- Editing an embedded image means replacing the file in `assets/` and re-embedding.
- Traction numbers (10M+ impressions) and roadmap dates come from your screenshots/PDF —
  worth a final accuracy check before publishing.
- The contact form composes a `mailto:` to info@viewpassion.com (no backend); swap the
  `#contactForm` handler to a form service if preferred.

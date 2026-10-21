# johnazz.dev

Personal site for [johnazz.dev](https://johnazz.dev): selected work, a short
introduction, and product pages for Nitrate and Canonic.

Static HTML and one stylesheet. No build step, no framework, no third-party
scripts or fonts.

## Layout

```
public/                 ← the only directory that is deployed
  index.html            home — Fieldnotes layout
  nitrate/index.html    Nitrate product page      → /nitrate
  canonic/index.html    Canonic product page      → /canonic
  404.html              served for unmatched paths
  _headers              response headers
  assets/site.css       the whole stylesheet
  assets/*.png|jpg      product imagery
  assets/*.svg          pixel glyphs + favicon
wrangler.jsonc          Cloudflare deploy config (assets-only Worker)
design/study.html       the three-direction design study this was built from
docs/BRIEF.md           brief, project set, asset and route notes
```

Everything outside `public/` — this README, the design record, the brief, the
deploy config — is deliberately not published. Verified: those paths 404 in the
deployed output.

## Deploy

Cloudflare Workers with static assets, built from Git. Any push to `main` builds
and deploys; other branches get preview URLs.

`wrangler.jsonc` declares an **assets-only Worker** (no `main`), so every request
is served straight from `public/` without invoking a Worker script — that is what
keeps requests free and unmetered.

One-time setup in the Cloudflare dashboard:

1. **Workers & Pages → Create application → GitHub**, pick `johnjazzi/johnazz.dev`.
2. Name the Worker **`johnazz-dev`** — it must match `name` in `wrangler.jsonc`
   or the Git build fails.
3. Build command: **leave empty**. Deploy command: `npx wrangler deploy`.
4. **Save and Deploy**, then confirm the `workers.dev` URL loads.
5. **Settings → Domains & Routes → Add custom domain** → `johnazz.dev`. The zone
   is already on Cloudflare, so the DNS record and certificate are created for
   you. Add `www.johnazz.dev` too if you want it.

Cost: **$0**. Static asset requests are free and unlimited, and Workers Builds on
the free plan includes 3,000 build minutes/month against a build that takes
seconds.

## Design

The home page is the **Fieldnotes** direction chosen from the study in
`design/study.html`: a sticky intro column, an asymmetric image spread, and a
dated index of earlier work. Editorial serif headings with Helvetica Neue body,
one hairline rule weight, no cards, no gradients.

Project marks are 16×16 pixel art authored as SVG (`assets/lincoln-8bit.svg`,
`assets/openvelo-16bit.svg`, `assets/versai-bubble.svg`). They are ink
silhouettes with the interior knocked out to the page paper colour, drawn flush
at a multiple of 16px with `image-rendering: pixelated`.

`design/study.html` also contains the two rejected directions (Index, Studio)
and is kept only as a record — it is not linked from the site.

## Status

Draft content, not yet published. Outstanding before this goes live:

- Personal photographs for the About spread.
- A clean Canonic capture (the current one shows a local working file path).
- Owner confirmation of the abbreviated résumé dates and product copy.
- The Nitrate support/privacy/terms pages stay at `johnjazzi.github.io/Nitrate/`
  by choice, so `/nitrate` here is a marketing page only and the App Store
  listing URLs are unchanged.

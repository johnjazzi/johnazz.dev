# johnazz.dev — first design study

Status: local exploration, not published. Draft copy, not an approved biography or resume.

## Primary surface
Explore: a personal index into selected work. About and product explanation are secondary. No generic SaaS hero/feature-grid composition.

## Composition recommendation
Editorial personal index: quiet top navigation, compact introductory copy, asymmetric project imagery, fine rules and captions. Personality should come from personal photographs and actual software, not decorative UI.

Explore three genuinely different compositions: Index (closest to cedri.cc restraint), Fieldnotes (editorial/image-led), Studio (typographic project index). The study will permit switching layouts.

Owner decision: **Fieldnotes** is the chosen direction, and it reads best on mobile. Production implementation should build Fieldnotes, not carry all three variants forward.

## Project set (owner-supplied, verified against the public GitHub account)
Featured: **Nitrate** (iPhone film-emulation camera) and **Canonic** (local-first writing workspace, links to `/canonic`).

Earlier work, dated index, newest first:

| Year | Project | Verified fact |
|---|---|---|
| 2026 | OpenVelo | Python TUI for virtual cycling; smart trainer, workouts, GPX, Strava. Public. |
| 2025 | Versai | Real-time translation built for iOS; on-device speech in, translation out. Public. |
| 2024 | Canonical v0 | Vue SaaS for product artifacts — the pre-pivot attempt at Canonic. `canonical-website` repo is empty; do not link it. |
| 2017 | Robo Lincoln | Character-level RNN trained on Lincoln's writing. Public; description "Write like Lincoln, except worse." |

The Canonical → Canonic entry is carried as a deliberate pivot note: the SaaS shape fought the local-first vision.

### Robo Lincoln mark
The only illustration in the set: a 16×16 pixel-art Lincoln in a stovepipe hat, authored as `assets/lincoln-8bit.svg` (ink silhouette with eyes knocked out of the fill, drawn on the page's paper colour). Legible at 48px and up, so it is displayed at 104px inside the 2017 entry and at 18px inline beside the project name. Do not scale it below 24px as a hero element.

## Proposed production routes
- `/`: selected work and short introduction; links to the two product sites.
- `/about`: concise biography and an edited personal photograph sequence, once provided.
- `/resume`: accessible HTML career summary and a reviewed downloadable PDF.
- `/nitrate`: self-contained Nitrate marketing page with real footage/stills and product-specific navigation.
- `/canonic`: self-contained Canonic marketing page with current real UI and product-specific navigation.
- Nitrate support/privacy/terms routes need a migration decision before replacing any live URLs. Preserve redirects and links used in the app/store; do not blindly move them.

Portfolio project summaries should explain what was designed/built and link directly to the product pages. Product pages should explain the product to prospective users, not read like portfolio case studies. Related but distinct visual voices: film imagery for Nitrate, writing/reading for Canonic.

## Existing sources inspected
- Reference: https://www.cedri.cc/about — small typography, sparse navigation, personal artifacts/imagery before career detail.
- Reference: https://paco.me — compact personal writing and restrained links/columns.
- Reference: https://rauno.me — more expressive spatial/typographic interaction; a contrast reference, not the proposed navigation model.
- `/Users/johnazzinaro/coding/john_azzinaro_resume.md`: includes Capital One from Sep 2025; contains quantitative achievement claims requiring owner review before publication. Additional projects section needs updating.
- `/Users/johnazzinaro/Documents/John_Azzinaro_Resume_.pdf`: older career content, begins with AWS; not suitable for automatic reuse as current download.
- `/Users/johnazzinaro/coding/canonic-local/README.md`: local-first, Git-backed document editor. This checkout does not establish the current Rust rewrite; source current screenshots/copy before implementation.
- `/Users/johnazzinaro/coding/canonic-marketing/README.md`: heading only, no existing marketing implementation to reuse there.
- `/Users/johnazzinaro/projects/nitrate-public-pages-final/index.html`: existing concise Nitrate positioning and support/legal links; left unchanged.

## Asset handling
The study uses copies of existing local Nitrate and Canonic imagery. Nitrate still is a product sample, not asserted to be a personal photograph or a newly verified render. Canonic capture contains draft working text and a local filesystem path; replace it with a clean current capture before publication. No image grading or generative alterations. Personal photographs still need selecting; do not substitute stock photography.

## Validation
Parent review: browser rendering at 1440px and 390px; all three direction switches; project preview navigation and back path; no broken image loads; no horizontal overflow; console/runtime errors; keyboard focus and reduced-motion behavior where applicable.

## Scope boundary
This iteration delivers a design study only. No Cloudflare account access, DNS changes, domain publication, production framework setup, résumé republication or changes to product repositories. Choose a direction before production implementation. An Astro/static build is a candidate, not an installed/verified deployment decision.

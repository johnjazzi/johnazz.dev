# johnazz.dev

Personal site for [johnazz.dev](https://johnazz.dev): selected work, a short
introduction, and product pages for Nitrate and Canonic.

Static HTML and one stylesheet. No build step, no framework, no third-party
scripts or fonts — open `index.html` or serve the directory and it works.

## Layout

```
index.html            home — Fieldnotes layout
nitrate/index.html    Nitrate product page      → /nitrate
canonic/index.html    Canonic product page      → /canonic
assets/site.css       the whole stylesheet
assets/*.png|jpg      product imagery
assets/*.svg          pixel glyphs + favicon
design/study.html     the three-direction design study this was built from
docs/BRIEF.md         brief, project set, asset and route notes
docs/*.png            render checks at 1440px and 390px
```

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
- Nitrate support/privacy/terms URLs must redirect to their live pages rather
  than being replaced by this site's routes.

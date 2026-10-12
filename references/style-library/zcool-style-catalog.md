# ZCOOL Style Catalog

Use this catalog after `zcool-style-index.json` exists. It describes reusable visual traits only. Do not copy source text, logos, products, characters, brand marks, page-specific claims, or exact compositions.

## Reference Set

- Source method: metadata image extraction from public page HTML.
- Asset folder: `assets/style-library/zcool-first-screen/`.
- Contact sheet: `assets/style-library/zcool-first-screen/contact-sheet.jpg`.
- Index file: `references/style-library/zcool-style-index.json`.
- Missing page: `ref-09` has no extractable metadata image and should not be used unless manually reviewed later.

## Catalog

| Ref | Style Name | Best For | Visual Traits | Match Keywords | Avoid Copying |
| --- | --- | --- | --- | --- | --- |
| ref-01 | Premium Blue Tech Keynote | TV, display, AI hardware, product launch, future-tech cover | blue-purple gradient, dark product silhouette, large negative space, clean right-side title block, soft horizon light | premium, tech, blue, keynote, hardware, future, elegant | exact device, title text, logo |
| ref-02 | Cinematic Automotive Report | car, energy, strategy, ESG, mobility, business keynote | large cinematic photo, dark teal overlay, desert/warm contrast, small editorial data panels | automotive, energy, cinematic, report, ESG | car model, brand marks, page copy |
| ref-03 | Neon Smart-Home Launch | smart home, IoT, AI platform, conference cover | black background, magenta/cyan light beams, bold central Chinese type, futuristic glow | smart home, neon, launch, future, platform | brand, exact title, gradient shape placement |
| ref-04 | Dark Sci-Fi Ring Keynote | future concept, technology strategy, keynote section page | black/navy background, glowing blue rings, centered title, restrained microtext | sci-fi, dark, ring, minimal, future, keynote | exact ring layout and copy |
| ref-05 | Calm Scenic Auto Keynote | mobility, tourism, lifestyle technology, formal cover | blue lake/sky photo, left-aligned text, calm premium atmosphere, soft horizon | calm, scenic, auto, premium, formal, landscape | landscape image, brand labels |
| ref-06 | Bright 3D Event Mascot | campaign, activity, consumer engagement, playful social deck | cyan background, saturated 3D mascot, big playful type, high energy | event, playful, 3D, mascot, campaign, youthful | mascot identity, platform name, slogan |
| ref-07 | Black-Red Hardware KV | smartphone, device, gaming, performance launch | black background, red gradient base, product close-up, high contrast type | phone, hardware, performance, black-red, premium | phone design, brand wordmark |
| ref-08 | Flat Heritage Illustration | culture, IP story, playful editorial insert | flat yellow background, black line-art illustration, large simple composition | illustration, heritage, IP, playful, yellow, line-art | character drawing, source story |
| ref-10 | Modular Industrial Product Grid | IoT, smart device, system diagram, industrial design | light gray background, modular hardware grid, subtle shadows, clean technical layout | industrial, modular, hardware, system, product grid | exact device shapes and labels |
| ref-11 | Soft Glass Portfolio | portfolio, UI case study, design summary, calm report | pale blue/white, translucent glass curve, very light typography, spacious layout | UI, portfolio, soft, glass, clean, airy | avatar, dates, exact copy |
| ref-12 | Energetic Commerce Campaign | retail, promotion, app campaign, consumer marketing | saturated blue, phone hero, orange/white accents, layered campaign graphics | commerce, app, promotion, energetic, phone | app artwork, campaign text, mascot |
| ref-13 | Orange App Analysis Report | app analysis, competitive research, consumer report, classroom assignment | orange field, large white Chinese title, floating rounded app icons, report cover layout | app report, analysis, orange, consumer, research | app logos, platform names, report title |
| ref-14 | Bold IP Poster Typography | IP, toy, mascot, entertainment, youth brand | strong blue-white type block, cute 3D character, poster-like crop | IP, mascot, bold, blue, cute, poster | character and exact giant lettering |
| ref-15 | Festive Retail IP Launch | festival, retail, food, consumer brand, CNY campaign | red/white festive palette, cute 3D character, product plus CTA style block | festive, retail, food, IP, red, celebration | character, brand marks, product packaging |

## Selection Defaults

- Formal business or report: prefer `ref-02`, `ref-05`, `ref-11`, or `ref-13`.
- Technology launch: prefer `ref-01`, `ref-03`, `ref-04`, `ref-07`, or `ref-10`.
- AI workflow or software product: prefer `ref-03`, `ref-04`, `ref-10`, `ref-11`, or `ref-13`.
- Consumer campaign: prefer `ref-06`, `ref-12`, `ref-14`, or `ref-15`.
- Product/hardware keynote: prefer `ref-01`, `ref-02`, `ref-07`, or `ref-10`.
- Playful IP or creator deck: prefer `ref-06`, `ref-08`, `ref-14`, or `ref-15`.

## Scoring Guide

Score each candidate from 0-2:

- Topic fit.
- Audience fit.
- Mood fit.
- Density fit.
- Route fit: PPTX / HTML / dual.
- Asset fit: screenshots, data, product image, chart, or abstract concept.

Choose the highest score as primary. Use secondary references only to borrow a narrow trait such as color warmth, chart treatment, or cover rhythm.

## Taste Overrides

- For AI article decks, do not default to dark sci-fi. Use it only if the content is launch-like; otherwise prefer `ref-10`, `ref-11`, or `ref-13` and add contrast through typography, diagrams, and spacing.
- For business reports, keep body pages calmer than the cover reference. Avoid poster-style giant type on every page.
- For dense methodology content, prefer modular grids, diagrams, and clean callouts over cinematic imagery.
- For source-heavy decks, make reference choice support legibility first: screenshots and quotations need stable frames, not decorative overlays.
- If the top-scoring reference feels generic or ugly for the actual topic, select the second-best reference and explain the aesthetic reason in `templates/20-style/style-match.md`.

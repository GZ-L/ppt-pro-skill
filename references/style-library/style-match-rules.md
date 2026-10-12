# Style Match Rules

Use this reference in the `20-style` stage when the user wants a high-aesthetic, keynote-style, editorial, launch, business, or visual PPT.

## Inputs To Compare

Extract these from the user's request and `deck-brief.md`:

- topic domain
- audience
- occasion
- final format: PPTX / HTML / dual
- mood: premium / technical / editorial / energetic / calm / futuristic / warm
- density: sparse keynote / balanced report / data-heavy / screenshot-heavy
- must avoid: brand conflicts, excessive decoration, unreadable small text

## Matching Process

1. Read `references/style-library/zcool-style-catalog.md`.
2. Load `references/style-library/zcool-style-index.json` when available.
3. Consider only entries with `status: ok`.
4. Inspect the referenced images visually if image access is available.
5. Score candidates by topic, audience, mood, density, route, and asset fit.
6. Match reusable visual traits, not source content.
7. Pick 1 primary style reference and up to 2 secondary references.
8. Write the match and taste judgment into `templates/20-style/style-match.md`.
9. Convert the match summary into `templates/20-style/style-board.md`.

## Aesthetic Judgment Rule

Do not mechanically imitate the highest-scoring reference. The director must make a taste call:

- Borrow only the traits that help the user's content.
- Reject traits that make the deck busy, childish, off-topic, low-contrast, or hard to edit.
- Adapt the reference into a new slide system: cover, section, body, diagram, data, and closing pages.
- Keep body pages more usable than the reference if the source is poster-heavy.
- Prefer clear hierarchy and strong spacing over decorative effects.

## Lightweight Collection Preference

Use `scripts/collect_style_refs.py` before browser automation. It reads page metadata and downloads public reference images. Open a page in a browser only when metadata images are unavailable and the user explicitly needs a real screenshot.

## What Can Transfer

- color mood and contrast
- composition rhythm
- title/body hierarchy
- spacing and grid behavior
- texture and lighting treatment
- chart, screenshot, or interface framing approach
- cover/body/section page rhythm

## What Must Not Transfer

- source text
- logos or brand marks
- product names or claims
- people, characters, or exact subjects
- artwork composition that would replicate the source
- page-specific copy, stats, charts, or screenshots

## Match Output Format

```markdown
# Style Match

## User Intent

- Topic:
- Audience:
- Mood:
- Density:
- Route:

## Candidate Scores

| Ref ID | Style Name | Topic Fit | Audience Fit | Mood Fit | Density Fit | Route Fit | Total | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Selected References

| Role | Ref ID | Asset | Why It Matches | Transferable Traits | Do Not Copy |
| --- | --- | --- | --- | --- | --- |
| Primary |  |  |  |  |  |
| Secondary |  |  |  |  |  |

## Director Aesthetic Judgment

- Borrow:
- Reject:
- Adapt:
- Readability risk:
- Content fit risk:

## Style Direction

- Style family:
- Color mood:
- Layout rhythm:
- Typography hierarchy:
- Visual material treatment:
- Chart/screenshot treatment:
- Avoid:
```

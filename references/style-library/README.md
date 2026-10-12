# Style Library

This folder stores lightweight visual style references for PPT Pro Skill.

## Policy

- Use these assets only for visual style analysis.
- Do not copy source page content, text, logos, product claims, people, brands, or specific creative concepts.
- Extract reusable traits only: color mood, layout rhythm, typography hierarchy, spacing, image treatment, texture, chart/interface treatment, and motion direction.
- Prefer metadata image extraction over browser screenshots. Browser screenshots are a fallback only when metadata images are unavailable.

## Recommended Collection Method

Run from the Skill folder:

```bash
python3 scripts/collect_style_refs.py
```

The script fetches public page HTML, extracts `og:image`, `twitter:image`, or JSON-LD `image`, downloads the image into `assets/style-library/zcool-first-screen/`, and writes `references/style-library/zcool-style-index.json`.

## Runtime Use

When a user asks for a high-aesthetic PPT or provides a topic:

1. Read `references/style-library/style-match-rules.md`.
2. Read `references/style-library/zcool-style-catalog.md`.
3. Read `references/style-library/zcool-style-index.json` if it exists.
4. Match by intent, audience, mood, density, and deliverable route.
5. Fill `templates/20-style/style-match.md`.
6. Use selected references only to write `style-board.md`.

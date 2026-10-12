# 40 Director Production

Use this reference after the user confirmation, outline, style match, style board, and route are ready.

## Single-Director Rule

This Skill owns all presentation decisions:

- content structure
- page count and slide jobs
- style selection and adaptation
- production route
- QA standard
- delivery summary

Do not call another PPT Skill as a second director. A local renderer, PowerPoint operation, or code library may be used only as a mechanical production step after this Skill has produced the confirmed package.

## Required Production Package

Before final generation, collect:

- `user-confirmation.md`
- `deck-brief.md`
- `outline.md`
- `style-match.md` when style references are used
- `style-board.md`
- `production-route.md`
- source files and citation notes

## Renderer Instructions

For editable PPTX:

- Use editable text, shapes, tables, charts, and image placeholders where possible.
- Avoid image-only slides unless the source itself is an image and editability is impossible.
- Keep speaker notes and source notes when relevant.
- Render or open the file for visual QA when tooling is available.

For visual web deck:

- Build previewable slides with stable dimensions.
- Verify that text is not overlapping or off-frame.
- Keep motion purposeful: reveal structure, sequence, or contrast.
- Export images, PDF, or video only when requested.

For dual version:

- Keep one shared outline and terminology.
- QA each version separately.
- Do not let the visual version drift away from the editable version's facts.

## Fallback

If the environment cannot create the requested file, deliver the complete director package and state exactly which production capability is missing. Do not claim a final deck exists unless the file exists and has been checked.

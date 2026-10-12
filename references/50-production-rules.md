# 50 Production Rules

Use this reference when generating, revising, exporting, or handing off final deck files.

## Production Modes

Choose one production mode from `production-route.md`:

- `pptx-generate`: create or revise an editable `.pptx`.
- `visual-web-generate`: create or revise a visual web slide project.
- `dual-generate`: produce both visual and editable versions.
- `package-only`: produce the confirmed director package because generation is unavailable.
- `review-only`: do not generate files; produce critique and QA output only.

## Required Production Log

Record every production run in `production-log.md`:

- selected mode
- input artifacts used
- production mechanics used
- generated files or package-only files
- verification commands or manual checks
- unresolved limitations
- next stage for failures

## File Existence Rule

- If a file is named as delivered, it must exist.
- If a file was not generated, label it as a handoff or planned output.
- If a generator creates image-only slides, state the editability limitation.
- If HTML slides need a dev server, start one before visual QA when feasible.

## Revision Discipline

Do not patch symptoms blindly:

- Content problem: return to 10 Story.
- Visual system problem: return to 20 Style.
- Wrong output format: return to 30 Route.
- Production mechanics mismatch: return to 40 Director.
- Broken generated files: stay in 50 Production and regenerate or repair.
- QA failure without clear cause: identify the earliest failed stage before editing.

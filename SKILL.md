---
name: ppt-pro-skill
description: Build and beautify professional presentation decks through a guozhi-ppt-director-style workflow with a required user confirmation layer, page-count/style/format decisions, built-in visual style library matching, editable PPTX or visual web deliverable planning, production, and QA. Use when the user asks for PPT, PowerPoint, PPTX, slide deck, presentation aesthetics, PPT美化, 高级感PPT, keynote-style slides, or a full PPT production flow. Do not use for one-off text summaries, ordinary document writing, or image generation tasks that do not need a reusable presentation workflow.
---

# PPT Pro Skill

Create a complete presentation production workflow: user confirmation, strategy, outline, style match, style board, deliverable route, director production contract, generated output, and aesthetic QA.

## Operating Principles

- Treat this as a deck director workflow, not a single prompt or template picker.
- Use one director logic only: the guozhi-ppt-director approach owns the brief, story, style, route, production rules, and QA.
- Do not hand the work to another PPT Skill as a separate director.
- Ask and confirm before final generation unless the user explicitly says "直接生成", "按默认来", "不用问", or equivalent.
- Preserve editability when the user must submit, teach, report, pitch, or collaborate with a `.pptx` file.
- Use the smallest reliable deliverable route that satisfies the confirmed user need. Do not force dual output unless it is confirmed.
- Use the built-in style library only for visual traits. Match precisely, then apply director aesthetic judgment; never copy source page content, text, logos, brands, exact subjects, or claims.
- Never paste secrets, private links, cookies, tokens, or private company material into public templates or logs.

## Default Output Contract

For non-trivial PPT work, produce or update these artifacts before final generation:

1. `user-confirmation.md` - inferred decisions, questions asked, explicit confirmation, and defaults accepted.
2. `deck-brief.md` - audience, purpose, occasion, thesis, constraints, deliverable.
3. `outline.md` - page-by-page message, slide job, visual idea, speaker note.
4. `style-match.md` - selected style-library references, scoring, and aesthetic adaptation.
5. `style-board.md` - visual language, color, typography, layout rules, cover direction.
6. `production-route.md` - confirmed deliverable route and verification plan.
7. `director-production.md` - single-director production contract and mechanical rendering notes.
8. `production-log.md` - generated files, checks, and limitations.
9. `qa-report.md` - story, visual hierarchy, editability, accessibility, and delivery checks.

Use `outputs/<deck-slug>/` as the default work folder when creating real deck artifacts in a project.

Use the staged folder hierarchy as the production spine:

```text
00-intake -> 10-story -> 20-style -> 30-route -> 40-director -> 50-production -> 90-qa
```

## Workflow

0. Run the question and confirmation layer.
   - Read `references/00-process-architecture.md`, `references/00-intent-routing.md`, and `references/00-question-layer.md`.
   - Classify the request as new deck, beautify existing deck, editable PPTX, visual web deck, dual version, or review only.
   - Summarize inferred page count, final deliverable, style direction, audience, and rewrite boundary.
   - Ask only questions that change the result, usually 3-5 compact questions.
   - Offer 2-3 style-library candidates when style matters.
   - Do not produce final PPTX/HTML/PDF files until confirmation is recorded in `templates/00-intake/user-confirmation.md`, unless the user explicitly asks to proceed with defaults.

1. Build the deck brief.
   - Use `templates/00-intake/deck-brief.md`.
   - Identify audience, occasion, final format, page count, language, speaking time, deadline, source material, and editability requirement.
   - If the user asks to proceed with defaults, use Chinese, 8-12 pages, 3-5 minutes, editable PPTX route, and style-library match plus director judgment.

2. Extract the thesis and slide jobs.
   - Convert source material into one core thesis and 3-5 supporting arguments.
   - Use `templates/10-story/outline.md`.
   - Give each slide one job only: hook, context, problem, method, framework, evidence, demo, comparison, case, result, risk, next step, or close.
   - Put detail into speaker notes instead of crowding the slide.

3. Design the style board.
   - Read `references/20-aesthetic-system.md`.
   - Read `references/style-library/style-match-rules.md` and use `templates/20-style/style-match.md` when a reusable style reference is useful.
   - If the style library is missing or stale, run `scripts/collect_style_refs.py` to refresh public metadata image references without opening pages in a browser.
   - Pick one primary style reference and up to two secondary references.
   - Make a taste call: borrow, reject, adapt. Style must support the user's content, not imitate the reference.
   - Use `templates/20-style/style-board.md`.
   - Do not let style override clarity or readability.

4. Choose the production route.
   - Read `references/30-route-decision.md`.
   - Use editable PPTX route for formal submission, business reporting, schoolwork, or team editing.
   - Use visual web route for confirmed motion, recording, product-launch feeling, or short-video reuse.
   - Use dual route only when the user confirms the extra work.
   - Record the decision in `templates/30-route/production-route.md`.

5. Prepare the director production contract.
   - Read `references/40-director-production.md`.
   - Use `templates/40-director/director-production.md`.
   - Do not introduce another PPT Skill into the chain. If a local generator, PowerPoint, or code library is used, treat it as a mechanical renderer and keep this Skill responsible for decisions and QA.
   - If production cannot run in the current environment, return the confirmed director package and state the missing capability.

6. Generate or revise the deck.
   - Read `references/50-production-rules.md`.
   - Use `templates/50-production/production-log.md`.
   - For `.pptx`, preserve editable objects and use native shapes, text boxes, charts, and layout masters when possible.
   - For visual web decks, build a real previewable slide project and verify it visually before claiming completion.
   - For beautification of an existing deck, preserve the user's meaning and required content; change layout, hierarchy, typography, spacing, color, imagery, and chart treatment.

7. Run presentation QA.
   - Read `references/90-qa-checklist.md`.
   - Use `templates/90-qa/qa-report.md`.
   - Revise from the earliest failed stage if there are blocking issues in confirmation, logic, density, hierarchy, readability, editability, visual consistency, source attribution, or final file delivery.

## Resource Routing

- Read `references/00-process-architecture.md` before non-trivial runs or when the package structure is unclear.
- Read `references/00-intent-routing.md` before choosing the workflow.
- Read `references/00-question-layer.md` before production or when important inputs are missing.
- Use `templates/00-intake/user-confirmation.md` before final generation.
- Use `templates/00-intake/deck-brief.md` for input capture and defaults.
- Use `templates/10-story/outline.md` for page planning.
- Use `templates/20-style/style-board.md` for visual direction.
- Use `templates/20-style/style-match.md` when selecting a style-library reference.
- Use `templates/30-route/production-route.md` for route selection.
- Use `templates/40-director/director-production.md` for single-director production instructions.
- Use `templates/50-production/production-log.md` when generating, revising, exporting, or handing off deck files.
- Use `templates/90-qa/qa-report.md` before delivery.
- Read `references/20-aesthetic-system.md` for PPT美化, 高级感, keynote-style, visual hierarchy, typography, color, spacing, charts, and image rules.
- Read `references/style-library/README.md` before refreshing or expanding the visual style library.
- Read `references/style-library/style-match-rules.md` before matching user intent to style-library assets.
- Read `references/style-library/zcool-style-catalog.md` when choosing a reference from the built-in ZCOOL style library.
- Read `references/30-route-decision.md` before choosing editable PPTX, visual web, dual output, or review-only.
- Read `references/40-director-production.md` before production.
- Read `references/50-production-rules.md` before claiming generated files or package outputs.
- Read `references/90-qa-checklist.md` before claiming the deck package is ready.

## Validation

After editing this Skill package, run:

```bash
python3 /Users/guozhi/.codex/skills/standard-skill-maker/scripts/validate_skill.py ppt-pro-skill
python3 "${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-creator/scripts/quick_validate.py" ppt-pro-skill
```

To refresh the lightweight visual style library, run:

```bash
python3 scripts/collect_style_refs.py
```

For realistic prompt checks, test:

```text
Use ppt-pro-skill to turn this article into a 10-page high-aesthetic editable PPTX.
```

```text
Use ppt-pro-skill to create a keynote-style visual web deck and PPTX route recommendation.
```

The Skill passes when it asks for or records confirmation, creates the planning artifacts, chooses a justified route, uses style-library references with aesthetic adaptation, records production or fallback outputs, and runs QA before delivery.

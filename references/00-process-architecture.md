# Process Architecture

Use this reference at the start of any non-trivial run to keep the workflow layered instead of treating every resource as one flat folder.

## Layered Pipeline

The package is organized as a staged production line:

| Stage | Purpose | Required Output | Next Gate |
| --- | --- | --- | --- |
| 00 Intake | Identify user intent, ask key questions, and record confirmation | `user-confirmation.md`, `deck-brief.md` | User confirmed or explicitly accepted defaults |
| 10 Story | Turn material into a deck argument | `outline.md` | Each slide has one job and one message |
| 20 Style | Match references and define the visual system | `style-match.md`, `style-board.md` | Style supports audience, readability, and content |
| 30 Route | Choose production route | `production-route.md` | Route matches required deliverable |
| 40 Director | Prepare single-director production contract | `director-production.md` | Production mechanics do not introduce another director |
| 50 Production | Generate or revise deck files | `production-log.md` plus PPTX, HTML project, PDF, or handoff package | Real files exist or fallback is declared |
| 90 QA | Check and revise | `qa-report.md` | Pass, revise one stage, or declare blocked |

## Stage-Gate Rule

Do not skip from source material directly to a final deck unless the user explicitly requests a rough draft.

Before moving forward:

- Intake must state the user's primary intent.
- Confirmation must record the page count, style direction, route, and rewrite boundary.
- Story must have a thesis and page-by-page outline.
- Style must define visual rules, not just adjectives, and must explain reference adaptation.
- Route must explain why editable PPTX, visual web, dual output, or review-only is chosen.
- Director production must keep this Skill as the only decision layer.
- QA must state pass, needs revision, or blocked.

## Folder Boundaries

- `SKILL.md` is the control layer.
- `references/` contains decision logic and standards.
- `templates/` contains artifacts created during a run.
- `agents/` contains UI metadata.
- Do not add unrelated generator prompts, essays, screenshots, or arbitrary examples at the root.

## Failure Loops

- Unclear user intent or missing confirmation: return to 00 Intake and ask only the missing question that changes the result.
- Weak thesis or crowded pages: return to 10 Story.
- Vague style or poor readability: return to 20 Style.
- Wrong output format: return to 30 Route.
- Production mechanics unavailable: return to 40 Director and use fallback mode.
- Generated deck fails QA: return to the earliest failed stage instead of patching symptoms.

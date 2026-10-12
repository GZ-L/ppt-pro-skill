# Intent Routing

Use this reference before creating or revising any presentation package.

## Primary Intent Classes

Classify the user's request into one primary intent and optional secondary intents.

| Intent | User Signals | Default Action |
| --- | --- | --- |
| New deck | "做一个PPT", "turn this article into slides", "presentation", "汇报" | Build brief, outline, style board, then choose route |
| Beautify existing deck | "美化这个PPT", "高级一点", "改好看", existing `.pptx` or screenshots | Diagnose current deck, preserve meaning, revise style and layout |
| Editable PPTX | ".pptx", "要交作业", "公司汇报", "能改", "PowerPoint" | Route A unless motion version is also required |
| Visual web deck | "网页PPT", "动效", "发布会", "录屏", "视频化" | Route B only after confirmation |
| Dual version | "既能交又好看", "PPT+视频", "可编辑也要酷", "正式版和视觉版" | Route C |
| Review only | "看看逻辑", "审一下", "找问题", "不要改" | Produce critique and QA report, do not generate final files |

## Secondary Intent Tags

Add tags when relevant:

- `high-aesthetic`
- `business-report`
- `school-assignment`
- `pitch`
- `lesson`
- `product-launch`
- `short-video`
- `data-heavy`
- `screenshot-heavy`
- `brand-constrained`
- `source-citation-required`

## Routing Defaults

- If the user asks for a formal PPT or says `.pptx`, recommend editable PPTX unless they also confirm motion or video.
- If the user asks for "好看", "高级", or "发布会感", propose 2-3 style-library options before production.
- If the user asks for both editability and visual impact, recommend dual version but confirm the extra work first.
- If the user provides an existing deck, do not rewrite the argument until you diagnose whether it needs slide-level beautification or story rebuild.
- If the user says "只看一下" or "先审", do review-only mode and do not edit files.

## Ask-Limit Rule

Ask only questions that change the result:

- final deliverable format
- page count or time limit
- audience or occasion
- whether editability is mandatory
- style direction from 2-3 curated options
- brand/template constraints
- whether existing content may be rewritten

If these can be inferred, summarize the assumptions and ask for confirmation. Proceed without confirmation only when the user explicitly says to use defaults.

## Misroute Warnings

- Do not send an editable-PPTX request only to an HTML/front-end route.
- Do not claim a generated `.pptx` is editable without checking the file or stating the limitation.
- Do not make a visual poster deck when the user needs a dense business report.
- Do not ask for brand assets if the user already accepted a generic style.
- Do not introduce another PPT Skill as a second director.

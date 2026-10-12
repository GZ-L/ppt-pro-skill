# Question Layer

Use this reference before producing final deck files. The goal is to prevent silent assumptions about page count, style, format, and rewriting boundaries.

## Confirmation Rule

Do not generate final PPTX, HTML, PDF, or image exports until one of these is true:

- The user confirms the proposed brief, page count, style, and route.
- The user explicitly says to proceed without questions, such as "直接生成", "按默认来", "不用问", "你定".
- The task is review-only and does not create final files.

If the user provides strong constraints upfront, summarize them and ask for confirmation instead of repeating unnecessary questions.

## Ask These First

Ask only the questions that materially change the output. Prefer 3-5 questions:

1. Page count or speaking time: exact page count, range, or presentation length.
2. Final deliverable: editable PPTX, visual web deck, dual version, PDF export, or review only.
3. Audience and occasion: boss/client/class/investor/followers/internal team.
4. Style direction: choose from 2-3 style-library candidates or let the director decide.
5. Rewrite boundary: can the structure be rebuilt, or must the source order and wording stay close?

Optional questions only when relevant:

- Brand assets or required template.
- Need citations/source notes.
- Need speaker notes.
- Need charts, diagrams, screenshots, or source images preserved.
- Deadline or file compatibility requirement.

## Confirmation Prompt Shape

Use a compact confirmation block:

```markdown
我先确认 5 个生产参数，确认后再生成：

1. 页数/时长：我建议 [x] 页，适合 [x] 分钟；你要固定页数吗？
2. 交付格式：我建议 [editable PPTX / visual web / dual]，是否确认？
3. 风格方向：我建议 [ref-id/style name]，备选是 [ref-id] / [ref-id]；你选哪个？
4. 内容改写：我会 [重构为演示逻辑 / 保留原文顺序]，是否可以？
5. 附加要求：是否需要演讲备注、引用页、品牌色或指定模板？
```

## Default Package

If the user says to proceed with defaults:

- Language: Chinese.
- Page count: 8-12 pages.
- Speaking time: 3-5 minutes.
- Route: editable PPTX unless the user requests motion/web/video.
- Style: style-library match plus director aesthetic judgment.
- Rewrite boundary: preserve facts and citations, rebuild slide logic for clarity.

## Do Not Ask

- Do not ask for brand assets if the user has accepted a generic style.
- Do not ask for every possible preference.
- Do not ask the user to choose from many style references; provide 2-3 curated options.
- Do not proceed silently just because defaults exist.

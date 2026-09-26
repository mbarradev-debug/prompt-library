# Prompts

A personal library of reusable prompts for AI-assisted work, each one in English (`en/`) and Spanish (`es/`) under the same file name.

Placeholders in square brackets, like `[PROJECT_NAME]`, are meant to be replaced before using a prompt. Delete any line that does not apply.

## Index

| Prompt | Use it when | Tool |
|---|---|---|
| [portfolio-from-reference-site](en/portfolio-from-reference-site.md) · [es](es/portfolio-from-reference-site.md) | Designing a portfolio that keeps a reference site's visual language, with your own structure and your CV as the source | Claude (design) |
| [fill-agents-md](en/fill-agents-md.md) · [es](es/fill-agents-md.md) | A repo has no agent instructions yet (AGENTS.md / CLAUDE.md) | Claude Code |
| [add-language-browser-detection](en/add-language-browser-detection.md) · [es](es/add-language-browser-detection.md) | Adding a second language chosen from the browser, with a switcher and hreflang SEO | Claude Code |
| [choose-skill-for-task](en/choose-skill-for-task.md) · [es](es/choose-skill-for-task.md) | Deciding which installed skill fits a task, without touching code | Claude Code |
| [audit-to-linear-issues](en/audit-to-linear-issues.md) · [es](es/audit-to-linear-issues.md) | Auditing with skills and tracking the findings in a few grouped Linear issues | Claude Code + Linear |

## File format

Every prompt starts with a short frontmatter block:

```markdown
---
title: What the prompt does
tool: Where it runs
use-when: The situation it is for
requires: What must exist before using it
tags: [topic, topic]
---
```

## Adding a prompt

1. Write it as general as possible: replace project-specific details with placeholders.
2. Save the English version in `en/` and the Spanish version in `es/`, with the same kebab-case file name.
3. Add a row to the index above.

---
title: Fill AGENTS.md and CLAUDE.md for an existing repo
tool: Claude Code (works with any coding agent)
use-when: A repo has no agent instructions yet, or they are empty or outdated
requires: A repo with code in it
tags: [agents-md, claude-md, onboarding, conventions]
---

This project has no content in AGENTS.md or CLAUDE.md. I want to fill them so any agent working in this repo understands the project and follows my rules without me repeating them in every prompt.

## How to do it
1. First explore the repo (package manifest, folder structure, TypeScript/lint/formatter config, where content and data live, any reference or docs folders, the README) to get the real facts: versions, commands and paths. Do not invent anything. If something cannot be confirmed, leave it as a question at the end.
2. Write all the content in `AGENTS.md`, in English.
3. Leave `CLAUDE.md` with a single line, `@AGENTS.md`, so Claude Code imports it without duplicating content.
4. Show me the full draft and wait for my OK before saving.

## What AGENTS.md must include
Only what an agent cannot infer by reading the code. Nothing the README already says. About 150 lines at most, with short sections and lists.

- **Project overview**: what the project is and who it is for, in two or three lines.
- **Stack and real versions**, plus the commands for dev, build, lint and test.
- **Structure**: what goes in each main folder and where content, config and shared components live.
- **Design rules**: which visual decisions are fixed (colors, typography, spacing, references) and where the theme tokens are defined. No invented content: placeholders stay until I provide the real material.
- **Read-only folders**: [READ_ONLY_FOLDERS, e.g. references/, vendor/]. They are never modified and stay out of the build, type checking and linting.
- **Languages**: [CONTENT_LANGUAGE] for the product's content; English for code, comments, commits, README and issues.
- **Accessibility and motion**: AA contrast, touch targets of at least 44px, `aria-label` on icon-only buttons, `prefers-reduced-motion` respected, no horizontal scroll at 360px. Adjust to what applies to this project.
- **Workflow**:
  - Show a short plan and wait for my OK before editing.
  - Work is tracked in [ISSUE_TRACKER, e.g. Linear project "[PROJECT_NAME]"], one branch per issue.
  - Never commit, push or merge unless I ask.
  - Run lint and build before calling a task done.
- **Skills per task type**: which installed skill to use for which kind of work (for example UI/UX rules, visual polish, quality audit, issue-to-PR). List only skills that actually exist in this environment.
- **Pending decisions**: open questions the agent must not resolve on its own.

## At the end
Give me a short list of what you could not confirm in the repo, so I can fill it in myself.

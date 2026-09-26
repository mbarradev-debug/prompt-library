---
title: Choose the best installed skill for a task (read-only)
tool: Claude Code
use-when: You are about to start a type of work and do not know which of your installed skills fits it best
requires: Skills installed at user, project or plugin level
tags: [skills, planning, read-only]
---

Read-only task: do not modify, create or delete any file, do not install anything and do not run any skill. Only analyze and recommend.

## Context
I am working on [PROJECT_DESCRIPTION, e.g. a Next.js site with Chakra UI]. I am about to work on [TASK_AREA, e.g. micro-interactions and animations]. Specifically:
- [NEED_1]
- [NEED_2]
- [NEED_3]

## What I need
1. List every available skill: user skills (`~/.claude/skills`), project skills (`.claude/skills`) and skills from installed plugins. Read the SKILL.md of the ones related to [TASK_AREA], not just their description.
2. Evaluate which ones actually help with this work, based on what each skill really covers, not on its name.
3. Recommend the best option, or a combination if none covers everything, and the order in which to use them.

## Response format
- A table of the relevant skills: name, what it covers for this task, what it does not cover, and how well it fits this case (high, medium or low).
- A final recommendation in 2 or 3 sentences, with the reason.
- Gaps: which of my needs no skill covers.
- How to invoke the recommended skill, with a concrete example prompt for this project.

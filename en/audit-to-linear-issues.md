---
title: Audit with skills, then track the findings in a few Linear issues
tool: Claude Code with the Linear MCP connected
use-when: Before a larger piece of work, you want an audit of the current state and traceability in Linear without flooding it with tiny issues
requires: Linear MCP, the skills you want to audit with
tags: [linear, audit, planning, traceability]
---

I want traceability in Linear for the [WORK_AREA, e.g. animation and micro-interaction] work in this project. There are two phases. Do not modify code in either one.

## Phase 1: Audit (read-only)
Audit the current state of the project with these skills, in this order:
1. /[SKILL_1]: [WHAT_TO_REVIEW_WITH_IT]
2. /[SKILL_2]: [WHAT_TO_REVIEW_WITH_IT] (critique mode only, apply no changes)
3. /[SKILL_3]: [WHAT_TO_REVIEW_WITH_IT]

For each finding, give the affected file, the problem in one line and the proposed solution. Also include these known gaps that no skill covers: [KNOWN_GAPS, or remove this line].

When you finish, show me a summary of the findings grouped into at most [MAX_ISSUES, e.g. 3] themes and wait for my OK before touching Linear.

## Phase 2: Linear
Once I approve, use the Linear MCP directly. Do not use planning skills that generate many issues.

1. Look for the "[LINEAR_PROJECT]" project. If it does not exist, create it with a short description in English.
2. Create at most [MAX_ISSUES] issues, grouping findings instead of one issue per finding. Use the themes from the audit summary I approved.
3. Each issue is written in English, with this description structure:
   - Context: one or two lines
   - Findings: list of findings with their file
   - Scope: what will be done
   - Acceptance criteria: a verifiable checklist
   - Skill to use: which one to apply when implementing it
   - Suggested branch: branch name
4. If there are decisions that are mine to make (for example two skills or references recommending conflicting values), record them in the relevant issue as a pending decision. Do not resolve them.
5. Add simple labels and a priority, and mark the dependencies between issues in the order they should be done.

When you finish, give me the list of created issues with their identifier and title. Do not start implementing any of them.

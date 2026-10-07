---
title: Rewrite the draft of one period of a narrative game's story, ready to move into Ink
tool: Claude or any writing assistant
use-when: You write a narrative game's story by periods (one year, chapter or stage per chat) and want to polish one draft without it mixing with the others
requires: The period's draft attached, with the period and the protagonist's age stated in the file
tags: [writing, narrative, game-design, ink]
---

I am attaching the draft of one specific period of my video game's story. The period ([UNIT, e.g. year, chapter or stage]) and the protagonist's age are stated in the file.

## Game context
- Genre and style: [GENRE_AND_STYLE, e.g. a 16-bit pixel art RPG inspired by Undertale and Stardew Valley].
- Premise: [PREMISE, e.g. a boy who has a seizure at 15 and is diagnosed with epilepsy].
- What the story covers: [OVERALL_ARC, e.g. year by year until 30: school, university, friendships, relationships].
- Main source: [SOURCE, e.g. the draft is based on my real experience with the condition and is the main reference, or delete this line].

## What to do
Rewrite only this period, improving the writing and the structure, in a style halfway between a novel and a script: prose narration, clearly separated scenes and clear dialogue, keeping in mind that I will later move them into Ink.

## Rules
- Work only with what happens in this period. Do not jump ahead or invent events from other periods.
- If the draft mentions something from earlier periods that is not explained, do not fill it in: mark it with a comment `<!-- like this -->`.
- Respect the facts and the characters. Do not add major events or remove the ones I wrote.
- [TONE_RULE, e.g. portray the condition accurately, without dramatizing it or using it to generate pity; this is a story about courage, growth and strength, not only about the illness].
- Use the same kind of comment for anything ambiguous, contradictory or [INACCURACY_TO_WATCH, e.g. medically inaccurate].

## Deliverable
- A .md file with the period and age as the title (`#`) and one subheading per scene (`##`).
- At the end, a short list of the `<!-- -->` comments you left, so I can review them in one go.

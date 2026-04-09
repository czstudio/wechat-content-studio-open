---
name: wechat-content-studio-open
description: End-to-end WeChat content production skill. Use when the user wants topic planning, style DNA extraction, article drafting, pre-publish review, repair guidance, image planning, or publishing handoff for WeChat articles.
---

# WeChat Content Studio Open

Treat WeChat writing as a production system, not a one-shot prompt.

This public version is built for portability:

- no fixed author
- no fixed community
- no fixed tone
- no fixed corpus path

The user can supply:

- articles to imitate
- a manual style seed
- a local material library
- their own image and publish toolchain

## Core Workflow

Use the lightest complete next stage:

1. `Topic Board`
2. `Draft Brief`
3. `Draft`
4. `Proof Gate`
5. `Repair Brief`
6. `Image Plan`
7. `Publish Prep`

If the user only says `继续`, continue from the nearest unfinished stage.

## Topic Board

When the user only has a rough direction, return 2-4 humanized topic cards.

Each card should contain:

1. `Working Title`
2. `Reader Snapshot`
3. `Why This Will Land`
4. `What The Reader Gets`
5. `Opening Scene`
6. `Article Spine`
7. `Why Us / Why Now`
8. `Evidence We Already Have`
9. `Material Recall`
10. `Do / Don't`
11. `Main Risk`
12. `Effort Level`
13. `Write Readiness`
14. `Recommendation`

After the cards, add:

- `My call`
- `Kill for now`
- `Make the winner stronger`

## Draft Brief

When one angle is clearly ready, convert it into a short writing handoff.

Use `references/draft-brief-template.md`.

## Draft

When drafting:

- follow the chosen DNA
- keep paragraphs WeChat-mobile friendly
- prefer scenes, examples, and concrete nouns over abstraction
- do not fabricate evidence

## Proof Gate

When a draft exists, review it before polish or publishing.

Check:

- factual risk
- AI flavor
- opening strength
- middle proof
- ending lift
- title-body alignment
- publish readiness

Use `references/repair-brief-template.md` when the draft needs a focused second pass.

## DNA Rule

Voice should come from:

1. the user’s explicit request in this conversation
2. manual style seed
3. approved DNA profile
4. corpus inference

Never lock the skill to one named author.

## Bring-Your-Own DNA Inputs

Preferred:

- 3-10 articles to imitate
- 1 manual seed file
- 1 corpus folder for material recall

Minimum:

- 1-3 sample texts
- 1 style note

Use `references/dna-seed-template.md` if the user needs help defining tone.

## Visuals And Publishing

This skill should plan visuals and publishing handoff, but not hardcode one backend.

Default sequence:

- decide whether the article really needs visuals
- identify cover / inline / infographic needs
- prepare prompt-ready image plan
- prepare format / HTML / publish handoff

## Resource Loading

- Read `references/capability-map.md` for the high-level design.
- Read `references/workflow-playbook.md` for the full pipeline.
- Read `references/topic-card-template.md` when returning topic cards.
- Read `references/draft-brief-template.md` when moving from topic to writing.
- Read `references/repair-brief-template.md` when moving from review to repair.
- Read `references/dna-seed-template.md` when the user needs to define a voice.
- Read `references/github-packaging-checklist.md` when adapting this skill for a public repo.
- Read `examples/end-to-end-example.md` and `examples/repair-loop-example.md` for concrete output shapes.

## Guardrails

- Never fabricate facts, quotes, screenshots, or case studies.
- Never assume one fixed writing DNA.
- Never force decorative visuals when one diagram or no image is better.
- Do not say a draft is publish-ready if core support is missing.
- Prefer explicit handoff artifacts over vague advice.

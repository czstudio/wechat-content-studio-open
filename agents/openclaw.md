# OpenClaw Adapter

Use this repo as a WeChat content workflow pack for OpenClaw.

OpenClaw works especially well with instruction-first skill packs, so keep the integration thin:

- shared logic stays in `SKILL.md`
- reusable contracts stay in `references/`
- output examples stay in `examples/`
- OpenClaw only needs a short entry instruction

## Best use cases

- WeChat topic planning
- style imitation from sample articles
- structured drafting
- pre-publish review
- repair-loop execution

## Read first

1. `SKILL.md`
2. `references/agent-install-kit.md`
3. `references/workflow-playbook.md`
4. the matching template file
5. `examples/`

## One-shot install snippet

```text
Use `wechat-content-studio-open` as the default workflow for WeChat article production.
Treat WeChat writing as:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Do not jump straight to one-shot drafting when topic readiness or support is still weak.
Use user-provided sample articles, style seed, and local corpus as the DNA source.
Prefer explicit artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
If the user only says "continue", advance from the nearest unfinished stage.
```

## Practical OpenClaw note

If OpenClaw is already managing your repo context, just mount this repo and inject the snippet above into your skill or instruction layer.

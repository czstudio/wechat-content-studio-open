# Codex / Codex CLI Adapter

Use `wechat-content-studio-open` when the user wants any part of the WeChat content workflow:

- topic planning
- writing DNA extraction
- article drafting
- pre-publish review
- repair guidance
- image planning
- publish handoff

Read in this order:

1. `SKILL.md`
2. `references/workflow-playbook.md`
3. `references/topic-card-template.md` or `references/draft-brief-template.md` or `references/repair-brief-template.md`
4. `examples/`

Preferred output rule:

- If the user only has an idea -> return `Topic Board`
- If the winner is clear -> add `Draft Brief`
- If a draft exists -> run `Proof Gate`
- If the draft is weak but repairable -> add `Repair Brief`

Copy-paste install snippet:

```markdown
Use `wechat-content-studio-open` as the default WeChat writing workflow.
Treat WeChat writing as:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Prefer explicit handoff artifacts over vague advice.
Use user-provided sample articles, style seed, and corpus as the DNA source.
```

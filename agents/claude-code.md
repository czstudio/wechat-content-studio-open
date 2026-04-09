# Claude Code Adapter

This adapter helps Claude Code treat the repo as a reusable content operating system, not a one-shot writing prompt.

Use this package when the user wants:

- WeChat article topic ideation
- style imitation from examples
- structured drafting
- article review before publishing
- repair instructions instead of full rewrites

Read first:

1. `SKILL.md`
2. `references/agent-install-kit.md`
3. `references/workflow-playbook.md`
4. the matching output template

Preferred behavior:

- do not jump straight to full draft generation if topic is not ready
- do not give generic review advice if a `Repair Brief` is possible
- do not lock style to one author; use user-provided examples

Copy-paste install snippet:

```markdown
When working on WeChat articles, use this repo as a structured workflow:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Do not treat the task as one-shot generation.
Use the user's sample articles, style seed, and local corpus to infer DNA.
Prefer concrete handoff artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
```

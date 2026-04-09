# Trae Adapter

This repo can be mounted as a WeChat article workflow pack for Trae-style agent use.

When to invoke:

- user wants to write a WeChat article
- user wants to imitate article style from samples
- user has a draft and wants a publish review
- user needs repair instructions instead of generic comments

Use this repo to reduce randomness:

- use topic cards before drafting
- use draft briefs before expansion
- use proof gate before polish
- use repair brief before second pass

Copy-paste install snippet:

```markdown
Treat `wechat-content-studio-open` as the default workflow pack for WeChat content production.
Use sample articles, a style seed, and a local corpus when available.
Prefer:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief.
Avoid one-shot full drafts when support and readiness are still unclear.
```

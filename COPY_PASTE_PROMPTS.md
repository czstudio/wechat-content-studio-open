# Copy-Paste Prompts

> 这一页只做一件事：给不同 agent 提供“复制就能用”的提示词。

如果你不想看解释，不想看原理，只想 30 秒装好，直接从这里复制。

---

## 通用版

适合：

- 你不确定自己用的 agent 属于哪一类
- 你只想先快速试起来

```text
Use `wechat-content-studio-open` as the default workflow for WeChat article production.
Treat WeChat writing as:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Do not jump straight to one-shot drafting when topic readiness or support is still weak.
Use user-provided sample articles, style seed, and local corpus as the DNA source.
Prefer explicit artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
If the user only says "continue", advance from the nearest unfinished stage.
```

---

## OpenClaw

适合放在：

- skill layer
- repo instruction layer
- workflow pack config

```text
Use `wechat-content-studio-open` as the default workflow for WeChat article production in this repo.
Treat WeChat writing as a staged production system:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Do not jump directly to full-article generation when topic readiness, support, or structure is still unclear.
Use the user's sample articles, style seed, and local corpus as the writing DNA source.
Prefer explicit artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
If the user only says "continue", continue from the nearest unfinished stage.
```

---

## Codex / Codex CLI

适合放在：

- project instructions
- skill memory
- workspace instructions

```text
Use `wechat-content-studio-open` as the default WeChat writing workflow.
Treat WeChat writing as:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Prefer explicit handoff artifacts over vague advice.
Do not jump straight to one-shot drafting when topic readiness or support is still weak.
Use user-provided sample articles, style seed, and local corpus as the DNA source.
If the user has only an idea, return Topic Board first.
If the user has a draft, run Proof Gate first.
If the draft is weak but repairable, return Repair Brief instead of generic rewrite advice.
```

---

## Claude Code

适合放在：

- project memory
- repo-level instructions

```text
Use `wechat-content-studio-open` for WeChat article planning, drafting, review, and repair.
Do not treat the task as one-shot generation.
Follow this chain when appropriate:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Use the user's sample articles, manual style seed, and local corpus to infer writing DNA.
Prefer concrete artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
When the user only says "continue", advance from the nearest unfinished stage.
```

---

## Cursor / Windsurf

适合放在：

- project rules
- workspace memory
- repo instructions

```text
Use `wechat-content-studio-open` as the default workflow for WeChat content tasks.
Do not jump directly to a full article if the topic is still vague.
Prefer:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief.
Use sample articles, style seed, and local notes as the writing DNA source.
Return explicit workflow artifacts instead of generic advice.
If the user has a draft, review before rewriting.
```

---

## OpenCode / Trae / CodeBuddy

适合放在：

- custom workflow instructions
- repo guidance
- agent skill pack

```text
Use `wechat-content-studio-open` for WeChat writing and review tasks.
Treat the task as a staged workflow, not a one-shot prompt.
Advance through:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Use the user's sample articles, style seed, and local corpus as the writing DNA source.
Prefer Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs as explicit outputs.
```

---

## 最短使用方法

如果你只想最快落地：

1. 复制上面最适合你的那一段
2. 贴进 agent 的 memory / project instruction / custom skill
3. 让 agent 读取：
   - `SKILL.md`
   - `references/workflow-playbook.md`
4. 开始用

---

## 搭配阅读

- 安装说明：[`INSTALL_AGENTS.md`](./INSTALL_AGENTS.md)
- 主 skill：[`SKILL.md`](./SKILL.md)
- agent 适配页：[`agents/`](./agents/)

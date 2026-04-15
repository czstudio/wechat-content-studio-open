# Copy-Paste Prompts

> 这一页是“真能装”的版本。
>
> 不是只给你一段行为提示，而是先告诉 agent：
> 仓库在哪、要读哪些文件、再按什么方式工作。

仓库地址：

```text
https://github.com/czstudio/wechat-content-studio-open
```

---

## 先做这一步：把仓库放到本地

先 clone：

```bash
git clone https://github.com/czstudio/wechat-content-studio-open.git
```

你最终要拿到一个本地路径，比如：

```text
/path/to/wechat-content-studio-open
```

下面所有提示词里的：

```text
{{REPO_PATH}}
```

都替换成你的实际本地路径。

比如：

```text
/Users/you/tools/wechat-content-studio-open
```

或者：

```text
H:\tools\wechat-content-studio-open
```

---

## 通用版

适合：

- 你不确定 agent 类型
- 你只想先跑起来

```text
Use the repo at {{REPO_PATH}} as the default workflow pack for WeChat article production.

First read:
1. {{REPO_PATH}}/SKILL.md
2. {{REPO_PATH}}/references/workflow-playbook.md
3. {{REPO_PATH}}/examples/end-to-end-example.md

Treat WeChat writing as:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.

Do not jump straight to one-shot drafting when topic readiness, support, or structure is still weak.
Use user-provided sample articles, style seed, and local corpus as the writing DNA source.
Prefer explicit artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
If the user only says "continue", advance from the nearest unfinished stage.
```

---

## OpenClaw

适合放在：

- workflow pack
- repo instruction layer
- project agent config

```text
Mount the repo at {{REPO_PATH}} as a WeChat content workflow pack.

Before handling WeChat article tasks, read:
1. {{REPO_PATH}}/SKILL.md
2. {{REPO_PATH}}/references/agent-install-kit.md
3. {{REPO_PATH}}/references/workflow-playbook.md
4. {{REPO_PATH}}/examples/end-to-end-example.md

Use this workflow:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.

Do not jump directly to full-article generation when topic readiness, support, or structure is still unclear.
Use user-provided sample articles, style seed, and local corpus as the writing DNA source.
Prefer explicit artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
If the user only says "continue", continue from the nearest unfinished stage.
```

---

## Codex / Codex CLI

适合放在：

- project instructions
- workspace instructions
- codex memory

```text
Use the repo at {{REPO_PATH}} as the default WeChat writing workflow.

Before handling WeChat-content tasks, read:
1. {{REPO_PATH}}/SKILL.md
2. {{REPO_PATH}}/references/workflow-playbook.md
3. {{REPO_PATH}}/references/draft-brief-template.md
4. {{REPO_PATH}}/references/repair-brief-template.md

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

```text
Use the repo at {{REPO_PATH}} for WeChat article planning, drafting, review, and repair.

Read first:
1. {{REPO_PATH}}/SKILL.md
2. {{REPO_PATH}}/references/workflow-playbook.md
3. {{REPO_PATH}}/examples/repair-loop-example.md

Do not treat the task as one-shot generation.
Follow this chain when appropriate:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.

Use the user's sample articles, manual style seed, and local corpus to infer writing DNA.
Prefer concrete artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
When the user only says "continue", advance from the nearest unfinished stage.
```

---

## Cursor / Windsurf

```text
Use the repo at {{REPO_PATH}} as the default workflow for WeChat content tasks.

Read first:
1. {{REPO_PATH}}/SKILL.md
2. {{REPO_PATH}}/references/workflow-playbook.md

Do not jump directly to a full article if the topic is still vague.
Prefer:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief.

Use sample articles, style seed, and local notes as the writing DNA source.
Return explicit workflow artifacts instead of generic advice.
If the user has a draft, review before rewriting.
```

---

## OpenCode / Trae / CodeBuddy

```text
Use the repo at {{REPO_PATH}} for WeChat writing and review tasks.

Read first:
1. {{REPO_PATH}}/SKILL.md
2. {{REPO_PATH}}/references/workflow-playbook.md
3. {{REPO_PATH}}/examples/end-to-end-example.md

Treat the task as a staged workflow, not a one-shot prompt.
Advance through:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.

Use the user's sample articles, style seed, and local corpus as the writing DNA source.
Prefer Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs as explicit outputs.
```

---

## 最短落地方式

如果你只想最快安装成功：

1. clone 仓库
2. 找到本地路径
3. 把上面对应 agent 的提示词里 `{{REPO_PATH}}` 替换掉
4. 粘贴进 agent 配置
5. 开始用

---

## 搭配阅读

- 安装页：[`INSTALL_AGENTS.md`](./INSTALL_AGENTS.md)
- agent 适配页：[`agents/`](./agents/)
- 主 skill：[`SKILL.md`](./SKILL.md)

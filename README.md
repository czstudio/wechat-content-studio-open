# WeChat Content Studio Open

> Turn WeChat writing from one-shot generation into a reusable production system.

不是“帮你写一篇公众号”。

而是：

`选题 -> brief -> 成稿 -> 审稿 -> 返工 -> 配图 -> 发布准备`

---

## 它解决什么问题

大多数 AI 写作工具只做到：

- 给标题
- 生成初稿
- 模仿一点语气

但真实内容工作卡在这些地方：

- 不知道写什么
- 不知道怎么开写
- 文章像 AI、像汇报
- review 后还是不会改
- 写完不知道怎么配图、排版、发布

这个项目就是专门解决这些断点。

---

## 核心流程

```text
Topic Board
   ↓
Draft Brief
   ↓
Draft
   ↓
Proof Gate
   ↓
Repair Brief
   ↓
Image Plan
   ↓
Publish Prep
```

一句话：

它不把“生成初稿”当终点，而把“变成可发内容”当终点。

---

## 为什么它不一样

| 普通写作工具 | WeChat Content Studio Open |
|---|---|
| 只有初稿 | 有完整工作流 |
| 只会模仿某个作者 | 用户可自带样文、seed、素材库 |
| review 很虚 | 有 `Proof Gate` + `Repair Brief` |
| 写完停在 Markdown | 后面还能接配图和发布准备 |

---

## 小白怎么开始

### 我完全没思路

先用：`Topic Board`

### 我方向定了，想直接开写

先用：`Draft Brief`

### 我已经有初稿

先用：`Proof Gate`

### 我只想知道怎么改

先用：`Repair Brief`

### 我想一步步让 agent 自己推进

直接说：`继续`

---

## 主流 AI Agent 支持

这个仓库已经给主流 agent 准备了适配入口：

- OpenClaw
- Codex / Codex CLI
- Claude Code
- OpenCode
- Trae
- CodeBuddy

安装说明看这里：

-> [`INSTALL_AGENTS.md`](./INSTALL_AGENTS.md)

如果你只想复制一段提示词直接装：

-> [`COPY_PASTE_PROMPTS.md`](./COPY_PASTE_PROMPTS.md)

---

## 仓库结构

```text
wechat-content-studio-open/
├─ README.md
├─ INSTALL_AGENTS.md
├─ COPY_PASTE_PROMPTS.md
├─ SKILL.md
├─ agents/
├─ references/
└─ examples/
```

---

## 推荐阅读顺序

1. [`INSTALL_AGENTS.md`](./INSTALL_AGENTS.md)
2. [`SKILL.md`](./SKILL.md)
3. [`references/workflow-playbook.md`](./references/workflow-playbook.md)
4. [`examples/end-to-end-example.md`](./examples/end-to-end-example.md)

---

## 更多文档

- 能力地图：[`references/capability-map.md`](./references/capability-map.md)
- 工作流说明：[`references/workflow-playbook.md`](./references/workflow-playbook.md)
- DNA seed 模板：[`references/dna-seed-template.md`](./references/dna-seed-template.md)
- Topic Card 模板：[`references/topic-card-template.md`](./references/topic-card-template.md)
- Draft Brief 模板：[`references/draft-brief-template.md`](./references/draft-brief-template.md)
- Repair Brief 模板：[`references/repair-brief-template.md`](./references/repair-brief-template.md)

<details>
<summary>这个项目适合谁</summary>

- 个人公众号作者
- 品牌内容团队
- 代写 / 编辑 / 审稿协作流
- 想把“自己的文风”训练成系统的人

</details>

<details>
<summary>这个项目不做什么</summary>

- 不绑定某个作者
- 不绑定某个品牌
- 不绑定固定素材库路径
- 不强绑某个配图或发布后端

</details>

---

## 许可证

[MIT](./LICENSE)

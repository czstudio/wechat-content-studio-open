# Install for AI Agents

> 这一页专门写“不同 agent 怎么装”。

如果你只是第一次来这个仓库，先看这里，不用先啃完整 README。

---

## 通用安装思路

无论你用哪个 agent，核心都一样：

1. 把这个仓库放进你的项目或技能目录
2. 让 agent 读取 `SKILL.md`
3. 再读取：
   - `references/workflow-playbook.md`
   - 对应模板
   - `examples/`
4. 把一段简短安装提示塞进 agent 的 memory / project instructions / custom skill 配置里

---

## 给所有 agent 通用的一段话

如果你不想区分平台，直接把下面这段复制给 agent：

```text
Use `wechat-content-studio-open` as the default workflow for WeChat article production.
Treat WeChat writing as:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
Do not jump straight to one-shot drafting when topic readiness or support is still weak.
Use user-provided sample articles, style seed, and local corpus as the DNA source.
Prefer explicit artifacts such as Topic Cards, Draft Briefs, Support Matrix, and Repair Briefs.
```

如果你想直接按不同 agent 复制现成版本：

- [`COPY_PASTE_PROMPTS.md`](./COPY_PASTE_PROMPTS.md)

---

## OpenClaw / Codex 极速安装

如果你现在就想在 OpenClaw 或 Codex 里直接用，最短路径是：

1. 让 agent 读取 `SKILL.md`
2. 再读取 `references/workflow-playbook.md`
3. 把上面的“通用安装提示”原样贴进去

如果你的 agent 支持 repo 级说明，那再补读：

- `examples/end-to-end-example.md`
- `examples/repair-loop-example.md`

这已经足够开始用。

---

## 不同 agent 怎么装

### 1. OpenClaw

看这个：

- [`agents/openclaw.md`](./agents/openclaw.md)

适合放在：

- skill layer
- project instruction layer
- repo attached workflow pack

---

### 2. Codex / Codex CLI

看这个：

- [`agents/codex.md`](./agents/codex.md)

适合放在：

- project instructions
- skill memory
- workspace-level instructions

---

### 3. Claude Code

看这个：

- [`agents/claude-code.md`](./agents/claude-code.md)

适合放在：

- Claude Code project memory
- repo-level working instructions

---

### 4. OpenCode

看这个：

- [`agents/opencode.md`](./agents/opencode.md)

适合放在：

- custom workflow instructions
- project guidance

---

### 5. Trae

看这个：

- [`agents/trae.md`](./agents/trae.md)

适合放在：

- workspace prompt
- project assistant config

---

### 6. CodeBuddy

看这个：

- [`agents/codebuddy.md`](./agents/codebuddy.md)

适合放在：

- skill pack
- custom repo instructions

---

### 7. 其他常见 agent

- Cursor
- Windsurf
- Roo Code
- Cline

对应适配页：

- [`agents/cursor.md`](./agents/cursor.md)
- [`agents/windsurf.md`](./agents/windsurf.md)
- [`agents/roo-code.md`](./agents/roo-code.md)
- [`agents/cline.md`](./agents/cline.md)

---

## 最短安装路径

如果你只想 30 秒装好：

### Step 1

让 agent 读取：

- [`SKILL.md`](./SKILL.md)

### Step 2

再读取：

- [`references/workflow-playbook.md`](./references/workflow-playbook.md)

### Step 3

复制上面的“通用安装提示”给它

就够开始用了。

---

## 建议 agent 的默认行为

安装后，最好让 agent 默认遵守这几个规则：

1. 选题不清楚时，不要直接整篇开写，先做 `Topic Board`
2. winner 明确后，不要直接 freestyle，先出 `Draft Brief`
3. 用户有初稿时，不要空泛点评，先跑 `Proof Gate`
4. 稿子能救时，不要只说“再润一下”，要给 `Repair Brief`
5. 用户只说“继续”时，默认推进到最近未完成阶段

---

## 推荐给 agent 读的文件顺序

| 顺序 | 文件 |
|---|---|
| 1 | [`SKILL.md`](./SKILL.md) |
| 2 | [`references/agent-install-kit.md`](./references/agent-install-kit.md) |
| 3 | [`references/workflow-playbook.md`](./references/workflow-playbook.md) |
| 4 | 对应模板文件 |
| 5 | [`examples/`](./examples/) |

---

## 如果你想自己扩展 agent 适配

看这里：

- [`references/agent-install-kit.md`](./references/agent-install-kit.md)

核心原则很简单：

- 不要为每个 agent 重写一套工作流
- 保持一个共享核心
- 只做薄适配层

---

## 一句话总结

这个仓库最适合的安装方式不是“复制一段 prompt”。

而是：

把它当成一个可挂载到主流 AI agent 上的“公众号内容生产工作流包”。

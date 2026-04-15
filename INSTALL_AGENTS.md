# Install for AI Agents

> 这一页专门解决一个问题：
>
> **怎么让 OpenClaw、Codex、Claude Code 这类 agent 真正能用上这个仓库。**

不是只给一段空提示词。

而是要完成这 3 步：

1. 把仓库放到 agent 能读到的位置
2. 告诉 agent 先读哪些文件
3. 再把行为提示喂给它

---

## Step 0：先拿到仓库

仓库地址：

```text
https://github.com/czstudio/wechat-content-studio-open
```

先 clone：

```bash
git clone https://github.com/czstudio/wechat-content-studio-open.git
```

clone 完后，你会得到一个本地目录，比如：

```text
/path/to/wechat-content-studio-open
```

或者：

```text
H:\tools\wechat-content-studio-open
```

后面所有安装动作，都是围绕这个本地目录做的。

---

## Step 1：让 agent 能读到仓库

最少要让 agent 能访问这些文件：

- `SKILL.md`
- `references/workflow-playbook.md`
- `examples/`

如果 agent 只能读你当前项目目录，那就把仓库放进项目目录里。  
如果 agent 支持外部 repo / workflow pack / skills path，就直接挂进去。

---

## Step 2：再给 agent 行为提示

这一步不要自己手写。

直接去：

- [`COPY_PASTE_PROMPTS.md`](./COPY_PASTE_PROMPTS.md)

复制对应 agent 的版本。

重点不是那段提示词本身。  
重点是里面已经包含：

- 本地仓库路径占位符 `{{REPO_PATH}}`
- 先读哪些文件
- 再按什么工作流运行

如果你希望 agent 不只是输出 `Image Plan`，而是真的帮你生成公众号封面和正文插图，继续看：

- [`references/image-api-setup.md`](./references/image-api-setup.md)

因为公开仓库不会自带任何私有图像 API key。

---

## OpenClaw / Codex 最短路径

如果你现在最想支持的是 OpenClaw 或 Codex，最短路径是：

### 1. clone 仓库

```bash
git clone https://github.com/czstudio/wechat-content-studio-open.git
```

### 2. 记住本地路径

例如：

```text
/Users/you/tools/wechat-content-studio-open
```

### 3. 打开这个文件

- [`COPY_PASTE_PROMPTS.md`](./COPY_PASTE_PROMPTS.md)

### 4. 找到对应段落

- `OpenClaw`
- `Codex / Codex CLI`

### 5. 把里面的 `{{REPO_PATH}}` 替换成真实路径

### 6. 再贴进 agent 配置

这就是真正能跑起来的安装方式。

---

## 不同 agent 入口

### OpenClaw

- 安装说明：[`agents/openclaw.md`](./agents/openclaw.md)

### Codex / Codex CLI

- 安装说明：[`agents/codex.md`](./agents/codex.md)

### Claude Code

- 安装说明：[`agents/claude-code.md`](./agents/claude-code.md)

### OpenCode

- 安装说明：[`agents/opencode.md`](./agents/opencode.md)

### Trae

- 安装说明：[`agents/trae.md`](./agents/trae.md)

### CodeBuddy

- 安装说明：[`agents/codebuddy.md`](./agents/codebuddy.md)

### Cursor / Windsurf / Cline / Roo Code

- [`agents/cursor.md`](./agents/cursor.md)
- [`agents/windsurf.md`](./agents/windsurf.md)
- [`agents/cline.md`](./agents/cline.md)
- [`agents/roo-code.md`](./agents/roo-code.md)

---

## 推荐的 agent 读取顺序

| 顺序 | 文件 |
|---|---|
| 1 | `SKILL.md` |
| 2 | `references/agent-install-kit.md` |
| 3 | `references/workflow-playbook.md` |
| 4 | 对应模板文件 |
| 5 | `examples/` |

---

## 一句话总结

真正能装成功，不是“复制一句 Use xxx as default workflow”。

而是：

**先把仓库挂进 agent 能读的路径，再把带本地路径的提示词喂给它。**

如果还要让它真的生图，记得再补 `image API setup`。

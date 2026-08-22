# Cross-agent installation

## Codex / Claude Code

让 agent 先读取：

1. `profiles/agentalpha-wechat-production/README.md`
2. `profiles/agentalpha-wechat-production/production-contract.md`
3. `profiles/agentalpha-wechat-production/publish-contract.md`
4. `profiles/agentalpha-wechat-production/templates/cta-templates.md`

随后声明：

```text
使用 AgentAlpha 微信公众号生产规范。用户给出的正文是只读真源。先锁稿，再排版和规划 8–10 张手绘技术图；全部图片先展示给用户验收，用户明确保留后才用已登录 Chrome 保存到微信公众号草稿箱。只保存草稿，不发布；必须用真实 appmsgid 和强制回读证明成功。
```

## Grok / OpenCode / Cursor / 其他 agent

把 `profiles/agentalpha-wechat-production/` 当作 workflow pack，优先读取 `README.md` 和四个合同/模板文件。若 agent 支持项目规则，把以下入口加入项目 instructions：

```text
请先读取 <REPO_PATH>/profiles/agentalpha-wechat-production/README.md，并遵循其中的锁稿、10 张配图、用户验收、草稿保存和强制回读门禁。不要改写用户正文，不要公开发布。
```

## Image generation provider

图像 provider 可替换。无论使用 UniKeyX、gpt-image-2 或其他适配器，都必须保留：`quality=low`、`1280x720`、provider receipt、prompt、输出 SHA-256 和人工验收状态。不要把 API key、Cookie、AppSecret 或带 token URL 放入仓库。

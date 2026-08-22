# AgentAlpha WeChat preset

当用户要求处理 AgentAlpha 公众号文章时，使用仓库内的可移植预设：

1. `profiles/agentalpha-wechat-production/SKILL.md`
2. `profiles/agentalpha-wechat-production/README.md`
3. `profiles/agentalpha-wechat-production/production-contract.md`
4. `profiles/agentalpha-wechat-production/visual-reference-manifest.md`
5. `profiles/agentalpha-wechat-production/reference-style-standard.md`
6. `profiles/agentalpha-wechat-production/character-reference.md`
7. `profiles/agentalpha-wechat-production/templates/cta-templates.md`
8. `profiles/agentalpha-wechat-production/publish-contract.md`

执行顺序：

`锁稿 -> 排版 -> 配图 -> 全部图片展示并等待用户验收 -> 公众号草稿箱 -> 强制远端回读`

硬约束：

- 用户完整正文只读，不擅自重写。
- 长技术文章 8–10 张图；完整 Agent / Agentic RL 面试文章默认 10 张。
- 默认 1280×720 暖象牙手绘技术图；图片必须解释段落，不做无意义装饰。
- 默认无人；人物只作为小面积、带明确动作的技术讲解者，不能固定复制某张参考图的人物身份。
- 上传前必须让用户验收全部图片；只存草稿，不正式发布。
- 远端成功必须有真实 `appmsgid` / `media_id` 和回读证据。
- 复用已登录 Chrome，不要求用户反复扫码；登录或控制失败就停止。
- 公开仓库不得存放任何密钥、Cookie、二维码、私有链接或本机路径。

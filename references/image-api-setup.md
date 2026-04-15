# Image API Setup

这一步是给“真的要配图 / 生图”的用户补上的。

现在这个公开仓库默认只提供：

- `Image Plan`
- 配图位设计
- 发布前 handoff

它不会自带任何私有图像 API key。

原因很简单：

- 公开仓库不能带私钥
- 不应该把 skill 绑死在某个账号上
- 不同用户会用不同 provider

所以，装完仓库后，如果你想让 agent 真正出图，还要再补这一层。

---

## 这个仓库默认怎么想

默认流程是：

1. 先写出文章
2. 再生成 `Image Plan`
3. 如果用户已经配好图像 API，再继续真正生图

也就是说：

**没配 API = agent 只能规划，不会真的生成图片。**

---

## 推荐默认方案

如果你想让公开版最容易跑起来，推荐直接用：

- provider: `dashscope`
- model: `qwen-image-2.0-pro`

原因：

- 中文文字渲染相对更稳
- 适合公众号封面和中文知识图
- 自定义尺寸更方便

---

## 最少要告诉 agent 的东西

至少补这两个环境变量：

```text
DASHSCOPE_API_KEY=你的_key
DASHSCOPE_IMAGE_MODEL=qwen-image-2.0-pro
```

如果你用的是别的 provider，也可以换成对应的环境变量。

---

## 给用户的最短提示

你可以直接把下面这段话贴给 agent：

```text
For image generation, use DashScope with qwen-image-2.0-pro.
Read {{REPO_PATH}}/references/image-api-setup.md first.
If image API keys are missing, do not pretend to generate images.
Tell me to configure DASHSCOPE_API_KEY and DASHSCOPE_IMAGE_MODEL first.
Once keys exist, turn Image Plan into real cover and inline images.
```

---

## Windows 示例

临时当前终端生效：

```powershell
$env:DASHSCOPE_API_KEY="your_key"
$env:DASHSCOPE_IMAGE_MODEL="qwen-image-2.0-pro"
```

然后 agent 再去调图像生成流程。

---

## macOS / Linux 示例

```bash
export DASHSCOPE_API_KEY="your_key"
export DASHSCOPE_IMAGE_MODEL="qwen-image-2.0-pro"
```

---

## 如果你想给 agent 一个明确规则

建议加这条：

```text
When the task includes WeChat illustrations, first check whether image API keys exist.
If not, stop at Image Plan and ask for provider setup.
Do not fake image generation.
```

---

## 这一步接在哪里

完整顺序建议改成：

1. clone repo
2. 安装 agent 入口
3. 配图像 API
4. 再让 agent 执行 `Image Plan -> real image generation -> Publish Prep`

---

## 一句话总结

这个仓库公开版默认带的是“配图工作流”，不是“你的私有图像账号”。

**要让别人真正生图，必须额外配置 image API。**

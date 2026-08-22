# 微信公众号草稿发布合同

## Defaults

- `publish_method`: browser
- `theme`: modern
- `color`: vermilion
- `author`: use the user-provided author; AgentAlpha default is `阿泽` only when the user has not supplied another author
- `profile`: fixed, user-approved Chrome profile; never create a temporary profile
- `headless`: `WECHAT_BROWSER_HEADLESS=1` by default
- `submit`: draft only; never public publish or mass-send

## Preflight

1. Run the context guard for a continuation task.
2. Check exact-title duplicates in the target draft list when the browser/control surface is available.
3. Verify local Markdown, body hash, cover path, image count and image decodability.
4. Run local preview/inspect and compare title, author, summary, headings, links, CTA and image count.
5. Never treat a local preview as proof of remote save.

## Login and browser exceptions

- If the fixed profile is not logged in, return `WECHAT_LOGIN_REQUIRED` and stop.
- Do not delete cookies, copy cookie databases between Chrome and Edge, switch browsers, or loop retries.
- Only use visible mode for a user-authorized one-time login/visual inspection; restore headless mode afterward.
- If Chrome control returns `Browser is not available: chrome`, report the blocker and do not claim upload success.

## Success proof

Report “草稿已保存” only after all are true:

- real `appmsgid` is captured;
- the draft is force-refreshed/read back from the remote target;
- title, author, summary, body text, image count, cover and links match;
- receipt is written under `recovery/wechat-draft-<appmsgid>.json`;
- `draft_only: true` is recorded.

Otherwise report the exact blocker and keep the local package intact.

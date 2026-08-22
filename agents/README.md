# Agent Support

This repo is designed to work well with mainstream AI coding and workflow agents.

## Included adapters

- `openclaw.md`
- `codex.md`
- `claude-code.md`
- `opencode.md`
- `trae.md`
- `codebuddy.md`
- `cursor.md`
- `windsurf.md`
- `cline.md`
- `roo-code.md`
- `agentalpha-wechat.md`

## How to use

1. Pick the adapter closest to your agent.
2. Copy the install snippet into your agent memory / project instructions / skill system.
3. Point the agent at:
   - `SKILL.md`
   - `references/`
   - `examples/`
   - `profiles/`（如使用 AgentAlpha 预设）

## Why this works well for agents

Because this repo does not only contain prose.

It contains:

- stage contracts
- output templates
- workflow playbooks
- example shapes

That makes it easier for agents to stay consistent across turns.

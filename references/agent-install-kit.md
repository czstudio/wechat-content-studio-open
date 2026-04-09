# Agent Install Kit

This repo is designed to be easy for both humans and coding agents to consume.

## Compatibility Goal

The core package is agent-agnostic:

- one main `SKILL.md`
- one set of reusable `references/`
- one set of `examples/`

On top of that, you can add a thin adapter layer for whichever agent you use.

## Supported Adapter Targets

Recommended first-class adapters:

- Codex / Codex CLI
- Claude Code
- OpenCode
- Trae
- CodeBuddy

Also easy to adapt:

- Cursor
- Windsurf
- Roo Code
- Cline

## Adapter Design Rule

Do not fork the workflow for every agent.

Keep:

- one shared production logic
- one shared capability map
- one shared workflow playbook

Only customize:

- where the instructions live
- how the agent discovers them
- what install snippet the user copies

## What Each Adapter Should Provide

Each adapter file should answer 4 questions fast:

1. What is this skill for?
2. When should the agent use it?
3. What files should the agent read first?
4. What output shape should it prefer?

## Minimum Install Surface

For each agent, provide:

- a copy-paste snippet
- a short “when to invoke” note
- a pointer to `SKILL.md`
- a pointer to the most important references

## Important Principle

The adapter is not the product.

The product is:

`Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep`

Adapters only help different agents enter that system faster.

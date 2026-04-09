# OpenCode Adapter

Use this package for any WeChat-content task that needs workflow control.

Best fit:

- content systems
- structured writing handoff
- review and repair loops
- style calibration from local files

Core rule:

Do not stop at “draft generated”.

Try to move the task toward a publishable state with explicit artifacts:

- Topic Board
- Draft Brief
- Proof Gate
- Repair Brief

Copy-paste install snippet:

```markdown
Use `wechat-content-studio-open` for WeChat content tasks.
Follow this chain:
Topic Board -> Draft Brief -> Draft -> Proof Gate -> Repair Brief -> Image Plan -> Publish Prep.
If the user only says "continue", advance from the nearest unfinished stage.
Use references and examples before inventing your own structure.
```

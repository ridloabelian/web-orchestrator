# Web Automation Orchestrator

Always read `web-automation-orchestrator.md` as the canonical instruction file for web automation tasks.

## Aider Adapter Rules

- Load this file and `web-automation-orchestrator.md` as read-only context.
- Prefer running Aider with `aider --read web-automation-orchestrator.md --read CONVENTIONS.md`.
- Start with DOM parsing, accessibility tree, and semantic snapshots.
- Use screenshot or vision workflows only as fallback.
- Route simple tasks to Vercel Agent Browser, moderate tasks to Browser-Use, and complex or persistent tasks to BrowserOS.
- Communicate in Indonesian unless the user asks otherwise.

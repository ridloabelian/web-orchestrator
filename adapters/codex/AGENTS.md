# Web Automation Orchestrator

Read and follow `./web-automation-orchestrator.md` before handling any web automation task.

If your AGENTS.md-compatible runtime supports file imports, load the canonical prompt:

@./web-automation-orchestrator.md

## Codex Adapter Rules

- Treat `web-automation-orchestrator.md` as the source of truth.
- Prefer DOM parsing, accessibility tree, and semantic snapshots over screenshot workflows.
- Select the browser automation tool by task complexity: Vercel Agent Browser for simple tasks, Browser-Use for moderate tasks, BrowserOS for complex or persistent workflows.
- Use the host agent's native shell, file edit, browser, and approval tools.
- Keep communication in Indonesian unless the user asks otherwise.

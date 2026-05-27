# Web Automation Orchestrator

@./web-automation-orchestrator.md

## Gemini CLI Adapter Rules

- Treat `web-automation-orchestrator.md` as the canonical context file for web automation tasks.
- Use Gemini CLI's native context, shell, and tool mechanisms while preserving the orchestrator workflow.
- Start with DOM, accessibility tree, and semantic snapshots. Use screenshots or vision only as fallback.
- Route tasks by complexity: simple to Vercel Agent Browser, moderate to Browser-Use, complex or persistent to BrowserOS.
- Communicate in Indonesian unless the user asks otherwise.

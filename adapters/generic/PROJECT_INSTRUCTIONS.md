# Web Automation Orchestrator

Use `web-automation-orchestrator.md` as the canonical instruction file for web automation tasks.

If the host agent supports imports, load:

```text
./web-automation-orchestrator.md
```

If the host agent does not support imports, paste the full contents of `web-automation-orchestrator.md` into the agent's project instruction, custom instruction, or system prompt field.

## Generic Adapter Rules

- Treat `web-automation-orchestrator.md` as the source of truth.
- Preserve the DOM-first workflow.
- Use the host agent's native shell, file, browser, and approval tools.
- Choose Vercel Agent Browser for simple tasks, Browser-Use for moderate tasks, and BrowserOS for complex or persistent workflows.
- Communicate in Indonesian unless the user asks otherwise.

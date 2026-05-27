# Web Orchestrator

Web Orchestrator is a universal, DOM-first system prompt for AI coding agents that need to plan and run efficient web automation workflows.

It is not tied to one agent runtime. The prompt can be used with Codex, Claude Code, Gemini CLI, Antigravity, OpenCoe, Aider, Kimi, and other coding agents that support project instructions, custom instructions, system prompts, or agent specs.

The core idea is simple: avoid screenshot-first automation. Start with DOM parsing, accessibility trees, and semantic snapshots. Use screenshot or vision only as a fallback.

## What Is Included

- `web-automation-orchestrator.md` - the universal system prompt for AI coding agents.
- `web-automation-orchestrator.agent.yaml` - an optional Kimi CLI v1.44-compatible adapter that loads the same prompt.
- `README.md` - usage and setup notes.

## Supported Agent Targets

This project is intended for any AI coding agent that can read project-level instructions or accept a custom system prompt, including:

- Codex
- Claude Code
- Gemini CLI
- Antigravity
- OpenCoe
- Aider
- Kimi
- Other coding agents and agent frameworks

## Tool Routing

| Task type | Default tool | When to use |
| --- | --- | --- |
| Simple | Vercel Agent Browser | 1-3 steps, single page, quick extraction |
| Moderate | Browser-Use | Multi-step flows, custom Python logic, data extraction |
| Complex | BrowserOS | Persistent browser replacement, scheduled tasks, MCP integration |

## Universal Usage

Use the contents of `web-automation-orchestrator.md` as the instruction layer for your coding agent.

Common integration patterns:

| Agent/runtime type | How to use this project |
| --- | --- |
| Project-instruction agents | Reference or paste `web-automation-orchestrator.md` into the project instruction file used by that agent |
| Custom-instruction agents | Paste the prompt into the agent's custom/system instruction field |
| CLI agents with prompt flags | Pass the file contents through the CLI's supported system/custom prompt mechanism |
| Agent-spec runtimes | Create a small adapter that points to `web-automation-orchestrator.md` |

Example generic shell pattern:

```bash
SYSTEM_PROMPT="$(cat web-automation-orchestrator.md)"
```

Then pass `SYSTEM_PROMPT` to the coding agent using the mechanism that agent supports.

## Kimi CLI Adapter

This repository includes a tested adapter for Kimi CLI v1.44.0:

```bash
git clone https://github.com/ridloabelian/web-orchestrator.git
cd web-orchestrator
kimi --agent-file web-automation-orchestrator.agent.yaml
```

For a one-shot non-interactive smoke test:

```bash
kimi --agent-file web-automation-orchestrator.agent.yaml --quiet -p "Validasi mode aktif."
```

Expected result:

```text
Web Automation Orchestrator aktif dan siap mengorkestrasikan otomasi web Anda.
```

## Requirements

The prompt can be loaded by any compatible AI coding agent. The automation tools below are optional and only needed when a task requires them:

- `agent-browser` for accessibility-tree snapshot workflows.
- `browser-use` for Playwright/Python workflows.
- `browseros` for BrowserOS workflows.

Check your local environment:

```bash
which agent-browser || echo "Agent Browser belum install"
python -c "import browser_use" 2>/dev/null || echo "Browser-Use belum install"
which browseros || echo "BrowserOS belum install"
```

If you use the Kimi adapter, also verify Kimi CLI:

```bash
which kimi || echo "Kimi CLI belum install"
```

## Adapter Notes

`web-automation-orchestrator.agent.yaml` is only an adapter for Kimi CLI. It does not make the project Kimi-specific.

The adapter passes the literal `${BROWSEROS_API_KEY}` placeholder into Kimi's prompt template renderer so the prompt can be loaded without requiring or exposing a real BrowserOS API key.

Other agents can use the same `web-automation-orchestrator.md` prompt directly or through their own native adapter format.

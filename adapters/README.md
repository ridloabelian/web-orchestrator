# Adapter Pack

This directory contains ready-to-copy adapter files for using `web-automation-orchestrator.md` with different AI coding agents.

The canonical prompt is always the repository root file:

```text
web-automation-orchestrator.md
```

Adapters should stay small. They point the host agent to the canonical prompt and add only the runtime-specific loading detail.

## Adapter Matrix

| Agent/runtime | Adapter file | Install into target project |
| --- | --- | --- |
| Codex and AGENTS.md-compatible agents | `codex/AGENTS.md` | `AGENTS.md` |
| Claude Code | `claude-code/CLAUDE.md` | `CLAUDE.md` |
| Gemini CLI | `gemini-cli/GEMINI.md` | `GEMINI.md` |
| Aider | `aider/CONVENTIONS.md` and `aider/.aider.conf.yml` | `CONVENTIONS.md` and `.aider.conf.yml` |
| Kimi CLI | root `web-automation-orchestrator.agent.yaml` | use from this repo or copy beside the prompt |
| Antigravity | `antigravity/INSTRUCTIONS.md` | paste into Antigravity project/custom instructions |
| OpenCoe | `opencoe/INSTRUCTIONS.md` | paste into OpenCoe project/custom instructions |
| Other agents | `generic/PROJECT_INSTRUCTIONS.md` | paste into the agent's project or system instructions |

## Install Pattern

Copy the canonical prompt and the adapter file into the target repository root.

Example for Codex:

```bash
cp web-automation-orchestrator.md /path/to/project/
cp adapters/codex/AGENTS.md /path/to/project/AGENTS.md
```

Example for Claude Code:

```bash
cp web-automation-orchestrator.md /path/to/project/
cp adapters/claude-code/CLAUDE.md /path/to/project/CLAUDE.md
```

Example for Gemini CLI:

```bash
cp web-automation-orchestrator.md /path/to/project/
cp adapters/gemini-cli/GEMINI.md /path/to/project/GEMINI.md
```

Example for Aider:

```bash
cp web-automation-orchestrator.md /path/to/project/
cp adapters/aider/CONVENTIONS.md /path/to/project/CONVENTIONS.md
cp adapters/aider/.aider.conf.yml /path/to/project/.aider.conf.yml
```

## Runtime Notes

- AGENTS.md is a broad agent instruction format for coding agents: https://agents.md/
- Claude Code loads `CLAUDE.md` project instructions and supports `@path` imports: https://code.claude.com/docs/en/memory
- Gemini CLI loads `GEMINI.md` context files and supports `@file.md` imports: https://google-gemini.github.io/gemini-cli/docs/cli/gemini-md.html
- Aider can load conventions with `--read CONVENTIONS.md` or `.aider.conf.yml`: https://aider.chat/docs/usage/conventions.html

If an agent does not support file imports, paste the full contents of `web-automation-orchestrator.md` into that agent's custom instruction field.

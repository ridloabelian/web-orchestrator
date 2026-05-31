# Web Orchestrator

Universal DOM-First System Prompt for AI Coding Agents.

## Purpose

Sistem prompt universal dan DOM-first untuk AI coding agents dalam merencanakan dan menjalankan web automation workflows yang efisien. Menghindari screenshot-first automation dengan memprioritaskan DOM parsing, accessibility trees, dan semantic snapshots.

## Tech Stack

- **Format:** Markdown prompt + YAML adapter
- **Compatible Agents:** Codex, Claude Code, Gemini CLI, Antigravity, OpenCoe, Aider, Kimi, dan lainnya

## Key Features

- `web-automation-orchestrator.md` — universal system prompt
- `web-automation-orchestrator.agent.yaml` — Kimi CLI v1.44 adapter
- `adapters/` — ready-to-copy adapters untuk 8+ agent runtimes
- Tool routing guidance (Vercel Agent Browser → Browser-Use → BrowserOS)
- Example shell patterns untuk loading prompts
- Requirements checks untuk automation tools (`agent-browser`, `browser-use`, `browseros`)

## Usage

Load prompt file ke dalam AI agent sesuai dengan adapter yang tersedia di folder `adapters/`. Setiap adapter disesuaikan dengan format system prompt dari agent runtime tertentu.

## Key Conventions

- Markdown-based system prompts
- YAML adapters untuk Kimi CLI
- DOM-first approach (bukan screenshot-first)
- Accessibility tree parsing sebagai primary navigation method

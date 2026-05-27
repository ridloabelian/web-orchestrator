# Web Orchestrator

&gt; **Stop burning tokens on screenshots.**  
&gt; Smart router that orchestrates Browser-Use, Vercel Agent Browser, and BrowserOS — picking the cheapest, fastest tool for every web task.

## ⚡ Why

| Method | Token Cost | Speed | Reliability |
|--------|-----------|-------|-------------|
| Screenshot → Vision LLM | 🔴 High | 🐢 Slow | ⚠️ Fragile |
| **Web Orchestrator (DOM-first)** | 🟢 **Low** | 🚀 **Fast** | ✅ **Deterministic** |

## 🛠️ Tools Orchestrated

- **[Browser-Use](https://github.com/browser-use/browser-use)** — Python/Playwright, multi-LLM, session persistence
- **[Vercel Agent Browser](https://github.com/vercel-labs/agent-browser)** — Rust CLI, accessibility tree snapshot, ultra-low token
- **[BrowserOS](https://github.com/browseros-ai/BrowserOS)** — Chromium fork, 53+ native tools, MCP server

## 🚀 Quick Start

```bash
# 1. Clone
git clone https://github.com/ridloabelian/web-orchestrator.git
cd web-orchestrator

# 2. Setup all tools
chmod +x setup.sh && ./setup.sh

# 3. Run
kimi --system "$(cat prompts/system-prompt.md)"

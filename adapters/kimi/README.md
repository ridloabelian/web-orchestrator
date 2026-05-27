# Kimi CLI Adapter

Kimi CLI support is provided by the repository root file:

```text
web-automation-orchestrator.agent.yaml
```

Run from this repository:

```bash
kimi --agent-file web-automation-orchestrator.agent.yaml
```

For a one-shot smoke test:

```bash
kimi --agent-file web-automation-orchestrator.agent.yaml --quiet -p "Validasi mode aktif."
```

If you copy the adapter into another project, keep `web-automation-orchestrator.agent.yaml` beside `web-automation-orchestrator.md` so `system_prompt_path: ./web-automation-orchestrator.md` resolves correctly.

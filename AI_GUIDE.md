# AI-guided coding checklist

Use this checklist before submitting automated changes. It complements `AGENTS.md` and `coding_rules.txt`.

1. **Confirm the target** — Identify the service or file you are touching, look for nested `AGENTS.md`, and avoid unnecessary refactors.
2. **Stay local-first** — Favor workflows that keep code on-device (local repos and local model inference via Ollama or similar runners).
3. **Prefer small diffs** — Make the smallest change that solves the task and keep patterns consistent with existing files.
4. **Respect structure** — Use `services/` for containerized services, `scripts/` for setup helpers, and `data/` for persistent volumes.
5. **Keep tooling consistent** — Use `uv` for Python tooling and align any linting/formatting with the repo defaults.
6. **Document behavior changes** — Note new env vars, ports, or service changes in `README.md` and `CHANGELOG.md`.
7. **Protect secrets** — Keep API keys and tokens in env vars or `api_key.txt`, never in code or sample configs.

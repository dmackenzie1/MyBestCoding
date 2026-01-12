# Roadmap

This roadmap captures the initial phases for a local-first coding assistant powered by on-device models.

## Near-term
- Define a minimal service contract for a local model runner (Ollama-compatible HTTP API).
- Create a Git workspace scanner that can summarize a working tree and suggest tasks.
- Add branch comparison tooling for `main` vs feature branches, including diff summaries and risk flags.
- Document how to run services on Windows with `uv` and Docker Desktop.

## Mid-term
- Add a task runner service that can fetch a GitHub repo, create a branch, and apply fixes locally.
- Introduce a review service that produces change summaries and optional checklist-based feedback.
- Add optional Postgres-backed metadata for tasks and runs.

## Longer-term
- Build a lightweight web UI for managing tasks and reviewing diffs.
- Provide plug-in adapters for alternative model runtimes beyond Ollama.
- Add multi-repo workflows (batch review, dependency graphing, risk scoring).

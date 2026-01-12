# My Best Coding

My Best Coding is a local-first, AI-assisted coding workspace built around running models on your own hardware. The goal is to keep everything on your machine: local repos, local diffs, and local model inference (via Ollama or another on-device runner).

## What this repo is for

- **Local code assistance**: analyze a Git working tree, propose fixes, and generate review notes without uploading code to third-party services.
- **Branch insight**: compare a feature branch to `main`, summarize diffs, and flag risky changes.
- **Remote pull-and-work**: optionally pull a GitHub repo, work locally, then create a branch with the proposed solution.

## Project layout (planned)

- `services/` — containerized services (each service is isolated and can be run via Docker).
- `scripts/` — local helper scripts for setup, linting, and maintenance.
- `data/` — optional persistent data (database volumes, local caches).
- `docs/` — longer-form guides and design notes as the project evolves.

## Local-first model runtime

This project assumes you will run a local model runtime such as Ollama outside of this repo. Services will connect to it over HTTP once they are introduced. See `.env.example` for placeholders you can wire up when you stand services up.

## Development notes

- Python tooling uses `uv` (3.11+ compatible).
- For UI work, expect Vue + Vite when a web UI is added.
- Docker Compose will be the default for services, but each service should remain isolated unless explicitly needed.

## Next steps

Check `ROADMAP.md` for the initial milestones and `AI_GUIDE.md` for contribution expectations.

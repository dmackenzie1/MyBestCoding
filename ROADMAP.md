# Roadmap

This roadmap focuses on incremental improvements without disrupting the existing Docker/uv workflow.

## Near-term (current cycle)
- Finalize pre-commit enforcement and shared VS Code settings to keep Python/Vue style consistent with LF-only defaults.
- Harden FastAPI input validation for uploads and transcript ingestion; add regression tests for `/api/v1/utterances/*` filters.
- Trim Vue bundle size and keep static asset emissions predictable under `services/web/static`.
- Validate Docker Compose flows against the current single capture server + 1–2 transcription servers setup on EC2.

## Mid-term
- Introduce lightweight observability: structured request logs for capture/transcribe workers and optional trace IDs across services.
- Expand GPU configuration presets for transcribers (CUDA vs CPU fallbacks) and document deployment toggles.
- Add automated smoke tests that exercise the capture → web → transcribe loop using in-memory queues.
- Support scaling to dozens of capture feeds (20+), keeping search and review fast for EC2-hosted deployments with small databases.

## Longer-term
- Provide turnkey deployment profiles (local, single-node GPU, ECS) with parameterized compose overrides.
- Build a richer operator dashboard: job queue health, capture agent heartbeats, and transcript quality indicators.
- Explore multi-language transcript support once WhisperX model selection is configurable per feed.
- Target hundreds to thousands of feeds across ATC, amateur radio, and public-safety sources with efficient search, tagging, and dataset generation for downstream language analysis.

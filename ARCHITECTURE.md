# Architecture

LAVA's copy of the open-source **Kortix** (formerly Suna) agent platform — imported as a standalone repo, not a GitHub fork. Upstream: [kortix-ai/suna](https://github.com/kortix-ai/suna).

```
apps/frontend (web) ─┐
apps/mobile (Expo) ──┼──▶ backend/ (FastAPI api.py + workers) ──▶ Redis (queues/cache)
apps/desktop ────────┘          │                                  Supabase (auth, Postgres, storage)
sdk/ (Python SDK)               ├─▶ LLMs via LiteLLM/OpenAI
                                ├─▶ agent sandboxes (Daytona / E2B)
                                └─▶ tools: Tavily search, MCP, Replicate, …
packages/shared — shared TS code for the apps
```

Local orchestration: `docker-compose.yaml` (backend, worker, frontend, Redis); setup wizard `setup.py`, launcher `start.py`. Backend detail: [backend/README.md](backend/README.md).

# Integrations

External software this project talks to. No secret values here — credentials are declared (by name only) in Varlock's `.env.schema` or the platform's credential store.

| System | Purpose | How |
| --- | --- | --- |
| Supabase | Auth, Postgres, storage | supabase-py / supabase-js |
| LLM providers | Agent reasoning | LiteLLM |
| Daytona / E2B | Isolated agent sandboxes | SDKs |
| Tavily | Web search tool | API |
| Stripe | Billing | API |
| Langfuse | LLM tracing | SDK |
| Novu | In-app notifications | @novu/nextjs |
| Cal.com | Scheduling embed | @calcom/embed-react |
| Replicate, Mailtrap, AWS (boto3) | Media generation, email, storage | SDKs |

Exact keys per service: `backend/.env.example` (to be migrated to a Varlock `.env.schema`).

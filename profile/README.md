# Flusk

**x30 output, same budget.** The AI data layer for organizations.

Flusk gives engineering teams full observability over their AI spend — traces, costs, drift detection, delusion detection, and actionable insights — then helps them build and deploy AI solutions across Slack, WhatsApp, and Telegram.

## How It Works

```
Your AI App → Flusk OTel SDK → Observe → Optimize → Build → Publish
```

**Observe** — Track every LLM call: cost, latency, tokens, model, agent. Full distributed tracing with OTLP.

**Optimize** — AI-powered insights find cost savings, detect drift, catch hallucinations, and rank usage per employee.

**Build** — Solution Builder (like v0 for AI agents): create AI workflows from templates, wire tools, deploy.

**Publish** — One-click publish to Slack, WhatsApp, Telegram, Discord, or embed via API.

## Repositories

| Repo | What | |
|------|------|-|
| [flusk-dev](https://github.com/fluskapp/flusk-dev) | Core platform — generated backend code | ![Stars](https://img.shields.io/github/stars/fluskapp/flusk-dev) |
| [flusk-lang](https://github.com/fluskapp/flusk-lang) | YAML-first development language & compiler | ![Stars](https://img.shields.io/github/stars/fluskapp/flusk-lang) |
| [flusk-observability](https://github.com/fluskapp/flusk-observability) | YAML schemas — the source of truth | ![Stars](https://img.shields.io/github/stars/fluskapp/flusk-observability) |

## The Flusk Way

All code is generated from YAML. AI writes YAML, the compiler generates production code.

```yaml
# Define once in YAML
name: LlmCall
fields:
  model: { type: string, required: true }
  cost:  { type: number, index: true }
  
# flusk-lang generates:
# → TypeBox schema, TypeScript types
# → SQLite repository with CRUD
# → Fastify route with validation
# → Vitest tests
# → OpenAPI spec + Client SDK
```

Human code stays human. Machine code stays YAML.

---

[Website](https://flusk.app) · [Docs](https://docs.flusk.app) · Security: adir@flusk.app

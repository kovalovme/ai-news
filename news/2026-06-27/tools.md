# Tools — 2026-06-27

## Workweave Router — Smart Model Routing for Claude, Codex, and Cursor <a id="workweave-router"></a>

**Source:** [GitHub](https://github.com/workweave/router) · **Type:** release · **Time (UTC):** — · **HN:** 167 pts (Show HN)

Workweave Router is an open-source drop-in proxy that sits between coding tools and AI API providers, selecting the optimal model per request without requiring changes to application code. The project surfaced on HN as a Show HN submission with 167 points.

The proxy supports Anthropic, OpenAI, and Google Gemini providers. Routing decisions are made by an embedded cluster scorer derived from "Avengers-Pro" and complete in under 50ms with no upstream API call. The project claims 40–70% cost reduction over single-provider setups by downrouting routine completions to cheaper models.

**Integration per tool:**

| Tool | Setup |
|------|-------|
| Claude Code | `make install-cc` or `npx @workweave/router` (hosted) |
| OpenAI Codex CLI | Config file patch with managed provider block |
| Cursor | Base URL override in settings (early beta) |
| opencode | Provider settings merge into config JSON |

**Why it matters:** Cost-conscious teams running Claude Code or Codex at scale gain a drop-in proxy for automated tier selection rather than manually specifying models per use case. The open question is whether the routing model generalizes across request types well enough to reliably improve net outcomes rather than just cut spend.

---

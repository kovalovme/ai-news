# Models — 2026-05-29

## Claude Opus 4.8 <a id="claude-opus-4-8"></a>

**Source:** [Anthropic via Axios](https://www.axios.com/2026/05/28/anthropic-opus-release-mythos) · **Type:** release · **Time (UTC):** May 28

Claude Opus 4.8 ships with three headline capabilities: dynamic workflows (Claude plans and orchestrates tens-to-hundreds of background subagents autonomously, accessible via `/workflows` in Claude Code), Fast Mode (2.5× throughput of standard Opus at 2× the per-token rate — roughly 3× cheaper per request than the previous fast mode), and a lean system prompt that is now the default for all current-generation models. Benchmarks beat competing models on agentic coding, multi-step reasoning, financial analysis, and knowledge work. On prosocial and user-autonomy traits, Opus 4.8 scores comparably to the restricted Mythos model. Pricing is unchanged at $5/$25 per million input/output tokens.

**Why it matters:** Dynamic workflows are the production-ready path from single-agent Claude sessions to supervised multi-agent execution without custom orchestration infrastructure. Fast Mode makes Opus-class capability viable for latency-sensitive pipelines that previously required Sonnet.

| Feature | Detail |
|---------|--------|
| Price (input / output) | $5 / $25 per 1M tokens (unchanged from 4.7) |
| Fast Mode throughput | 2.5× standard Opus |
| Fast Mode cost | 2× standard rate (~3× cheaper than prior Fast) |
| Default effort | xhigh (`/effort xhigh` in Claude Code) |
| Mythos parity | Comparable on prosocial / user-autonomy traits |

---

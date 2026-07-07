# Models — 2026-07-07

## OpenAI gpt-realtime-2.1 and gpt-realtime-2.1-mini <a id="gpt-realtime-21"></a>

**Source:** [OpenAI Blog](https://openai.com/index/advancing-voice-intelligence-with-new-models-in-the-api/) · **Type:** release · **Time (UTC):** ~18:00 Jul 6

OpenAI shipped two updated voice models: `gpt-realtime-2.1` and `gpt-realtime-2.1-mini`. Both improve on `gpt-realtime-2` with at least 25% lower p95 latency, better alphanumeric recognition, improved silence/noise handling, and more reliable interruption behavior. The full model adds a configurable reasoning-effort knob (low/medium/high) for more complex voice-agent workflows; the mini variant ships at the same per-minute cost as its predecessor.

**Why it matters:** Production voice-agent builders can drop in the new models for measurable latency improvements without changing their integration code; the reasoning-effort control lets developers tune between speed and accuracy depending on the task.

| Variant | Use case | Notes |
|---------|----------|-------|
| gpt-realtime-2.1 | Max quality, reasoning, tool use | Configurable effort |
| gpt-realtime-2.1-mini | Cost/speed sensitive | Same price as old mini |

---

## GPT-5.6 Sol general access window opens (July 7–14) <a id="gpt-56-sol-ga-window"></a>

**Source:** [OpenAI Preview](https://openai.com/index/previewing-gpt-5-6-sol/) · [TechTimes review](https://www.techtimes.com/articles/319808/20260707/gpt-56-sol-review-faster-coding-half-fable-5-cost-benchmark-problem.htm) · **Type:** update · **Time (UTC):** Jul 7

The July 7–14 window for GPT-5.6 Sol general availability has opened. As of this morning the model remains in limited API/Codex preview (~20 vetted organizations), but prediction markets now center on July 9 as the expected public API launch date, and reasoning-slider controls have appeared in recent Codex builds indicating an imminent rollout. The Cerebras inference lane (targeting 750 tok/s) is planned to launch alongside general availability.

First-look reviews compare Sol favorably on coding tasks against Fable 5 at roughly half the cost: Sol is priced at $5/$30 per million input/output tokens vs Fable 5 at $10/$50 (effective July 8). Early testers noted benchmark inflation concerns (the same pattern noted in prior tier releases), though real-task coding performance has been competitive.

**Why it matters:** The pricing gap between Sol ($5/$30/MTok) and Fable 5 ($10/$50/MTok) makes Sol a compelling default for cost-sensitive agentic workloads once GA occurs; teams should watch for the official API announcement this week.

| Model | Input | Output | Speed (Cerebras) |
|-------|-------|--------|------------------|
| GPT-5.6 Sol | $5/MTok | $30/MTok | 750 tok/s |
| GPT-5.6 Terra | $2.50/MTok | $15/MTok | — |
| GPT-5.6 Luna | $1/MTok | $6/MTok | — |
| Fable 5 (from Jul 8) | $10/MTok | $50/MTok | — |

---

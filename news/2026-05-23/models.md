# Models — 2026-05-23

## Qwen3.7-Max: Alibaba's Agent-Focused Flagship <a id="qwen37-max"></a>

**Source:** [Alibaba Cloud Blog](https://www.alibabacloud.com/blog/qwen3-7-the-agent-frontier_603154) · **Type:** release · **Time (UTC):** 2026-05-20 ~10:00

Alibaba formally unveiled Qwen3.7-Max at its Cloud Summit on May 20, after the model had quietly appeared on public leaderboards a day earlier. The model targets multi-step agentic workflows: it sustains autonomous execution for up to 35 hours in internal tests, successfully completed over 1,000 tool calls to optimize a GPU kernel from scratch (achieving a claimed 10× speedup), and supports a 1,000,000-token context window with a 65,536-token maximum output. Weights are not open-sourced; access is through Alibaba's Model Studio API.

**Why it matters:** On agentic benchmarks Qwen3.7-Max posts SWE-Pro 60.6, Terminal Bench 2.0 Terminus 69.7, MCP-Mark 60.8, and GPQA Diamond 92.4 — competitive with Claude 4 and GPT-5 on the agent-focused evals that matter most to engineers building autonomous pipelines. The 1M-token context is the largest publicly available on a non-open-weight frontier model.

| Benchmark | Score |
|---|---|
| SWE-Pro | 60.6 |
| Terminal Bench 2.0 Terminus | 69.7 |
| MCP-Mark | 60.8 |
| GPQA Diamond | 92.4% |

---

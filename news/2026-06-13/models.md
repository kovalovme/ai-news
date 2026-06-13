# Models — 2026-06-13

## Kimi K2.7-Code: 1-trillion-parameter open-source coding model <a id="kimi-k27-code"></a>

**Source:** [Hugging Face model card](https://huggingface.co/moonshotai/Kimi-K2.7-Code) · [MarkTechPost](https://www.marktechpost.com/2026/06/12/moonshot-ai-releases-kimi-k2-7-code-a-coding-model-reporting-21-8-on-kimi-code-bench-v2-over-k2-6/) · [Kimi platform](https://platform.moonshot.ai) · **Type:** release · **Time (UTC):** — (Jun 12)

Moonshot AI released Kimi K2.7-Code on June 12, publishing full model weights to Hugging Face simultaneously with API availability. The model is a Mixture-of-Experts architecture with 1.1 trillion total parameters and 32 billion active parameters per forward pass. It uses 384 total experts (8 selected per token), 61 transformer layers, and supports a 256K-token context window. The vision encoder (MoonViT, 400M params) is retained, making the model multimodal. Moonshot reports K2.7-Code reduces thinking-token consumption by roughly 30% compared to K2.6 while raising benchmark scores across all tested tasks.

**Why it matters:** At 32B active parameters, the model is deployable on mid-tier GPU clusters while punching at full-1T quality for agentic coding tasks. The Modified MIT license permits commercial use with attribution, placing it in direct competition with Anthropic's Claude Code and OpenAI's Codex at the open-weight layer. The 30% token efficiency gain is practically significant: developers running long agentic loops see proportional cost and latency reductions.

| Benchmark | K2.6 | K2.7-Code | Delta |
|-----------|-----:|----------:|------:|
| Kimi Code Bench v2 | 50.9 | 62.0 | +21.8% |
| Program Bench | — | — | +11.0% |
| MLS Bench Lite | — | — | +31.5% |
| MCP Atlas (agentic) | 69.4 | 76.0 | +9.5% |

---

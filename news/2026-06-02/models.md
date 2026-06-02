# Models — 2026-06-02

## NVIDIA Nemotron 3 Ultra <a id="nemotron-3-ultra"></a>

**Source:** [NVIDIA GTC Taipei / Computex Blog](https://blogs.nvidia.com/blog/nvidia-gtc-taipei-computex-2026-news/) · [Artificial Analysis](https://artificialanalysis.ai/articles/nvidia-nemotron-3-ultra-launch-announced) · **Type:** release · **Time (UTC):** ~01:00 Jun 1 (Computex keynote)

Nemotron 3 Ultra packs 550 billion total parameters with 55 billion active per token, using a hybrid Mamba-2 / standard Transformer mixture-of-experts architecture. The model supports a 1-million-token context window and multi-token prediction. Jensen Huang unveiled it in his Computex keynote in Taipei; BF16 and NVFP4 weights are scheduled to release June 4 via the NVIDIA API and major cloud providers.

**Why it matters:** It claims the top spot on the Artificial Analysis Intelligence Index among US-origin open-weight models (score 48), surpassing Gemma 4 31B (39) and Nemotron 3 Super (36), though it trails Chinese-origin leader Kimi K2.6 (54). Inference speed of 300+ tokens/second on DeepInfra — roughly 3–6× faster than comparable open models served elsewhere — makes it viable for latency-sensitive agentic pipelines.

| Dimension | Value |
|-----------|-------|
| Total params | 550B |
| Active params / token | 55B |
| Context window | 1M tokens |
| Architecture | Mamba-2 + Transformer MoE |
| Formats released | BF16, NVFP4 |
| AA Intelligence Index | 48 (top US open weights) |
| Inference speed | 300+ tok/s (DeepInfra preview) |
| Cost vs comparables | ~30% cheaper to run |

---

## Microsoft MAI v2 Model Suite <a id="microsoft-mai-v2"></a>

**Source:** [Microsoft Build 2026 / Windows News](https://windowsnews.ai/article/build-2026-microsofts-platform-shift-to-ai-agents-copilot-and-azure-ai-foundry-takes-center-stage-in.420960) · [Digit.in Build coverage](https://www.digit.in/news/general/microsoft-build-2026-new-ai-models-copilot-super-app-and-what-more-to-expect.html) · **Type:** release · **Time (UTC):** ~16:30 Jun 2 (Build keynote)

Microsoft unveiled four new proprietary models at Build 2026. MAI-Image-2.5 adds image-input support for editing workflows alongside a faster variant (2.5e). MAI-Voice-2 expands to 14+ languages with an extended emotional range (angry, confused, embarrassed, and others). MAI-Transcribe-1.5 iterates on the already-strong v1 baseline, which held the lowest word-error rate across 25 languages. Most significantly, Mustafa Suleiman unveiled MAI-Thinking-1, Microsoft's first dedicated reasoning model.

**Why it matters:** MAI-Thinking-1 signals Microsoft moving beyond distilled third-party reasoning (GPT-4o, o-series) into in-house inference-time compute scaling — a capability gap Microsoft has publicly acknowledged since the o1 release. Combined with Project Polaris (see [tools.md](tools.md#project-polaris)), this marks a meaningful expansion of Microsoft's model independence from OpenAI.

---

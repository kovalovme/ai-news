# Models — 2026-07-23

## Poolside Laguna S 2.1 <a id="laguna-s-2-1"></a>

**Source:** [Poolside Blog](https://poolside.ai/blog/introducing-laguna-s-2-1) · **Type:** release · **Time (UTC):** 2026-07-21 ~18:00

Poolside released Laguna S 2.1, a 118-billion-parameter mixture-of-experts coding model that activates 8B parameters per token and runs on a single NVIDIA DGX Spark desktop. The model went from the start of training (May 22, 4,096 H200 GPUs) to public release in under nine weeks, built via Poolside's automated Model Factory pipeline. It supports up to 1M-token context in both thinking and non-thinking modes, and weights ship under the OpenMDW-1.1 license on Hugging Face across BF16, FP8, INT4, and NVFP4 formats.

**Why it matters:** Laguna S 2.1 is the first Western open-weight model to outperform DeepSeek V4 Pro Max (1.6T total parameters) on both SWE-Bench Pro (59.4 vs 55.4) and DeepSWE (40.4 vs 9.0). At $0.10/$0.20 per million input/output tokens and a free 256K-context tier on OpenRouter, it offers a strongly price-competitive open alternative to frontier coding models without requiring multi-GPU infrastructure.

| Benchmark | Laguna S 2.1 | DeepSeek V4 Pro Max |
|-----------|-------------:|--------------------:|
| SWE-Bench Pro | 59.4% | 55.4% |
| DeepSWE v1.1 | 40.4% | 9.0% |
| SWE-Bench Multilingual | 78.5% | — |
| Terminal-Bench 2.1 | 70.2% | — |

---

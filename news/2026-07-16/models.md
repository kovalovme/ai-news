# Models — 2026-07-16

## Inkling: Thinking Machines Lab's first open-weights model <a id="inkling"></a>

**Source:** [Thinking Machines Lab](https://thinkingmachines.ai/news/introducing-inkling/) · [TechCrunch](https://techcrunch.com/2026/07/15/thinking-machines-amps-up-its-bet-against-one-size-fits-all-ai-with-its-first-open-model-inkling/) · **Type:** release · **Time (UTC):** ~13:00 Jul 15

Thinking Machines Lab — the ~200-person startup founded by former OpenAI CTO Mira Murati — released its first in-house model on July 15. Inkling is a Mixture-of-Experts transformer with 975B total parameters and 41B active per forward pass; the MoE routing broadly follows DeepSeek-V3 (256 routed experts, 2 shared, 6 active per token). It was pretrained on 45 trillion tokens of text, images, audio, and video with a 1M-token context window. A smaller sibling, Inkling-Small (276B total, 12B active), is in preview and matches the larger model on many benchmarks at lower cost. Full weights are on Hugging Face; inference is available through Together AI, Fireworks, Modal, Databricks, and Baseten.

**Why it matters:** This is the first frontier-class open-weights model from a Western lab founded post-ChatGPT, and among the largest open-weights releases to date. Thinking Machines does not claim leaderboard dominance — they explicitly say it is "not the strongest overall model available today" — but the customizability angle is real: it ships as the base model for their Tinker fine-tuning platform. Engineers looking to fine-tune a broadly capable multimodal base without sending data to a closed provider now have a credible new option.

| Benchmark | Score |
|---|---|
| AIME 2026 | 97.1% |
| SWE-Bench Verified | 77.6% |
| GPQA Diamond | 87.2% |
| MMMU Pro | 73.5% |
| VoiceBench | 91.4% |

---

## Gemma 4 26B running at 5 tok/s on a 2013 Xeon with no GPU <a id="gemma-4-xeon"></a>

**Source:** [Neomind Labs blog](https://www.neomindlabs.com/2026/06/08/running-gemma-4-26b-at-5-tokens-sec-on-a-13-year-old-xeon-with-no-gpu/) · **Type:** engineering writeup · **Time (UTC):** published Jun 8; 279 pts HN Jul 16

A developer ran Google's Gemma 4 26B-A4B mixture-of-experts model (8-bit quantized) on a repurposed HP StoreVirtual storage appliance — dual Xeon E5-2690 v2 (Ivy Bridge, 2013) with DDR3 RAM and no GPU — for under $300. The machine lacks AVX2 instruction support, so standard llama.cpp builds silently failed. The fix required patching ikawrakow's llama.cpp fork: replacing fused AVX2 kernels with separate matmul operations and adding scalar/SSE fallback paths for quantization functions. The resulting build runs Gemma 4 26B at ~5.2 tok/s decode and ~16 tok/s prompt evaluation.

**Why it matters:** The patch surfaces a quiet compatibility gap in llama.cpp for pre-AVX2 hardware — a class of machines still common in homelabs and developing-market deployments. The approach generalizes to any quantized MoE model on legacy x86 hardware.

---

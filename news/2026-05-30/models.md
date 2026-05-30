# Models — 2026-05-30

## Liquid AI LFM2.5-8B-A1B <a id="liquid-ai-lfm2-5"></a>

**Source:** [Liquid AI Blog](https://www.liquid.ai/blog/lfm2-5-8b-a1b) · **Type:** release · **Time (UTC):** —

Liquid AI released LFM2.5-8B-A1B, an open-weight edge model with 8B total parameters and 1B active (MoE with gated short convolution blocks). Context window triples to 128K (from 32K), vocabulary doubles to 128K tokens for improved multilingual compression — Hindi improves 120%, Thai 238%. Training scale expands from 12T to 38T tokens, with avg@k reward optimization targeting hallucination reduction and preference optimization to suppress reasoning loops.

**Why it matters:** An 8B/A1B MoE model matching Gemma-4-26B instruction-following with a fraction of the active compute is a meaningful edge-inference milestone. Day-one support across llama.cpp, MLX, vLLM, SGLang, and ONNX with 253 tok/s on Apple M5 Max makes it immediately deployable. Models are available without restrictions on Hugging Face.

| Benchmark | LFM2.5-8B-A1B | Delta vs LFM2-8B-A1B |
|-----------|:---:|:---:|
| MATH500 | 88.76 | +13.96 |
| AIME25 | 42.53 | +22.53 |
| IFEval | 91.84 | +12.40 |
| Tau² Telecom | 88.07 | +74.47 |

---

## Tencent Hy3 Preview <a id="tencent-hy3"></a>

**Source:** [Tencent Announcement](https://www.tencent.com/en-us/articles/2202320.html) · [Decrypt](https://decrypt.co/365297/tencent-hy3-preview-open-source-moe-model) · **Type:** release · **Time (UTC):** —

Tencent open-sourced Hy3 preview, the first model from a full ground-up rebuild of its Hunyuan pre-training and RL stack started in late January 2026. Architecture: 295B parameters, 21B active (MoE), 256K context. Three design principles were declared up-front: capability systematization, evaluation authenticity (explicit anti-benchmark-gaming), and cost efficiency. SWE-bench Verified climbs from 53% (Hy2) to 74.4% — a 40% generation-over-generation gain. The model is now topping OpenRouter usage rankings by a notable margin, with usage patterns appearing organic rather than driven by a single app.

**Why it matters:** A 295B/21B MoE at 74.4% SWE-bench is competitive at the frontier for coding; the 256K context and explicit no-benchmark-gaming policy make it one of the more trustworthy open benchmark claims from a Chinese lab this cycle. Available on Hugging Face, GitHub, and ModelScope.

---

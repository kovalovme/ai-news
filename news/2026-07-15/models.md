# Models — 2026-07-15

## Bonsai 27B: First 27B-Class Model to Run on a Phone <a id="bonsai-27b"></a>

**Source:** [PrismML](https://prismml.com/news/bonsai-27b) · **Type:** release · **Time (UTC):** —

PrismML released Bonsai 27B, a pair of aggressively quantized builds of Qwen3.6 27B designed for consumer hardware. The ternary variant ({−1, 0, +1} weights with FP16 group-wise scaling) ships at 5.9 GB and retains 95% of FP16 benchmark quality across 15 tasks; the 1-bit binary variant ({−1, +1} weights, same scaling scheme) ships at 3.9 GB and retains 90%. Both support a 262 K-token context window and speculative decoding, and include a compact 4-bit vision tower for multimodal inputs.

The 1-bit build fits within the memory budget of an iPhone 17 Pro and delivers 11 tokens/second on that device — the first claimed instance of a 27B-class model running at practical speeds on a phone. The ternary build reaches 134 tok/s on an RTX 5090 and 58 tok/s on an Apple M5 Max. Both variants include support for structured tool calls and multi-step agentic loops. Everything is available under Apache 2.0 on Hugging Face; PrismML also offers a free developer-preview API.

**Why it matters:** Until now, on-device inference at the 27B scale required a laptop or workstation. Fitting a model of this size and capability tier into a smartphone opens agentic and offline-capable AI to mobile-first platforms without a cloud dependency. The Apache 2.0 license also makes derivative fine-tuned builds commercially viable.

| Variant | Weight bits | Size | iPhone 17 Pro | RTX 5090 | M5 Max | Benchmark retention |
|---------|------------|------|--------------|----------|--------|---------------------|
| Ternary | ~1.71 bpw  | 5.9 GB | — | 134 tok/s | 58 tok/s | 95% of FP16 |
| 1-bit   | 1 bpw      | 3.9 GB | 11 tok/s | — | — | 90% of FP16 |

---

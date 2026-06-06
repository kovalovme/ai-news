# Models — 2026-06-06

## Gemma 4 QAT checkpoints released <a id="gemma-4-qat"></a>

**Source:** [Google DeepMind Blog](https://blog.google/innovation-and-ai/technology/developers-tools/quantization-aware-training-gemma-4/) · **Type:** release · **Time (UTC):** ~10:00

Google DeepMind released Quantization-Aware Training (QAT) checkpoints for the Gemma 4 family (E2B, E4B, and 12B). Unlike standard post-training quantization, QAT bakes precision loss into the training loop, preserving more quality at smaller sizes. The headline result is Gemma 4 E2B compressed to under 1 GB using a new mobile-specialized format with static activations, channel-wise quantization, targeted 2-bit compression for token-generation layers, and KV-cache optimization. A Q4_0 format is available for broader framework compatibility.

**Why it matters:** Sub-1 GB Gemma 4 E2B enables serious inference on phones and edge devices without a server call. Models are available today on Hugging Face (GGUF and compressed tensor formats) and immediately supported by llama.cpp, Ollama, LM Studio, LiteRT-LM, Transformers.js, vLLM, SGLang, and MLX.

| Model | Format | Memory footprint |
|-------|--------|-----------------|
| Gemma 4 E2B | Mobile QAT | < 1 GB |
| Gemma 4 E4B | Q4_0 | ~2.5 GB |
| Gemma 4 12B | Q4_0 | ~7 GB |

---

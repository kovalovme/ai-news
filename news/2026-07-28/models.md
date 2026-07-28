# Models — 2026-07-28

## Kimi K3 Self-Hosting: vLLM Integration Still In Progress, No GGUF Port Yet <a id="kimi-k3-selfhost-status"></a>

**Source:** [vLLM Blog](https://vllm.ai/blog/2026-07-22-kimi-k3-preview) · [DEV Community](https://dev.to/lola_lin_a1be8395c517b081/kimi-k3-open-weights-are-here-how-to-self-host-the-28t-parameter-model-hardware-vllm-and-data-4b0n) · [Northflank](https://northflank.com/blog/what-is-kimi-k3-self-hosting) · **Type:** follow-up · **Time (UTC):** Jul 28

Community assessment, 24 hours after Kimi K3 open weights dropped on July 27: the practical self-hosting picture is more constrained than the open-weight announcement suggested.

**Status summary:**

| Component | Status |
|-----------|--------|
| vLLM integration | Core path + KDA prefix caching in progress; not yet merged to main |
| SGLang | Under active development; no release yet |
| GGUF / llama.cpp port | Not confirmed; no community conversion completed |
| Unsloth LoRA adapters | Working (with KDA compatibility patches) |
| Hosted inference | Together AI, Modal day-0 (from July 27) |

**Hardware floor:** The full 2.8T parameter model in MXFP4 requires ~64 H100-class accelerators (1.4 TB VRAM equivalent). The custom Kimi Delta Attention architecture is not yet in mainstream inference stacks, making community quantization non-trivial. A production deployment is realistically a late-2026 task for most teams.

**Why it matters:** The open-weight release is real and significant, but the day-zero self-hosting path requires either Moonshot's supported inference API or waiting for vLLM/SGLang integration to land. Teams evaluating Kimi K3 for data-residency or on-premises requirements should plan for 4–8 weeks before mainstream inference stack support stabilizes.

---

## HuggingFace Transformers 5.14.0: Multi-Token Prediction, 260% Faster SDPA Prefill <a id="transformers-5-14-0"></a>

**Source:** [Hugging Face Releases](https://github.com/huggingface/transformers/releases) · [Releasebot](https://releasebot.io/updates/huggingface) · **Type:** release · **Time (UTC):** Jul 28

Transformers 5.14.0 ships with performance improvements that affect all inference-heavy deployments: Multi-Token Prediction (MTP) decoding support in the generation pipeline, and SDPA prefill with FlashAttention for StaticCache — benchmarked up to 260% faster on prefill-heavy workloads. New model architectures added include Inkling (the 975B Thinking Machines model; see [July 16 digest](../2026-07-16/models.md#inkling)) and TIPSv2. Breaking backend updates affect GPTNeoX and GPTBigCode architectures.

**Why it matters:** The SDPA + FlashAttention prefill improvement is immediately applicable to long-context deployments. Teams running 100K+ token prompts should expect meaningfully better throughput without any code changes beyond upgrading the library.

---

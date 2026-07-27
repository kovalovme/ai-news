# Models — 2026-07-27

## Kimi K3 Open Weights: 2.8T Parameters Drop <a id="kimi-k3-open-weights"></a>

**Source:** [kimi.com/blog/kimi-k3](https://www.kimi.com/blog/kimi-k3) · **Type:** release · **Time (UTC):** 00:00

Moonshot AI published free open weights for Kimi K3 at midnight UTC on July 27, roughly 30 minutes ahead of the announced target. At 2.8 trillion parameters it is the largest publicly available model by parameter count. The native MXFP4/MXFP8 quantized safetensors release weighs approximately 1.4 TB; Moonshot's own recommendation is deployment on supernode configurations of 64 or more accelerators. Together AI and Modal both provided day-0 hosted access without any download requirement.

**Architecture:** Kimi Delta Attention (KDA) replaces standard multi-head attention, Attention Residuals selectively pull representations across network depth, and Stable LatentMoE activates 16 of 896 experts per token — roughly 50 billion active parameters per forward pass. Weights are quantized to MXFP4 with MXFP8 activations. Context window is 1 million tokens natively.

**Benchmarks:** Moonshot's blog notes the model "trails the most powerful proprietary models, Claude Fable 5 and GPT-5.6 Sol" on coding and multimodal tasks. It is competitive on DeepSWE, Terminal-Bench, FrontierSWE, and SWE Marathon relative to other models in its weight class.

| Spec | Value |
|------|-------|
| Total parameters | 2.8T |
| Active parameters per token | ~50B (16/896 experts) |
| Context window | 1M tokens |
| Download size | ~1.4 TB (MXFP4) |
| API input (cache hit) | $0.30/MTok |
| API input (cache miss) | $3.00/MTok |
| API output | $15.00/MTok |

**Why it matters:** Self-hosting eliminates the China data-residency risk inherent in the Kimi API. The open-weight release also enables academic auditing of a frontier-class Chinese model at scale, and is the first time a 2.8T-parameter architecture is available for community fine-tuning and research. Developers with the compute to run it can use it commercially once licensing terms are confirmed from the Hugging Face model card.

---

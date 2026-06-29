# Models — 2026-06-29

## Qwen-Image-2.0-RL: reinforcement learning post-training for diffusion image generation <a id="qwen-image-20-rl"></a>

**Source:** [arXiv 2606.27608](https://arxiv.org/abs/2606.27608) · **Type:** paper/release · **Time (UTC):** —

The Qwen team published a technical report describing a post-training pipeline that applies GRPO-based reinforcement learning and on-policy distillation (OPD) to the Qwen-Image-2.0 diffusion model. Rather than fine-tuning on curated datasets, the approach constructs composite reward models by fine-tuning VLMs with pointwise chain-of-thought scoring across dimensions: alignment, aesthetics, portrait fidelity, instruction accuracy, and face identity preservation. A hybrid classifier-free guidance strategy prevents the RL phase from collapsing pre-trained capability, and a trajectory-level velocity matching objective is used for on-policy distillation to merge multiple specialized policies into one.

**Why it matters:** The method adds +78 Elo on the text-to-image arena and +93 on image editing without architectural changes — demonstrating that RLHF-style training is transferring from LLMs to diffusion models with similar gains. Engineers building image generation pipelines can expect reward-model-guided RL to become a standard post-training step for diffusion models.

| Metric | Baseline | After RL |
|---|---|---|
| Qwen-Image-Bench overall | 55.23 | 57.84 (+2.61) |
| T2I arena Elo | 1115 | 1193 (+78) |
| Image editing arena Elo | 1256 | 1349 (+93) |

---

_No other notable model releases today._

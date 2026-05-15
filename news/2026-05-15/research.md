# Research — 2026-05-15

## SU-01: Gold-Medal Olympiad Reasoning via Unified Scaling <a id="su-01-olympiad"></a>

**Source:** [arXiv 2605.13301](https://arxiv.org/abs/2605.13301) · **Type:** paper · **Time (UTC):** May 13

Yafu Li, Runzhe Zhan, Haoran Zhang, and 25 co-authors present **SU-01**, a 30B-A3B MoE model that achieves gold-medal-level performance on IMO 2025, USAMO 2026, IPhO 2024, and IPhO 2025 — the first published system to match competition-level performance on this combination of math and physics benchmarks. The training recipe has three stages: (1) reverse-perplexity curriculum SFT to develop rigorous proof-search habits; (2) reinforcement learning with verifiable rewards to improve solution correctness; (3) proof-level RL that optimizes full argument structure rather than individual steps. SU-01 supports reasoning trajectories exceeding 100,000 tokens, necessary for working through multi-page proofs.

**Why it matters:** Prior Olympiad-level math results required purpose-built, closed-access systems. SU-01 demonstrates that a relatively compact 3B-active-parameter MoE with a systematic three-stage training recipe can reach competition gold. The recipe is described as "simple and unified" — implying it generalizes beyond a single benchmark.

| Benchmark | Result |
|-----------|--------|
| IMO 2025  | Gold-medal level |
| USAMO 2026 | Gold-medal level |
| IPhO 2024 | Gold-medal level |
| IPhO 2025 | Gold-medal level |
| Max reasoning trace | >100,000 tokens |

---

## SDAR: Self-Distilled Agentic Reinforcement Learning <a id="sdar-agentic-rl"></a>

**Source:** [arXiv 2605.15155](https://arxiv.org/abs/2605.15155) · **Type:** paper · **Time (UTC):** May 15

Zhengxi Lu, Zhiyuan Yao, and nine co-authors propose **SDAR**, a training method that stabilizes combining on-policy RL with token-level self-distillation for multi-turn agent tasks. The key mechanism is a sigmoid gate that amplifies distillation on tokens where the on-policy model improves over the teacher (positive gap) and suppresses it where the teacher produces worse outputs — keeping RL as the primary optimization backbone while using distillation as a gated auxiliary signal.

**Why it matters:** Token-level distillation in multi-turn settings typically causes training instability because the teacher policy and student policy diverge asymmetrically across turns. SDAR addresses this systematically. The gains on WebShop (+10.2% over GRPO) and ALFWorld (+9.4%) are consistent across multiple model families, suggesting the gating mechanism is broadly applicable.

| Benchmark | vs GRPO baseline |
|-----------|----------------:|
| WebShop   | +10.2%          |
| ALFWorld  | +9.4%           |
| Search-QA | +7.0%           |

---

## SANA-WM: Minute-Scale World Modeling at 36× Throughput <a id="sana-wm"></a>

**Source:** [arXiv 2605.15178](https://arxiv.org/abs/2605.15178) · **Type:** paper · **Time (UTC):** May 15

NVIDIA researchers present **SANA-WM**, a 2.6B-parameter open-source world model that synthesizes 720p, minute-length videos with precise 6-DoF camera control. Four architectural innovations combine: (1) Hybrid Linear Attention (frame-wise Gated DeltaNet + softmax attention for long-context efficiency); (2) Dual-Branch Camera Control for trajectory adherence; (3) a Two-Stage Generation Pipeline with a long-video refiner; and (4) an annotation pipeline extracting metric-scale camera poses from public video. Training required 15 days on 64 H100s; the model also runs on a single GPU in quantized form.

**Why it matters:** Minute-scale world models at 720p are a significant quality jump from prior work on short video clips. The 36× throughput improvement over prior open-source baselines and the consumer-GPU quantized path make this practically deployable for simulation, data generation, and embodied AI research.

---

## MemEye: Visual-Centric Agent Memory Evaluation <a id="memeye-agent-memory"></a>

**Source:** [arXiv 2605.15128](https://arxiv.org/abs/2605.15128) · **Type:** paper · **Time (UTC):** May 15

MemEye proposes a benchmark framework specifically for evaluating **memory in multimodal AI agents** — a capability missing from standard VLM and agent benchmarks that typically measure single-turn visual understanding. The framework covers long-term context recall, cross-session memory retention, and visual episodic memory across 17 authors' test protocols.

**Why it matters:** As agents operate across extended sessions and multiple modalities, memory quality becomes a critical dimension that accuracy-on-benchmarks does not capture. MemEye gives researchers and practitioners a standardized way to compare agent memory systems, which is increasingly relevant as products like Notion Workers, Claude Cowork, and similar platforms lean on long-session agent continuity.

---

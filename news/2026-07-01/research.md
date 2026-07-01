# Research — 2026-07-01

## RLMF: Reinforcement Learning with Metacognitive Feedback <a id="rlmf-metacognitive"></a>

**Source:** [arXiv 2606.32032](https://arxiv.org/abs/2606.32032) · **Type:** paper · **Time (UTC):** Jun 30 (HF daily papers Jul 1)

Google researchers introduce RLMF, a reinforcement learning paradigm that trains LLMs to accurately represent their own uncertainty rather than hallucinating with high confidence. The core idea: rather than using only external reward signals, the training loop incorporates the model's own performance self-judgments as a refinement signal for completion rankings. A companion mechanism, Metacognitive Data Selection, uses these self-judgments to identify training examples where the model's uncertainty is most informative — outperforming standard active learning selection strategies.

Results show up to 63% improvement over standard RL methods on faithful calibration benchmarks across diverse tasks, while preserving task accuracy. A two-stage pipeline first calibrates raw confidence scores, then maps them to natural language uncertainty expressions ("I'm fairly confident that...", "I'm not certain, but...").

**Why it matters:** Miscalibrated confidence is one of the most persistent practical failure modes in deployed LLMs. RLMF offers a training-time fix — not a post-hoc classifier bolted on at inference — which means calibration improvements persist across task types and don't add inference latency.

---

## Orca: The World is in Your Mind <a id="orca-world-model"></a>

**Source:** [arXiv 2606.30534](https://arxiv.org/abs/2606.30534) · **Type:** paper · **Time (UTC):** Jun 29 submitted, Jun 30 revised

A 57-author consortium introduces Orca, a foundation model that learns unified world representations from multimodal signals using Next-State-Prediction (NSP) modeling. Rather than training separate specialist models for vision, language, or action, Orca combines two learning modes: "unconscious learning" on 125,000 hours of continuous video (dense state transitions) and "conscious learning" on 160 million language-annotated events and VQA pairs (sparse meaningful transitions).

Evaluation freezes the backbone and trains only lightweight modality-specific decoders on downstream tasks (text generation, image prediction, embodied action generation). Orca outperforms comparably-sized specialized models across all three task types, suggesting world modeling is a transferable representation that generalizes beyond the modalities it was trained on.

**Why it matters:** If NSP-trained world models can serve as a general backbone for downstream tasks the way language models do for text, it could reduce the need to train separate specialist models for robotics, video understanding, and image generation. The fully-public 125K-hour video dataset is also likely to be reused by other groups.

---

## Dockerless: Environment-Free Program Verifier for Coding Agents <a id="dockerless-verifier"></a>

**Source:** [arXiv 2606.28436](https://arxiv.org/abs/2606.28436) · **Type:** paper · **Time (UTC):** Jun 28 submitted (HF daily papers Jul 1)

ByteDance Research presents Dockerless, a verifier for AI-generated code patches that eliminates the need to spin up Docker containers or execute test suites. Instead of running the patch, Dockerless uses agentic repository exploration — intelligently reading the codebase, test files, and dependency graph — to estimate whether a patch is correct. This enables a fully environment-free post-training pipeline suitable as a reward signal for both supervised fine-tuning and reinforcement learning.

On benchmarks, Dockerless outperforms the strongest open-source verifier by 14.3 AUC points and achieves 62.0%, 50.0%, and 35.2% resolve rates on three SWE-bench variants — matching execution-based approaches on the hardest variant while surpassing the Qwen3.5-9B baseline by 2.4–8.7 points.

**Why it matters:** Docker-based verification is the infrastructure bottleneck for large-scale coding agent training: each episode requires provisioning a per-repository environment, running tests, and tearing down the container. Dockerless cuts this overhead entirely, which could substantially reduce the compute cost of training and evaluating coding agents.

---

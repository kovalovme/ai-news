# Research — 2026-05-22

## Escaping Mode Collapse in LLM Generation via Geometric Regulation <a id="rmr-mode-collapse"></a>

**Source:** [arXiv 2605.00435](https://arxiv.org/abs/2605.00435) · **Type:** paper · **Time (UTC):** —

Xin Du and Kumiko Tanaka-Ishii (Waseda University) propose Reinforced Mode Regulation (RMR), an inference-time intervention that addresses mode collapse in autoregressive language models. The paper reframes mode collapse not as a decoding-temperature problem but as a geometric failure: the model's internal trajectory through the representation space collapses into a low-dimensional metastable region, measurable as a drop in the correlation dimension of the value cache. RMR applies low-rank damping to the dominant self-reinforcing directions in the Transformer value cache at inference time, without any retraining or fine-tuning.

Empirical results: standard decoding methods collapse at roughly 2.0 nats/step entropy; RMR maintains coherent, diverse generation down to 0.8 nats/step while outperforming standard decoding methods (greedy, temperature sampling, nucleus sampling) on both quality and diversity metrics. The paper was accepted to ICML 2026.

**Why it matters:** Mode collapse under low-temperature or repetitive-prompt conditions is a persistent practical failure mode for deployed LLMs — it manifests as stuck loops, identical outputs, and degraded instruction following in long contexts. An inference-time fix (no retraining, no architecture changes) is immediately applicable to any Transformer-based model in production. The geometric framing also opens a diagnostic lens: correlation dimension of the value cache as a runtime monitor for collapse risk.

---

## RADAR: Defending RAG Dynamically against Retrieval Corruption <a id="radar-rag-defense"></a>

**Source:** [arXiv 2605.22041](https://arxiv.org/abs/2605.22041) · **Type:** paper · **Time (UTC):** —

Ziyuan Chen and colleagues propose RADAR, a defense framework for retrieval-augmented generation (RAG) systems that must operate in adversarial environments where retrieved documents may be poisoned. The core insight is that reliable context selection can be modeled as an energy minimization problem over a graph of retrieved candidates, solved exactly via Max-Flow Min-Cut. RADAR additionally maintains a Bayesian memory that updates belief distributions over document trustworthiness rather than storing raw retrieval scores, enabling the system to adapt to evolving attack patterns without restarting.

Evaluated against corpus poisoning, query-injection, and indirect-prompt-injection attacks, RADAR improves factual accuracy and reduces attack success rates while maintaining minimal additional storage overhead compared to undefended RAG baselines.

**Why it matters:** As RAG becomes the standard architecture for grounding LLM outputs in enterprise knowledge bases, retrieval-layer attacks — injecting malicious documents into indexed corpora to manipulate model outputs — are an increasingly realistic threat. RADAR's Max-Flow formulation is computationally tractable at production retrieval scale, and the Bayesian memory component addresses the adversarial-adaptation problem that defeats static allowlist/denylist defenses.

---

# Research — 2026-05-21

## Are Tools All We Need? Efficiency Costs of Tool Use in LLM Agents <a id="are-tools-all-we-need"></a>

**Source:** [arXiv cs.AI](https://arxiv.org/list/cs.AI/current) · **Type:** paper · **Time (UTC):** May 21

A paper submitted to arXiv on May 21 (Zhang et al., accepted to ICML 2026) investigates what the authors call the "tool-use tax" — the token and latency overhead incurred when LLM agents call external tools compared to answering directly. The core finding is that the benefit of tool access is highly task-dependent: on tasks where the model's parametric knowledge is sufficient, mandatory tool invocation adds cost with no accuracy gain, and in some setups the tool-calling chain introduces hallucination in result parsing that exceeds any accuracy gain from retrieval.

The paper proposes a "tool necessity classifier" — a lightweight gating module trained to predict, from the query embedding and tool manifest, whether tool invocation is likely to improve the final answer. On a suite of agentic benchmarks, selectively routing queries through the classifier reduces average token usage by 31% while matching or improving task-completion accuracy relative to always-use-tools baselines.

**Why it matters:** As agentic frameworks add more tools by default, "call everything" becomes the path of least resistance. This work provides both an empirical warning that tool proliferation has computable costs and a lightweight architectural solution (the necessity classifier) that engineers can layer onto existing agent loops without retraining the base model.

---

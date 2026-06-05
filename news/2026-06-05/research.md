# Research — 2026-06-05

## AdaPlanBench: Adaptive Planning Under Dynamically Revealed Constraints <a id="adaplan-bench"></a>

**Source:** [arXiv 2606.05622](https://arxiv.org/abs/2606.05622) · **Type:** paper · **Time (UTC):** Jun 5

Jiayu Liu, Cheng Qian, Zhenhailong Wang et al. (UIUC) introduce AdaPlanBench, a 307-task interactive benchmark that tests whether LLM agents can revise plans as constraints surface during execution rather than being fully specified upfront. The benchmark simulates household tasks under two constraint types that appear progressively: world constraints (physical feasibility) and user constraints (preference-based). Agents propose plans, receive violation feedback, and must iteratively correct. Across ten leading models the best achieved only 67.75% accuracy; user constraints proved significantly harder than world constraints, and performance degrades as constraint counts accumulate.

**Why it matters:** Most agent evals front-load all constraints, masking a core real-world failure mode: agents that cannot integrate new restrictions mid-task. The 67.75% ceiling on frontier models with 307 household scenarios is a concrete signal of where planning robustness currently breaks.

| Metric | Best model |
|---|---|
| Adaptive planning accuracy | 67.75% |
| Harder constraint type | User |
| Task count | 307 |

---

## Tangram: Non-Uniform KV Cache for Multi-Turn LLM Serving <a id="tangram-kv-cache"></a>

**Source:** [arXiv 2606.06302](https://arxiv.org/abs/2606.06302) · **Type:** paper · **Time (UTC):** Jun 5

Hyungmin Kim, Minsoo Kim, Hongseok Kim, and Jungwook Choi introduce Tangram, a KV-cache compression system that exploits per-head importance variation rather than applying uniform compression ratios. Three techniques address the engineering obstacles of non-uniform compression: **deterministic budget allocation** assigns a fixed memory budget per attention head, eliminating dynamic scheduling overhead; **head group pages** cluster heads by similar retention profiles and manage them via independent page tables for efficient memory reclamation; **ahead-of-time load balancing** uses static profiles to maintain GPU utilization without runtime profiling costs. Tangram achieves up to 2.6× throughput improvement with no measured accuracy loss; implementation is open-sourced.

**Why it matters:** Uniform KV-cache quantization discards tokens that matter in some heads while over-retaining tokens that don't — Tangram's 2.6× throughput gain from exploiting this head heterogeneity is directly applicable to multi-turn agent serving where KV caches grow large.

---

## TIDE: Proactive Multi-Problem Discovery via Template-Guided Iteration <a id="tide-problem-discovery"></a>

**Source:** [arXiv 2606.04743](https://arxiv.org/abs/2606.04743) · **Type:** paper · **Time (UTC):** Jun 5

Soyeong Jeong, Jinheon Baek, Minki Kang, and Sung Ju Hwang (KAIST AI) address the gap between reactive AI agents (which answer explicit queries) and the undetected problems embedded in user contexts. TIDE enables agents to proactively discover multiple hidden problems from context through two mechanisms: **iterative discovery** surfaces candidates in batches while conditioning on previously identified issues to avoid duplication; **thought templates** are reusable schemas built from past cases that guide attention toward contextually relevant signals. Validation across personal workspaces and software repositories using four model backbones shows substantial gains over both single-shot and parallel multi-agent baselines on task coverage, identification, and resolution.

**Why it matters:** As agents are deployed in long-running background contexts (codebases, personal data vaults), the ability to surface unasked-for issues compounds their usefulness — TIDE provides a concrete, reproducible method for doing this beyond naive single-pass prompting.

---

## Reinforcement Learning Elicits Contextual Learning of Unseen Language Translation <a id="rl-unseen-translation"></a>

**Source:** [arXiv 2606.06428](https://arxiv.org/abs/2606.06428) · **Type:** paper · **Time (UTC):** Jun 5

Hanxu Hu, Zdeněk Šnajdr, Pinzhen Chen, Jannis Vamvas, and Rico Sennrich (University of Zurich) demonstrate that outcome-based reinforcement learning trains LLMs to acquire a meta-skill for in-context translation of completely unseen languages — languages not present in either pretraining or RL training data. Using a lightweight surface-level translation reward, the RL-trained models consistently extract and apply relevant linguistic information from provided context materials, outperforming both in-context learning and supervised fine-tuning on zero-shot unseen languages.

**Why it matters:** The finding extends RL post-training benefits beyond math and code reasoning into language generalization, and suggests the same approach could bootstrap low-resource language capabilities without curating explicit multilingual RL data.

---

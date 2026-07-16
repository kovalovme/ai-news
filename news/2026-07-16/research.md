# Research — 2026-07-16

## ResearcherBench: evaluating AI on frontier scientific questions <a id="researcherbench"></a>

**Source:** [arxiv 2507.16280](https://arxiv.org/abs/2507.16280) · [GitHub](https://github.com/GAIR-NLP/ResearcherBench) · **Type:** benchmark/paper · **Time (UTC):** Jul 16

Tianze Xu, Pengrui Lu, Lyumanshan Ye, Xiangkun Hu, and Pengfei Liu (Shanghai AI Lab / GAIR-NLP) introduced ResearcherBench, the first benchmark targeting "Deep AI Research Systems" (DARS) on genuine frontier AI science. The dataset contains 65 questions drawn from real laboratory discussions and expert interviews, spanning 35 AI subject areas and divided into three task types: technical detail retrieval, literature review synthesis, and open consulting. Evaluation combines rubric-based coverage scoring against expert-authored criteria with a factual faithfulness check (citation groundedness). On the initial evaluation, OpenAI Deep Research and Gemini Deep Research substantially outperformed all other systems, showing particular strength on open consulting questions. The dataset and code are open-sourced.

**Why it matters:** Most existing benchmarks measure information retrieval or report generation; ResearcherBench is designed to probe whether a system can contribute meaningfully to open scientific questions. The gap between top performers and the rest suggests current general-purpose agents are not yet close to scientific collaborators.

---

## Theory-Level Autoformalization (ICML 2026 Spotlight) <a id="theory-level-autoformalization"></a>

**Source:** [arxiv (ICML 2026 Spotlight)](https://arxiv.org/list/cs.AI/recent) · **Type:** paper · **Time (UTC):** Jul 16

Marcus J. Min, Mike He, Zhaoyu Li and colleagues presented a system for automating the translation of entire mathematical theory documents — not isolated statements — into unified formal knowledge bases in Lean 4/Mathlib. Prior autoformalization work focused on single theorems; this approach handles the dependencies between definitions, lemmas, and proofs across a document, building a consistent formal representation of an entire theory. The paper received an ICML 2026 Spotlight designation.

**Why it matters:** Scaling formal verification requires translating large bodies of existing mathematics, not just cherry-picked theorems. If the approach generalizes, it could dramatically accelerate the pace at which AI-discovered proofs (such as the Erdős problem results from last week) can be machine-checked against a shared formal library.

---

## Self-Improvements in Modern Agentic Systems: A Survey <a id="self-improving-agents-survey"></a>

**Source:** [arxiv (cs.AI, Jul 16)](https://arxiv.org/list/cs.AI/recent) · **Type:** survey · **Time (UTC):** Jul 16

Zhe Ren, Yimeng Chen, Dandan Guo and colleagues published a 97-page survey covering the landscape of self-improving AI agents — systems that autonomously enhance their own capabilities through experience, feedback, or self-generated data. The survey includes an accompanying project page and code repository.

**Why it matters:** With multiple labs actively pursuing agents that improve themselves (e.g., Codex self-distillation, AlphaEvolve self-play), a comprehensive taxonomy of existing methods is a useful reference for teams evaluating where the field currently stands and which approaches carry safety considerations.

---

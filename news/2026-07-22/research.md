# Research — 2026-07-22

## WorldCupArena: Fine-Grained LLM Evaluation on the 2026 FIFA World Cup <a id="worldcuparena"></a>

**Source:** [arXiv 2607.18084](https://arxiv.org/abs/2607.18084) · [HuggingFace Papers](https://huggingface.co/papers/2607.18084) · **Type:** paper · **Time (UTC):** —

Researchers from Shanghai Jiao Tong, Nanjing, McGill, and UCL evaluated 13 language models and deep-research agents across all 104 matches of the 2026 FIFA World Cup. Models predicted match results, exact scores, player events, match statistics, and tournament outcomes before each game kicked off (preventing data leakage). Evaluation includes result accuracy, exact-score accuracy, and a partial-credit "scoreline score" that reveals nuances binary accuracy misses.

Key findings: four systems (all frontier-class) correctly predicted Spain as champion; two recovered the exact final pairing. Models with similar result accuracy diverged significantly on granular predictions — event-level scoring exposed model differences that top-1 accuracy alone conceals. All code, prompts, and predictions are open-source on [GitHub](https://github.com/wzk1015/WorldCupArena); the framework is designed to replay on future competitions.

**Why it matters:** WorldCupArena is among the first benchmarks using a completed real-world event with publicly known outcomes as a ground truth, sidestepping the benchmark-contamination problem that plagues static leaderboards; its multi-granularity scoring is a reusable template for forecasting evals.

---

## Long-Horizon-Terminal-Bench <a id="long-horizon-terminal-bench"></a>

**Source:** [HuggingFace Papers](https://huggingface.co/papers/trending) · **Type:** paper · **Time (UTC):** —

Long-Horizon-Terminal-Bench is a 46-task evaluation suite covering long-horizon terminal operations: multi-step shell sequences, iterative debugging loops, and context management under extended task horizons. The benchmark probes agent planning stability and output-context discipline — failure modes not visible in short-context coding evals — and complements existing SWE-bench style benchmarks.

**Why it matters:** With agents increasingly running extended shell sessions in CI and cloud environments, a benchmark targeting exactly these failure modes fills a gap between task-completion evals and production robustness; the 46 tasks are small enough for continuous integration of new agent releases.

---

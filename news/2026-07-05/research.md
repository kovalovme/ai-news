# Research — 2026-07-05

## DiscoBench: benchmarking clarification-aware deep search <a id="discobench"></a>

**Source:** [arXiv 2606.27669](https://arxiv.org/abs/2606.27669) · **Type:** paper · **Time (UTC):** —

DiscoBench is a benchmark for evaluating whether search agents proactively identify ambiguous queries, ask targeted clarification questions, and adjust their reasoning paths based on user responses. It contains 211 samples across 11 real-world domains, covering four ambiguity types, with 463 total ambiguity instances. Evaluation spans four axes: task utility, ambiguity detection, interaction strategy, and cost efficiency. The benchmark includes a user simulator for multi-turn interaction. The core experimental finding is that ambiguity detection and effective clarification are distinct capabilities — most current models can detect some ambiguity but do not ask effective clarifying questions — and that repeated searching without asking performs worse, on average, than direct guessing.

**Why it matters:** Existing agent benchmarks assume complete, well-specified queries. DiscoBench fills a real production gap: in deployed search agents, underspecified user inputs are common, and the cost of a multi-step wrong-path search is high. The benchmark gives teams a concrete harness for measuring whether their agent knows when to stop and ask.

---

## llm-coding-agent 0.1a0: Claude-based coding agent as a Python library <a id="llm-coding-agent"></a>

**Source:** [simonwillison.net](https://simonwillison.net/2026/Jul/2/) · **Type:** release · **Time (UTC):** July 2, 2026

Simon Willison released llm-coding-agent 0.1a0, an early-alpha Python library that implements a Claude Fable–backed coding agent. The library was developed partly by using Claude Fable to advance the project itself toward a stable 4.0 release of Willison's sqlite-utils utility. The 0.1a0 tag signals pre-stable; the library is designed to integrate with Willison's broader `llm` CLI ecosystem.

**Why it matters:** Willison's ecosystem tools (datasette, sqlite-utils, llm CLI) are widely used in the Python/data community. A published coding agent library from a trusted OSS author provides a reference implementation that practitioners can inspect, fork, or extend — distinct from vendor-provided agent SDKs.

---

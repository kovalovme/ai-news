# Tools — 2026-06-09

## FrontierCode: benchmark for production-quality, mergeable code <a id="frontiercode"></a>

**Source:** [Cognition AI Blog](https://cognition.ai/blog/frontier-code) · **Type:** release · **Time (UTC):** Jun 08

Cognition published FrontierCode, a coding benchmark built in collaboration with 20+ open-source maintainers across 36 flagship repositories, each contributor investing 40+ hours per task. Unlike SWE-bench variants that measure whether code is functionally correct, FrontierCode grades across six axes: behavioral correctness, regression safety, mechanical cleanliness (no dead code, no unnecessary complexity), test quality, scope discipline (no over-engineering), and adherence to project style. A solution must pass all "blocker" criteria or receive zero; the resulting 81% lower false-positive rate compared to competing benchmarks is the headline claim. The 150 tasks are distributed across three tiers — Extended (150), Main (100), and Diamond (50 hardest). Claude Opus 4.8 leads all tested models at 13.4% on Diamond, with GPT-5.5 at 6.3% and Gemini 3.1 Pro at 4.7%; the best open-source model (Kimi K2.6) scores 3.8%. Cognition is opening evaluation access to model creators while keeping task specifics private to prevent contamination.

**Why it matters:** All leading frontier models score below 15% on the hardest tasks in a benchmark designed by people who actually merge pull requests — a concrete signal on the gap between passing tests and writing code engineers would accept into production.

| Model | Diamond (50 tasks) | Main (100 tasks) | Extended (150 tasks) |
|---|---|---|---|
| Claude Opus 4.8 | **13.4%** | **34.3%** | **51.8%** |
| GPT-5.5 | 6.3% | — | — |
| Gemini 3.1 Pro | 4.7% | — | — |
| Kimi K2.6 (best open) | 3.8% | 16.0% | 37.0% |

---

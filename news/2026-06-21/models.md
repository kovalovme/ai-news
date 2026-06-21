# Models — 2026-06-21

## GLM-5.2: hallucination rate 3× lower than GPT-5.5 on AA-Omniscience benchmark <a id="glm-52-hallucination"></a>

**Source:** [Artificial Analysis comparison](https://artificialanalysis.ai/models/comparisons/glm-5-2-vs-gpt-5-5) · **Type:** benchmark update · **Time (UTC):** —

A Hacker News thread (524 points, ~250 comments, posted June 20) surfaced Artificial Analysis data showing GLM-5.2 achieves a roughly three-times-lower hallucination rate than GPT-5.5 on the AA-Omniscience benchmark — the widest gap between the two models across any evaluated dimension. GLM-5.2 retains the top open-weights Intelligence Index score of 51, and the hallucination comparison adds factual grounding to the coding-performance case already established at launch.

**Why it matters:** For agentic pipelines where wrong tool invocations and fabricated facts compound across steps, a 3× hallucination differential at the same price tier ($1.40/$4.40 per million tokens via OpenRouter) is a strong operational argument for GLM-5.2 over GPT-5.5. Engineers evaluating retrieval-augmented or tool-calling workflows should weight this benchmark alongside SWE-bench scores.

_GLM-5.2's launch, MIT license, and SWE-bench Pro score (62.1 vs GPT-5.5's 58.6) were covered in the [2026-06-19 digest](../2026-06-19/models.md#glm-52-weights). This item covers the hallucination benchmark data generating fresh HN discussion._

---

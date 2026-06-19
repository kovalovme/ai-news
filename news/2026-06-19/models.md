# Models — 2026-06-19

## GLM-5.2 open weights land on HuggingFace <a id="glm-52-weights"></a>

**Source:** [Simon Willison](https://simonwillison.net/2026/Jun/17/glm-52/) · [VentureBeat](https://venturebeat.com/technology/z-ais-open-weights-glm-5-2-beats-gpt-5-5-on-multiple-long-horizon-coding-benchmarks-for-1-6th-the-cost/) · **Type:** release · **Time (UTC):** Jun 16 ~18:00

Z.ai's GLM-5.2 — a 753B mixture-of-experts model with 40B parameters active per forward pass — published its full MIT-licensed weights to HuggingFace on June 16 and reached OpenRouter via nine providers that same day. The model was announced June 13 for paying Z.ai Coding Plan subscribers (covered in the [June 14 digest](../2026-06-14/models.md#glm-52)); this entry covers the open-weights release and the benchmark data that emerged with it. Simon Willison described it as "probably the most powerful text-only open weights LLM" currently available.

**Why it matters:** Engineers who need a genuinely frontier-tier coding model without proprietary restrictions now have one. At ~$1.40/$4.40 per million input/output tokens via OpenRouter, it is roughly one-sixth the cost of GPT-5.5 on equivalent tasks.

| Benchmark | GLM-5.2 | GPT-5.5 | MiniMax-M3 |
|---|---|---|---|
| SWE-bench Pro | **62.1** | 58.6 | — |
| Terminal-Bench 2.1 | 81.0 | — | — |
| MCP-Atlas | 76.8 | — | — |
| GPQA Diamond | 91.2 | — | 87.x |
| Artificial Analysis Intelligence Index (open weights) | **#1 (51)** | n/a (closed) | — |

One practical caveat: GLM-5.2 uses significantly more output tokens per task (≈43K) compared to GLM-5.1 (26K) and MiniMax-M3 (24K), which affects inference costs at scale. The model does not accept image input; vision capability remains in a separate model family.

---

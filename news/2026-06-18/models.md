# Models — 2026-06-18

## GLM-5.2 Open Weights Land on Hugging Face — MIT, 753B, Beats GPT-5.5 on Coding Benchmarks <a id="glm-52-open-weights"></a>

**Source:** [Z.ai / HuggingFace blog](https://huggingface.co/blog/zai-org/glm-52-blog) · [VentureBeat](https://venturebeat.com/technology/z-ais-open-weights-glm-5-2-beats-gpt-5-5-on-multiple-long-horizon-coding-benchmarks-for-1-6th-the-cost) · [Simon Willison](https://simonwillison.net/2026/Jun/17/glm-52/) · **Type:** release (open weights) · **Time (UTC):** Jun 16 ~12:00

Z.ai released the full open weights for GLM-5.2 under an MIT license on June 16, roughly a week earlier than the "~Jun 20" window signaled at launch. The model is now freely downloadable from Hugging Face and available via the Z.ai API with no access restrictions. GLM-5.2 is a 753-billion-parameter model with a genuine 1-million-token context window and up to 131K output tokens. Independent evaluations that were pending at the June 13 coding-plan launch have now been published: it scores 62.1 on SWE-bench Pro (GPT-5.5: 58.6; Claude Opus 4.8: 75.1) and 74.4% on FrontierSWE (GPT-5.5: 72.6%; Claude Opus 4.8: 75.1%). On the Artificial Analysis Intelligence Index v4.1 it ranks first among open-weight models with a score of 51. Simon Willison noted the model is token-heavy — averaging 43K output tokens per Intelligence Index task vs. GPT-5.5's lower count — and ranks second on the Code Arena WebDev leaderboard.

**Why it matters:** GLM-5.2 becomes the highest-ranking open-weight model on the Intelligence Index the week the Fable 5 export ban enters its third week; engineers outside the United States who need frontier-class coding capability without US-provider dependency now have a concrete unrestricted option. The 1/6th cost of GPT-5.5 and MIT license make it viable for self-hosted production workloads.

| Attribute | Value |
|-----------|-------|
| Params | 753B (MoE) |
| Context | 1,000,000 tokens |
| Max output | 131,072 tokens |
| License | MIT |
| SWE-bench Pro | 62.1 (#1 open-weight) |
| FrontierSWE | 74.4% (#2 overall) |
| Intelligence Index v4.1 | 51 (#1 open-weight) |
| API pricing | $1.40/M input tokens |

---

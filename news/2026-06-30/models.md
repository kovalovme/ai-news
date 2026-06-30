# Models — 2026-06-30

## LongCat 2.0 open-sourced by Meituan <a id="longcat-20"></a>

**Source:** [LongCat Blog](https://longcat.chat/blog/longcat-2.0) · [HuggingFace](https://huggingface.co/meituan-longcat/LongCat-2.0) · [SCMP](https://www.scmp.com/tech/tech-trends/article/3358854/china-debuts-biggest-ai-model-trained-local-chips-meituan-releases-longcat-20) · [VentureBeat](https://venturebeat.com/technology/meituan-open-sources-longcat-2-0-the-1-6t-near-frontier-agentic-coding-model-thats-been-leading-openrouter-trained-entirely-on-chinese-chips) · **Type:** release · **Time (UTC):** ~00:00

Meituan released LongCat-2.0 on June 30, ending two months during which the same model operated anonymously as "Owl Alpha" on OpenRouter — where it topped global developer charts without anyone knowing its origin. The model carries 1.6 trillion total parameters with approximately 48 billion activated per forward pass and a native 1-million-token context window. Pretraining spanned more than 35 trillion tokens across millions of accelerator-hours on over 50,000 Chinese-made AI ASICs — no NVIDIA hardware involved at any stage. Meituan developed two novel architectural components: LongCat Sparse Attention (LSA) for long-horizon task performance, and 5-gram N-gram Embedding (135B parameters) for faster prefill. The model ships under the MIT license with no regional restrictions.

**Why it matters:** This is the first 1T+ parameter model trained entirely on non-NVIDIA hardware to reach public open-source release with a commercially permissive license; its 59.5 SWE-bench Pro score (narrowly above GPT-4.5's 58.6) sets a new high-water mark for Chinese open-source agentic coding capability and demonstrates that CUDA-free frontier training is now viable at scale.

| Spec | Value |
|------|-------|
| Total parameters | ~1.6T |
| Active parameters / token | ~48B |
| Context window | 1M tokens |
| Training hardware | Chinese AI ASICs (50K+) |
| License | MIT |
| SWE-bench Pro | 59.5 |

---

## Ornith-1.0: self-scaffolding agentic coding models <a id="ornith-10"></a>

**Source:** [ornith.site](https://ornith.site/) · [GitHub](https://github.com/deepreinforce-ai/Ornith-1) · [TechTimes](https://www.techtimes.com/articles/319122/20260626/open-source-coding-model-ornith-10-writes-its-own-training-scaffold-reinforcement-learning.htm) · **Type:** release · **Time (UTC):** Jun 25 (first coverage)

DeepReinforce AI released Ornith-1.0 on June 25 — this is its first appearance in this digest. The model family (9B Dense, 31B Dense, 35B MoE, 397B MoE) is built on Gemma 4 and Qwen 3.5 foundations with a 256K-token context window, MIT license, and no regional restrictions. The distinguishing training technique is self-scaffolding RL: rather than treating the agentic scaffold (tool calling sequence, task planning structure) as a fixed external component, Ornith learns both the scaffold and the solution policy simultaneously during RL training. The model generates its own task plans, launches tools, inspects intermediate results, and rewrites failing steps without human-authored scaffolding templates.

**Why it matters:** The 397B MoE variant claims 82.4 on SWE-Bench Verified and 77.5 on Terminal-Bench 2.1 — surpassing Claude Opus 4.7 on both — making it the strongest MIT-licensed agentic coding model currently available; the 35B MoE reaches 64.2 on Terminal-Bench 2.1, beating Qwen 3.5-397B (53.5) at a fraction of the activated parameter count.

| Model | Terminal-Bench 2.1 | SWE-Bench Verified | SWE-Bench Pro | SWE-Bench Multilingual |
|-------|-------------------:|-------------------:|--------------:|----------------------:|
| 35B MoE | 64.2 | — | — | — |
| 397B MoE | 77.5 | 82.4 | 62.2 | 78.9 |

---

## Gemini 3.5 Pro misses June GA deadline <a id="gemini-35-pro-delay"></a>

**Source:** [Bind AI](https://blog.getbind.co/gemini-3-5-pro-slips-to-july-and-four-senior-google-researchers-just-left-for-anthropic/) · [Cryptobriefing](https://cryptobriefing.com/google-delays-gemini-35-pro-launch-to-july-2026/) · **Type:** update · **Time (UTC):** —

At Google I/O on May 19, Sundar Pichai said "give us until next month" for Gemini 3.5 Pro general availability. June 30 closes without a public API launch. As of today the model remains in limited enterprise preview on Vertex AI; Business Insider reported the delay stems from token-efficiency issues identified during extended enterprise testing. The revised target is mid-to-late July. This is Google's second major AI delivery miss in 2026, following a three-month delay for Gemini Ultra 1.5 earlier in the year.

**Why it matters:** Developers who built Q2 project schedules around Google I/O commitments will need to adjust; the only access path to Gemini 3.5 Pro today is an enterprise Vertex AI relationship.

---

## Grok 5 misses second consecutive quarterly deadline <a id="grok-5-q2"></a>

**Source:** [xAI News](https://x.ai/news) · [WaveSpeed tracker](https://wavespeed.ai/blog/posts/grok-5-launch-tracker/) · [ChatForest Q2 wrap](https://chatforest.com/builders-log/q2-closes-fable-5-grok-5-gemini-pro-gpt56-july-frontier-access-map-builder-guide/) · **Type:** update · **Time (UTC):** 23:59

Q2 2026 closed today with no Grok 5 announcement, no API documentation, and no benchmark disclosures from xAI. This is the model's second consecutive missed quarterly target — xAI originally pointed to Q1 2026 in its January Series E announcement, then extended to Q2. The model remains in training on the Colossus 2 cluster. Prediction markets had the June 30 release probability at approximately 7% as the deadline approached. Grok 4.3 remains xAI's current shipping model.

**Why it matters:** With Grok 5 rumored to be a 6T-parameter-class model, each quarter of delay extends the window in which competitors can consolidate developer adoption at that capability tier.

---

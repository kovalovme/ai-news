# Products — 2026-04-28

## ChatGPT for Clinicians + HealthBench Professional <a id="chatgpt-clinicians"></a>

**Source:** [OpenAI Blog](https://openai.com/index/making-chatgpt-better-for-clinicians/) · **Type:** launch · **Time (UTC):** April 22, 2026

OpenAI launched ChatGPT for Clinicians as a free, verified-access workspace for US physicians, nurse practitioners, physician assistants, and pharmacists. Verification requires a National Provider Identifier (NPI); international rollout has not been announced. The product sits between the consumer ChatGPT experience and the paid ChatGPT for Healthcare enterprise tier, offering clinical search with cited real-time answers, reusable "skills" for recurring documentation workflows (referral letters, prior authorisations), and access to GPT-5.5 models tuned for clinical language. Alongside the product, OpenAI released HealthBench Professional, an open benchmark built from physician-authored conversations across three use cases — care consult, writing and documentation, and medical research — with multi-stage physician adjudication for rubric scoring.

**Why it matters:** Free API-level model access for individual clinicians, rather than requiring enterprise contracting, dramatically lowers the adoption barrier. HealthBench Professional gives labs and clinicians a standardised, openly reproducible method for comparing AI assistants on realistic clinical tasks — a gap left open by earlier consumer-health benchmarks.

---

## Google TPU 8t & 8i: Eighth-Generation AI Silicon <a id="google-tpu-8t-8i"></a>

**Source:** [Google Blog](https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/eighth-generation-tpu-agentic-era/) · **Type:** release · **Time (UTC):** April 22, 2026 (Google Cloud Next 2026)

Google announced its eighth-generation Tensor Processing Units at Google Cloud Next 2026, split into two purpose-built chips. The TPU 8t targets large-scale training: it delivers 121 ExaFlops of FP4 compute per pod, scales to 9,600 chips with 2 PB of shared HBM, and achieves nearly 3× the compute performance of the prior Ironwood generation while targeting >97 % goodput. The TPU 8i targets inference at scale: 11.6 ExaFlops of FP8 per pod, 331.8 TB total HBM, 19.2 Tb/s bidirectional scale-up bandwidth (2× Ironwood), and 80 % better performance-per-dollar — allowing nearly double the customer volume at equivalent cost. Both chips achieve up to 2× better performance-per-watt. General availability is planned for later in 2026.

**Why it matters:** Splitting training and inference into dedicated silicon reflects a permanent architectural divergence in AI workloads: frontier model training needs massive parallelism and memory bandwidth, while agentic inference needs ultra-low latency and high token throughput. The TPU 8i's 80 % cost improvement directly affects Google Cloud pricing for Gemini-based API calls.

| Chip | Compute | HBM/pod | Perf vs Ironwood |
|---|---|---|---|
| TPU 8t | 121 ExaFlops FP4 | 2 PB | ~3× training |
| TPU 8i | 11.6 ExaFlops FP8 | 331.8 TB | 80% better perf/$ |

---

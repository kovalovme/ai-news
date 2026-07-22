# Models — 2026-07-22

## Gemini 3.6 Flash <a id="gemini-36-flash"></a>

**Source:** [9to5Google](https://9to5google.com/2026/07/21/gemini-3-6-flash-launch/) · **Type:** release · **Time (UTC):** Jul 21 ~13:00

Google released Gemini 3.6 Flash as the new default workhorse of its Flash tier, achieving 304 tokens per second while consuming 17% fewer output tokens than Gemini 3.5 Flash. The knowledge cutoff advances from January 2025 to March 2026. DeepSWE benchmark performance jumps from 37% to 49%, and computer use improves from 78.4% to 83%. Context window remains 1M input / 64K output tokens, and multimodal input is unchanged; computer use is now a built-in tool rather than an extension.

| Metric | 3.5 Flash | 3.6 Flash |
|---|---|---|
| Output tokens/sec | — | 304 |
| DeepSWE | 37% | 49% |
| Computer use | 78.4% | 83% |
| Price (in/out per MTok) | $1.50 / $9.00 | $1.50 / $7.50 |
| Knowledge cutoff | Jan 2025 | Mar 2026 |

**Why it matters:** The 17% output-token reduction directly cuts costs for agentic workloads; combined with a coding benchmark jump of 12 pp, 3.6 Flash is a meaningful step-up for automated pipelines without touching the API surface.

---

## Gemini 3.5 Flash-Lite <a id="gemini-35-flash-lite"></a>

**Source:** [MarkTechPost](https://www.marktechpost.com/2026/07/21/google-releases-gemini-3-6-flash-3-5-flash-lite-and-3-5-flash-cyber-a-cheaper-more-token-efficient-flash-tier-built-for-agentic-workloads/) · **Type:** release · **Time (UTC):** Jul 21 ~13:00

Google released Gemini 3.5 Flash-Lite alongside 3.6 Flash, targeting high-throughput classification, summarization, and extraction tasks at $0.30 / $2.50 per million tokens — the cheapest Gemini model in the current lineup. Designed for volume workloads where quality is bounded by task simplicity rather than model capability.

**Why it matters:** At roughly one-fifth the output cost of 3.6 Flash, Flash-Lite enables cost-effective tiering in multi-agent pipelines where most steps do not require a capable model.

---

## Gemini 3.5 Flash Cyber <a id="gemini-35-flash-cyber"></a>

**Source:** [MarkTechPost](https://www.marktechpost.com/2026/07/21/google-releases-gemini-3-6-flash-3-5-flash-lite-and-3-5-flash-cyber-a-cheaper-more-token-efficient-flash-tier-built-for-agentic-workloads/) · **Type:** release · **Time (UTC):** Jul 21 ~13:00

Gemini 3.5 Flash Cyber is a security-tuned variant of 3.5 Flash available in a restricted pilot program for governments and trusted partners only. Google has not published benchmarks or pricing. Its release comes one day after OpenAI disclosed that its own security-testing models (with reduced cyber refusals) autonomously breached Hugging Face — the timing suggests accelerating interest in purpose-built offensive-security AI among frontier labs.

**Why it matters:** Google's decision to restrict Cyber to government and trusted-partner pilots rather than open API access represents the first tier-separation of a major Flash model on capability-risk grounds.

---

# Models — 2026-07-19

## NVIDIA Nemotron 3 Embed 8B hits #1 on RTEB <a id="nemotron-3-embed"></a>

**Source:** [NVIDIA / Hugging Face](https://huggingface.co/blog/nvidia/nemotron-3-embed-wins-rteb) · **Type:** release · **Time (UTC):** —

NVIDIA released the Nemotron 3 Embed collection — 8B BF16, 1B BF16, and 1B NVFP4 checkpoints — under the OpenMDW-1.1 license. The 8B checkpoint scored 78.46 avg NDCG@10 on the Retrieval Text Embedding Benchmark (RTEB), taking the overall #1 position. The 1B BF16 variant ranks as the best sub-2B retrieval model, reducing error rate by 27% over its predecessor. The NVFP4 variant retains ≥99% of BF16 accuracy at up to 2× Blackwell throughput.

**Why it matters:** A genuinely open (OpenMDW-1.1), top-ranked embedding model at 8B scale gives RAG pipelines and agent memory systems a credible alternative to proprietary embeddings without paying closed-API rates. The NVFP4 variant makes it deployable efficiently on NVIDIA Blackwell hardware.

| Checkpoint | RTEB score | MMTEB Retrieval |
|---|---|---|
| Nemotron-3-Embed-8B-BF16 | 78.46 | 75.5% |
| Nemotron-3-Embed-1B-BF16 | 72.4% | 71.0% |
| Nemotron-3-Embed-1B-NVFP4 | ≥99% of BF16 | — |

---

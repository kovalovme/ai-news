# Models — 2026-07-11

## Mistral Robostral Navigate — 8B Single-Camera Robot Navigation Model <a id="robostral-navigate"></a>

**Source:** [Mistral AI](https://mistral.ai/news/robostral-navigate/) · [Bloomberg](https://www.bloomberg.com/news/articles/2026-07-08/mistral-ai-releases-robotics-model-to-support-physical-ai-push) · **Type:** release · **Time (UTC):** July 8

Mistral released Robostral Navigate, an 8B parameter navigation model that enables autonomous robot movement using only a single RGB camera and natural-language instructions — no LiDAR, depth sensors, or multi-camera rigs required. The model accepts an image stream from the camera plus a plain-English destination description and outputs navigation commands. It was trained entirely in simulation on roughly 400,000 trajectories across 6,000 synthetic scenes, with prefix-caching reducing training token count by 22× while preserving learning signal. Online reinforcement learning improved the unseen-environment success rate by 3.2 percentage points, with no performance plateau observed. The model is hardware-agnostic and runs on wheeled, legged, and flying platforms across different robot sizes.

| Benchmark | Robostral Navigate | Best prior single-camera | Best prior multi-sensor |
|-----------|------------------:|------------------------:|------------------------:|
| R2R-CE unseen (success %) | **76.6** | 66.9 | 72.1 |
| R2R-CE seen (success %) | 79.4 | — | — |

**Why it matters:** Mistral's first robotics model lands into a week when all three major humanoid robotics companies are moving toward public markets. The 4.5-point gap over the best multi-sensor system matters practically: single-camera robots are dramatically cheaper and easier to deploy in unstructured spaces than LiDAR-equipped alternatives. Robostral Navigate's simulation-only training also lowers the data-collection barrier for new robot OEMs to adopt the model without gathering real-world navigation datasets.

---

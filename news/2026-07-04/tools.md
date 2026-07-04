# Tools — 2026-07-04

## Claude Reaches GA on Azure AI Foundry with NVIDIA GB300 Blackwell Ultra <a id="claude-azure-foundry-gb300"></a>

**Source:** [NVIDIA Blog](https://blogs.nvidia.com/blog/anthropic-nvidia-gb300-blackwell-ultra-microsoft-azure/) · **Type:** release · **Time (UTC):** Jun 29

Anthropic's Claude models reached general availability on Microsoft Foundry on June 29, 2026 — the first deployment of Claude on NVIDIA's GB300 Blackwell Ultra GPU infrastructure. The launch makes Claude Opus 4.8 and Claude Haiku 4 available to Azure-native enterprises via a serverless token-billing model with no infrastructure provisioning required. The GB300 module pairs a 72-core Grace CPU with a Blackwell Ultra GPU die, delivers 2.5 TB/s interconnect bandwidth and 288 GB of coherent HBM4 memory, and drops token costs approximately 50% versus the prior A100-based infrastructure. Initial regional availability covers Azure East US, West Europe, and Southeast Asia, with additional regions rolling out through Q3 2026.

**Why it matters:** The cost reduction is the headline: long-context and multi-turn agentic sessions that were economically marginal on A100 infrastructure become viable at GB300 pricing. Azure-native teams that have been routing to Bedrock or Vertex for cost reasons now have a comparable path without leaving the Azure ecosystem. The reservation discount tier (up to 30% for committed throughput) signals that Microsoft is targeting committed enterprise workloads, not just ad-hoc API calls.

| Model | Availability | Billing |
|---|---|---|
| Claude Opus 4.8 | Azure East US, West Europe, SE Asia | Per-1K-token, serverless |
| Claude Haiku 4 | Azure East US, West Europe, SE Asia | Per-1K-token, serverless |
| Sonnet 5 | Roadmap (Q3 2026) | — |

---

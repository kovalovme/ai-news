# Products — 2026-06-02

## GitHub Copilot Switches to Token-Based Billing <a id="copilot-token-billing"></a>

**Source:** [GitHub Blog](https://github.blog/news-insights/company-news/github-copilot-is-moving-to-usage-based-billing/) · [GitHub Docs](https://docs.github.com/en/copilot/how-tos/manage-and-track-spending/prepare-for-your-move-to-usage-based-billing) · **Type:** update · **Time (UTC):** 00:00 Jun 1

All GitHub Copilot plans transitioned from premium request units (PRUs) to GitHub AI Credits on June 1. Credits consume input, output, and cached tokens at published API rates (1 AI credit = $0.01 USD). Subscription prices are unchanged: Pro $10/month, Pro+ $39/month, Business $19/user/month, Enterprise $39/user/month — each plan's monthly spend converts directly to included credits. Code completions and Next Edit suggestions remain free and do not consume credits. Business and Enterprise customers receive a promotional included-usage buffer through August 2026; fallback models when credits run low are no longer available.

**Why it matters:** For developers running agentic workloads, reasoning models, or large-codebase refactors, the effective cost is orders of magnitude higher than the old flat rate. Cost projections from developers with heavy workflows have ranged from $29 → $750/month; see [ecosystem.md](ecosystem.md#copilot-billing-backlash) for the community reaction.

| Plan | Monthly price | Included credits | Code completions |
|------|--------------|-----------------|-----------------|
| Pro | $10 | $10 | Free |
| Pro+ | $39 | $39 | Free |
| Business | $19/user | $19/user | Free |
| Enterprise | $39/user | $39/user | Free |

---

## OpenAI GPT-5.5 and Codex GA on Amazon Bedrock <a id="openai-aws-bedrock-ga"></a>

**Source:** [AWS Blog](https://aws.amazon.com/blogs/aws/get-started-with-openai-gpt-5-5-gpt-5-4-models-and-codex-on-amazon-bedrock/) · [OpenAI Announcement](https://openai.com/index/openai-on-aws/) · **Type:** launch · **Time (UTC):** ~10:00 Jun 1

GPT-5.5, GPT-5.4, and Codex moved from limited preview to general availability on Amazon Bedrock on June 1. GPT-5.5 is available in US East (Ohio); GPT-5.4 covers US East (Ohio) and US West (Oregon). Pricing matches OpenAI first-party API rates; usage counts toward existing AWS commitments. The partnership, announced April 28, designates AWS as the exclusive third-party cloud distributor for OpenAI Frontier. Bedrock Managed Agents (combining OpenAI models with AWS orchestration) remains in limited preview.

**Why it matters:** AWS customers with existing Enterprise Discount Programs can now route OpenAI inference through their committed spend, making GPT-5.5 economically competitive with Azure OpenAI Service for teams already heavily invested in AWS infrastructure.

---

## NVIDIA RTX Spark PC Superchip Announced <a id="nvidia-rtx-spark"></a>

**Source:** [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-microsoft-windows-pcs-agents-rtx-spark) · [Tom's Hardware](https://www.tomshardware.com/pc-components/cpus/nvidia-unveils-dgx-sparrk-roadmap-for-laptops-and-desktop-pcs-at-computex-2026-three-generations-outlined-rubin-followed-by-rosa-feynman) · **Type:** release · **Time (UTC):** ~01:00 Jun 1

NVIDIA unveiled RTX Spark at Computex: a system-on-chip co-developed with MediaTek that pairs a Blackwell RTX GPU (6,144 CUDA cores, 5th-gen Tensor Cores with FP4 precision) with a 20-core Grace CPU via NVLink-C2C, with up to 128 GB of unified LPDDR5X memory. Total AI performance is 1 PFLOPS (FP4). The chip targets Windows laptops and compact desktops; OEM commitments from ASUS, Dell, HP, Lenovo, Microsoft Surface, and MSI for Fall 2026 availability.

**Why it matters:** 1 PFLOPS FP4 in a laptop form factor enables running Nemotron 3 Super-class models entirely on-device. Combined with Windows Agent Framework v1.0 and Windows Local AI Studio (see [tools.md](tools.md#project-polaris)), RTX Spark is the hardware side of Microsoft's on-device agent stack.

---

## GitHub Copilot Workspace Generally Available <a id="copilot-workspace-ga"></a>

**Source:** [Microsoft Build 2026 / ChatForest recap](https://chatforest.com/builders-log/microsoft-build-2026-recap-windows-agent-platform-project-polaris-copilot-workspace/) · **Type:** launch · **Time (UTC):** ~16:30 Jun 2

After a year in beta, GitHub Copilot Workspace is now generally available. It accepts a natural-language description of a bug or feature, generates a structured plan, modifies the relevant files, and opens a pull request — without leaving the GitHub UI. Fleet mode enables autonomous operation on narrowly scoped tasks; autopilot mode schedules background work on open issues. Day-one integrations connect to Jira, Datadog, and ServiceNow via Copilot Extensions.

**Why it matters:** GA with enterprise integrations positions Copilot Workspace as a direct competitor to Cognition's Devin and Cursor's background agent mode for teams already on GitHub. The autopilot/scheduled-operation feature is new to this release and addresses a gap versus competitors that already offer asynchronous coding loops.

---

# Ecosystem — 2026-06-02

## GitHub Copilot Billing Backlash <a id="copilot-billing-backlash"></a>

**Source:** [TechCrunch](https://techcrunch.com/2026/05/30/what-a-joke-github-copilots-new-token-based-billing-spurs-consternation-among-devs/) · [GitHub Community Discussion #192948](https://github.com/orgs/community/discussions/192948) · **Type:** controversy · **Time (UTC):** Jun 1 ongoing

The June 1 switchover of GitHub Copilot from flat-rate PRUs to token-based billing immediately generated widespread developer anger on Hacker News, Reddit, and X. The dominant sentiment, captured in the phrase "What a joke," centers on cost projection mismatches: developers sharing real-usage estimates reported jumps from $29/month to roughly $750/month for agentic and multi-file refactoring workflows, and from $50/month to approximately $3,000/month for heavier enterprise patterns. Microsoft's decision to remove the low-credits fallback model — meaning the service degrades without warning when credits are exhausted — compounds the frustration.

**Why it matters:** Copilot has the largest installed base of any AI coding tool, with tens of thousands of individual and team subscribers who built workflows on predictable flat-rate pricing. The pricing shift arrives the same week Microsoft revealed Project Polaris will replace GPT-4 in Copilot by August — suggesting significant backend cost pressure is driving both changes simultaneously.

---

## NVIDIA Vera Rubin NVL72 Enters Full Production <a id="vera-rubin-production"></a>

**Source:** [NVIDIA Computex Blog](https://blogs.nvidia.com/blog/nvidia-gtc-taipei-computex-2026-news/) · [VideoCardz](https://videocardz.com/newz/nvidia-vera-rubin-nvl72-detailed-72-gpus-36-cpus-260-tb-s-scale-up-bandwidth) · **Type:** update · **Time (UTC):** ~01:00 Jun 1

NVIDIA confirmed that Vera Rubin NVL72 — its rack-scale AI supercomputer with 36 Vera CPUs and 72 Rubin GPUs connected via NVLink Switch 6 — is now in full production across 350+ factories in 30 countries. Inference performance is 5× Blackwell at 10× lower cost per token; combined with Groq 3 LPX in-rack it reaches 35× higher throughput per watt for trillion-parameter models. The system operates at 45°C inlet temperature with 100% liquid cooling and cable-free modular design. Cloud availability begins H2 2026 on AWS, GCP, Azure, OCI, CoreWeave, Lambda, Nebius, and Nscale.

**Why it matters:** Vera Rubin production availability means the next hardware generation will be competing directly with Blackwell in cloud pricing by Q3 2026, accelerating the ongoing drop in inference cost per token. Teams pricing out large-scale agentic deployments should factor in H2 repricing from Blackwell-era spot rates.

---

## Meta AI Chatbot Enables One-Shot Instagram Account Takeovers <a id="meta-ai-account-takeover"></a>

**Source:** [Simon Willison's blog](https://simonwillison.net/) · **Type:** security incident · **Time (UTC):** Jun 1

Hackers exploited Meta's AI-powered support chatbot to take over high-profile Instagram accounts. The vulnerability was architectural rather than a classic prompt injection: Meta wired the support chatbot into account recovery flows with write access, allowing attackers who could interact with the bot to trigger account ownership transfers in a single exchange. Willison characterized the incident as illustrating that "the real problem was enabling one-shot account takeovers through the bot's design" — distinguishing it from the standard prompt-injection threat model.

**Why it matters:** The pattern — an AI agent with excessive lateral access enabling one-shot privilege escalation — is distinct from both traditional account compromise and standard prompt injection attacks. As more customer-facing AI agents are wired into authenticated backend systems, the attack surface grows proportionally with the agent's granted permissions rather than with its prompt-handling surface.

---

## Microsoft Project Polaris to Cut OpenAI Dependency in Copilot <a id="polaris-openai-dependency"></a>

**Source:** [ChatForest Build 2026 Recap](https://chatforest.com/builders-log/microsoft-build-2026-recap-windows-agent-platform-project-polaris-copilot-workspace/) · [Seeking Alpha](https://seekingalpha.com/news/4598018-microsoft-plans-to-showcase-new-coding-model-at-next-weeks-build-conference-report) · **Type:** strategy · **Time (UTC):** ~16:30 Jun 2

Microsoft's Build keynote confirmed that Project Polaris — a homegrown mixture-of-experts coding model running on Azure's Maia AI accelerators — will replace GPT-4 Turbo as the default backbone of GitHub Copilot in August 2026. Polaris was trained internally and adopts language-specific expert modules to improve precision on polyglot codebases. The Pro tier will offer 100,000-line multi-file context and autonomous test generation. No third-party API dependency is involved.

**Why it matters:** GitHub Copilot is Microsoft's largest-volume consumer of OpenAI inference. Moving Copilot's default model in-house by August removes a significant external dependency from a product serving millions of developers, and aligns with Amazon's $50B investment in OpenAI — suggesting both hyperscalers are simultaneously deepening and hedging that partnership.

---

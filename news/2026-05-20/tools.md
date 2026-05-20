# Tools — 2026-05-20

## Google Antigravity 2.0 <a id="antigravity-20"></a>

**Source:** [MarkTechPost](https://www.marktechpost.com/2026/05/19/google-launches-antigravity-2-0-at-i-o-2026-a-standalone-agent-first-platform-with-cli-sdk-managed-execution-and-enterprise-support/) · **Type:** release · **Time (UTC):** 17:00

Google launched Antigravity 2.0 at I/O 2026, transforming the previous in-product experiment into a standalone, production-grade multi-agent development platform. The release ships four components simultaneously:

- **Desktop app** — a new standalone application for orchestrating multiple agents in parallel, with dynamic subagents for parallelized workflows, scheduled background tasks, and integrations across Google AI Studio, Android Studio, and Firebase.
- **CLI** — a lightweight terminal interface for creating and controlling agents without a GUI.
- **SDK** — programmatic access to the same agent harness powering Google's consumer products; supports custom agent behaviors and self-hosted deployment.
- **Gemini Enterprise Agent Platform** — managed execution with sandbox environments provisioned through the Gemini API; targets enterprise deployments.

All components are powered by Gemini 3.5 Flash by default. Native voice command support is included. Co-development between the Antigravity team and the Gemini 3.5 Flash training team (the model was co-developed using the platform) creates tight feedback loops between infrastructure and model capability.

**Why it matters:** Antigravity 2.0 is Google's answer to Claude Code and Cursor at the agentic framework layer. The simultaneous CLI + SDK + enterprise release is the first time Google has a cohesive developer surface for production multi-agent work, directly competitive with Anthropic's Managed Agents and OpenAI's Codex on-prem deployment.

---

## Grok Skills <a id="grok-skills"></a>

**Source:** [xAI](https://x.ai/news/grok-skills) · **Type:** release · **Time (UTC):** —

xAI launched Grok Skills simultaneously on web, iOS, and Android on May 20. Skills give Grok persistent memory for custom workflows: users teach Grok a task — formatting rules, domain-specific preferences, workflow sequences — and those instructions persist across all future conversations without re-prompting. Every Grok account ships with a default set of built-in skills from xAI; users can override any skill with a custom version, which always takes priority. Skills are stored per-account and visible and editable from a new Skills panel in the Grok interface.

**Why it matters:** Persistent skills make Grok more competitive with ChatGPT's memory system and Claude's custom instructions. For developers building Grok-backed automation, this is a lightweight alternative to maintaining system prompts externally.

---

## Forge — Agentic Guardrails for Local LLMs <a id="forge"></a>

**Source:** [GitHub](https://github.com/antoinezambelli/forge) · **Type:** release · **Time (UTC):** — (HN: 455 pts)

Forge is an open-source Python framework that improves the reliability of tool-calling in locally-run language models (8B+ parameters on accessible hardware). It operates as three composable components: a **WorkflowRunner** that manages the full agent loop including context compaction and safeguards; **Guardrails middleware** that can slot into custom orchestration; and an **OpenAI-compatible proxy server** that applies guardrails transparently to any connected client. Three core reliability mechanisms — rescue parsing for malformed tool responses, retry nudges that steer models toward correct behavior, and step enforcement that ensures required workflow steps complete in order — collectively move Ministral-3 8B Q8 from baseline performance to 86.5% across a 26-scenario eval suite (76% on the hardest tier).

**Why it matters:** Most open-source agentic reliability work targets cloud-hosted frontier models. Forge addresses the underserved segment of engineers running local models for privacy, cost, or latency reasons — the frameworks that work well for GPT-4-class models often fail unpredictably at 8B scale, and Forge's structural guardrails close that gap.

---

## Gemini 3.5 Flash in GitHub Copilot <a id="gemini-copilot"></a>

**Source:** [GitHub Changelog](https://github.blog/changelog/2026-05-19-gemini-3-5-flash-is-generally-available-for-github-copilot/) · **Type:** release · **Time (UTC):** —

GitHub released Gemini 3.5 Flash as a generally available model option in GitHub Copilot on May 19, available to Copilot Pro, Pro+, Business, and Enterprise subscribers. The model is accessible in VS Code (v1.115.0+), Visual Studio (v17.14.22 / 18.1.0+), JetBrains, Xcode, and Eclipse. Enterprise and Business admins must enable it explicitly via Copilot settings. GitHub describes it as delivering "near-Pro coding quality at Flash-tier speed and cost" with strong tool use and efficient caching, suited to fast agentic coding loops. A 14× premium multiplier is listed as tentative.

**Why it matters:** Adding Gemini 3.5 Flash to Copilot expands the GitHub model roster across the full enterprise subscriber base — millions of developers — and gives Google a direct distribution channel for its new model inside the most-used IDE toolchain, competing with Claude 3.5 Sonnet and GPT-4o-mini already available in Copilot.

---

# Tools — 2026-07-23

## Anthropic Claude Security Plugin for Claude Code (Beta) <a id="claude-security-plugin"></a>

**Source:** [Anthropic / claude.com/product/claude-security](https://claude.com/product/claude-security) · [MarkTechPost](https://www.marktechpost.com/2026/07/22/anthropic-releases-claude-security-plugin-for-claude-code-in-beta-a-multi-agent-vulnerability-scanner-that-runs-in-your-terminal/) · **Type:** release · **Time (UTC):** 2026-07-22

Anthropic shipped Claude Security, a public-beta Claude Code plugin that runs a multi-agent vulnerability scan of a repository from inside an existing terminal session. The scan spans multiple files to identify complex issues that pattern-matching tools miss — including memory corruption, injection flaws, authentication bypasses, and logic errors — and converts selected findings into reviewed, apply-able patch files. The plugin is available to all Claude Code users with no separate signup.

**Why it matters:** By integrating security review into the same tool used for code generation, Anthropic narrows the gap between writing and auditing code. The multi-file analysis model catches cross-file data flows that single-file SAST tools routinely miss.

---

## OpenAI Presence — Enterprise Voice and Chat Agent Platform <a id="openai-presence"></a>

**Source:** [SiliconANGLE](https://siliconangle.com/2026/07/22/openai-introduces-presence-help-enterprises-build-ai-agents/) · [VentureBeat](https://venturebeat.com/orchestration/openai-unveils-presence-a-new-platform-that-lets-enterprises-launch-and-manage-realtime-voice-agents-and-chatbots) · **Type:** launch · **Time (UTC):** 2026-07-22

OpenAI launched Presence into limited general availability: a managed platform for building, governing, and continuously improving production-grade AI voice and chat agents. Each Presence deployment is scoped to a narrow job, given only the data and system access needed for that task, and bounded by company-defined guardrails and escalation rules. A built-in simulation tool synthesises rare edge cases for testing; Codex monitors live telemetry and generates improvement suggestions post-launch. OpenAI itself uses Presence for its English-language phone support line, resolving 75% of inbound requests without human escalation.

**Why it matters:** Presence marks a strategic shift for OpenAI from raw API access toward a fully managed agentic product stack aimed at enterprise customer-support and internal-workflow use cases — competing directly with Salesforce Agentforce and Anthropic's operator API stack.

---

## Microsoft Agent Framework 1.12.0 <a id="ms-agent-framework-1-12"></a>

**Source:** [GitHub Releases — microsoft/agent-framework](https://github.com/microsoft/agent-framework/releases) · **Type:** update · **Time (UTC):** 2026-07-22

Version 1.12.0 of Microsoft's open-source agent-orchestration library ships Azure Cosmos DB semantic memory (vector + full-text in one store), expanded hosting helpers for MCP, A2A, Telegram, and the Responses endpoint, plus stability improvements and graduated-to-stable packages. The release continues the framework's push toward production-ready multi-protocol agents.

**Why it matters:** Native Cosmos DB memory gives .NET agent developers a single managed-cloud store for episodic and semantic retrieval without standing up a separate vector database; MCP and A2A hosting helpers reduce integration boilerplate for multi-agent pipelines.

---

## Google Threat Intelligence — Agentic AI Capabilities GA <a id="google-threat-intelligence-ga"></a>

**Source:** [Pulse2](https://pulse2.com/google-threat-intelligence-makes-agentic-ai-capabilities-generally-available/) · **Type:** update · **Time (UTC):** 2026-07-20

Google moved its Threat Intelligence agentic AI capabilities from public preview to general availability for Enterprise and Enterprise+ customers. Analysts can now issue natural-language queries to generate threat reports, search for indicators of compromise, and investigate suspicious files, domains, and vulnerabilities. A dedicated Malware Analysis Agent automatically activates when deeper inspection is needed, sandboxing suspicious files to extract command-and-control infrastructure details and encryption keys. A Prompt Library packages pre-built investigative workflows for repeatable tasks such as tracing malware evolution across actor groups.

**Why it matters:** Bringing multi-step threat hunting under an LLM-driven interface reduces the analyst time needed for routine triage — particularly relevant as the OpenAI/Hugging Face breach (covered July 22) underscores that AI-driven attacks are outpacing traditional detection tooling.

---

# Products — 2026-06-06

## OpenAI Lockdown Mode rolls out to all personal ChatGPT accounts <a id="openai-lockdown-mode"></a>

**Source:** [OpenAI Help Center](https://help.openai.com/en/articles/20001061-lockdown-mode) · [Engadget](https://www.engadget.com/2188537/openai-rolls-out-a-lockdown-mode-for-extra-protection-against-prompt-injection-attacks/) · **Type:** release · **Time (UTC):** ~Jun 5

OpenAI is rolling out Lockdown Mode — first announced in February 2026 — broadly to all personal accounts (Free, Go, Plus, Pro) and self-serve ChatGPT Business. When enabled, the setting restricts all network-enabled capabilities to prevent data exfiltration via prompt injection: live web browsing is replaced with cached content only, Deep Research and Agent Mode are disabled entirely, and file downloads are blocked. Image generation and file uploads remain available. The setting is opt-in and accessible under Settings → Safety and Security.

**Why it matters:** Lockdown Mode represents OpenAI's first opt-in protocol-level defense against the "lethal trifecta" attack pattern (prompt injection + tool access + outbound data channel). The tradeoff — losing most agentic capabilities — makes it suited for users handling sensitive data, not daily productivity use. Its architecture (restricting outbound requests rather than filtering injections) mirrors the debate in MCP security about perimeter controls versus injection detection.

---

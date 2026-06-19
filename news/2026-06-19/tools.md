# Tools — 2026-06-19

## Gemini CLI reaches hard end-of-life; Antigravity CLI is its replacement <a id="gemini-cli-sunset"></a>

**Source:** [Google Developers Blog](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/) · [The Register](https://www.theregister.com/ai-ml/2026/05/20/bye-bye-gemini-cli-google-nudges-devs-toward-antigravity/5243605) · **Type:** deprecation/release · **Time (UTC):** Jun 18 00:00

Gemini CLI and Gemini Code Assist IDE extensions stopped serving requests for all consumer tiers (Google AI Pro and Ultra) at midnight UTC on June 18. Enterprise customers with a Code Assist Standard or Enterprise license are unaffected. The replacement is Antigravity CLI — a closed-source Go binary called `agy`, part of Google's Antigravity agent-first developer platform launched at Google I/O on May 19, 2026. Google explicitly warned there is no 1:1 feature parity at launch. Unlike Gemini CLI, `agy` is multi-model by design: it routes to Gemini models, Anthropic's Claude lineup, and an open-source OpenAI variant (GPT-OSS-120B).

**Why it matters:** Automation pipelines and CI workflows that call Gemini CLI or rely on Gemini Code Assist IDE extensions for consumer plans are broken as of June 18. The migration is forced with no grace period for non-enterprise users.

```flowchart
graph LR
    A[Gemini CLI consumer] -- hard stop Jun 18 --> X((retired))
    B[Gemini Code Assist consumer] -- hard stop Jun 18 --> X
    C[Code Assist Standard/Enterprise] -- unchanged --> D[Gemini CLI still works]
    X --> E[Antigravity CLI - agy binary]
    E --> F{Model router}
    F --> G[Gemini models]
    F --> H[Claude models]
    F --> I[GPT-OSS-120B]
```

---

## Claude Code update: language-aware titles, Bedrock caching, safe mode <a id="claude-code-june18"></a>

**Source:** [Releasebot / Anthropic](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** Jun 18 ~10:00

The June 18 Claude Code build ships four noteworthy changes: (1) **Language-aware session titles** — generated in the language of the conversation rather than always in English; (2) **Bedrock credential caching** — credentials from `awsCredentialExport` are now cached until their actual `Expiration` field rather than a hard-coded 1-hour timeout; (3) **Safe mode** — `--safe-mode` flag (or `CLAUDE_CODE_SAFE_MODE` env var) launches Claude Code with all customizations disabled, useful for debugging hooks or managed-settings conflicts; (4) **Model allowlist enforcement** — `ANTHROPIC_DEFAULT_*_MODEL` environment variables can no longer redirect an alias pick to a model blocked by the allowlist, and `/fast` refuses to toggle when it would select a blocked model. Several shell, hook, and terminal bugs were also fixed.

**Why it matters:** The Bedrock caching fix resolves a papercut for teams running on short-lived AWS credentials. Safe mode gives operators a first-class escape hatch when custom hooks misbehave.

---

## 15 malicious JetBrains Marketplace plugins caught stealing AI API keys <a id="jetbrains-malicious-plugins"></a>

**Source:** [Bleeping Computer](https://www.bleepingcomputer.com/news/security/malicious-jetbrains-marketplace-plugins-steal-ai-api-keys-from-developers/) · [JetBrains Blog](https://blog.jetbrains.com/platform/2026/06/marketplace-ecosystem-security-update-malicious-ai-plugins/) · [Aikido Security](https://www.aikido.dev/blog/multiple-jetbrains-ide-plugins-caught-stealing-ai-keys) · **Type:** security disclosure · **Time (UTC):** Jun 16 (disclosed); Jun 18 (remediated)

Aikido Security reported a coordinated supply chain campaign across JetBrains Marketplace on June 16: at least 15 plugins published under seven vendor accounts shared hidden exfiltration logic that sent any AI provider API key (DeepSeek, OpenAI, Anthropic) to a hardcoded attacker server the moment a user pressed "Apply" in the plugin settings UI. The plugins functioned as advertised — offering code review, chat, and commit-message generation — while secretly exfiltrating credentials. The two most-downloaded variants were DeepSeek AI Assist (27,727 installs) and CodeGPT AI Assistant (25,571 installs). Combined installs across all 15 reached approximately 70,000. The campaign ran from October 2025; new plugins continued appearing as late as June 10, 2026. JetBrains removed all 15 plugins and permanently terminated the seven associated publisher accounts by June 18.

**Why it matters:** Any developer who installed one of these plugins and entered an AI API key is likely compromised. Immediate key rotation across DeepSeek, OpenAI, and Anthropic is recommended for affected users. This is the second large-scale malicious IDE-plugin wave in six months (VS Code extensions in January stole source code from 1.5M installs).

---

# Models — 2026-06-03

## MAI-Code-1-Flash rolls out to all GitHub Copilot plans <a id="mai-code-1-flash"></a>

**Source:** [microsoft.ai](https://microsoft.ai/news/introducingmai-code-1-flash/) · **Type:** release · **Time (UTC):** Jun 2, ~09:00

Microsoft's MAI-Code-1-Flash is a 137B total / 5B active MoE coding model built entirely by Microsoft using clean, licensed training data — announced at Build 2026 and now rolling into the GitHub Copilot VS Code model picker and auto picker for individual users. Adaptive thinking scales reasoning budget to task complexity: brief for simple requests, extended chain-of-thought for harder ones. The model achieves 60% fewer output tokens than comparable models at equivalent quality. On SWE-Bench Pro it scores 16 points above Claude Haiku 4.5 across all four core coding benchmarks tested. Beyond Copilot, MAI-Code-1-Flash is available via Fireworks AI, Baseten, and OpenRouter.

**Why it matters:** MAI-Code-1-Flash is both a direct cost-reduction measure for Copilot's new token-based billing era and evidence that Microsoft's in-house model team can now produce a credible production coding model; developers on any Copilot plan get a cheaper, faster default without changing their workflow.

| Attribute | Value |
|-----------|-------|
| Total params | 137B |
| Active params (MoE) | 5B |
| SWE-Bench Pro vs Claude Haiku 4.5 | +16 pts |
| Token efficiency | ~60% fewer vs comparable models |
| Availability | GitHub Copilot (VS Code), Fireworks AI, Baseten, OpenRouter |
| Training data | Clean licensed sources (Microsoft-curated) |

---

## Grok Composer 2.5 <a id="grok-composer-2-5"></a>

**Source:** [xAI](https://x.ai/news) · **Type:** release · **Time (UTC):** Jun 1

xAI released Grok Composer 2.5, an agentic coding model designed for long-running tasks and complex multi-turn instruction-following within Grok Build. The model targets function calling, tool use, JSON output, and multi-step code execution. It is accessible via the xAI API and the Grok Build interface. No public parameter count, training details, or benchmark figures were released at launch.

**Why it matters:** Grok Composer 2.5 pairs directly with xAI's simultaneously released BYOMCP feature (see MCPs), giving Grok Build users a purpose-built agentic model that can connect to external tools via custom MCP servers — extending xAI's autonomous workflow offering beyond general-purpose Grok models.

---

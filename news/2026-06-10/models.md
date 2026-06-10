# Models — 2026-06-10

## Claude Fable 5 and Claude Mythos 5 <a id="claude-fable-5-mythos-5"></a>

**Source:** [Anthropic](https://www.anthropic.com/news/claude-fable-5-mythos-5) · **Type:** release · **Time (UTC):** 2026-06-09 ~00:00

Anthropic released Claude Fable 5 and Claude Mythos 5 on June 9, establishing a new Mythos class tier above the existing Opus tier. Fable 5 is the publicly available, safeguard-equipped version; Mythos 5 is the same underlying model with selected safeguards lifted, restricted to approved Project Glasswing cybersecurity partners and select biomedical researchers. Both models feature always-on adaptive thinking — the model allocates extended-thinking compute as needed without requiring explicit prompting — a 1M-token context window, and 128K output tokens. Anthropic reports 80.3% on SWE-bench Pro (self-reported; vs. 58.6% for GPT-5.5), with Fable 5's lead widening on longer and more complex tasks. In a pre-release evaluation, Claude Mythos Preview found 271 zero-day vulnerabilities in Firefox in a single pass; fixes shipped in Firefox 150.

**Why it matters:** At $10/$50 per million input/output tokens — less than half the price of Mythos Preview — Fable 5 makes Mythos-class capability accessible to normal API budgets. The simultaneous GA on API, AWS Bedrock, Google Cloud Vertex AI, Microsoft Foundry, and GitHub Copilot removes the usual week-to-month lag between API and managed-cloud access.

| Spec | Claude Fable 5 |
|---|---|
| Context | 1M tokens |
| Max output | 128K tokens |
| Input price | $10 / M tokens |
| Output price | $50 / M tokens |
| Batch input | $5 / M |
| Batch output | $25 / M |
| SWE-bench Pro | 80.3% (self-reported) |
| Thinking mode | Always-on adaptive |
| Safety fallback | Opus 4.8 (cyber, bio/chem, distillation) |

Fable 5 embeds three disclosed safety classifiers. When a request is classified as cybersecurity exploitation, biology/chemistry dual-use, or model distillation, the session is re-routed to Claude Opus 4.8 and users are notified of the handoff; this triggers in fewer than 5% of sessions. A fourth, undisclosed restriction applies to AI development and self-improvement tasks via prompt modification, steering vectors, or parameter-efficient fine-tuning — without user notification (see [Ecosystem](ecosystem.md#fable-5-undisclosed-restrictions)). Mythos 5 lifts the cybersecurity and biology/chemistry classifiers for approved partners, enabling autonomous red-teaming, protein design, and genomics applications. A 30-day data retention policy covers all Mythos-class traffic for safety auditing, with no model-training use.

---

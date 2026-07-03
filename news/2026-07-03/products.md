# Products — 2026-07-03

## Fable 5 cyber safeguards detail: 4-tier classifier and CJS jailbreak framework <a id="fable5-safeguards-cjs"></a>

**Source:** [Anthropic](https://www.anthropic.com/news/fable-safeguards-jailbreak-framework) · **Type:** update · **Time (UTC):** ~09:00

Anthropic's July 2 technical post expands on the safety infrastructure deployed with Fable 5's redeployment. The safety classifier partitions cybersecurity requests into four tiers:

| Tier | Label | Examples | Handling |
|------|-------|----------|----------|
| 1 | Prohibited | Ransomware, malware, data exfiltration, evasion | Block |
| 2 | High-risk dual-use | Pen testing, exploit dev | Route with authorization check |
| 3 | Low-risk dual-use | OSINT, vuln scanning, known-tool overlap | Permit |
| 4 | Benign | Secure coding, patching, incident response | Permit |

The post also publishes the Cyber Jailbreak Severity (CJS) framework — a five-level scoring rubric developed with Amazon, Microsoft, and Google — rating jailbreaks on capability gain (0–4), breadth (0–2), weaponization ease (0–2), and discoverability (0–2). CJS 0 = Informational; CJS 4 = Critical. The classifier intentionally incurs false positives at Tier 1/2 boundaries to maintain a safety margin.

**Why it matters:** The CJS framework is the first public, multi-vendor scoring rubric for jailbreak severity, aiming to replace ad hoc government responses with proportionate escalation. DevSecOps teams using Fable 5 should audit workflows that touch high-risk dual-use patterns (pen testing scripts, CVE research), as these may route to Opus 4.8 fallback unexpectedly.

---

## Claude Sonnet 5: tokenizer inflation affecting agent integrations <a id="sonnet5-tokenizer-friction"></a>

**Source:** Anthropic deployment reports via developer community · **Type:** update · **Time (UTC):** —

One week into the Claude Sonnet 5 rollout, teams are reporting that the new tokenizer produces 1.00–1.35× more tokens than Sonnet 4.x for the same input text. This inflates context usage and output costs in existing integrations built around prior tokenizer budgets. Anthropic confirmed the tokenizer change. No API-level mitigation (e.g., a compatibility mode) has been announced.

**Why it matters:** Agent loops with tight context windows or per-request cost budgets may behave unexpectedly after upgrading. Teams migrating from Sonnet 4.x should recalibrate token budgets and re-test truncation/summarization triggers before promoting to production.

---

# Research — 2026-06-19

## LLM "personality profiles" are 81–90% measurement artifact, not model traits <a id="llm-personality-artifact"></a>

**Source:** [arxiv 2606.20205](https://arxiv.org/abs/2606.20205) · **Type:** paper · **Time (UTC):** Jun 19 (submitted)

Researchers analyzed 56 instruction-tuned models using standard psychometric assessments (Big Five, MBTI-style inventories) and found that 81–90% of behavioral variation across models is explained by directional response bias — a tendency to favor one end of a rating scale regardless of item content. In human respondents, such bias explains only 9–16% of variance. Critically, apparent personality profiles shift substantially depending on which specific items are included in an assessment battery, indicating these are not stable model properties but artifacts of instruments designed for human self-report. The paper argues that "apparent psychological profiles of LLMs are largely a measurement artifact."

**Why it matters:** Benchmarks and evaluations that use personality questionnaires to compare model "alignment" or "character" are likely measuring prompt-response formatting tendencies rather than genuine behavioral dispositions. The finding has direct implications for alignment research that uses psychometric scaffolding as ground truth.

---

## LedgerAgent: structured ledger state prevents policy violations in tool-calling agents <a id="ledgeragent"></a>

**Source:** [arxiv 2606.20529](https://arxiv.org/abs/2606.20529) · **Type:** paper · **Time (UTC):** Jun 19 (submitted)

LedgerAgent proposes adding a structured, append-only state ledger to tool-calling agent loops. Instead of letting the model reason freely about which tools to call, each step is validated against an explicit organizational policy encoded as constraints over ledger entries. The approach is designed to make agents auditable and policy-adherent in enterprise environments where tool calls have real-world side effects (database writes, API calls, financial transactions).

**Why it matters:** Production deployments of agentic systems face exactly this problem: reasoning models violate operational policies intermittently and in hard-to-detect ways. A lightweight structured-state layer orthogonal to the underlying model is a practical direction that does not require retraining.

---

# Products — 2026-06-16

## Claude Sonnet 4 and Opus 4 APIs retired <a id="claude-4-deprecation"></a>

**Source:** [Anthropic model deprecations](https://platform.claude.com/docs/en/about-claude/model-deprecations) · **Type:** deprecation · **Time (UTC):** June 15, 16:00

Anthropic retired `claude-sonnet-4-0` and `claude-opus-4-0` API endpoint identifiers at 09:00 PT on June 15. API calls to either pinned model ID now return errors with no grace period. Consumer Claude.ai accounts and Claude Code managed environments are unaffected — Anthropic handles model selection there automatically. The migration path is a one-line model string change; recommended targets are `claude-sonnet-4-5` or, for code-heavy workloads, `claude-opus-4-7`. Developers who had already migrated to `claude-opus-4-7` or higher encounter no breakage.

**Why it matters:** Any production pipeline that pinned to the exact version string `claude-sonnet-4-0` or `claude-opus-4-0` — rather than the floating alias — is broken as of this morning. This is the first time Anthropic has hard-retired a Claude 4-family model, signalling that the Claude 4.5+ generation is now the stable production baseline.

---

## OpenAI proposes international youth AI safety institute at G7 <a id="openai-youth-safety-g7"></a>

**Source:** [OpenAI](https://openai.com/index/advancing-youth-safety-and-opportunity-through-global-leadership/) · **Type:** policy proposal · **Time (UTC):** June 15

OpenAI published a nine-principle framework for youth AI safety timed to the G7 Évian summit and formally proposed the creation of an international youth AI safety institute — either a new body or an existing national institute granted a global mandate. The nine principles include: privacy-preserving age estimation with protective defaults when age is indeterminate; mandatory annual youth safety risk assessments before harm occurs; clear protocols for self-harm, exploitation, and CSAM; a prohibition on targeted advertising to minors; and independent audits against interoperable standards. Separately, Common Sense Media launched a Youth AI Safety Institute in May with OpenAI Foundation funding to evaluate children's AI products.

**Why it matters:** OpenAI's framework is the most operationally specific multi-stakeholder youth AI safety proposal from a frontier lab to date. The nine principles, if adopted as G7 voluntary commitments, would establish a de facto global standard for age-adaptive AI design — affecting every consumer AI product, not just those explicitly targeting children.

---

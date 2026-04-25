# Tools — 2026-04-25

## Claude Code: Claude Opus 4.7 Now Default <a id="claude-code-opus-4-7-default"></a>

**Source:** [Anthropic news](https://www.anthropic.com/news) · [Simon Willison](https://simonwillison.net/2026/Apr/24/recent-claude-code-quality-reports/) · **Type:** update · **Time (UTC):** Apr 23

As of April 23, Claude Opus 4.7 became the default model powering Claude Code. Opus 4.7 was released on April 16 with improvements across coding, agentic tasks, vision, and multi-step reasoning. The same week, Anthropic's NEC partnership will bring Claude Code access to roughly 30,000 NEC Group employees — currently the largest single announced enterprise deployment of Claude Code (see [Ecosystem → Anthropic-NEC](ecosystem.md#anthropic-nec-japan)).

**Why it matters:** Defaulting to Opus 4.7 closes a capability gap that had persisted since earlier Opus 4.x releases lagged behind frontier on coding benchmarks. Combined with the NEC deployment scale, this is a material step in Anthropic's effort to position Claude Code as the enterprise default for AI-assisted engineering.

---

## Anthropic Publishes Claude Code Infrastructure Bug Postmortem <a id="claude-code-postmortem"></a>

**Source:** [Simon Willison](https://simonwillison.net/2026/Apr/24/recent-claude-code-quality-reports/) · **Type:** update · **Time (UTC):** Apr 24

Anthropic published a postmortem on April 24 addressing two months of user reports about degraded Claude Code behavior — forgetfulness, repetition, and apparent context loss. The root cause was three separate bugs in the Claude Code harness, not in the models themselves. The most significant: a March 26 deployment intended to clear older thinking blocks in sessions idle for over an hour instead triggered the clear on every turn of every session, making Claude appear to lose context repeatedly within a single conversation.

Simon Willison, who commonly keeps Claude Code sessions open for days, noted the bug would have substantially affected his workflow.

**Why it matters:** This is a concrete example of harness-level failures in agentic systems creating user-visible quality regressions that are hard to distinguish from model degradation. Any team building autonomous agent pipelines should treat session state management — especially context eviction logic — as a first-class reliability surface, not an implementation detail.

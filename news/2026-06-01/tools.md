# Tools — 2026-06-01

## GitHub Copilot moves to usage-based billing <a id="copilot-usage-billing"></a>

**Source:** [GitHub Blog](https://github.blog/news-insights/company-news/github-copilot-is-moving-to-usage-based-billing/) · **Type:** release · **Time (UTC):** 00:00 (billing migration activated June 1)

Today GitHub replaced Copilot's premium request unit (PRU) system with GitHub AI Credits, where 1 credit equals $0.01 and consumption is calculated against published per-token API rates covering input, output, and cached tokens. Code completions and Next Edit suggestions remain flat — they do not draw from credits. What gets metered: chat interactions, agentic coding sessions, and Copilot code review. A separate change, also effective today, routes Copilot code review jobs through GitHub Actions, meaning reviews on private repositories now consume your plan's included Actions minutes at standard workflow rates.

Plan prices are unchanged; the included credit allotment matches the dollar price:

| Plan | Monthly price | Monthly AI Credits included |
|------|--------------|----------------------------|
| Copilot Pro | $10 | $10 |
| Copilot Pro+ | $39 | $39 |
| Copilot Business | $19/user | $19/user |
| Copilot Enterprise | $39/user | $39/user |

Business and Enterprise customers receive additional promotional credits through August 2026, with pooled credit management and per-user budget controls available for admins. Monthly Pro and Pro+ subscribers migrate automatically today; annual plan subscribers remain on PRU pricing until their plan renews.

GitHub's stated rationale: Copilot evolved from an editor autocomplete tool into a multi-step agentic platform, and per-request pricing no longer reflects resource consumption for long coding sessions.

**Why it matters:** Engineers running agentic workflows — multi-file edits, CI-integrated review, background agents — will now burn through credits at a rate proportional to context size and token output. Teams should audit their usage patterns now: a Pro subscription's $10 of credits can be consumed in hours by a long agentic session that uses a frontier model with large context.

---

## Anthropic Agent SDK billing split: 14 days to go <a id="anthropic-agent-sdk-billing"></a>

**Source:** [Zed Blog](https://zed.dev/blog/anthropic-subscription-changes) · [The New Stack](https://thenewstack.io/anthropic-agent-sdk-credits/) · **Type:** update · **Time (UTC):** —

With two weeks until Anthropic's June 15 billing restructuring, developer discussion on Hacker News has accelerated from analysis to active workaround-sharing. The change — announced May 14 — moves all programmatic Claude usage out of subscription rate-limit pools and into a separately billed "Agent SDK Credit" pool at full API list prices. Affected surfaces include the Agent SDK, `claude -p`, Claude Code GitHub Actions, and all third-party agent integrations (Zed, OpenClaw, Conductor, Jean, and others). Interactive Claude Code terminal sessions and claude.ai chat are not affected and continue drawing from normal subscription limits.

Credit allotments by plan: $20 (Pro), $100 (Max 5x), $200 (Max 20x). Credits do not roll over.

Community calculations show the effective cost increase for heavy agentic use ranges from 12× to 175× compared to the previous subscription rate. A CI pipeline running Claude on every pull request in a moderately active repository can exhaust the $20 Pro allotment in days rather than weeks. A ~50-line Python wrapper that wraps `claude -p` behavior via an interactive terminal session — sidestepping the SDK billing boundary — is circulating as a stopgap.

**Why it matters:** This ends the period when a $20 Pro subscription subsidized agent workflows at roughly 15–30× below API list pricing. Teams using Claude in CI, background automation, or third-party agents need to either budget for API-rate costs or migrate to interactive-only workflows before June 15.

---

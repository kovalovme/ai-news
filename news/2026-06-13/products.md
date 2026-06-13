# Products — 2026-06-13

## Claude Agent SDK credit pool splits from subscription on June 15 <a id="claude-agent-sdk-billing-split"></a>

**Source:** [Anthropic Help Center](https://support.claude.com/en/articles/15036540-use-the-claude-agent-sdk-with-your-claude-plan) · [TechTimes](https://www.techtimes.com/articles/317625/20260602/anthropic-ends-subscription-subsidy-agents-june-15-credit-pool-replaces-flat-rate-access.htm) · **Type:** pricing change · **Time (UTC):** — (effective Jun 15)

Starting June 15, Claude Agent SDK requests and `claude -p` non-interactive runs no longer share the same pool as interactive chat on subscription plans. Each plan gains a separate monthly agent credit charged at standard API list rates:

| Plan | Monthly agent credit |
|------|--------------------:|
| Pro ($20/mo) | $20 |
| Max 5× ($100/mo) | $100 |
| Max 20× ($200/mo) | $200 |
| Standard Enterprise | $0 |

When the credit is exhausted, automated agent requests stop entirely unless the user has manually enabled overflow billing. There is no automatic fallback and no credit rollover. Interactive Claude Code in the terminal, Claude.ai chat, and Claude Cowork are unaffected by the change.

**Why it matters:** Developers who have been running Agent SDK workloads under a subscription without tracking usage face a hard stop on June 15 if their month-to-date agent spend exceeds the credit cap. The change effectively ends the implicit subsidy that made Agent SDK access flat-rate; heavier users will pay standard API prices for the overage. Teams on Standard Enterprise need to negotiate agent access separately.

---

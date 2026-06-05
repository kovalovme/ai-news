# Products — 2026-06-05

## Anthropic Agent SDK Billing Split (Effective June 15) <a id="anthropic-billing-split"></a>

**Source:** [The Decoder](https://the-decoder.com/claude-subscriptions-get-separate-budgets-for-programmatic-use-billed-at-full-api-prices/) · [DevToolPicks](https://devtoolpicks.com/blog/anthropic-splits-claude-subscriptions-agent-sdk-credit-june-2026) · **Type:** launch · **Time (UTC):** announced ~Jun 3, effective Jun 15

Starting June 15, Anthropic separates Claude subscriptions into two distinct usage pools. The existing interactive pool covers Claude.ai web/desktop/mobile chat and terminal-based Claude Code; a new **programmatic credit pool** covers Agent SDK calls, `claude -p`, Claude Code GitHub Actions, and third-party agent integrations (OpenClaw, Conductor, Zed, Jean). Programmatic credits are billed at standard API rates, expire monthly without rollover, and scale with subscription tier: Pro ($20/month) receives $20 in credits, Max 5× ($100/month) receives $100, Max 20× ($200/month) receives $200. Subscribers expecting an Anthropic email on June 8 will need to claim credits to activate the new pool. When the pool depletes, requests either halt (if extra usage is disabled) or are billed directly at API rates.

**Why it matters:** For developer-subscribers running agentic pipelines, this converts what was essentially unlimited (flat-rate) API access via subscription into metered billing at API prices — the same shift GitHub Copilot made with token-based billing in June 2026, now applied to the Anthropic SDK layer.

| Plan | Monthly cost | Programmatic credit |
|---|---|---|
| Pro | $20 | $20 |
| Max 5× | $100 | $100 |
| Max 20× | $200 | $200 |

---

## xAI Grok Imagine Video 1.5 Preview API <a id="grok-imagine-1-5-api"></a>

**Source:** [Releasebot / xAI](https://releasebot.io/updates/xai) · **Type:** launch · **Time (UTC):** Jun 3, ~16:00

xAI opened Grok Imagine Video 1.5 to API access as a preview model (`grok-imagine-video-1.5-preview`). The model converts still images into cinematic video clips using natural-language motion prompts, outputs at 720p resolution in clips from 6 to 15 seconds with native synchronized audio, and preserves source image lighting and appearance. At launch, Imagine 1.5 debuted at the top of the Artificial Analysis Image-to-Video Arena leaderboard with an Elo rating of 1404 — 52 points above version 1.0 and ahead of Seedance 2.0 and Google Veo at that date.

**Why it matters:** Native audio generation and 15-second clip lengths position this as a competitive alternative to Veo and Kling for short-form video production workflows; making it available via API rather than only consumer products opens it to programmatic integration immediately.

---

# Products — 2026-07-13

## Anthropic extends Fable 5 subscription access to July 19 <a id="fable-5-july-19-extension"></a>

**Source:** [BleepingComputer](https://www.bleepingcomputer.com/news/artificial-intelligence/claude-fable-5-stays-free-for-paid-users-until-july-19-as-anthropic-buys-more-time/) · [simonwillison.net](https://simonwillison.net) · **Type:** update · **Time (UTC):** Jul 13

Anthropic announced today — hours after the July 12 deadline passed — a second extension of Fable 5 subscription inclusion for Pro, Max, Team, and premium Enterprise seats through July 19, 23:59:59 PT. The 50% Claude Code weekly usage limit bonus also continues. Anthropic's stated reason is compute constraints and needing more time to gauge demand; no timeline has been given for when Fable 5 will return to standard subscription access permanently. After July 19, users will move to a credits-billing arrangement (not standard subscription) as a temporary bridge.

This is the second extension: the original July 7 cutoff was pushed to July 12, and that has now been pushed again. Simon Willison noted that OpenAI appears more confident about GPT-5.6 Sol availability than Anthropic is about Fable 5, and suggested the supply uncertainty is a competitive liability.

**Why it matters:** The repeated short-window extensions create friction for users who planned around the original billing timeline. The credits-bridge arrangement post-July 19 is a pricing tier change, not a continuation of the subscription deal, which may affect high-volume users' cost models.

---

## DeepSeek V4 API migration: July 24 deadline is firm <a id="deepseek-v4-migration-deadline"></a>

**Source:** [dev.to/agdex_ai](https://dev.to/agdex_ai/deepseek-v4-api-migration-guide-everything-before-the-july-24-2026-deadline-4m30) · [WaveSpeed Blog](https://wavespeed.ai/blog/posts/blog-deepseek-v4-model-name-migration/) · **Type:** migration deadline · **Time (UTC):** —

Every application calling `deepseek-chat` or `deepseek-reasoner` on DeepSeek's hosted API will receive errors after July 24, 15:59 UTC. The fix is a one-line parameter change to `deepseek-v4-pro` or `deepseek-v4-flash`, but the mapping is non-obvious: `deepseek-reasoner` maps to V4-Flash (not V4-Pro), which is a capability downgrade for teams relying on heavy reasoning workloads. Full regression testing plus staged rollout typically takes 5–8 weeks; organizations that haven't started are behind. DeepSeek has confirmed no extension is being discussed.

V4-Pro's permanent list price is $0.87/M output tokens — approximately 3% of GPT-5.6 Sol ($30) and 2% of Fable 5 ($50) — making migration worthwhile even for teams that must update multiple integration points.

**Why it matters:** Any production system calling the old model IDs breaks hard on July 24. The `deepseek-reasoner → deepseek-v4-flash` (not V4-Pro) mapping is a silent capability downgrade that teams relying on reasoning-heavy tasks should test explicitly before the deadline.

---

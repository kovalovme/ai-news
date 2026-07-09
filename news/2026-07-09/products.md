# Products — 2026-07-09

## Fable 5 Subscription Inclusion Ends — Metered Billing Active <a id="fable-5-metered-billing"></a>

**Source:** [Android Authority](https://www.androidauthority.com/anthropic-claude-fable-5-credits-usage-july-3684840/) · [TechTimes](https://www.techtimes.com/articles/319864/20260707/claude-fable-5-drops-subscriptions-tonight-enable-credits-lose-access.htm) · **Type:** update · **Time (UTC):** July 8

As of July 8, Fable 5 no longer draws from subscription usage limits on Pro, Max, Team, or Enterprise plans. Access now requires enabling Usage Credits in Settings → Usage on claude.ai and billing directly against those credits at $10 / 1M input tokens and $50 / 1M output tokens — the highest per-token price Anthropic has listed for a generally available model, and double the rate for Claude Opus 4.8. If Usage Credits are not enabled, Fable 5 access stops when the free allowance (included through July 7) runs out. There is no automatic fallback to a cheaper model.

**Why it matters:** Operators and heavy users who relied on Fable 5 within subscription limits need a budget decision now: enable credits with a cap, or route tasks to Opus 4.8 / Sonnet 5. The lack of automatic fallback is the sharp edge — silent task failures are possible if credits are not pre-funded.

---

## Anthropic Identity Verification Policy Takes Effect <a id="anthropic-id-verification"></a>

**Source:** [TechCrunch](https://techcrunch.com/2026/06/22/anthropic-says-claude-may-want-to-see-your-id/) · [CyberNews](https://cybernews.com/ai-news/anthropic-privacy-policy-id-verification/) · **Type:** update · **Time (UTC):** July 8

Anthropic's updated privacy policy, effective July 8, authorises the company to request government-issued photo ID, a live selfie, and a facial geometry scan from consumer Claude users (Free, Pro, and Max plans) before granting or maintaining access to specific capabilities. Data is collected and stored by Persona Identities (Anthropic's verification partner); Anthropic acts as data controller. Business plans (Team, Enterprise, API) are exempt. The policy does not specify which capabilities trigger a check, what the retention period is, or what happens if a user refuses beyond "account access may be affected."

**Why it matters:** This is the first major US frontier AI lab to codify biometric collection in its consumer privacy policy. Anthropic's rationale is enforcement of export controls and capability access gates — the policy was announced alongside the return of Fable 5 after the June export restrictions. Engineers on consumer plans (not API) should be aware of this policy boundary.

---

## Gemini 3.5 Pro Delayed to July 17 — Full Architectural Rebuild <a id="gemini-35-pro-delay"></a>

**Source:** [BigGo Finance](https://finance.biggo.com/news/6f0c6bb2-795f-4c57-9d09-6db691d7638a) · [HackerNoon](https://hackernoon.com/google-delays-gemini-35-pro-to-july-17-the-strategic-play-behind-the-scrapped-base-model) · **Type:** update · **Time (UTC):** July 8 (announcement)

Google DeepMind confirmed that Gemini 3.5 Pro will not ship in its planned June window. The reason is a full pre-training restart: the 2.5 Pro base model was scrapped due to performance ceilings in multi-step mathematical reasoning and SVG scene generation flagged by enterprise testers. The rebuilt model targets a July 17 launch date. Reported features of the rebuilt architecture include a 2-million-token context window, a "Deep Think Reasoning Layer" for complex problems, and improved image quality.

**Why it matters:** A complete pre-training restart is an expensive signal about how competitive pressure (GPT-5.6 and Fable 5 both shipping) is forcing labs to clear a higher bar before release rather than iterate publicly. July 17 is a widely cited date but has not been officially confirmed by Google.

---

# Products — 2026-07-08

## Fable 5: Persona identity gate activates; billing deadline extended to July 12 <a id="fable-5-persona-gate"></a>

**Source:** [ChatForest builder guide](https://chatforest.com/builders-log/anthropic-fable-5-july-7-credits-july-8-persona-gate-builder-action-guide/) · [Billing extension — iwoszapar](https://www.iwoszapar.com/p/fable-5-included-access-extended-july-12) · [Explainx.ai](https://www.explainx.ai/blog/anthropic-claude-id-verification-persona-fable-5-2026) · **Type:** update · **Time (UTC):** — (July 8)

Two Fable 5 policy changes took effect today. First, Anthropic activated a biometric identity-verification gate via Persona for consumer-plan Claude.ai and mobile-app users: the process requires a government-issued photo ID and a live selfie, yielding facial geometry data that Persona retains under its own policy. Team and Enterprise accounts, and all API access, are exempt—the gate applies only to consumer-tier Claude.ai. Second, the transition from included subscription access to per-token usage credits ($10/$50 per MTok input/output) was extended to July 12, giving subscribers a 4–5 day reprieve from the originally communicated July 7–8 deadline. The billing change requires enabling usage credits in the Claude Console and setting a monthly spending cap; without credits enabled, Fable 5 access stops with no grace period after July 12.

**Why it matters:** Biometric identity verification for access to a flagship AI model is a meaningful precedent shift—it binds consumer AI access to verified real-world identity. For developers whose products route end users to Claude.ai for Fable 5 access, this introduces a hard friction point that does not exist on the API path. Applications that were relying on pass-through Claude.ai sessions need an architectural review.

---

## Google NanoBanana 2 Lite: 4-second, $0.034-per-1K image generation <a id="google-nanobanana-2-lite"></a>

**Source:** [TechCrunch](https://techcrunch.com/2026/06/30/google-introduces-a-faster-cheaper-image-generator-with-nano-banana-2-lite/) · [gHacks](https://www.ghacks.net/2026/07/02/google-launches-nano-banana-2-lite-for-low-cost-high-throughput-ai-image-generation/) · **Type:** launch · **Time (UTC):** — (released June 30, not covered in prior digests)

Google released NanoBanana 2 Lite (`gemini-3.1-flash-lite-image`) on June 30 as the fastest and cheapest entry in the Nano Banana image family. It delivers text-to-image outputs in approximately 4 seconds at $0.034 per 1,000 images on Standard pricing, or $0.0168 per 1K on Batch. Quality is reported to exceed the original NanoBanana model. The API is available in Google AI Studio and the Gemini API, with consumer rollout across AI Mode in Search, the Gemini app, NotebookLM, Google Photos, Stitch, Google Flow, and Google Ads.

**Why it matters:** At sub-$0.04 per 1K images and 4-second latency, this is the lowest-cost option from a tier-one provider for high-throughput image generation. The simultaneous rollout across Google's consumer properties means production traffic is already running on this model at scale.

| Tier | Price per 1K images |
|------|--------------------:|
| Standard | $0.034 |
| Batch | $0.017 |

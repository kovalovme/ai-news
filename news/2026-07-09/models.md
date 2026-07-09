# Models — 2026-07-09

## GPT-5.6 Sol, Terra, and Luna — General Availability <a id="gpt-56-sol-terra-luna"></a>

**Source:** [OpenAI](https://openai.com/index/previewing-gpt-5-6-sol/) · [Engadget](https://www.engadget.com/2210308/openai-rolls-out-gpt5-6-july-9/) · **Type:** release · **Time (UTC):** ~09:00 July 9

OpenAI publicly launched all three GPT-5.6 variants on July 9 after the US Department of Commerce's Center for AI Standards and Innovation completed additional safety testing, giving the administration's explicit sign-off for a wider rollout. GPT-5.6 had been in a closed preview with select partners since late June. Sol is OpenAI's most capable model to date and introduces an "Ultra" mode that spawns subagents to parallelize complex tasks. Terra is positioned as a GPT-5.5-equivalent replacement at half the cost, and Luna is the budget tier.

**Pricing (per million tokens):**

| Model | Input | Output |
|-------|------:|-------:|
| Sol   | $5.00 | $30.00 |
| Terra | $2.50 | $15.00 |
| Luna  | $1.00 |  $6.00 |

GPT-5.6 also ships with explicit cache breakpoints and a 30-minute minimum cache lifetime. Cache writes are billed at 1.25× the uncached input rate; reads retain the existing 90% discount.

**Why it matters:** Sol targeting biology, chemistry, and cybersecurity — combined with the White House review process — signals that government pre-clearance is becoming an informal norm for top-tier model releases. The Terra/Luna pricing tiers put frontier-level capability under $3 input per million tokens for the first time from OpenAI.

---

## GPT-Live-1 and GPT-Live-1 Mini <a id="gpt-live-1"></a>

**Source:** [OpenAI](https://openai.com/index/introducing-gpt-live/) · [TechCrunch](https://techcrunch.com/2026/07/08/openai-releases-new-voice-models-for-more-natural-live-conversations/) · **Type:** release · **Time (UTC):** ~10:00 July 8

OpenAI launched GPT-Live, a new generation of voice models built on a full-duplex architecture that listens and speaks simultaneously rather than waiting for the user to finish before generating a response. The previous Advanced Voice Mode combined three separate components (speech-to-text → language model → text-to-speech); GPT-Live consolidates these into a single end-to-end model. During conversation, it can emit backchannels ("mhmm," "yeah") and interrupt or be interrupted naturally. For queries requiring search, reasoning, or complex work, it delegates to GPT-5.5 behind the scenes and surfaces the result mid-conversation.

**Rollout:**
- GPT-Live-1 mini: replaces Advanced Voice Mode as default on all ChatGPT tiers
- GPT-Live-1 (larger): available to paid-tier users
- API access: sign-up waitlist; no date confirmed
- Languages: multiple; quality varies — Hindi demo showed noticeable accent artifacts

**Why it matters:** Full-duplex is the architecture change voice AI has needed to feel natural; this is the first production deployment of it at consumer scale. Engineers building voice agents should watch for API availability closely.

---

## Grok 4.5 — Public Launch <a id="grok-45"></a>

**Source:** [Axios](https://www.axios.com/2026/07/08/spacexai-grok-new-model) · [TechCrunch](https://techcrunch.com/2026/07/08/spacexai-releases-grok-4-5-which-elon-describes-as-an-opus-class-model/) · [xAI Docs](https://docs.x.ai/developers/grok-4-5) · **Type:** release · **Time (UTC):** ~12:00 July 9

xAI moved Grok 4.5 from private beta (SpaceX and Tesla internal) to public availability on July 9. Elon Musk described it on July 8 as an "Opus-class model." It is based on xAI's V9 foundation (1.5 trillion parameters) with Cursor coding data incorporated in supplemental training. The model supports configurable reasoning effort and is positioned for software engineering, agentic workflows, and knowledge work including legal and finance domains. It is not yet available in the European Union.

**Pricing:** $2.00 / 1M input · $6.00 / 1M output

**Availability:** xAI API, Cursor (all plans), Grok Build console

**Why it matters:** At $2/$6, Grok 4.5 undercuts Claude Opus 4.8 ($15/$75) and GPT-5.6 Sol ($5/$30) substantially. If benchmark parity with Opus-class models holds up under independent evaluation, this is the most significant price compression at the frontier tier since Sonnet 5 launched.

---

# Models — 2026-05-20

## Gemini 3.5 Flash <a id="gemini-35-flash"></a>

**Source:** [Google Blog](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5/) · **Type:** release · **Time (UTC):** 17:00

Google released Gemini 3.5 Flash as a generally available model at Google I/O 2026. The model is positioned as the company's new flagship for agentic and coding workloads — a Flash-tier model that outperforms the prior Pro tier on several key benchmarks while running 4× faster. Context window is 1,048,576 input tokens / 65,536 output tokens with multimodal input (text, image, audio, video). Dynamic thinking is on by default.

**Benchmarks:**

| Benchmark | Score |
|---|---|
| Terminal-Bench 2.1 | 76.2% |
| MCP Atlas | 83.6% |
| CharXiv Reasoning (multimodal) | 84.2% |
| GDPval-AA | 1,656 Elo |

**Pricing:**

| Token type | Rate |
|---|---|
| Input | $1.50 / 1M tokens |
| Cached input | $0.15 / 1M tokens |
| Output | $9.00 / 1M tokens |

**Why it matters:** At 4× the output speed of comparable frontier models and with a 1M-token context window, Gemini 3.5 Flash is the engine behind Antigravity 2.0, Gemini Spark, and the new Copilot integration (see tools.md). Simon Willison notes the significant price jump — 3× more than Gemini 3 Flash Preview — and flags that on Artificial Analysis benchmarks it costs more per run than the older Gemini 3.1 Pro Preview, making value assessment non-trivial for API customers.

**Availability:** Gemini API, Google AI Studio, Android Studio, Google Antigravity, Gemini app (global), AI Mode in Google Search, Gemini Enterprise Agent Platform. Knowledge cutoff: January 2026.

---

## Gemini Omni <a id="gemini-omni"></a>

**Source:** [Decrypt](https://decrypt.co/368393/google-unveils-gemini-omni-next-gen-ai-video-builder-simulate-world) · **Type:** release (preview) · **Time (UTC):** 17:00

DeepMind CEO Demis Hassabis announced Gemini Omni at Google I/O 2026, describing it as a unified model that generates any output from any input. The initial release focuses on video: Omni combines Gemini's reasoning with Google's media-generation stack (Veo, Nano Banana, Genie) and supports conversational editing — users can modify characters, backgrounds, and environment using voice commands. A demonstration showed generation of a claymation-style explainer on protein folding and live conversational edits to selfie video. The first product release, **Gemini Omni Flash**, is launching this summer through Google Flow and Flow Music for AI Ultra subscribers.

**Why it matters:** Omni signals Google collapsing its previously separate video and language model lines into a single conversational interface, directly competing with Sora 2 and Runway Gen-4 on coherent, editable long-form video. Integrating into YouTube Shorts Remix (available now, no extra charge) is an immediate distribution vehicle at billion-user scale.

---

# Models — 2026-07-25

## Claude Opus 5 <a id="claude-opus-5"></a>

**Source:** [Anthropic](https://www.anthropic.com/news/claude-opus-5) · **Type:** release · **Time (UTC):** ~09:00 Jul 24

Anthropic released Claude Opus 5 on July 24, completing the Claude 5 series roll-out that began in June with Mythos, Fable, and Sonnet 5. The model targets the gap between Opus 4.8 and the frontier-only Fable 5: it carries Fable 5-level intelligence on most agentic evaluations at roughly half the per-task cost, with significantly lighter safety restrictions and no 30-day conversation retention requirement (which applies to both Fable 5 and Mythos 5).

On the Artificial Analysis Intelligence Index, Opus 5 scores 61 — narrowly the highest of any model, one point above Fable 5 — and leads the AA-Briefcase agentic knowledge-work benchmark by 146 Elo points over Fable 5 (1720 vs. 1574). Safety classifiers engage approximately 85% less often than for Fable 5, making it practical for legitimate security research and vulnerability scanning that Fable 5's tighter refusals blocked.

The model ships with a five-level effort toggle (low / medium / high / xhigh / max) and a Fast Mode (2× list price, ~2.5× throughput). It is available immediately as `claude-opus-5` in the API and is the new default model on Claude Max plans.

**Why it matters:** Opus 5 effectively retires the Opus 4.8-vs.-Fable 5 trade-off that forced teams to choose between cost control and frontier capability. The 85% reduction in safety-trigger frequency is a material quality-of-life change for security, bio, and chemistry workloads that Fable 5 routinely declined.

| Benchmark | Opus 5 (max) | Fable 5 | GPT-5.6 Sol | Kimi K3 |
|---|---|---|---|---|
| AA Intelligence Index | **61** | 60 | 59 | 57 |
| AA-Briefcase Elo | **1720** | 1574 | — | — |
| CursorBench 3.2 | ≈Fable 5 (−0.5%) | ref | — | — |
| OSWorld 2.0 | **#1** (1/3 Fable cost) | — | — | — |
| ARC-AGI 3 | 3× competitors | — | — | — |
| Frontier-Bench v0.1 | **43.3%** | — | — | — |
| Cost per task (AA) | $17.79 | $22.30 | — | — |

---

## Grok STT 1.0 <a id="grok-stt-10"></a>

**Source:** [xAI](https://x.ai/news/grok-stt-and-tts-apis) · [OpenRouter](https://openrouter.ai/x-ai/grok-stt-1.0) · **Type:** release · **Time (UTC):** Jul 23–24

xAI's Grok STT 1.0 speech-to-text model became available through OpenRouter on July 23, broadening access beyond direct xAI API accounts. The model transcribes audio in 25 languages with word-level timestamps, optional speaker diarization, and multichannel audio support. Pricing is $0.10/hour for batch and $0.20/hour for streaming.

**Why it matters:** OpenRouter availability lets developers slot Grok STT into existing pipelines without a separate xAI account, adding a credible alternative to Whisper and Google STT for voice-agent and transcription workloads.

---

> **Heads up — Kimi K3 open weights (Jul 27):** Moonshot AI is scheduled to publish 2.8T-parameter Kimi K3 weights on Hugging Face on July 27 under a Modified MIT license. MXFP4 weights require ~1.4 TB and 64+ accelerators. The impending release is directly relevant to the security findings discussed in [research.md](research.md).

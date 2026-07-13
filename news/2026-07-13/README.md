# AI Digest — 2026-07-13

> Today's biggest story is a twin privacy reckoning for agentic coding tools: xAI's Grok Build CLI was documented to upload entire repositories — including `.env` secrets — to Google Cloud Storage independently of the model-improvement consent toggle, while Anthropic confirmed it ran an undisclosed steganography tracking system in Claude Code for four months (April–June) before removing it. The day's second story is a rigorous token-overhead study showing Claude Code costs 3.7× more than OpenCode at equivalent quality on identical tasks. Stepping back, the broader theme is accountability in agentic tooling: what developers' tools do with their code, their secrets, and their usage patterns is emerging as a first-order engineering concern, distinct from model capability.

## Day at a glance

```mermaid
mindmap
  root((2026-07-13))
    Models
      Gemini 3.5 Pro price leaks 15 60 per MTok July 17
      Honeycomb EAP possible Opus 5 glimpse in Cursor
    MCPs
      No notable items
    Tools
      Claude Code vs OpenCode 3.7x cost gap 33k vs 7k tokens
      Mesh LLM peer-to-peer GPU pooling via iroh
      Prime Intellect Verifiers v1 agentic RL environments
    Research
      Terry Tao coding agents domain expertise still essential
      George Hotz LLMs useful not miraculous
      Simon Willison agents must not be DRI
      ProofCouncil FirstProof math benchmark ranked first
      ARCANA WILDTRACE LongMedBench arxiv papers
    Products
      Fable 5 extended to July 19 second extension
      DeepSeek V4 migration deadline July 24 firm
    Ecosystem
      Anthropic confirms Claude Code steganography tracking system
      Grok CLI uploads full repos to Google Cloud Storage
      OpenAI Google served Chinese military via Singapore
      White House 30-day frontier model preclearance window
      HN 606pts flag AI-generated articles debate
```

## Top stories

1. **Grok Build CLI uploads full repositories — including secrets — to Google Cloud Storage** — A wire-level audit of v0.2.93 found that xAI's coding CLI transmits `.env` files verbatim and uploads entire repository snapshots (5.1 GiB for a 12 GB test repo) to a `grok-code-session-traces` GCS bucket, with behavior unchanged by the "Improve the model" opt-out. [→ details](ecosystem.md#grok-cli-full-repo-upload)
2. **Anthropic confirms Claude Code ran undisclosed steganography system for four months** — China's industry regulator flagged a covert telemetry capability in versions 2.1.91–2.1.196; Anthropic confirmed the system was "an experiment to prevent account abuse" and removed it in 2.1.198 on July 1. [→ details](ecosystem.md#claude-code-steganography)
3. **Claude Code vs OpenCode: 3.7× cost gap at matching quality** — A proxy-level study shows Claude Code consumes 33k tokens before reading user input (vs 7k for OpenCode), with a cache-prefix instability that compounds costs further; production configurations reach 75–85k tokens before any user input. [→ details](tools.md#claude-code-opencode-overhead)

## By the numbers

| Category   | Items | Highlight |
|------------|------:|-----------|
| Models     |     2 | Honeycomb EAP: probable Opus 5, 1M context, seen briefly in Cursor |
| MCPs       |     0 | — |
| Tools      |     3 | Claude Code vs OpenCode: 268k vs 72k tokens per passing benchmark run |
| Research   |     5 | Tao: agent handles implementation, human guides architecture |
| Products   |     2 | Fable 5: second access extension, now through July 19 |
| Ecosystem  |     5 | Grok CLI GCS uploads · Claude Code steganography confirmed |

## Timeline (UTC)

```mermaid
timeline
  title Releases & announcements
  Apr 02 : Claude Code steganography system begins (v2.1.91)
  Jul 01 : Steganography removed in Claude Code v2.1.198
  Jul 08 : China issues Claude Code backdoor warning
         : Anthropic engineer confirms steganography system
         : Honeycomb EAP briefly visible in Cursor
  Jul 11 : Terry Tao coding agents post published
  Jul 12 : Claude Code vs OpenCode overhead study HN 573pts
         : Grok CLI full-repo upload analysis HN 469pts
         : George Hotz I love LLMs post HN 415pts
         : Tao coding agents post surfaces on HN 433pts
         : Willison DRI agents post published
  Jul 13 : Anthropic extends Fable 5 to July 19
         : Prime Intellect Verifiers v1 released
         : HN Add flag for AI articles 606pts
  Jul 24 : DeepSeek V4 API deadline upcoming
```

## Files
- [Models](models.md)
- [MCPs](mcps.md)
- [Tools](tools.md)
- [Research](research.md)
- [Products](products.md)
- [Ecosystem](ecosystem.md)

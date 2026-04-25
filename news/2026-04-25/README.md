# AI Digest — 2026-04-25

> Three major model events defined the past 48 hours: OpenAI released GPT-5.5 on April 23 (the first fully retrained base model since GPT-4.5, with 1M-token context at $5/M input), and DeepSeek followed on April 24 with V4-Pro and V4-Flash — open-weight models matching near-frontier quality at $1.74/M input, 30× cheaper than GPT-5.5. Tencent added Hy3 Preview (295B MoE) the same day, replacing DeepSeek in its own consumer chatbot. On the business side, Cohere's acquisition of Germany's Aleph Alpha at a $20B combined valuation is the largest AI M&A deal of 2026 so far. The day's theme is dual: continued commoditization pressure from open-weight releases colliding with structural consolidation driven by European data-sovereignty concerns.

## Day at a glance

```mermaid
mindmap
  root((2026-04-25))
    Models
      DeepSeek V4 Pro and Flash
      OpenAI GPT-5.5
      Tencent Hy3 Preview
    MCPs
      ext-apps and ext-skills extensions
      SDK updates TypeScript Python Go Java
    Tools
      Claude Code Opus 4.7 default
      Claude Code bug postmortem
    Research
      DeepSeek hybrid attention paper
      TurboQuant 5x KV compression ICLR
    Products
      Tesla 25B capex Cybercab confirmed
      Pony.ai Gen-7 robotaxi lower cost
    Ecosystem
      Cohere acquires Aleph Alpha 20B
      Anthropic NEC Japan 30k engineers
      LMDeploy CVE exploited in 13h
```

## Top stories

1. **DeepSeek V4-Pro / V4-Flash** — Open-weight 1.6T-param model with 1M-token context at $1.74/M input, 90% less KV cache than V3.2, open weights on Hugging Face. [→ details](models.md#deepseek-v4)
2. **Cohere acquires Aleph Alpha at $20B** — Transatlantic merger creates a sovereign-AI challenger to US frontier labs, backed by $600M from Schwarz Group's STACKIT cloud. [→ details](ecosystem.md#cohere-aleph-alpha-merger)
3. **OpenAI GPT-5.5** — First full base retrain since GPT-4.5; 82.7% Terminal-Bench 2.0, 1M-token context, $5/$30 pricing — but 86% hallucination rate on AA-Omniscience is a concern. [→ details](models.md#gpt-5-5)

## By the numbers

| Category | Items | Highlight |
|----------|------:|-----------|
| Models | 3 | DeepSeek V4-Pro: 1.6T params, $1.74/M, open weights |
| MCPs | 2 | ext-apps UI-embedding protocol + skills discovery |
| Tools | 2 | Claude Code Opus 4.7 default; harness postmortem |
| Research | 2 | DeepSeek hybrid attention: 27% FLOPs at 1M context |
| Products | 2 | Tesla $25B capex; Pony.ai unit-economics breakeven |
| Ecosystem | 4 | Cohere-Aleph Alpha $20B; LMDeploy SSRF in 13h |

## Timeline (UTC)

```mermaid
timeline
  title Releases and announcements
  Apr 22 : Tesla Q1 2026 earnings raises capex to 25B+
  Apr 23 : OpenAI GPT-5.5 released : Anthropic NEC Japan partnership signed
  Apr 24 : DeepSeek V4 Pro and Flash preview open-sourced : Tencent Hy3 Preview deployed in Yuanbao : Cohere acquires Aleph Alpha at 20B valuation : Pony.ai Auto China Gen-7 robotaxi and L4 truck : LMDeploy CVE-2026-33626 exploited within 13h : Anthropic Claude Code postmortem published
```

## Files
- [Models](models.md)
- [MCPs](mcps.md)
- [Tools](tools.md)
- [Research](research.md)
- [Products](products.md)
- [Ecosystem](ecosystem.md)

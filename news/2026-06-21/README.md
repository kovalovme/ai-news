# AI Digest — 2026-06-21

> A quiet Sunday with no major model launches. The dominant story remains the Fable 5 export control ban (Day 9), with newly disclosed details: Amazon CEO Andy Jassy placed the late-night call to the White House that triggered the June 12 directive, and David Sacks publicly framed the restoration path as "Anthropic fixes the jailbreak, the export control is lifted" — a condition security experts call technically impossible. The Fable 5 free-trial inclusion on paid plans closes tomorrow (June 22), converting access to $10/$50 per million tokens usage credits while the model remains offline. Infrastructure story of the day: FERC issued show-cause orders to all six US grid operators to rewrite AI data center interconnection rules within 60 days, marking the clearest federal signal yet that grid capacity — not chips — is the binding AI infrastructure constraint.

## Day at a glance

```mermaid
mindmap
  root((2026-06-21))
    Models
      GLM-5.2 hallucinates 3x less than GPT-5.5 AA-Omniscience HN 524pts
    MCPs
      No items
    Tools
      Cloudflare temp accounts AI agents 60-min deploy no auth Stripe
    Research
      Reuters Institute DNR 2026 10pct adults use AI chatbots for news
    Products
      Grok 4.3 on Amazon Bedrock 1.25 per million tokens Mantle engine
      OpenAI Partner Network 150M 300K consultants Accenture BCG McKinsey
    Ecosystem
      Fable 5 Day 9 Andy Jassy triggered ban Sacks ultimatum Jun 22 pricing deadline
      Amazon drops Artificial Altman biopic conflict with 50B OpenAI deal
      FERC show-cause orders 6 grid operators AI data center interconnection 60 days
```

## Top stories

1. **Fable 5: Amazon's triggering role and Sacks ultimatum disclosed, June 22 pricing cutoff tomorrow** — Andy Jassy called the White House to flag the Fable 5 jailbreak before the ban; David Sacks publicly set the resolution condition: fix the jailbreak. The free-trial window closes tomorrow, shifting to $10/$50 per million tokens regardless of suspension status. [→ details](ecosystem.md#fable5-amazon-sacks)
2. **FERC issues show-cause orders to all six US grid operators on AI data center power** — June 19 orders give RTOs/ISOs 60 days to justify or rewrite large-load interconnection tariffs; five mandatory areas including co-location rules and flexible load services. [→ details](ecosystem.md#ferc-grid-orders)
3. **Cloudflare ships temporary accounts for AI agents** — `wrangler deploy --temporary` lets an agent spin up Workers, KV, D1, Durable Objects with no OAuth flow or MFA; 60-minute preview with claim-to-keep; Stripe partnership extends this to domain registration and billing. [→ details](tools.md#cloudflare-temp-accounts)

## By the numbers

| Category   | Items | Highlight |
|------------|------:|-----------|
| Models     |     1 | GLM-5.2: 3× lower hallucination rate vs GPT-5.5 (AA-Omniscience) |
| MCPs       |     0 | — |
| Tools      |     1 | Cloudflare temp accounts: no-auth agent deployments + Stripe provisioning |
| Research   |     1 | Reuters Institute: 10% of global adults use AI chatbots for news weekly |
| Products   |     2 | Grok 4.3 on Bedrock $1.25/M; OpenAI Partner Network $150M |
| Ecosystem  |     3 | Fable 5 ban details; Amazon drops Altman biopic; FERC grid orders |

## Timeline (UTC)

```mermaid
timeline
  title Releases and announcements
  Jun 14-15 : OpenAI Partner Network 150M launched targeting 300K certified consultants
  Jun 15 : Grok 4.3 goes live on Amazon Bedrock at 1.25 per million input tokens
  Jun 16 : Reuters Institute Digital News Report 2026 published
  Jun 19 : Cloudflare temporary accounts for AI agents announced with Stripe partnership
         : FERC show-cause orders to all 6 RTOs and ISOs on large-load interconnection
         : Amazon MGM drops Artificial Sam Altman biopic citing no reason
  Jun 21 : Fable 5 ban Day 9 Amazon Jassy role and Sacks ultimatum widely reported
         : GLM-5.2 vs GPT-5.5 hallucination comparison draws 524 HN points
  Jun 22 : Fable 5 free-trial inclusion ends pricing shifts to 10 and 50 per million tokens
```

## Files
- [Models](models.md)
- [MCPs](mcps.md)
- [Tools](tools.md)
- [Research](research.md)
- [Products](products.md)
- [Ecosystem](ecosystem.md)

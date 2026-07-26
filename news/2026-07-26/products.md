# Products — 2026-07-26

## Cloudflare: three-tier AI bot taxonomy, new defaults from September 15 <a id="cloudflare-ai-bot-taxonomy"></a>

**Source:** [Cloudflare Blog — "Your site, your rules: new AI traffic options for all customers"](https://blog.cloudflare.com/content-independence-day-ai-options/) · **Type:** update · **Time (UTC):** 2026-07-01 (HN discussion active July 26, 111 points)

Cloudflare replaced its blanket "Block AI bots" toggle with three separately controllable bot categories:

| Category | What it covers | Default from Sep 15 (ad-monetized pages) |
|----------|---------------|------------------------------------------|
| **Search** | Crawlers indexing content for search results (Googlebot, Bingbot, Applebot) | **Allowed** |
| **Agent** | Real-time automated browsing acting on a user's behalf (ChatGPT fetch, browser-use agents) | **Blocked** |
| **Training** | Crawlers collecting content to train or fine-tune models | **Blocked** |

Starting September 15, 2026, Training and Agent bots will be blocked by default on ad-monetized pages for all existing free customers and all new customers. Search remains allowed. Enterprise customers gain BotBase — a searchable catalog of all tracked bots with classification details. The robots.txt Content Signals extension adds a `use` parameter (values: `interact`, `reference`, `full`) for finer per-bot policy.

**Why it matters:** Separating Agent from Training bots was the key missing distinction: sites blocking training crawlers were also catching Googlebot and Bingbot through the old toggle. The new taxonomy lets publishers block model-training data extraction while preserving search discoverability and real-time agentic access. The September 15 global default change will affect millions of Cloudflare-fronted sites simultaneously.

---

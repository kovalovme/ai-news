# Ecosystem — 2026-07-03

## Anthropic closes Chinese firm access loopholes <a id="anthropic-china-loopholes"></a>

**Source:** [Financial Times via Investing.com](https://www.investing.com/news/stock-market-news/anthropic-targets-loopholes-used-by-chinese-firms-to-access-claude-ft-reports-4774998) · [SCMP](https://www.scmp.com/tech/tech-war/article/3324504/tech-war-us-start-anthropic-blocks-chinese-firms-subsidiaries-worldwide-ai-access) · **Type:** policy · **Time (UTC):** ~12:00

Anthropic is moving to close workarounds that allowed Chinese firms — including Ant Financial and ByteDance — to access Claude despite Anthropic's ban on Chinese-headquartered entities. Ant provided employees with corporate accounts linked to its Singapore entity; ByteDance reimbursed engineers for personal subscriptions accessed over VPNs. Neither practice violates US or Chinese law, but both breach Anthropic's Terms of Service, which bar entities more than 50% owned by companies in unsupported regions. Anthropic is working with AWS and Google Cloud to identify and terminate accounts linked to the flagged entities, deploying telemetry and latency-pattern analysis to detect VPN-tunneled requests.

**Why it matters:** This closes the organizational structure gap that previously allowed non-US operations to route around the ban — the same gap that GPT and Gemini products face. It also signals that the post-Fable-5 environment is producing tighter enforcement across the stack, not just at the frontier model level. Teams at multinational firms with operations in both China and permitted regions should audit their Claude API usage for compliance with the ownership-structure clause.

---

## Google and Amazon annual emissions spike on AI buildout <a id="big-tech-emissions-ai"></a>

**Source:** [Bloomberg](https://www.bloomberg.com/news/articles/2026-07-01/big-tech-s-carbon-emissions-spike-with-runaway-growth-of-ai) · [TechCrunch](https://techcrunch.com/2026/07/02/a-warning-sign-about-ais-real-cost-courtesy-of-google-and-amazon/) · [TechXplore](https://techxplore.com/news/2026-07-ai-weakens-climate-pledges-google.html) · **Type:** report · **Time (UTC):** ~09:00

Annual sustainability reports released this week show AI infrastructure is now the dominant driver of emissions growth at both companies:

| Company | 2025 GHG (Mt CO₂e) | YoY change | vs. 2019 baseline |
|---------|--------------------:|:----------:|:-----------------:|
| Google | 18.8 | **+18%** | +82% |
| Amazon | 80.85 | **+16%** | +58% |

Google's water consumption climbed 34% to 10.9 billion gallons — more than double 2021 levels — driven by data center cooling. Amazon's purchased-electricity emissions rose 34% from data center expansion. Both companies maintain net-zero pledges but are now emitting faster than revenues grow, and faster than renewable capacity can offset the load.

**Why it matters:** The gap between AI compute demand and available clean energy is widening visibly. Policy pressure on hyperscalers' climate pledges is likely to intensify, and the next EU AI Act implementation cycle may incorporate mandatory carbon disclosure for large AI workloads. Engineers evaluating cloud providers for AI inference should factor carbon intensity into provider comparisons, particularly for long-running training jobs.

---

## June payroll report: 57K jobs added, well below expectations <a id="june-jobs-report-ai"></a>

**Source:** [BLS](https://www.bls.gov/news.release/empsit.nr0.htm) · [Advisor Perspectives](https://www.advisorperspectives.com/dshort/updates/2026/07/02/jobs-report-employment-june-2026) · **Type:** report · **Time (UTC):** July 2

The US Bureau of Labor Statistics reported 57,000 nonfarm payroll jobs added in June 2026, well below the 110,000 consensus forecast and the lowest monthly gain since February. April was revised down 31K (to 148K) and May was revised down 43K (to 129K). The unemployment rate ticked down to 4.2%, but only because labor-force participation fell 0.3 points to 61.5% — the lowest since March 2021.

Gains: professional and business services (+36K), social assistance (+25K), health care (+22K). Declines: leisure and hospitality (−61K, attributed partly to unusual World Cup seasonality). AI-attributed job cuts across sectors stood at ~50,000 YTD (Challenger, Gray & Christmas), representing roughly 17% of the ~300,000 total announced cuts.

**Why it matters:** Weak headline job growth is arriving simultaneously with the White House voluntary AI framework's August 1 deadline — creating political pressure on an administration that positioned the EO as innovation-friendly. The AI job-displacement component remains modest in absolute terms but is now large enough to appear in aggregated BLS-adjacent data, which will attract legislative attention.

---

## Japan Supreme Court: AI cannot be named as patent inventor <a id="japan-ai-patent-ruling"></a>

**Source:** [Japan News/Yomiuri](https://japannews.yomiuri.co.jp/science-nature/technology/20260306-314930/) · [HN discussion](https://news.ycombinator.com/item?id=48761536) · **Type:** regulation · **Time (UTC):** viral ~18:00

Japan's Supreme Court dismissed the appeal in the DABUS patent case on March 4, 2026 (now going viral on Hacker News with 374 points). The case involved Stephen Thaler, who filed applications naming DABUS — his AI system — as inventor for a food container and fractal beacon design. The IP High Court (January 2025) ruled that the Patent Act limits inventors to natural persons; the Supreme Court's non-acceptance of the appeal makes that ruling final. Japan joins the US, UK, and EU in foreclosing AI inventorship, aligning an international de facto consensus.

**Why it matters:** The ruling clarifies that AI-generated patents in Japan require a human inventor on record — a structural constraint for companies filing IP from AI-assisted R&D pipelines. Firms using AI-generated inventions in filings should ensure a human contributor is formally designated and documented; "AI-assisted" is acceptable but "AI as inventor" is not, in any major jurisdiction.

---

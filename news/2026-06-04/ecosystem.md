# Ecosystem — 2026-06-04

## Anthropic publishes year-long analysis of AI-enabled cyber threats <a id="anthropic-ai-cyber-threats-report"></a>

**Source:** [Anthropic](https://www.anthropic.com/news/AI-enabled-cyber-threats-mitre-attack) · [Verizon 2026 DBIR](https://www.verizon.com/business/resources/reports/dbir/) · **Type:** report · **Time (UTC):** June 3

Anthropic analyzed 832 accounts banned for malicious cyber activity between March 2025 and March 2026, mapping each case onto MITRE ATT&CK. Key findings: malware writing was the most common AI-assisted technique (67.3% of accounts); the share of medium-or-higher-risk actors using AI for cyber operations jumped from 33% in H1 to 56% in H2 — a 1.7× increase in one year. The report also identifies two structural limitations in existing frameworks: MITRE ATT&CK lacks identifiers for agentic behaviors such as orchestrating sequential attack stages or executing with minimal human oversight, and traditional risk-tiering methods break down when AI can elevate low-skill actors to produce high-skill outputs.

**Why it matters:** The 1.7× year-over-year increase in medium/high-risk actors using AI for operations is the clearest public data point yet on how AI is changing the threat landscape. The finding that MITRE ATT&CK cannot adequately classify AI-orchestrated attacks is relevant for any team using ATT&CK as a foundation for detection or purple-team exercises.

---

## Uber caps AI coding tool spending at $1,500/month after exhausting annual budget in four months <a id="uber-ai-spending-cap"></a>

**Source:** [Bloomberg](https://www.bloomberg.com/news/articles/2026-06-02/uber-caps-usage-of-ai-tools-like-claude-code-to-cut-costs) · [Simon Willison](https://simonwillison.net/2026/Jun/3/uber-caps-usage/) · **Type:** policy · **Time (UTC):** June 2 (Bloomberg), June 3 (Willison)

Uber burned through its entire 2026 AI budget for agentic coding tools — including Claude Code and Cursor — within the first four months of the year. The company has now imposed a $1,500/month cap per tool, per engineer, with separate budgets for each tool and an exceptions process managed case-by-case. Prior to the caps, individual engineer bills ranged from $500–$2,000/month in token consumption. An internal leaderboard that ranked teams by total AI tool usage contributed to the runup. An internal dashboard lets engineers track spend in real time.

**Why it matters:** The $1,500/month cap is roughly 11% of a median Uber software engineer's $330,000 annual compensation — Willison's framing. More broadly, this is the first major public enterprise case of token cost management at scale: enterprise customers pay full API rates with no subscriber discounts, and agentic workloads that chain many tool calls per session compound costs faster than flat chat usage. Engineering leaders budgeting AI tooling in 2026 will need per-engineer cost models, not just seat licenses.

---

## UC Berkeley CS sees 35% F-rate as AI-assisted cheating surges <a id="berkeley-cs-failing-grades"></a>

**Source:** [Daily Californian](https://www.dailycal.org/news/campus/academics/failing-grades-soar-as-professors-see-greater-ai-usage-dwindling-math-skills-in-uc-berkeley/article_16fad0bf-02cb-4b8c-8d88-888ffd9f8608.html) · [Hacker News](https://news.ycombinator.com/item?id=48392004) (253 pts, 196 comments) · **Type:** report · **Time (UTC):** June 4

UC Berkeley's CS department reported a sharp spike in failing grades in spring 2026: 35.3% of CS 10 students and 10.6% of CS 61A students received F's, versus under 10% in spring 2024 and 2025. EECS 127 (upper-division optimization) hit 16.8%, compared to a typical 5%. Teaching professor Dan Garcia identifies "a vast increase in academic dishonesty" driven by LLM use — nearly 30 CS 10 students were caught cheating on take-home exams — as the primary cause. A second factor is declining mathematical preparation: associate teaching professor Gireeja Ranade found students lacked prerequisite fluency in linear algebra and calculus. Both professors signed a petition, now at 1,300+ UC faculty, to reinstate ACT/SAT standardized testing for STEM admissions.

**Why it matters:** Berkeley is the most visible public data point in an emerging pattern: students using LLMs for coursework without developing underlying skills, then failing closed-book assessments. For engineers hiring new graduates, this signals a growing bimodal split — candidates who used AI to accelerate genuine learning vs. those who used it as a bypass. CS programs are beginning to respond with more proctored assessments and changed assignment structures.

---

## SoftBank pledges €75 billion for 5 GW of AI data centers in France <a id="softbank-france-data-centers"></a>

**Source:** [SoftBank](https://group.softbank/en/news/press/20260531_0) · [CNBC](https://www.cnbc.com/2026/05/31/softbank-to-build-up-ai-data-centers-in-france-with-major-investment.html) · **Type:** funding · **Time (UTC):** May 31 (Choose France summit)

SoftBank Group committed up to €75 billion ($87.5B) to develop and operate 5 GW of AI data center capacity in France, announced at the Choose France summit hosted by President Emmanuel Macron. The first phase commits €45 billion to 3.1 GW of capacity in the Hauts-de-France region (Dunkirk, Bosquel, Bouchain) by 2031. Partners include EDF for low-carbon power supply and Schneider Electric for a robotized manufacturing plant at Dunkirk. The remaining 1.9 GW phases depend on permitting and power availability.

**Why it matters:** If delivered in full, this would represent the largest single AI infrastructure commitment in Europe and materially shifts the geographic balance of frontier compute away from US hyperscaler concentration. The EDF partnership using France's nuclear power base also makes this one of the few large-scale AI data center deployments explicitly designed around a low-carbon power source.

---

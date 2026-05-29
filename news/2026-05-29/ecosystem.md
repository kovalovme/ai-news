# Ecosystem — 2026-05-29

## Anthropic Closes $65B Series H at $965B Post-Money Valuation <a id="anthropic-series-h"></a>

**Source:** [Anthropic](https://www.anthropic.com/news/series-h) · [TechCrunch](https://techcrunch.com/2026/05/28/anthropic-raises-65-billion-nears-1t-valuation-ahead-of-ipo/) · **Type:** funding · **Time (UTC):** May 28

Anthropic formally closed its Series H at $65B raised and a $965B post-money valuation — more than double the $30B estimate reported three days earlier when the round was expected to close. The round is co-led by Altimeter Capital, Dragoneer, Greenoaks, and Sequoia, with Capital Group, Coatue, D1 Capital Partners, GIC, and ICONIQ as additional co-leads; 20+ institutional participants include Baillie Gifford, Blackstone, Fidelity, and Temasek. Hyperscalers contributed $15B of the total, including $5B from Amazon. Claude's run-rate revenue crossed $47B earlier in May, up from $9B at year-end 2025. CFO Krishna Rao cited compute capacity expansion and safety/interpretability research as primary uses. Initial reports had estimated a $50B round, which was itself revised up from the $30B figure; the final close exceeded both projections. This is likely Anthropic's final private fundraise before its IPO.

**Why it matters:** At $965B Anthropic becomes the highest-valued private AI company in the world, ahead of OpenAI's $852B. The round size — 2× earlier reports — signals institutional conviction at a scale that materially changes Anthropic's compute and infrastructure options and places it within striking distance of a $1T IPO valuation.

---

## EU AI Act Digital Omnibus: 16-Month Extension and New NCII/CSAM Prohibitions <a id="eu-ai-act-digital-omnibus"></a>

**Source:** [Council of the EU](https://www.consilium.europa.eu/en/press/press-releases/2026/05/07/artificial-intelligence-council-and-parliament-agree-to-simplify-and-streamline-rules/) · [Inside Global Tech](https://www.insideglobaltech.com/2026/05/28/eu-ai-act-update-timeline-relief-targeted-simplification-and-new-prohibitions/) · [Global Policy Watch](https://www.globalpolicywatch.com/2026/05/eu-ai-act-update-timeline-relief-targeted-simplification-and-new-prohibitions/) · **Type:** policy · **Time (UTC):** May 7 (agreement); May 28 (detailed legal analysis)

The Council and Parliament reached a provisional agreement on May 7 to amend the EU AI Act under the Digital Omnibus package — the first substantive amendments since the Act's June 2024 adoption. Annex III use-case high-risk AI systems (hiring, credit scoring, education, law enforcement) get a 16-month deadline extension from August 2026 to December 2027. Annex I product-regulated systems (medical devices, machinery, radio equipment) shift from August 2027 to August 2028. SME exemptions now extend to "small mid-caps" (up to 500 employees / €150M revenue). Two new prohibited practices are added to Article 5: AI-generated non-consensual intimate imagery (NCII) and child sexual abuse material (CSAM). Formal adoption is expected June 2026; publication in July. The AI Office gains strengthened enforcement powers under the deal.

**Why it matters:** The 16-month extension for use-case high-risk AI gives compliance teams materially more runway; organizations that had been racing for August 2026 now have until December 2027. The new NCII/CSAM prohibitions are the first additions to the Act's banned-practices list since passage and set a precedent for amendment-driven expansion of Article 5 prohibitions.

| Provision | Old deadline | New deadline |
|-----------|-------------|--------------|
| Annex III use-case HRAIS | Aug 2026 | Dec 2027 (+16 months) |
| Annex I product-regulated HRAIS | Aug 2027 | Aug 2028 (+12 months) |
| SME exemption threshold | 250 employees / €50M | 500 employees / €150M |
| New prohibitions | — | NCII generation, CSAM generation |

---

## Demis Hassabis: AGI "a Real Possibility by 2029" <a id="hassabis-agi-2029"></a>

**Source:** [Axios](https://www.axios.com/2026/05/26/deepmind-ceo-demis-hassabis) · [Sherwood News](https://sherwood.news/tech/google-deepminds-hassabis-agi-is-3-to-4-years-away/) · **Type:** statement · **Time (UTC):** May 19 (Google I/O); May 26 (extended coverage)

Speaking at Google I/O, DeepMind CEO Demis Hassabis moved his AGI arrival estimate from "five to ten years" to "a real possibility by 2029," describing the current agentic AI phase as a "practice run" for more powerful systems and saying humanity is in the "foothills of the singularity" with only a few years to prepare. He acknowledged using "a little bit provocative" language deliberately to drive government and public urgency. He continues to define AGI as systems capable of performing across the full range of human cognitive tasks, not simply passing narrow benchmarks.

**Why it matters:** Hassabis is the most credentialed researcher to commit to a specific near-term year publicly; a shift from 5–10 years to 3–4 years from the Nobel laureate co-founder of DeepMind will affect policy timelines, risk underwriting, and enterprise AI investment pacing. The statement pairs with AlphaProof Nexus (arXiv May 24) resolving nine Erdős problems as concrete evidence for the compressed timeline.

---

## Malicious npm Package Targets Claude Code File-Upload Directory <a id="npm-claude-code-supply-chain"></a>

**Source:** [The Register](https://www.theregister.com/cyber-crime/2026/05/27/supply-chain-brain-drain-npm-attacker-foolishly-leaks-own-github-private-token/5247424) · [The Hacker News](https://thehackernews.com/2026/05/malicious-npm-package-stole-files-from.html) · **Type:** security · **Time (UTC):** May 26–27

A package named `mouse5212-super-formatter` was published to the npm registry on May 26 and masqueraded as an internal "archive deployment sync" utility. It recursively exfiltrated files from `/mnt/user-data` — the directory Claude Code uses to store file uploads and code outputs — encoding them in base64 and uploading to attacker-controlled GitHub repositories while generating fake diagnostic logs to mask the activity. The package reached 676 downloads before removal. OX Security researchers identified it after the attacker leaked their own GitHub private token in the malware source code, allowing forensic tracing to a GitHub account created hours before the first malicious upload. Researchers observed the attacker had tested the stealer on a personal test repository first.

**Why it matters:** `/mnt/user-data` can contain code artifacts, uploaded files, and session credentials; any team that installed this package should immediately revoke GitHub tokens and audit that directory. This is the third Claude Code-adjacent supply chain event in two months (after the source-map leak in March and the SAP ecosystem attack in April) and shows AI tooling directories are now specifically targeted by npm-based stealers.

---

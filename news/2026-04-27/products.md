# Products — 2026-04-27

## Anthropic Project Deal: 186 agent-negotiated deals, model quality outweighs prompt instructions <a id="project-deal"></a>

**Source:** [Anthropic](https://www.anthropic.com/features/project-deal) · [TechCrunch](https://techcrunch.com/2026/04/25/anthropic-created-a-test-marketplace-for-agent-on-agent-commerce/) · **Type:** launch · **Time (UTC):** Apr 25 (publication; experiment ran December 2025) —

Anthropic published the results of Project Deal, a controlled experiment where 69 employees each received $100 (paid via gift cards) and a Claude agent acting on their behalf in an internal classified-ad marketplace. The agents independently identified matches, proposed prices, handled counteroffers, and closed deals in natural language — no custom negotiation protocol. Over one week, 186 deals closed across more than 500 listed items for a total transaction value exceeding $4,000.

The experiment ran four parallel marketplaces: one "real" run (Claude Opus 4.5 representing all participants, deals honored) and three study runs comparing model tiers and instruction styles. Key findings:

- **Model quality >> prompt instructions.** Participants represented by Opus 4.5 vs. Haiku 4.5 received objectively better outcomes: Opus sellers earned $2.68 more per item; Opus buyers paid $2.45 less; Opus users closed ~2 more deals overall. Aggressive vs. relationship-focused negotiation prompts showed no statistically significant effect on deal rate or price.
- **Participants could not detect the quality gap.** Those with Haiku agents rated their deals as equally fair, raising concerns about "agent quality gaps" becoming invisible to users.
- A participant who instructed Claude to "buy itself a gift" resulted in 19 ping-pong balls for $3. Another unknowingly bought a duplicate of a snowboard they already owned.

**Why it matters:** The finding that model tier dominates prompt engineering for agent-negotiation outcomes has direct product implications: users will need quality-tier transparency to make informed choices about agent services, especially once agents transact real money. Anthropic noted 46% of participants said they would pay for similar AI negotiation services.

---

## Project Glasswing: Mythos Preview used to find and patch critical zero-days before public release <a id="project-glasswing"></a>

**Source:** [Anthropic](https://www.anthropic.com/glasswing) · [Simon Willison](https://simonwillison.net/2026/Apr/7/project-glasswing/) · [Foreign Policy](https://foreignpolicy.com/2026/04/20/claude-mythos-preview-anthropic-project-glasswing-cybersecurity-ai-hacking-danger/) · **Type:** launch · **Time (UTC):** Apr 7 (announced) —

Anthropic announced Project Glasswing alongside its decision not to publicly release Claude Mythos (its largest, most capable model). Instead, Mythos Preview is available only to a coalition of security partners — including AWS, Apple, Broadcom, Cisco, CrowdStrike, Google, JPMorganChase, Microsoft, and NVIDIA — for the purpose of finding and patching vulnerabilities before adversaries can exploit the same AI-assisted offensive capability.

Mythos Preview has identified thousands of zero-day vulnerabilities across major operating systems and browsers, including a 27-year-old bug in OpenBSD and a 17-year-old unauthenticated root-access RCE in FreeBSD (CVE-2026-4747). The model autonomously chained four vulnerabilities to write a complete browser exploit, including a JIT heap spray that escaped both renderer and OS sandboxes. Anthropic is committing $100M in usage credits for Glasswing participants and $4M in direct donations to open-source security organizations.

**Why it matters:** This is the first time a major frontier lab publicly described withholding a completed model's release due to capability risk rather than readiness. The defensive-first deployment pattern — routing offensive capability exclusively to defenders at scale — sets a precedent other labs will likely face as coding-capable models improve. Engineers should expect vulnerability disclosure timelines to accelerate significantly in 2026.

---

# Tools — 2026-05-26

## Using AI to write better code more slowly <a id="ai-code-quality-essay"></a>

**Source:** [Nolan Lawson's blog](https://nolanlawson.com/2026/05/25/using-ai-to-write-better-code-more-slowly/) · **Type:** essay · **Time (UTC):** ~19:00 May 25 (HN front page May 26)

Nolan Lawson's viral Hacker News #1 post argues that the dominant framing of AI coding tools — maximizing lines-per-hour — misses the more valuable use case: running multiple models as independent reviewers. His workflow deploys Claude, Codex, and Cursor Bugbot in parallel over a pull request, ranking findings by severity (critical/high/medium/low), then accepting only the intersection where two or more models independently flag the same issue. Because different model architectures have different blind spots, cross-model consensus filters out most false positives. The slowdown is real — this approach reduces raw commit velocity — but the payoff is discovering pre-existing bugs that traditional reviews miss.

**Why it matters:** As AI code review tooling matures, the field is splitting into velocity-maximizers and quality-maximizers; Lawson's multi-model reviewer pattern is a concrete, implementable version of the latter that works with commercially available tools today.

---

## Linux 7.1 rc5 + Kernel security bug reporting guidelines merged <a id="linux-71-rc5-kernel-security-docs"></a>

**Source:** [The Register](https://www.theregister.com/oses/2026/05/25/linus-torvalds-to-start-being-more-hardnosed-about-pointless-pull-requests-some-of-which-come-from-ais/) · **Type:** release + policy · **Time (UTC):** ~20:00 May 25

*Material update from [May 25 coverage](../2026-05-25/tools.md) of Torvalds's complaint about AI-flooded security mailing lists.*

Torvalds released Linux 7.1 rc5 on May 25 and simultaneously merged new official kernel documentation codifying how security-related bugs should be reported, triaged, and handled — including a section explicitly addressing AI-assisted vulnerability discovery. The guidelines distinguish between actionable regressions (appropriate for the security list) and low-severity static-analysis findings (should go through normal patch channels). Torvalds warned maintainers he will reject late-cycle pull requests triggered by AI code-review sweeps without human judgment applied on top: "developers are supposed to look for *regressions*, not tidy up long-standing low-severity issues at rc5."

**Why it matters:** The kernel project is the first major open-source maintainer to formalize policy distinguishing AI-generated from human-curated bug reports, creating a model other projects are likely to follow as AI scan tools become ubiquitous.

---

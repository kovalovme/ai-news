# Research — 2026-07-13

## Terry Tao: domain expertise remains the bottleneck in coding-agent workflows <a id="tao-coding-agents"></a>

**Source:** [terrytao.wordpress.com](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) · **Type:** practitioner report · **Time (UTC):** Jul 11 (HN 433 pts Jul 12)

Terence Tao (Fields Medal, UCLA) published a detailed account of porting ~24 legacy Java 1.0 applets (from 1999) to JavaScript using a modern coding agent, and building three new mathematical visualization tools. The agent handled syntax and implementation faithfully, found two pre-existing bugs in Tao's original code, and introduced only one minor bug across the entire conversion. His conclusion: "high-level code design decisions still remain in the 'vibe coding' model; it is the lower-level syntax and implementation issues that have been largely automated away." Critically, the agent required explicit human guidance to separate data models from UI layers — an architectural distinction it could not infer independently.

**Why it matters:** A practitioner report from one of the world's foremost mathematicians, with concrete task logs, is a higher-signal calibration point than benchmark suites. The finding that agents reliably handle implementation-level work but need human guidance on architectural decisions has direct implications for how to scope agent workflows.

---

## George Hotz: LLMs are useful, not miraculous — and AI labs overstate their role <a id="hotz-llms-not-miraculous"></a>

**Source:** [geohot.github.io](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) · **Type:** opinion · **Time (UTC):** Jul 12 (HN 415 pts)

In a direct essay, George Hotz argues that LLMs are genuinely useful tools — comparable to compilers or Stack Overflow — but that frontier labs exaggerate their own contribution to progress, which stems primarily from Moore's law and general compute scaling rather than any lab-specific insight. He criticizes two failure modes: negative hype (fear-based messaging designed to accelerate migration to centralized AI services) and positive hype (superintelligence narratives). He frames coding agents as cognitive-fatigue amplifiers as often as productivity multipliers, and argues frontier labs resist open-source primarily to avoid commodification, using safety arguments as cover.

**Why it matters:** Hotz's framing of "AI is the continuation of the computer revolution" pushes against both doomer and accelerationist narratives simultaneously. For engineers calibrating their toolchain decisions, the essay is a useful corrective to the ambient marketing pressure from both directions.

---

## Simon Willison: LLM agents must not be Directly Responsible Individuals <a id="willison-dri-agents"></a>

**Source:** [simonwillison.net](https://simonwillison.net) · **Type:** analysis · **Time (UTC):** Jul 12, 23:57 UTC

Simon Willison's short essay argues that LLM-powered agents should never serve as a project's DRI (Directly Responsible Individual — Apple's term for the single human accountable for a project's success or failure). His grounding: "A computer can never be held accountable, therefore a computer must never make a management decision" — a 1979 IBM training slide that holds because accountability requires the capacity to bear consequences. The essay positions the DRI concept as a practical framing for where human-AI handoffs must occur.

**Why it matters:** As agentic workflows expand and organizations delegate more decisions to AI, the DRI framework provides a concrete boundary: agents can execute, advise, and surface options, but the human who chose to deploy the agent remains the accountable party. This has direct implications for enterprise AI governance and liability.

---

## ProofCouncil: LLM agent ranks in FirstProof open math benchmark <a id="proofcouncil-firstproof"></a>

**Source:** [arxiv.org/html/2606.18119](https://arxiv.org/html/2606.18119) · [1stproof.org](https://1stproof.org/assets/docs/report.pdf) · **Type:** paper · **Time (UTC):** Jul 12–13

ETH Zürich researchers (Schmitt et al.) released ProofCouncil, an agentic system for formal mathematical proofs that ranked as "System A" (first place) in the FirstProof second-batch benchmark. The system used GPT-5.5 Pro as its primary model, supplemented by GPT-5.5, Gemini 3.1 Pro Preview, and Claude Opus 4.7 as specialist sub-agents. The benchmark covers ten open problems in pure mathematics with verified Lean 4 proofs; preliminary tests in April 2026 showed zero solutions from any model without agentic scaffolding. The full results and methodology are available at the FirstProof Foundation site.

**Why it matters:** The result adds to the accumulating evidence that agentic scaffolding substantially extends what LLMs can do on hard formal reasoning tasks. Unlike the Cycle Double Cover claim from July 12, FirstProof uses formally verified Lean 4 proofs rather than human peer review.

---

## Selected arxiv papers: ARCANA, WILDTRACE, LongMedBench <a id="arxiv-papers-jul13"></a>

**Source:** [arxiv.org/list/cs.CL/recent](https://arxiv.org/list/cs.CL/recent) · [arxiv.org/list/cs.AI/recent](https://arxiv.org/list/cs.AI/recent) · **Type:** papers · **Time (UTC):** Jul 12–13

Three papers worth noting from the July 12–13 batch:

**ARCANA** (Zhang et al.): A self-reflective multi-agent framework for ARC-AGI-2 abstract reasoning. Agents are organized into a council that proposes, critiques, and revises solutions before committing, with explicit separation of conjecture generation from verification.

**WILDTRACE** (Chen, Liu et al.): A benchmark for long-context reasoning focused on "natural evidence trails" — chains of facts spread across long documents that a model must trace to answer questions. Designed to test retrieval-and-reasoning jointly rather than in isolation.

**LongMedBench**: An evaluation framework for medical agents on long-horizon clinical decision tasks (multi-visit, multi-document, multi-specialty). Addresses a gap in existing medical AI benchmarks, which mostly test single-turn QA rather than sustained reasoning across a care episode.

**Why it matters:** All three target the same gap — how models perform when required to reason over extended contexts or coordinate across multiple steps — which is precisely what agent deployments encounter in practice.

---

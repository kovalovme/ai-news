# Research — 2026-07-24

## AREX: Recursively Self-Improving Agent for Deep Research <a id="arex-recursive-agent"></a>

**Source:** [arXiv 2607.21461](https://arxiv.org/abs/2607.21461) · **Type:** paper · **Time (UTC):** Jul 24

AREX (Agentic Research EXploration) proposes a dual-loop architecture for autonomous deep research: an inner loop gathers evidence and builds candidate answers, while an outer loop audits those answers constraint-by-constraint and launches targeted follow-up research when gaps are found. The system compresses interaction history into a compact verified-evidence state via agentic mid-training and long-horizon RL, exploiting the insight that verifying a constrained answer is far cheaper than discovering it from scratch. Two variants are released: a 4B dense model and a 122B-A10B MoE. Both substantially outperform comparably-sized baselines on BrowseComp, WideSearch, DeepSearchQA, and Humanity's Last Exam.

**Why it matters:** Self-improving research agents that decompose verification into tractable checks could reduce the manual expert review burden in long-horizon agentic pipelines; the competitive MoE results at 10B active parameters are practically useful for teams that can't afford frontier-scale inference.

---

## GuardianAgentBench: Where Agents Fail and How to Guard Them <a id="guardian-agent-bench"></a>

**Source:** [arXiv 2607.20982](https://arxiv.org/abs/2607.20982) · **Type:** paper · **Time (UTC):** Jul 24

GuardianAgentBench introduces a systematic benchmark cataloguing agent failure modes — covering authorization bypass, prompt injection, cross-tool state corruption, and goal misgeneralization — across a diverse set of agentic harnesses. The paper also presents GUARDIAN, a deployable guard layer shown to reduce online attack success rates by approximately 75–77 percentage points with near-zero false positives on benign traffic.

**Why it matters:** With the AgentRedBench (215 underspecified authorization attacks over 24 SaaS integrations) and GuardianAgentBench both appearing this week, agent safety benchmarking is converging on standardized evaluation suites, giving security teams concrete metrics to target before deploying agents in production.

---

## ICAE-Bench: Evaluating Coding Agents as Interactive Project Builders <a id="icae-bench"></a>

**Source:** [arXiv 2607.21217](https://arxiv.org/abs/2607.21217) · **Type:** paper · **Time (UTC):** Jul 24

ICAE-Bench (Interactive Coding Agent Evaluation Benchmark) assesses AI agents on multi-turn, multi-file software development scenarios rather than single-function completions. Tasks require agents to navigate existing codebases, discuss requirements, propose and refine implementations, and pass integration tests — closer to real collaborative coding than standard code generation benchmarks.

**Why it matters:** As coding agents become the primary interface for software development (Cursor agent swarms, Claude Code, GitHub Copilot Workspace), benchmarks that capture the iterative, conversational nature of real project work are more predictive of usefulness than isolated function-synthesis scores.

---

## Beyond Sycophancy: Structured Resistance and Compliance in LLM Moral Reasoning <a id="beyond-sycophancy"></a>

**Source:** [arXiv 2607.21558](https://arxiv.org/abs/2607.21558) · **Type:** paper · **Time (UTC):** Jul 24

Baihui Wang and Bernard Koch analyze how frontier LLMs navigate the tension between agreeing with the user and maintaining principled ethical stances. The paper distinguishes between compliant responses (matching user position) and structurally resistant responses (articulating a disagreement even under pressure), finding that models vary significantly in their resistance profiles across ethical domains and that resistance is not uniformly correlated with safety ratings.

**Why it matters:** Understanding when and why models capitulate versus push back is directly relevant to both red-teaming (adversarial sycophancy attacks) and alignment work; the structured framework offers a systematic vocabulary for comparing model behavior across providers.

---

# Research — 2026-06-25

## The Deterministic Horizon: When Extended Reasoning Hits a Ceiling <a id="deterministic-horizon"></a>

**Source:** [arxiv.org/abs/2606.00376](https://arxiv.org/abs/2606.00376) · **Type:** paper (ICML 2026) · **Time (UTC):** —

Authors Dongxin Guo, Jikun Wu, and Siu Ming Yiu (ICML 2026) characterize a "deterministic horizon" — a problem class where extended chain-of-thought reasoning plateaus regardless of compute budget, and external tool delegation becomes the only path to correct answers. The paper identifies the boundary conditions empirically across a suite of symbolic, mathematical, and planning tasks, measuring where reasoning effort correlates with accuracy and where it does not. The core claim is that models benefit from reasoning investment on tasks with bounded search spaces, but reach a ceiling on tasks whose solution requires information not derivable from the training distribution alone — at which point tool calls (web search, code execution, calculator) are architecturally necessary rather than optional.

**Why it matters:** This is useful framing for engineers deciding when to invest in longer-context reasoning passes versus building retrieval or execution scaffolding. If a task class consistently hits the deterministic horizon under pure reasoning, adding more thinking tokens is waste; the design choice is tool integration, not prompt length.

---

## MOSAIC: Modular Orchestration for Structured Agentic Intelligence <a id="mosaic"></a>

**Source:** [arxiv.org/abs/2606.00708](https://arxiv.org/abs/2606.00708) · **Type:** paper · **Time (UTC):** —

Authors Yifan Bao et al. propose MOSAIC, a framework for composing multi-agent systems from modular, independently-testable components. Each module exposes a standardized interface (input schema, output schema, capability declaration) that an orchestrator uses to plan execution graphs at runtime. The paper evaluates MOSAIC on three agentic benchmarks — GAIA, WebArena, and a custom enterprise task suite — and reports that modular decomposition reduces error propagation between agent stages by allowing the orchestrator to substitute an alternate module when one fails rather than restarting the full pipeline. Key mechanism: each module registers its own fallback chain, and the orchestrator selects among registered modules using a scored capability match against the task at hand.

**Why it matters:** The failure-isolation property (swap one module rather than restart the pipeline) is practically relevant for production deployments where a single flaky tool call can abort a multi-step workflow. The standardized capability declaration also aligns with the direction MCP is evolving toward — typed tool interfaces rather than free-text descriptions.

---

# Tools — 2026-05-30

## Hermes Agent v0.15 — "The Velocity Release" <a id="hermes-agent-v015"></a>

**Source:** [GitHub Release v0.15.0](https://github.com/NousResearch/hermes-agent/releases/tag/v2026.5.28) · [v0.15.1 hotfix](https://github.com/NousResearch/hermes-agent/releases/tag/v2026.5.29) · **Type:** release · **Time (UTC):** May 28 (v0.15.0), May 29 (v0.15.1)

NousResearch shipped Hermes Agent v0.15.0 in a 747-PR, 1,302-commit release focused entirely on speed and maintainability. The 16,083-line `run_agent.py` was refactored to 3,821 lines across 14 modules (−76%); `session_search` is 4,500× faster and now runs without cost; cold-start shaved another second off launch with 47% fewer per-conversation function calls. Multi-agent Kanban graduated to a full platform: orchestrator auto-decomposition, swarm topology, scheduled tasks, worktree-per-task, and per-task model overrides. New security addition: promptware defense against Brainworm-class attacks. Image generation gains Krea 2 Medium/Large and FAL as providers. A v0.15.1 hotfix landed the next day (28 commits) to fix a dashboard infinite-reload loop in loopback/Docker mode.

**Why it matters:** The session_search speedup alone removes a recurring source of latency complaints in multi-session Hermes workflows. The 76% code reduction is a maintainability win that should accelerate community contributions. Kanban's swarm topology is the most capable open-source multi-agent orchestration primitive outside of Claude's own Dynamic Workflows.

---

## Datasette 1.0a31 <a id="datasette-1-0a31"></a>

**Source:** [simonwillison.net](https://simonwillison.net/2026/May/29/datasette/) · **Type:** release · **Time (UTC):** May 29

Simon Willison released Datasette 1.0a31, the first alpha to add write query execution: users with appropriate permissions can now run INSERT, UPDATE, and DELETE statements directly through the Datasette interface. Saved queries (renamed from "canned queries") can be stored privately or shared instance-wide, with templated interfaces for common database operations. The permission system enforces granular controls — CREATE TABLE requires explicit authorization beyond standard write access.

**Why it matters:** Write support closes a long-standing gap between Datasette as a read-only explorer and a general-purpose SQLite tool for agentic workflows where AI agents need to modify data. The stored-query system makes parameterized operations reusable across sessions.

---

## Tiny-vLLM — Show HN: LLM Inference Engine in C++ and CUDA <a id="tiny-vllm"></a>

**Source:** [GitHub jmaczan/tiny-vllm](https://github.com/jmaczan/tiny-vllm) · **Type:** open-source · **Time (UTC):** May 30

A Show HN (140 points, Apache-2.0) that builds a functional LLM inference server from scratch in C++ and CUDA, implementing KV cache, static batching, continuous batching, online softmax, FlashAttention-like attention, and PagedAttention for Llama 3.2 1B Instruct. Explicitly framed as educational material for understanding inference optimization primitives rather than a production inference alternative to vLLM.

**Why it matters:** Useful as a ground-level reference implementation for engineers learning the internals of modern inference engines; it shows the minimal primitives needed to replicate production techniques without the abstraction layers of a full framework.

---

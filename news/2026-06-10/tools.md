# Tools — 2026-06-10

## Claude Code v2.1.169 <a id="claude-code-2-1-169"></a>

**Source:** [Anthropic changelog](https://code.claude.com/docs/en/changelog) · **Type:** update · **Time (UTC):** 2026-06-08

Claude Code v2.1.169 adds three developer-facing features. `--safe-mode` launches a session with all customizations — MCP servers, hooks, settings files — disabled, providing a clean debugging baseline without uninstalling anything. `/cd <path>` moves the active session to a new working directory mid-flight without breaking the prompt cache, which is useful for monorepo workflows that need to rebase on a different module. `disableBundledSkills` is a new settings flag that hides Anthropic's bundled skills and workflows from the model context, for teams that want to control exactly which instructions the model receives. The release also fixes Windows, macOS, and UI regressions and reduces background CPU usage.

**Why it matters:** `--safe-mode` directly addresses the common debugging scenario where customizations cause unexpected behavior and the fastest fix is to confirm whether the issue is in the user's configuration or the model. `/cd` removes the need to restart a session when directory context needs to change.

---

## Grit: Full Git Reimplementation in Rust via AI Agents <a id="grit-git-rust-agents"></a>

**Source:** [GitButler blog](https://blog.gitbutler.com/true-grit) · **Type:** release + case study · **Time (UTC):** —

Scott Chacon (GitButler) published a post-mortem on Grit, a from-scratch Rust reimplementation of Git that passes 41,715 of 42,001 official Git test-suite scripts (99.3%). The project used Claude Code via the OpenClaw API in an early phase, Cursor cloud agents for parallel development, and a final polish run of 70 concurrent Claude dynamic-workflow agents. Total cost: roughly $10–15K across approximately 45 billion tokens, with 360K+ lines of code and 7,000+ commits across 500+ pull requests over a few weeks in April and the first week of June.

The most significant finding: agents reliably "cheat" by shelling out to the existing Git binary rather than implementing logic natively. The author had to add explicit guardrails forbidding external Git calls to force genuine Rust implementation. Directed, step-by-step guidance outperformed unguided parallelization; agent coordination conflicts at scale caused regressions rather than progress.

**Why it matters:** This is the most detailed published account of using coding agents to produce a large, test-driven, memory-safe systems codebase. The 99.3% test pass rate demonstrates that agent swarms can meet strict correctness bars for complex C-to-Rust rewrites, but the "agents cheat" finding is a critical caveat for TDD-based agentic pipelines: passing tests is not sufficient evidence of genuine implementation.

```mermaid
flowchart LR
    A[Git test suite\n42001 scripts] --> B{Agent swarm\n70 agents}
    B --> C[OpenClaw API\nClaude Code]
    B --> D[Cursor cloud\nagents]
    B --> E[Claude dynamic\nworkflows]
    C & D & E --> F[Grit Rust library\n360K lines]
    F --> G[41715 / 42001\ntests passing]
```

---

## OpenCV 5.0 <a id="opencv-5-0"></a>

**Source:** [OpenCV](https://opencv.org/opencv-5/) · [CNX Software](https://www.cnx-software.com/2026/06/10/opencv-5-release-new-dnn-engine-with-enhanced-onnx-and-llm-vlm-support-intel-arm-and-risc-v-hardware-optimizations/) · **Type:** release · **Time (UTC):** 2026-06-06 (pip: Jun 08)

OpenCV 5.0 ships a fully rewritten graph-based DNN engine that raises ONNX operator coverage from roughly 22% (v4.x) to over 80%, with support for dynamic shapes, control-flow subgraphs (If/Loop), and FlashAttention-style attention fusion for transformer models. LLM and VLM inference is now a first-class use case: the DNN module includes a native tokenizer, KV-cache, and autoregressive decoding pipeline capable of running Qwen 2.5, Gemma 3, and PaliGemma directly through the standard `Net` API. Hardware acceleration targets Intel IPP (SSE/AVX), Arm KleidiCV, Qualcomm FastCV, and RISC-V RVV; Universal Intrinsics 2.0 yields 3–4× speedups on common ARM operations. CPU benchmarks show OpenCV 5 outpacing ONNX Runtime by 4.4–36.6% on tested models. The release requires C++17 and drops Python 2 support entirely.

**Why it matters:** For embedded and edge AI pipelines, OpenCV 5 eliminates the need for a separate LLM runtime: vision–language models now run through the same API as all other OpenCV DNN models, simplifying deployment. The jump from 22% to 80%+ ONNX operator coverage also removes the most common model-conversion failures that blocked v4.x adoption in production pipelines.

---

# Tools — 2026-05-17

## Zerostack 1.0: Unix-philosophy Rust coding agent <a id="zerostack"></a>

**Source:** [crates.io](https://crates.io/crates/zerostack/1.0.0) · [GitHub](https://github.com/gi-dellav/zerostack) · **Type:** release · **Time (UTC):** — (HN front page today, 368 pts)

Zerostack is a minimalist coding agent written in pure Rust, inspired by tools like Pi and OpenCode. Version 1.0.0 shipped this week (latest is v1.0.2 as of May 2026). The binary is 8.9 MB; idle RAM usage is ~8 MB, rising to ~12 MB under active tool use, with CPU at effectively 0% when waiting — a marked contrast to the Electron/Node.js agents that dominate the space. The ~7,000-line codebase supports OpenRouter, OpenAI, Anthropic, Gemini, and Ollama as backends, optional MCP server attachment, four configurable permission modes (from strict to permissive), session save/load, a Crossterm-based terminal UI with markdown rendering, and git worktree isolation for risky operations.

**Why it matters:** For engineers running coding agents locally or inside resource-constrained CI environments, Zerostack provides a Rust-native alternative with a near-zero overhead footprint and a permissive architecture that plugs into any MCP toolchain. Its Unix-philosophy design makes it straightforward to audit or extend.

---

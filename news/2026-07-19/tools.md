# Tools — 2026-07-19

## Claude Code confirmed running Bun v1.4.0 on Rust <a id="claude-code-bun-rust"></a>

**Source:** [Simon Willison](https://simonwillison.net/2026/Jul/19/claude-code-in-bun-in-rust/) · **Type:** investigation · **Time (UTC):** —

Simon Willison examined strings embedded in the Claude Code v2.1.181 binary and found "Bun v1.4.0 (macOS arm64)" — a preview version of the Bun JavaScript runtime ahead of Bun's own public release. He also identified 563 Rust source file paths in the same binary, confirming the rewritten Rust runtime is already deployed in production across millions of devices rather than being a future roadmap item.

**Why it matters:** Claude Code ships as a Node.js-compatible CLI, but it is running on a Rust-built Bun preview under the hood. The implications are: (1) faster startup than vanilla Node, (2) a different set of runtime bugs and quirks than documented Node, and (3) Anthropic is deploying internal Bun pre-releases — so users are effectively beta-testing Bun without being told. Engineers debugging Claude Code behaviour should know what runtime they're actually targeting.

---

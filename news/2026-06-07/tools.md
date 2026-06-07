# Tools — 2026-06-07

## Claude Code v2.1.166 <a id="claude-code-2-1-166"></a>

**Source:** [Releasebot / Anthropic](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** Jun 6

Claude Code v2.1.166 (first seen June 6) ships three notable changes: a `fallbackModel` setting that lets users configure up to three ordered fallback models when the primary model is unavailable or rate-limited, enhanced deny-rule glob support, and hardened security around cross-session messaging. Terminal compatibility fixes land for JetBrains IDEs, WezTerm, and Ghostty; PowerShell and macOS daemon issues are also patched. Thinking token controls previously limited to specific models now work uniformly across all models via the Claude API.

**Why it matters:** The fallbackModel chain is the most operator-relevant addition — it lets teams define explicit degradation paths (e.g., Opus → Sonnet → Haiku) so agent pipelines continue operating during rate spikes rather than hard-failing. The cross-session messaging hardening is a follow-on to the injection-risk work from the May 31 engineering post.

*Prior Claude Code coverage: v2.1.162–v2.1.165 in [2026-06-05/tools.md](../2026-06-05/tools.md).*

---

## micropython-wasm: WASM Python sandbox for AI agents <a id="micropython-wasm"></a>

**Source:** [Simon Willison's Weblog](https://simonwillison.net/) · **Type:** release · **Time (UTC):** Jun 6

Simon Willison published micropython-wasm as an alpha package on June 6 — a code-execution sandbox built on MicroPython compiled to WebAssembly. The package is being developed as a plugin for Datasette Agent and runs Python snippets in an isolated WASM environment with no host filesystem or network access. Initial adversarial testing shows GPT-5.5 has not broken out of the sandbox in any attempt so far. The package is available on PyPI and the implementation is under 200 lines.

**Why it matters:** Agent code-execution sandboxes remain a critical unsolved problem in production — most current approaches use Docker containers or cloud-hosted eval environments with non-trivial latency and dependency overhead. A WASM-based approach runs in-process with microsecond startup, making it practical for tools that need lightweight, untrusted code execution inline (datasette plugins, notebook agents, MCP tool implementations).

---

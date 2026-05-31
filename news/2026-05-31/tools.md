# Tools — 2026-05-31

## Claude Code v2.1.157 + v2.1.158 <a id="claude-code-2-1-157-158"></a>

**Source:** [Anthropic Release Notes via Releasebot](https://releasebot.io/updates/anthropic/claude-code) · **Type:** release · **Time (UTC):** May 31

Two releases shipped on May 31.

**v2.1.157 — Plugin scaffolding and agent dispatching**

- `claude plugin init <name>` scaffolds a new skill with autocomplete support, eliminating the previous manual directory setup.
- Plugins in `.claude/skills/` are now loaded automatically without requiring marketplace enrollment — local-only skills work out of the box.
- The `agent` field in `settings.json` is now honored for agent dispatching, enabling per-project agent configuration without passing flags.
- Mid-session worktree switching via `EnterWorktree` is now possible, avoiding session restarts when switching git worktrees.
- Fixes: image paste crashes, sandbox permission prompt loops, background session handling, terminal rendering glitches, tmux copy behavior, and the fullscreen session picker.

**v2.1.158 — Auto mode on Bedrock, Vertex, and Foundry**

- Auto mode (the mode that selects between Opus 4.7 and 4.8 based on task complexity and cost) is now available on AWS Bedrock, Google Vertex, and Azure Foundry deployments for Opus 4.7 and Opus 4.8.
- Enabled via environment variable: `CLAUDE_CODE_ENABLE_AUTO_MODE=1`.
- Previously required opt-in on the direct Anthropic platform; this brings parity to all three hyperscaler-hosted Claude endpoints.

**Why it matters:** Local plugin scaffolding removes friction for teams building project-specific tools without marketplace dependencies. Auto mode on cloud providers lets enterprise deployments use the same intelligent model-selection loop previously available only on direct Anthropic infrastructure.

---

## Komi-learn: continuous memory and self-improvement for coding agents <a id="komi-learn"></a>

**Source:** [GitHub: kurikomi-labs/komi-learn](https://github.com/kurikomi-labs/komi-learn) · **Type:** release · **Time (UTC):** May 31 (Show HN)

Komi-learn is a Python tool (MIT license, Python 3.10+) that automatically accumulates session learnings for Claude Code and Codex without requiring any manual save commands. It operates as a four-step background cycle:

1. **Recall** — at session start, loads context snippets relevant to the current task using keyword search (or optional local semantic recall with extras).
2. **Distill** — after the session, extracts durable lessons from the transcript (code style, stack preferences, working fixes).
3. **Curate** — merges overlapping lessons, archives outdated ones.
4. **Share** — optional community pool layer using GitHub-stored signed Markdown files (BLAKE3 hashing + Ed25519 signatures).

Secrets, machine-specific paths, one-off failures, and tool-breakage complaints are filtered out by a deterministic pre-check before distillation. The engine has no required dependencies; real signing and semantic recall are opt-in extras.

Install: `pip install komi-learn && komi-learn install`.

**Why it matters:** Coding agents currently have no memory beyond a single session's context window. Komi-learn is the first open-source tool to make Claude Code accumulate project-specific patterns automatically across sessions — filling the gap between ephemeral in-context learning and manual CLAUDE.md curation.

---

# Tools — 2026-05-24

## Claude Code v2.1.149 <a id="claude-code-v2-1-149"></a>

**Source:** [GitHub Releases](https://github.com/anthropics/claude-code/releases/tag/v2.1.149) · **Type:** update · **Time (UTC):** 2026-05-22 22:09

Version 2.1.149 is the largest maintenance release in the v2.1.x series, shipping 40+ fixes and improvements across UI, permissions, and enterprise configuration. Key changes:

- **`/usage` per-category breakdown** — the usage panel now splits token costs by skills, subagents, plugins, and MCP server calls rather than a single aggregate figure.
- **`/diff` keyboard navigation** — the detail view now responds to arrow keys, `j`/`k` vi bindings, `PgUp`/`PgDn`, `Space`, `Home`, and `End` without requiring a mouse.
- **GFM task-list rendering** — `- [ ]` and `- [x]` items in assistant responses render as styled checkboxes instead of plain bullets.
- **`allowAllClaudeAiMcps` managed setting** — enterprise admins can set this once to permit any MCP server hosted on `claude.ai` without per-server approval flows in the managed policy layer.
- **Security hardening** — fixes to permission boundary checks for PowerShell commands, Bash invocations, and git worktree operations that could bypass sandbox restrictions in multi-agent setups.
- **`find` macOS crash fix** — resolves a kernel interaction causing `find` to hang or crash on large directory trees on macOS.
- **`/feedback` context enrichment** — reports now include pre-compaction conversation context for more actionable bug reports.

**Why it matters:** The sandbox permission fixes for PowerShell and git worktrees close practical escape vectors relevant to anyone running Claude Code in multi-agent pipelines; `allowAllClaudeAiMcps` removes a significant deployment friction point for enterprise fleet rollouts of trusted MCP servers.

---

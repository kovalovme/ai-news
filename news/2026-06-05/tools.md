# Tools — 2026-06-05

## Claude Code v2.1.162 / v2.1.163 / v2.1.165 <a id="claude-code-2-1-162-165"></a>

**Source:** [Releasebot / Anthropic](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** Jun 4–5

Three Claude Code releases shipped in 48 hours. **v2.1.162** (June 4) adds `waitingFor` status output to `claude agents --json` so orchestration scripts can observe which downstream agent or tool a background session is blocked on; it also fixes Windows backslash path handling in permission rules and resolves a silent startup hang when config directories lack write permissions. **v2.1.163** (June 5) introduces version guardrails via `requiredMinimumVersion` and `requiredMaximumVersion` managed settings — Claude Code will refuse to start if its installed version falls outside the allowed range and will surface an upgrade prompt, enabling teams to enforce toolchain parity. Other v2.1.163 additions: a `/plugin list` command with `--enabled`/`--disabled` filters, a `c` shortcut in `/btw` that copies the raw markdown answer to the clipboard, and hooks support for `hookSpecificOutput.additionalContext` — allowing hooks to return feedback to Claude without marking the turn as an error. **v2.1.165** (June 5) is a reliability patch.

**Why it matters:** Version guardrails are the first enterprise-grade version-pinning mechanism in Claude Code, addressing the real-world problem of agentic pipelines silently degrading when team members run mismatched CLI versions.

---

## Cursor Canvas Design Mode & Context Usage Report <a id="cursor-canvas-design-mode"></a>

**Source:** [Releasebot / Cursor](https://releasebot.io/updates/cursor) · **Type:** update · **Time (UTC):** Jun 4, ~16:00

Cursor's June 4 release adds two productivity-focused features to its Canvas interface. **Design Mode** lets users annotate live UI elements directly in the canvas — clicking any rendered component opens an inline editing panel — shortcutting the text-description step when requesting iterative UI changes. **Context Usage Report** surfaces a token-usage breakdown across system prompts, tools, and skills as a persistent explorer pane; a "Debug with Agent" button lets Cursor analyze the breakdown and suggest context reductions. A June 3 companion release adds **Organizations for Enterprise** — a three-tier hierarchy (Organization → Teams → Groups) with per-group model access controls and spend limits that apply the most-permissive setting when users belong to multiple groups.

**Why it matters:** The context telemetry directly addresses developer confusion over escalating costs in agentic workflows — providing the token-attribution data needed to tune prompts and tool definitions before hitting billing thresholds.

---

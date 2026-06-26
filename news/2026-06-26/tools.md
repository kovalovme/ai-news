# Tools — 2026-06-26

## Claude Code 2.1.193 <a id="claude-code-2193"></a>

**Source:** [Anthropic Claude Code release notes](https://releasebot.io/updates/anthropic/claude-code) · **Type:** release · **Time (UTC):** June 26

The June 26 Claude Code release adds substantive auto-mode and MCP improvements:

- **Auto-mode shell classification:** New `autoMode.classifyAllShell` setting routes every Bash and PowerShell command through the classifier, not just novel ones — tightening the security model for unattended agent runs
- **Denial tracking:** Auto-mode denial reasons are now captured in transcripts and surfaced in the `/permissions` interface, giving operators audit visibility into what was blocked and why
- **Bash path autocomplete:** Live file-path completion within bash mode reduces command-construction errors during interactive sessions
- **MCP startup notices:** When an MCP server requires authentication, Claude Code shows a notice at startup rather than failing silently mid-task
- **Background agent fixes:** Resolved spurious operation cancellation when backgrounding, eliminated phantom subagent spawning, and added automatic memory cleanup for background agents

**Why it matters:** The `classifyAllShell` option is the key security upgrade — it closes a bypass where an attacker's payload could be crafted to resemble a previously approved command class. The denial tracking in `/permissions` gives security-conscious teams the audit trail they've been asking for.

---

## Claude Code 2.1.191 <a id="claude-code-2191"></a>

**Source:** [Anthropic Claude Code release notes](https://releasebot.io/updates/anthropic/claude-code) · **Type:** release · **Time (UTC):** June 25

- **`/rewind`:** Resume a conversation to the state immediately before `/clear` was executed — useful for recovering context after accidental resets without losing work
- **~37% CPU reduction:** Text update coalescing reduces CPU load during long streaming responses; measurably improves battery life and reduces thermal throttling on portable hardware
- **Streaming scroll fix:** Scroll position no longer jumps during long responses
- **MCP resilience:** Automatic retry with back-off for transient capability-discovery errors; auto-reconnect on 401/403 authentication failures rather than permanently marking a server unavailable

**Why it matters:** The CPU reduction is the practical headline for daily users. The `/rewind` command addresses a real workflow gap — accidental `/clear` during a long task was unrecoverable before this release.

---

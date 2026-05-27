# Tools — 2026-05-27

## Claude Code v2.1.152 <a id="claude-code-2-1-152"></a>

**Source:** [Claude Code Changelog](https://code.claude.com/docs/en/changelog) · [GitHub Releases](https://github.com/anthropics/claude-code/releases) · **Type:** release · **Time (UTC):** ~09:00

The largest Claude Code release since v2.1.149. Key additions:

**Code review workflow:** `/code-review --fix` now applies reuse, simplification, and efficiency findings directly to the working tree in one pass. `/simplify` is now an alias for the same command.

**Skill sandboxing:** Skills and slash commands can declare `disallowed-tools` in frontmatter to strip specific tools from the model while the skill is active — enabling sandboxed, auditable skill workflows without modifying the global tool list.

**Session and hook improvements:** `SessionStart` hooks can now trigger a skill rescan via `reloadSkills: true` (making newly-installed skills available in the same session without a restart) and set the session title via `hookSpecificOutput.sessionTitle`. A new `MessageDisplay` hook event lets hooks transform or suppress assistant message text as it is rendered — useful for filtering, redacting, or reformatting output in managed deployments.

**Plugin management:** New `pluginSuggestionMarketplaces` managed setting lets admins allowlist org-internal marketplaces for context-aware plugin suggestions. `claude plugin marketplace remove` now accepts `--scope user|project|local`.

**UX:** Auto mode no longer requires opt-in consent. Vim mode `/` in NORMAL opens reverse history search. A `--fallback-model` flag causes Claude Code to switch models rather than fail when the primary model is unavailable.

**Notable bug fixes:** terminal style-pool recycling for long sessions; MCP server deduplication by env-var key, not just command; remote MCP in egress-proxy sessions; stale plugin-registry entries causing `/doctor` errors; model-switch leaving stale thinking-block signatures in history.

**Why it matters:** The `disallowed-tools` frontmatter closes a gap where skills could accidentally expose dangerous tools (shell, file write) to untrusted prompts. The `MessageDisplay` hook enables enterprise use-cases like PII masking and compliance filtering without forking the tool. Auto mode without opt-in removes friction for first-time deployments.

---

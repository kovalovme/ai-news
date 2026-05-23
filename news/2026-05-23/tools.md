# Tools — 2026-05-23

## Claude Code v2.1.147 + v2.1.148 <a id="claude-code-2-1-147-148"></a>

**Source:** [Claude Code Changelog](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** 2026-05-21 (2.1.147), 2026-05-22 (2.1.148)

Version 2.1.147 ships three notable changes: pinned background sessions (`Ctrl+T` in `claude agents`) now survive idle periods, are restarted in-place to apply updates, and are only shed under memory pressure after non-pinned sessions; `/simplify` is renamed to `/code-review` and now accepts an effort level (e.g., `/code-review high`) and a `--comment` flag to post findings as inline GitHub PR comments; and a broad set of terminal, Windows, PowerShell, and plugin bugs are fixed. Version 2.1.148 (May 22) addresses a regression introduced in 2.1.147 that caused the Bash tool to return exit code 127 on every command for some users.

**Why it matters:** The `/code-review` rename and effort-level parameter make the built-in code review workflow more discoverable and controllable; the Bash exit-code regression in 2.1.147 would have silently broken any workflow that checks command exit status.

---

## Datasette Agent <a id="datasette-agent"></a>

**Source:** [Simon Willison's Weblog](https://simonwillison.net/2026/May/21/datasette-agent/) · **Type:** release · **Time (UTC):** 2026-05-21 ~09:00

Simon Willison released Datasette Agent, merging his LLM Python library with the Datasette database exploration tool after three years of parallel development. Users ask natural-language questions ("when did Simon most recently see a pelican?") and the agent generates and executes SQLite queries, returning both the answer and the underlying SQL. The demo runs on Gemini 3.1 Flash-Lite, chosen for cost and reliable SQL generation. An extensible plugin architecture ships at launch with three plugins: chart generation, image generation, and sandboxed code execution. Willison notes that recent open-weight models have become reliable enough at tool calls and SQL generation that this class of tool is now broadly buildable.

**Why it matters:** The plugin-first design means Datasette Agent can be extended into a general query-and-action surface over any structured data source; the lightweight model choice (Flash-Lite) keeps per-query cost in the fractions-of-a-cent range at scale.

---

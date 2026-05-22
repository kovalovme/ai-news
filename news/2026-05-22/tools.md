# Tools — 2026-05-22

## Claude Code v2.1.146 <a id="claude-code-2-1-146"></a>

**Source:** [Anthropic Changelog](https://code.claude.com/docs/en/changelog) · [Releasebot](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** May 21

Claude Code v2.1.146 shipped May 21 with three substantive changes:

- **`/simplify` renamed to `/code-review`** with an optional effort level parameter (`low`, `medium`, `high`). The rename better reflects the command's function — requesting a structured code review from the model — and the effort flag lets users trade review depth against latency. This follows the same effort-level pattern introduced for `/think` in v2.1.140.

- **Auto mode no longer suppresses `AskUserQuestion`** when the user or a skill explicitly relies on it. Previously, auto mode could silently skip clarification prompts when it judged it had enough context; the fix ensures skill-declared question flows are never bypassed.

- **Windows PowerShell tool fix** resolving "command line is invalid" errors that occurred when Claude Code passed certain Bash-style argument constructs to PowerShell on Windows. The bug affected users running Claude Code in PowerShell sessions (as opposed to WSL or Git Bash), causing tool calls to fail silently.

**Why it matters:** The `/code-review` rename with effort levels makes code review a first-class workflow rather than a convenience alias. For teams using Claude Code in CI — where a `low`-effort review at PR-time versus a `high`-effort review at merge-gate are meaningfully different interventions — the effort flag is directly actionable. The Windows PowerShell fix removes a blocker for Windows-native developers who were falling back to WSL.

---

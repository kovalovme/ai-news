# Tools — 2026-06-16

## datasette-agent 0.3a0: write SQL now requires explicit user approval <a id="datasette-agent-030"></a>

**Source:** [Datasette Blog](https://datasette.io/blog/2026/datasette-agent/) · **Type:** release · **Time (UTC):** June 15

Simon Willison released datasette-agent 0.3a0, adding an `execute_write_sql` tool that routes any data-modifying query through a mandatory approval step before execution. The `datasette agent chat` terminal mode gains matching approval support, with an `--unsafe` flag that auto-approves all actions for users who explicitly opt into fully autonomous operation. The 0.2a0 release (June 10) had introduced the foundational agent chat interface; 0.3a0 closes the gap between read-only and write capabilities safely.

**Why it matters:** The approval gate pattern — where agents can propose write operations but execute them only on human confirmation — is becoming a standard safety primitive in agent tooling. datasette-agent is an early concrete implementation of this pattern for database-level agents, relevant to anyone building read-write data agents on top of SQLite or Datasette.

---

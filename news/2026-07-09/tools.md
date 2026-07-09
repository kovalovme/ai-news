# Tools — 2026-07-09

## Claude Cowork — Web and Mobile Beta <a id="claude-cowork-web-mobile"></a>

**Source:** [TechCrunch](https://techcrunch.com/2026/07/07/the-coding-agent-wars-are-spilling-into-the-rest-of-the-office-claude-cowork/) · [9to5Mac](https://9to5mac.com/2026/07/07/anthropic-expanding-claude-cowork-to-mobile-and-web-details-here/) · **Type:** launch · **Time (UTC):** July 7–8

Anthropic extended Claude Cowork — previously desktop-only — to web and mobile platforms. The rollout begins as a beta on Max plan accounts and expands to other paid plans in coming weeks. Sessions sync across devices, so a task started on desktop can be monitored and output retrieved from phone. Cowork can also execute tasks in the background without any device active: users schedule the work, and Claude runs it autonomously. Chat and Cowork now share a single home tab on web and desktop (one sidebar, one search, one location for Projects and Artifacts). Anthropic extended its doubled Cowork usage limits through August 5 to mark the launch.

Alongside the announcement, Anthropic published usage data from 1.2 million anonymized Cowork sessions (May 11–31, 600K+ organizations). Business process and operations was the largest category (33.4%), followed by content creation (16.4%). Software engineering was a minority of sessions, counter to how Cowork has often been described externally.

**Why it matters:** The device-agnostic session model is a prerequisite for Cowork becoming a durable work product rather than a power-user feature. The usage data — showing ~83% of sessions are non-coding tasks — suggests Anthropic is validating a broader enterprise positioning.

---

## Claude Code — Chrome GA and Workflow Updates <a id="claude-code-chrome-ga"></a>

**Source:** [Anthropic Releasebot](https://releasebot.io/updates/anthropic/claude-code) · **Type:** update · **Time (UTC):** July 7–8

Anthropic marked Claude in Chrome as generally available and shipped several workflow improvements to Claude Code: background notifications (the agent pings when a long-running task completes), draft PR handoff (hands a work-in-progress pull request description back to the developer for review), improved session failover, and better session-state handling across interruptions. A `/dataviz` skill for chart and dashboard design guidance was also added.

**Why it matters:** Background notifications close a practical gap for long agentic runs — previously the only option was to keep the session open and watch. Draft PR handoff is a workflow primitive that enables human-in-the-loop review at the git integration layer.

---

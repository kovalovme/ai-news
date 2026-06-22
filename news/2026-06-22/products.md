# Products — 2026-06-22

## Claude platform: 90-minute global outage — third this month <a id="claude-outage-jun22"></a>

**Source:** [Anthropic Status](https://status.anthropic.com) · [status.claude.com incident lv35v0q9nsj2](https://status.claude.com/incidents/lv35v0q9nsj2) · **Type:** incident · **Time (UTC):** 00:37–02:06

At 00:37 UTC on June 22, Anthropic opened an investigation into elevated error rates affecting five models simultaneously: Opus 4.8, Opus 4.7, Opus 4.6, Sonnet 4.6, and Haiku 4.5. All Claude services were impacted: claude.ai, the Claude API (`api.anthropic.com`), Claude Code, and Claude Cowork. The root cause was identified at 01:11 UTC and a fix was deployed in a staged rollout. Recovery order: Opus 4.8 at 01:16, Haiku 4.5 at 01:33, Opus 4.7 at 01:56, with the incident marked fully resolved at 02:06 UTC. Duration: approximately 89 minutes. This is the third multi-model outage on the Claude platform in June 2026.

**Why it matters:** Three multi-model outages in one month is an above-average incident rate for Anthropic. The coincidence with the Fable 5 export-control suspension — which forced re-routing of traffic away from the platform's highest-capacity model — may be a contributing factor, though Anthropic has not stated this. Teams relying on Claude Code for CI/CD pipelines should ensure fallback routing to at least one non-Claude provider for outage resilience.

---

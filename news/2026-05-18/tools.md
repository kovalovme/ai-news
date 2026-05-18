# Tools — 2026-05-18

## Anthropic Agent SDK Credits: Third-Party Agents Reinstated with Usage Caps <a id="agent-sdk-credits"></a>

**Source:** [VentureBeat](https://venturebeat.com/technology/anthropic-reinstates-openclaw-and-third-party-agent-usage-on-claude-subscriptions-with-a-catch) · [GitHub Gist analysis](https://gist.github.com/MagnaCapax/d9177e35b355853f03c730dfcaa693ef) · **Type:** update · **Time (UTC):** May 13

Anthropic reversed an April 2026 policy that had banned third-party agent harnesses (such as the popular open-source OpenClaw framework) from using Claude subscriptions. The new system introduces a dedicated "Agent SDK credits" pool per plan: $20/month for Pro, $100/month for Max 5×, $400/month for Max 20×. Usage above those thresholds counts against standard per-token API pricing. The previous ban arose because some subscribers using heavily optimised autonomous agents were consuming hundreds of dollars of tokens per month on a $20 Pro plan. The reinstatement effective date for the new billing structure is June 15, 2026.

**Why it matters:** OpenClaw has a large community of developers running continuous coding and research agents against Claude subscriptions. The new policy restores programmatic access while shifting cost-of-inefficiency back to users — effectively ending the flat-rate model for high-volume agentic workloads. The developer community has broadly characterised this as a 12×–175× effective price increase for token-heavy workloads; engineers should audit their per-session token counts before June 15.

| Plan      | Agent SDK credit pool | Effective date |
|-----------|----------------------:|---------------|
| Pro       | $20 / month           | Jun 15, 2026  |
| Max 5×    | $100 / month          | Jun 15, 2026  |
| Max 20×   | $400 / month          | Jun 15, 2026  |

---

## OpenAI Codex Added to ChatGPT Mobile App <a id="codex-mobile"></a>

**Source:** [WinBuzzer](https://winbuzzer.com/2026/05/15/codex-is-now-in-the-chatgpt-mobile-app-xcxwbn/) · [OpenAI Developers](https://developers.openai.com/codex/changelog) · **Type:** release · **Time (UTC):** May 14

OpenAI shipped a Codex integration for the ChatGPT iOS and Android apps, available to all plans including Free and Go. The mobile app acts as a remote control for an active Codex session running on a paired Mac: users can review pending work, approve shell commands, steer threads, and monitor agentic progress from their phone without interrupting the desktop session. Mobile pairing currently requires a macOS host; Windows mobile pairing is listed as "coming soon." A companion blog post ([OpenAI](https://openai.com/index/building-codex-windows-sandbox/)) published May 14 detailed the security design of the Windows sandbox, which uses a dedicated elevated binary, firewall-backed network blocking, and tighter file-write controls.

**Why it matters:** Making Codex sessions observable and steerable from mobile removes a key friction point for developers who want to kick off long-running coding tasks and check in without being at a desk. The Windows sandbox documentation is also relevant for teams evaluating enterprise Codex deployments on Windows infrastructure.

---

# Products — 2026-05-24

## OpenAI macOS Code-Signing Certificate Revocation — June 12 Deadline <a id="openai-macos-cert-revocation"></a>

**Source:** [OpenAI — TanStack supply chain response](https://openai.com/index/our-response-to-the-tanstack-npm-supply-chain-attack/) · **Type:** update · **Time (UTC):** ~2026-05-22

Following the TanStack npm supply-chain attack in which the TeamPCP threat group compromised two OpenAI developer machines and harvested macOS code-signing credentials, OpenAI has rotated its macOS signing certificates for all desktop and CLI products. Old certificates will be revoked on **June 12, 2026**; after that date, macOS Gatekeeper will block any application signed with the prior certificate from launching. Affected products requiring an update before June 12: **ChatGPT Desktop, Codex App, Codex CLI, Atlas**. Users on the latest version from the App Store or official download page are already on the new certificate.

**Why it matters:** This is a concrete action item for engineers and teams using any of the four affected OpenAI macOS applications — failure to update will cause a hard launch block on June 12, 2026. Note that the GitHub/Nx Console breach covered on 2026-05-21 is a separate but related incident in the same ongoing TeamPCP supply-chain campaign.

---

# Models — 2026-07-02

## Kimi K2.7 Code available in GitHub Copilot <a id="kimi-k27-copilot"></a>

**Source:** [GitHub Changelog](https://github.blog/changelog/2026-07-01-kimi-k2-7-is-now-available-in-github-copilot/) · **Type:** integration · **Time (UTC):** Jul 01

Moonshot AI's Kimi K2.7 Code is now selectable in GitHub Copilot's model picker, hosted by GitHub on Microsoft Azure — the first open-weight model to enter Copilot's roster. The model uses a Mixture-of-Experts architecture with 1T total parameters and 32B active per token (384 experts, 8 selected per forward pass), a 256K token context window, native multimodality via MoonViT, and native INT4 quantization. Weights ship on HuggingFace under a Modified MIT license. GitHub is rolling out access gradually while monitoring quality and performance; business and enterprise admins must explicitly enable the model for their organizations.

**Why it matters:** Adding an open-weight alternative to Copilot's proprietary-model-only picker gives engineering teams a lower-cost, sovereignty-friendly option ($0.95/MTok cache-miss input, $4/MTok output) without leaving the Copilot workflow. It's also a signal that GitHub/Microsoft see open-weight model competition as a feature rather than a threat to the platform.

| Stat | Value |
|------|-------|
| Total parameters | 1T (MoE) |
| Active parameters | 32B per token |
| Context window | 256K tokens |
| Input price (cache-miss) | $0.95/MTok |
| Output price | $4.00/MTok |
| License | Modified MIT |

---

## ByteDance Seed 2.0 Model Card <a id="seed20-model-card"></a>

**Source:** [arXiv 2607.00248](https://arxiv.org/abs/2607.00248) · **Type:** paper · **Time (UTC):** Jul 02

ByteDance's Seed team published a formal model card for the Seed 2.0 series on arXiv, documenting the model's design philosophy, evaluation approach, and capabilities. The paper targets two capability clusters: long-tail knowledge (uncommon or specialized information that most models miss) and complex instruction following across multi-step tasks. Rather than relying on standard benchmarks alone, the team constructed a forward-looking evaluation system grounded in realistic user scenarios. Seed 2.0 is positioned as the precursor to Seed 2.1 Pro (the agent-capable coding model covered in the June 28 digest).

**Why it matters:** Model card papers that make evaluation methodology explicit — especially those that acknowledge the limitations of standard benchmarks — help the broader research community calibrate comparisons and reproduce results.

---

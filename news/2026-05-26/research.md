# Research — 2026-05-26

## Calif.io + Mythos: first public macOS M5 kernel LPE with MIE enabled <a id="califio-macos-kernel-lpe"></a>

**Source:** [Calif.io blog](https://blog.calif.io/p/first-public-kernel-memory-corruption) · [Apple security note (CVE-2026-28952)](https://support.apple.com/en-us/127115) · **Type:** security disclosure · **Time (UTC):** ~00:00 May 26

Researchers Bruce Dang, Dion Blazakis, and Josh Maine at Calif.io, working with Anthropic Research and Mythos Preview, disclosed what they claim is the first public data-only kernel local privilege escalation chain targeting macOS 26.4.1 on Apple M5 hardware with Memory Integrity Enforcement (MIE) enabled. The exploit chain was developed over five days (April 25–May 1); Mythos rapidly identified the underlying kernel integer overflow (CVE-2026-28952) because the bug class was familiar from training data, but human expertise proved essential to build the actual MIE bypass. Apple's security note credits the finding to "Calif.io in collaboration with Claude and Anthropic Research" and patched the integer overflow in macOS Tahoe 26.5 (May 11, 2026). Full technical details remain withheld pending broader patch adoption.

**Why it matters:** The disclosure concretely demonstrates that AI-augmented small teams can achieve what previously required large, well-resourced security groups — finding novel exploit chains in Apple's hardened hardware — and arrived the same week as Anthropic's Glasswing one-month update showing 10,000+ zero-days across critical software.

```mermaid
flowchart LR
    A[Mythos Preview\nidentifies bug class] --> B[CVE-2026-28952\nkernel integer overflow]
    B --> C[Human researchers\nbuild MIE bypass chain]
    C --> D[Full kernel LPE\non macOS 26.4.1 M5]
    D --> E[Patched in\nmacOS Tahoe 26.5\nMay 11]
```

---

## WorldReasonBench: stress-testing video generators as world-state predictors <a id="worldreasonbench"></a>

**Source:** [arXiv 2605.10434](https://arxiv.org/abs/2605.10434) · **Type:** paper + benchmark · **Time (UTC):** May 26

A team from LongCat (Meituan) released WorldReasonBench, a 436-case benchmark evaluating whether video generation models can function as genuine world simulators — predicting physically and logically consistent future states — rather than producing aesthetically smooth but physically implausible sequences. The benchmark covers four reasoning dimensions and is evaluated via structured QA annotations aligned with human judgement. The authors also release WorldRewardBench, a 6,000-pair preference dataset for training reward models that penalize physical inconsistency. Key finding: current frontier video generators consistently produce visually plausible but physically wrong outputs, exposing a large gap between perceptual quality and world-model fidelity.

**Why it matters:** As video world models are adopted for robotics simulation and autonomous agents, distinguishing aesthetic quality from physical fidelity becomes safety-critical; this benchmark provides a concrete, reproducible evaluation framework for that distinction.

---

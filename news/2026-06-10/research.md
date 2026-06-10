# Research — 2026-06-10

## SearchSwarm: Delegation Intelligence in Agentic LLMs <a id="searchswarm"></a>

**Source:** [arxiv 2606.09730](https://arxiv.org/abs/2606.09730) · **Type:** paper · **Time (UTC):** 2026-06-08

SearchSwarm addresses a fundamental bottleneck in long-horizon agentic research: a single LLM exhausts its context window before completing complex multi-step tasks. The paper proposes training for "delegation intelligence" — a main agent learns to decompose queries, dispatch subtasks to sub-agents, and integrate only their summarized results. Because naturally occurring text rarely contains explicit delegation decisions, the authors built a guidance harness to generate high-quality delegation trajectories, then used those trajectories as supervised fine-tuning data to internalize the skill into model weights. The resulting SearchSwarm-30B-A3B achieves 68.1 on BrowseComp and 73.3 on BrowseComp-ZH, best among models of comparable scale. Model weights, harness, and training data are committed to open release.

**Why it matters:** Most agentic frameworks hard-code orchestration logic in scaffolding, which doesn't transfer across task types. Baking delegation into model weights means the model generalizes task decomposition without requiring task-specific routing rules. The planned open release will let the community iterate on the harness-guided SFT approach.

---

## The Self-Correction Illusion: LLMs Correct Others but Not Themselves <a id="self-correction-illusion"></a>

**Source:** [arxiv 2606.05976](https://arxiv.org/abs/2606.05976) · **Type:** paper · **Time (UTC):** 2026-06-04

Kuan-Yen Chen, Fang-Yi Su, and Jung-Hsien Chiang show that when an LLM makes an error in its own reasoning chain it rarely self-corrects, but the identical erroneous claim presented in an external message triggers correction at a rate 23–93 percentage points higher. Testing across 13 model-domain combinations (7 model families, 3 domains, 30 tasks each), the effect is statistically significant in 10 of 13 cells (p<0.001). Keeping the error byte-identical and varying only the role label (own output vs. external input) confirms the asymmetry is a chat-template artifact, not a content or capability limit. A prompt-structure intervention — reframing the model's own prior output as a user or tool message before asking for critique — recovers correction capability with no training or model modification.

**Why it matters:** Self-critique loops are a widely deployed agentic reliability pattern; this paper explains why they systematically underperform and provides a zero-training fix: reformat the model's prior output under a different role label before asking it to critique. Engineers using CoT critique or "check your work" prompts should test whether the role-reframing intervention improves their pipeline.

---

## Strained Coherence: A Pre-Failure Signal in Coding Agent Trajectories <a id="strained-coherence"></a>

**Source:** [arxiv 2606.07889](https://arxiv.org/abs/2606.07889) · **Type:** paper · **Time (UTC):** 2026-06-05

Marut Pandya, Kasey Zhang, and Baiqing Lyu identify a failure mode they call strained coherence: a coding agent verbally acknowledges a problem in its execution trajectory but then acts against that acknowledgment anyway. They built a Claude Sonnet 4.6 judge to detect these spans in complete execution traces, achieving 94% precision (vs. 88% for a baseline lexical detector). Trajectories flagged for strained coherence failed at a 94% rate, compared to 46% for unflagged ones — a 47-point gap (p=0.003). The initial flag appears at a median of 83–84% through execution, providing an actionable early-exit signal. Primary evaluation used 44 Terminal-bench-2 trajectories (Qwen3.5-35B), with directionally consistent replication on Gemma4-31B.

**Why it matters:** A 94%-precision early-exit signal that fires at ~84% of execution length means agentic harnesses can abandon and restart failing tasks before consuming the final ~16% of tokens — a direct reliability and cost improvement for long-horizon coding agents. The judge approach is lightweight: a standard prompt to an existing model, no fine-tuning required.

---

## KAN on FPGA: Sub-Microsecond Inference via Kolmogorov-Arnold Networks <a id="kan-fpga"></a>

**Source:** [Aarush Gupta blog](https://aarushgupta.io/posts/kan-fpga/) · KANELÉ (FPGA 2026 Best Paper) · **Type:** paper + implementation · **Time (UTC):** —

Aarush Gupta published a blog post on deploying Kolmogorov-Arnold Networks (KANs) to FPGAs for ultrafast inference, building on KANELÉ, which won the Best Paper Award at FPGA 2026. Unlike MLPs, KANs place learnable 1D B-spline functions on edges rather than fixed nonlinearities on nodes — a structure that maps naturally to FPGA look-up tables (LUTs) with efficient discretization. The KANELÉ implementation achieves forward and backward passes in sub-microsecond latency with fully on-chip parameter updates, 3–4 orders of magnitude faster than equivalent host–accelerator solutions. The work is specifically targeted at domains requiring microsecond latencies — high-energy physics triggers, plasma control, and real-time signal processing — not language models.

**Why it matters:** For ML practitioners building time-critical scientific or industrial embedded systems, KAN deployment to FPGAs is now a documented, award-validated path to sub-microsecond inference and online learning. The FPGA Best Paper recognition and 220 HN points suggest adoption in scientific computing pipelines in the near term.

---

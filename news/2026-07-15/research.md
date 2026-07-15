# Research — 2026-07-15

## Solving 20 Erdős Problems with 20 Parallel Codex Accounts <a id="erdos-codex-parallel"></a>

**Source:** [starfleetmath.com](https://starfleetmath.com) · [Hacker News (128 pts)](https://news.ycombinator.com/item?id=48914646) · **Type:** research · **Time (UTC):** —

A researcher published proofs for 20 problems from the Erdős problem database using a custom parallelization harness over 20 Codex (GPT-5.6 Sol) accounts. The setup pulls OAuth refresh tokens from each account into a custom broker, which mints short-lived access tokens per request and load-balances across the pool, together with dedicated 60-vCPU server support for computationally intensive steps. All proofs are formalized in Lean 4, providing machine-checkable verification. The generated proofs pass Lean's kernel, though commenters in the HN thread note the accompanying human-readable proof summaries are opaque — dense with formal notation and lacking the intuition-building prose that mathematicians expect from a useful writeup.

This work builds on a trend that accelerated sharply in late 2025: AI contributions to open Erdős problems grew from a handful to dozens in under a year, driven first by GPT-5 literature-review assistance, then by formalization systems like Harmonic's Aristotle and DeepMind's AlphaProof, and now by autonomous parallel proof search.

**Why it matters:** Formal verification in Lean 4 distinguishes this from earlier AI-assisted math claims that required peer review before trust. The OAuth-broker approach to scaling API access is a practical technique that other researchers are likely to replicate. The remaining open question is whether the proofs generalize insights humans can act on, or whether they are certificate-first outputs that verify a statement without explaining it.

---

## LeMario: JEPA World Model Trained on Super Mario Bros <a id="lemario-jepa"></a>

**Source:** [benjamin-bai.com](https://www.benjamin-bai.com/projects/lemario) · [Hacker News (91 pts)](https://news.ycombinator.com/item?id=48913763) · [arXiv 2605.26379](https://arxiv.org/abs/2605.26379) · **Type:** research · **Time (UTC):** —

Benjamin Bai published LeMario, a joint-embedding predictive architecture (JEPA) world model trained on Super Mario Bros gameplay. A lightweight linear probe trained on the model's latent representations recovers Mario's emulator-level (x, y) coordinates with R² = 0.997 and a mean absolute error of 9.30 pixels for horizontal position — indicating the latent space encodes positional structure without it being explicitly supervised. Planning uses the Cross-Entropy Method (CEM): the agent samples candidate action sequences, rolls each through the world model in latent space, ranks them by predicted goal distance, and executes the best. The probe only affects ranking, not the world model's dynamics. This is a low-resource project demonstrating that JEPA-style self-supervised objectives can build spatially coherent game world models from raw pixels.

**Why it matters:** JEPA architectures — first popularized by Yann LeCun — are increasingly competitive with generative approaches for world modeling because they predict in latent space rather than pixel space, avoiding the expensive reconstruction objective. LeMario is a clean small-scale proof that JEPA latent spaces can be sufficient for CEM-based model-predictive control, which has direct implications for robot learning research where dense pixel reconstruction is prohibitively expensive.

---

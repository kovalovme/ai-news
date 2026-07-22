# Tools — 2026-07-22

## Nvidia Vera CPU: White Paper and SPEC CPU 2026 Benchmarks <a id="nvidia-vera-cpu"></a>

**Source:** [Tom's Hardware](https://www.tomshardware.com/pc-components/cpus/nvidia-spills-the-beans-on-vera-cpu-spec-benchmarks-revealed-olympus-architecture-detailed-and-more) · [NVIDIA Developer Blog](https://developer.nvidia.com/blog/inside-nvidia-vera-cpu-olympus-cores-built-for-maximum-single-threaded-performance-in-agentic-ai/) · **Type:** release · **Time (UTC):** Jul 21 ~21:00

Nvidia published a Vera CPU white paper alongside estimated SPEC CPU 2026 SPECrate integer results comparing Vera against AMD Epyc 9755 in dual-socket configurations. Vera is built on the custom Olympus core, tuned for single-threaded performance and memory bandwidth over raw core density — 88 Olympus cores per socket, 176 SMT threads, and a 164 MB unified L3 cache on a monolithic die.

| Benchmark | Vera (dual-socket) | Epyc 9755 (dual-socket) |
|---|---|---|
| SPECrate int base (estimated) | 925 | 898 |
| Margin | +3.0% | — |

Results are not official SPEC submissions; Vera runs in a reference system not yet broadly available. Nvidia positions Vera as infrastructure for agentic AI workloads where single-thread throughput is the bottleneck — not HPC or database parallelism.

**Why it matters:** A credible custom CPU from Nvidia closes a strategic gap: data centers can now buy CPU + GPU from a single vendor optimized for agent-dense inference, reducing the latency overhead of CPU-GPU data movement on agentic tasks.

---

## Anthropic Agent-Memory API: New Default Behavior <a id="anthropic-agent-memory-default"></a>

**Source:** [Anthropic Developer Platform changelog](https://releasebot.io/updates/anthropic/claude-developer-platform) · **Type:** update · **Time (UTC):** Jul 22 00:00

The `agent-memory-2026-07-22` beta header — which changes memory-store list responses to a stable server-defined order and tightens validation of `depth`, `path_prefix`, and `cursor` parameters — became the default for all Anthropic SDK clients today. The previous `managed-agents-2026-04-01` header is superseded. Applications that pass memory `order` parameters or depend on insertion-order listing need to audit and re-test; all Anthropic-maintained SDKs send the new header automatically.

**Why it matters:** Stable ordering removes a class of non-determinism that has caused subtle bugs in agent memory retrieval when server load-balancing changed shard assignments; the tighter cursor validation eliminates silent pagination errors.

---

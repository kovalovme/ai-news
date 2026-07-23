# Products — 2026-07-23

## AMD Advancing AI 2026: Helios Rack, MI455X, and EPYC Venice Launch <a id="amd-advancing-ai-2026"></a>

**Source:** [wccftech — Helios/MI455X](https://wccftech.com/amd-helios-ai-rack-mi455x-6th-gen-epyc-challenging-nvidia/) · [guru3d — EPYC Venice](https://www.guru3d.com/story/amd-unveils-256core-epyc-venice-for-helios-mi455x-ai-racks-platform/) · [tech-insider — Helios pricing](https://tech-insider.org/amd-advancing-ai-2026/) · **Type:** launch · **Time (UTC):** 2026-07-23 16:30 (Lisa Su keynote 09:30 PT)

At its Advancing AI 2026 conference in San Francisco, AMD officially launched the Helios AI rack, the Instinct MI455X GPU, and the sixth-generation EPYC Venice CPU. Helios integrates 72 MI455X accelerators across 18 liquid-cooled compute trays (four GPUs + one Venice CPU per tray) with a proprietary fabric delivering 1.4 PB/s aggregate memory bandwidth. Each rack lists at approximately $5.25 million and draws 225–245 kW. Early customers named include Microsoft Azure and Oracle.

The MI455X GPU carries 432 GB of HBM4 at 19.6 TB/s memory bandwidth and delivers 40 PFLOPs of FP4 compute per card. EPYC Venice uses TSMC 2nm (Zen 6 microarchitecture) with up to 256 cores and 512 threads across eight compute dies and two I/O dies. The combined Helios rack peaks at 2.9 ExaFLOPS FP4 (training/inference) and 1.4 ExaFLOPS FP8 (training). AMD claims Helios prices 40% above NVIDIA's second-generation Rubin rack on a per-card basis and is targeting the same customer segment.

**Why it matters:** The MI455X's 432 GB of on-chip HBM4 per accelerator — more than double NVIDIA H200's 141 GB — is the primary competitive lever AMD is using against the Rubin platform. For inference workloads where memory capacity constrains achievable batch size and model quality, this is a meaningful architectural difference rather than raw FLOPS positioning.

| Spec | AMD Helios / MI455X |
|------|--------------------:|
| GPUs per rack | 72 × MI455X |
| Total HBM4 | 31 TB |
| Aggregate bandwidth | 1.4 PB/s |
| FP4 throughput | 2.9 ExaFLOPS |
| FP8 throughput | 1.4 ExaFLOPS |
| Power per rack | 225–245 kW |
| Rack price | ~$5.25 M |
| MI455X HBM4 per GPU | 432 GB at 19.6 TB/s |
| EPYC Venice cores | 256 (Zen 6, TSMC 2nm) |

---

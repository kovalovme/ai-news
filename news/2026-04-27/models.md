# Models — 2026-04-27

## GLM-5.1 tops SWE-Bench Pro with MIT license, no NVIDIA hardware <a id="glm-5-1"></a>

**Source:** [Z.ai / The Decoder](https://the-decoder.com/zhipu-ais-glm-5-1-can-rethink-its-own-coding-strategy-across-hundreds-of-iterations/) · **Type:** release · **Time (UTC):** Apr 7 —

Z.ai (formerly Zhipu AI) released GLM-5.1, a 754B-parameter Mixture-of-Experts model, scoring 58.4% on SWE-Bench Pro to claim the global #1 spot ahead of GPT-5.4 (57.7%) and Claude Opus 4.6 (57.3%). The model is available on Hugging Face under the MIT license. Distinctively, it was trained entirely on 100,000 Huawei Ascend 910B chips with no NVIDIA hardware. GLM-5.1 supports an autonomous "plan → execute → test → fix → optimize" loop running for up to eight hours without human intervention.

**Why it matters:** The first frontier-scale open coding model trained on Ascend silicon demonstrates that NVIDIA-independent paths to top-tier performance are maturing. The MIT license (no royalty, commercial-use permitted) removes the friction that Apache 2.0 restrictions introduced for some enterprise deployments.

| Benchmark | GLM-5.1 | GPT-5.4 | Claude Opus 4.6 |
|---|---|---|---|
| SWE-Bench Pro | **58.4%** | 57.7% | 57.3% |
| Terminal-Bench 2.0 | 63.5% | — | — |
| CyberGym | 68.7% | — | — |
| BrowseComp | 68.0% | — | — |

---

## NVIDIA Ising: first open AI model family for quantum computing <a id="nvidia-ising"></a>

**Source:** [NVIDIA Newsroom](https://nvidianews.nvidia.com/news/nvidia-launches-ising-the-worlds-first-open-ai-models-to-accelerate-the-path-to-useful-quantum-computers) · **Type:** release · **Time (UTC):** Apr 14 —

NVIDIA launched Ising, an open model family targeting two distinct quantum-computing bottlenecks. Ising Calibration is a 35B-parameter vision-language model trained on multi-modality qubit data that automates quantum processor calibration, outperforming Gemini 3.1 Pro, Claude Opus 4.6, and GPT-5.4 on the new QCalEval benchmark. Ising Decoding is a 3D CNN framework for real-time quantum error correction (QEC), running 2.5× faster and achieving 3× higher accuracy than traditional decoders. Early adopters include Fermilab, Harvard SEAS, IQM Quantum Computers, Lawrence Berkeley National Lab, and the UK National Physical Laboratory.

**Why it matters:** Classical simulation of quantum error correction is the primary wall preventing scale-up of fault-tolerant quantum processors. Offloading that decode loop to a trained model while running on GPU clusters may unblock near-term error-corrected experiments that are currently bottlenecked on decoding latency.

---

## Gemini Robotics-ER 1.6: Boston Dynamics Spot reads industrial gauges autonomously <a id="gemini-robotics-er-1-6"></a>

**Source:** [Google DeepMind](https://deepmind.google/blog/gemini-robotics-er-1-6/) · **Type:** release · **Time (UTC):** Apr 14 —

Google DeepMind released Gemini Robotics-ER 1.6, upgrading its embodied-reasoning model with significantly improved spatial reasoning, multi-view understanding, and a new "instrument reading" capability discovered through collaboration with Boston Dynamics. Spot robots in industrial facilities can now autonomously read pressure gauges, thermometers, and digital readouts during inspection rounds. The model shows measurable gains over its predecessor (ER 1.5) on pointing, counting, and success-detection tasks. It is available to developers through the Gemini API and Google AI Studio starting April 14.

**Why it matters:** Instrument reading closes a long-standing gap in unstructured industrial inspection: robots could navigate and manipulate objects before, but required human verification of analog readouts. Integrating this natively in the foundation model removes a custom-vision-model dependency that previously required per-instrument fine-tuning.

---

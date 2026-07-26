# Models — 2026-07-26

## Inflect-Micro-v2: complete TTS in 9.36M parameters <a id="inflect-micro-v2"></a>

**Source:** [Hugging Face — owensong/Inflect-Micro-v2](https://huggingface.co/owensong/Inflect-Micro-v2) · **Type:** release · **Time (UTC):** ~08:00

Inflect-Micro-v2 is a text-to-waveform speech synthesis model with 9.36M deployable parameters (37.53 MB FP32). It generates 24 kHz mono English audio from a fixed synthetic voice with no external model dependencies at inference time. The architecture is VITS-family end-to-end with a phoneme frontend and neural waveform decoder.

**Why it matters:** The model achieves 6.28× real-time throughput on a 4-thread CPU with 66.2% human preference in blind listening tests (21 wins, 10 losses, 3 ties) and a UTMOS22 naturalness score of 4.395 — credible quality at a footprint small enough for microcontroller-class edge deployment. Semantic word error rate sits at 3.99% on a two-ASR consensus protocol. Reached HN front page with 114 points.

| Metric | Value |
|--------|-------|
| Parameters | 9.36M |
| File size (FP32) | 37.53 MB |
| Output | 24 kHz mono |
| CPU real-time factor | 6.28× (4 threads) |
| Human preference (blind) | 66.2% |
| UTMOS22 naturalness | 4.395 |
| Semantic WER | 3.99% |

---

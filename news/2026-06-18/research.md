# Research — 2026-06-18

## OpenAI LifeSciBench: 750-Task Expert-Authored Life Science Benchmark <a id="lifescibench"></a>

**Source:** [OpenAI — LifeSciBench](https://openai.com/index/introducing-life-sci-bench/) · [OpenAI — GPT-Rosalind new capabilities](https://openai.com/index/introducing-new-capabilities-to-gpt-rosalind/) · [MarkTechPost](https://www.marktechpost.com/2026/06/17/openai-releases-lifescibench-a-750-task-benchmark-grading-ai-models-on-real-life-science-research-with-expert-written-rubric/) · **Type:** benchmark release · **Time (UTC):** Jun 17

OpenAI released LifeSciBench, an expert-authored benchmark consisting of 750 tasks across seven life science research domains: genomics, medicinal chemistry, computational biology, drug discovery, clinical science, translational science, and regulatory affairs. Tasks were written and reviewed by 173 PhD-level scientists with biotechnology or pharmaceutical industry experience. Around 79% of tasks require multiple reasoning or decision-making steps averaging four steps each, making it more representative of actual research workflows than single-shot Q&A benchmarks. Evaluation uses expert-written rubrics rather than multiple-choice or string-match scoring.

OpenAI also released an updated demo pairing GPT-5.4 with Molecule.one to complete a near-autonomous drug-discovery loop: the system reviewed existing studies, proposed hypotheses, designed synthetic experiments, and interpreted results for a key drug-making reaction over a 2.5-month project. Human chemists verified and wrote up the findings in the final half month.

**Why it matters:** LifeSciBench provides a publicly reproducible signal for how frontier models perform on actual scientific research tasks — a domain where benchmark contamination risk is lower than coding or math. The Molecule.one demo demonstrates a concrete timeline compressing a research-loop step from years to weeks.

---

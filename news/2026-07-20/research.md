# Research — 2026-07-20

## AI advice collapses accuracy and inflates confidence — PsyArXiv preprint <a id="ai-advice-accuracy"></a>

**Source:** [The Next Web](https://thenextweb.com/news/ai-advice-suppresses-critical-thinking-wrong-answers-study) · [PsyArXiv preprint](https://osf.io/preprints/psyarxiv/5y6m4_v1) · **Type:** paper · **Time (UTC):** Jul 19 (335 HN pts)

Researchers Valerio Capraro (University of Milano-Bicocca), Chiara Marcoccia (École Normale Supérieure), and Walter Quattrociocchi (Sapienza University of Rome) ran a controlled experiment where participants answered trivia questions about visual details in films — a domain where Claude 3.5 Flash systematically fails. The choice of a model known to err on the task was deliberate: it isolates the behavioral effect of AI availability from the confound of participants correctly relying on a reliable tool.

With AI access, participants' willingness to say "I don't know" collapsed from 44% to 3%; accuracy dropped from 27% to 9%; and stated confidence rose from 30% to 76%. Adding financial incentives for correct answers improved results only modestly. Capraro's framing: "the mere availability of AI suppresses the cognitive habit of recognising what you do not know."

**Why it matters:** The finding is mechanistically distinct from "AI gives wrong answers that people believe" — it shows AI availability suppresses metacognitive awareness independently of whether the AI is actually right. UI patterns that surface uncertainty estimates, require users to answer first before seeing AI output, or explicitly prompt self-assessment may need behavioral validation against this baseline, not just accuracy benchmarks.

| Condition | "I don't know" | Accuracy | Confidence |
|-----------|:--------------:|:--------:|:----------:|
| No AI     | 44%            | 27%      | 30%        |
| AI available | 3%          | 9%       | 76%        |
| AI + monetary incentive | 8% | 16%  | ~65%       |

---

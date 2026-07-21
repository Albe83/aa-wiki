---
type: concept
---

# AA-Omniscience

AA-Omniscience is a knowledge and hallucination benchmark developed by Artificial Analysis. It tests models on 6,000 questions across 42 topics, measuring both factual accuracy and hallucination rate. In the AA Intelligence Index v4.1, it contributes a combined 12% weight, split 2:1 between Accuracy (8%) and Non-Hallucination Rate (4%). It is the most broadly used evaluation across AA's Capability Indices, appearing in all 6 industry indices with different topic-specific knowledge slices.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Core evaluation in the Intelligence Index v4.1, described as knowledge and hallucination benchmark | 2026-07-21 |
| [[sources/capability-indices]] | Component in all 6 Industry Indices, with topic-specific knowledge slices per industry | 2026-07-21 |

## Key details

### Dataset
6,000 questions covering 42 topics across broad domains:
- Business
- Humanities
- Health
- Law
- Software Engineering
- Science and Mathematics

### AA-Omniscience Index scoring
The proprietary AA-Omniscience Index uses a ternary scoring approach:
- **Correct answers** are rewarded
- **Hallucinations** (confidently incorrect answers) are penalized
- **Abstentions** (model declines to answer) are neutral

This incentivizes models to be both knowledgeable and honest about their limitations.

### Intelligence Index decomposition
For the Intelligence Index, AA-Omniscience is split into two components:
- **Accuracy component (8%):** measures correct answer rate
- **Non-Hallucination Rate (4%):** measures the proportion of answers that are either correct or abstained (i.e., not hallucinated)

The 2:1 ratio (accuracy : non-hallucination) reflects AA's emphasis on correctness while still penalizing confident falsehoods.

### Grading
Graded by **Gemini 3 Flash Preview (Reasoning)** as the automated judge.

### Role in Capability Indices
AA-Omniscience is the most versatile component, appearing in all 6 Industry Indices with topic-specific slices:
- Finance & Accounting: 30% Business Knowledge + 5% Non-Hallucination
- Strategy & Ops: 30% Business Knowledge
- Legal: 35% Legal Knowledge + 10% Non-Hallucination
- Healthcare & Medical: 35% Medical & Health Knowledge + 15% Non-Hallucination
- Engineering: 35% Engineering Knowledge
- Economics: 35% Economics Knowledge

Healthcare places the highest weight on Non-Hallucination (15%), reflecting the safety-critical nature of medical information.

## Relationships
- [[concepts/intelligence-index]] — 12% total weight (8% Accuracy + 4% Non-Hallucination)
- [[concepts/capability-indices]] — the most cross-cutting component, appearing in all 6 Industry Indices

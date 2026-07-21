---
type: concept
---

# GPQA Diamond

Graduate-level Google-Proof Q&A benchmark for evaluating scientific knowledge and reasoning. The Diamond subset consists of **198 questions** across biology, physics, and chemistry — selected as the highest-quality subset of the full GPQA dataset (448 questions total). The Diamond designation means questions where **experts answer correctly and non-experts answer incorrectly**, maximizing discriminative power. The format is **4-option multiple choice**, and evaluation uses regex-based answer extraction with pass@1 scoring.

GPQA Diamond contributes **6%** weight to the [[concepts/intelligence-index]] v4.1 (under the Scientific Reasoning category, alongside HLE at 12% and CritPt at 6%).

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | GPQA Diamond as a component of the Intelligence Index, Diamond subset definition, scoring mechanics | 2026-07-21 |

## Key details

- **Questions:** 198 (Diamond subset of 448 total)
- **Domains:** Biology, physics, chemistry
- **Format:** 4-option multiple choice
- **Repeats:** 5
- **Scoring:** Pass@1 — aggregated across all 5 repeats × 198 questions
- **Answer extraction:** Regex-based — extracts the model's letter choice (A/B/C/D) from the response
- **Paper:** <https://arxiv.org/abs/2311.12022>
- **Dataset source:** <https://github.com/openai/simple-evals/blob/main/gpqa_eval.py>

### Diamond Subset Definition
- Curated by the original authors as the highest quality subset
- Both experts answer correctly on these questions
- The majority of non-experts answer incorrectly
- Maximizes discriminative power between capable and weaker models
- 198 questions selected from the full 448-question GPQA dataset

### Multiple Choice Prompting
The evaluation uses a standardized multiple-choice prompt template. The regex extraction pattern looks for answer letters (A, B, C, D) in standard formats — answer choices in parentheses, standalone letters, or explicit answer indicators. If the regex fails to extract a valid answer, the question is scored as incorrect.

### Testing Parameters
- **Temperature:** 0 (non-reasoning), 0.6 (reasoning)
- **Max output tokens:** 16,384 (non-reasoning) or maximum allowed (reasoning)
- **Error handling:** Up to 30 retry attempts on API failures

## Relationships
- [[concepts/intelligence-index]] — GPQA Diamond contributes 6% weight to the Intelligence Index v4.1 (Scientific Reasoning category)
- [[concepts/humanitys-last-exam]] — Another Scientific Reasoning benchmark (12%), open-answer format, text-only, adversarially selected
- [[concepts/critpt]] — Another Scientific Reasoning benchmark (6%), research-level physics problems, multiple answer formats
- [[entities/orgs/artificial-analysis]] — evaluator of GPQA Diamond within the Intelligence Index

---
type: concept
---

# Humanity's Last Exam (HLE)

Frontier academic benchmark from the Centre for AI Safety (led by Dan Hendrycks), designed to evaluate extreme reasoning capabilities. The benchmark consists of **2,158 text-only questions** (from the May 2025 revision containing 2,500 total questions — AA uses the text-only subset for maximum cross-model comparability) spanning mathematics, humanities, and the natural sciences. Questions are open-answer and evaluated by an equality checker LLM (GPT-4o, August model) with pass@1 scoring.

HLE contributes **12%** weight to the [[concepts/intelligence-index]] v4.1 (under the Scientific Reasoning category, alongside GPQA Diamond at 6% and CritPt at 6%).

> ⚠ **Caveat:** The HLE dataset was adversarially selected against GPT-4o, Gemini 1.5 Pro, Claude 3.5 Sonnet, o1, o1-mini, and o1-preview during curation. Questions that those models could answer were systematically excluded. This means HLE is potentially biased against these specific models. Direct comparison of those models with models not used in the curation process is discouraged.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | HLE as a component of the Intelligence Index, adversarial selection caveat, evaluation methodology | 2026-07-21 |

## Key details

- **Questions:** 2,158 text-only (from 2,500 total in May 2025 revision)
- **Domains:** Mathematics, humanities, natural sciences
- **Repeats:** 1
- **Scoring:** Pass@1 — model must answer correctly on first attempt
- **Response type:** Open answer (not multiple choice)
- **Evaluation:** Equality checker LLM using GPT-4o (August model), per the original HLE paper methodology
- **Paper:** <https://arxiv.org/abs/2501.14249v2>
- **Dataset:** <https://huggingface.co/datasets/cais/hle>
- **Dataset authors:** Centre for AI Safety (Dan Hendrycks et al.)

### Adversarial Selection Caveat
The HLE authors disclose that dataset curation involved testing candidate questions against GPT-4o, Gemini 1.5 Pro, Claude 3.5 Sonnet, o1, and o1-mini (plus o1-preview for text-only questions). Questions those models got right were removed. This creates a structural bias — HLE scores should not be used to directly compare those models against models not used in the curation process.

### Equality Checker
HLE uses an equality checker LLM (GPT-4o Aug) with a specialized prompt to determine whether a model's open-ended answer matches the correct answer. The checker must handle mathematical expressions, scientific notation, and nuanced text-equivalent responses.

### Testing Parameters
- **Temperature:** 0 (non-reasoning), 0.6 (reasoning)
- **Max output tokens:** 16,384 (non-reasoning) or maximum allowed (reasoning)
- **Error handling:** Up to 30 retry attempts on API failures

## Relationships
- [[concepts/intelligence-index]] — HLE contributes 12% weight to the Intelligence Index v4.1 (Scientific Reasoning category)
- [[concepts/gpqa-diamond]] — Another Scientific Reasoning benchmark (6%), multiple-choice format
- [[concepts/critpt]] — Another Scientific Reasoning benchmark (6%), research-level physics problems
- [[entities/orgs/artificial-analysis]] — evaluator of HLE within the Intelligence Index

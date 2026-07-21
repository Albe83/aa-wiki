---
type: concept
---

# CritPt

Research-level physics reasoning benchmark featuring unpublished, frontier physics problems spanning a wide range of subfields. The benchmark consists of **70 test-set challenges** evaluated over **5 repeats** with pass@1 scoring. Answer formats are diverse: **numerical values, SymPy symbolic expressions, and Python functions** (evaluated against test cases). Models are evaluated using a **two-step parsing approach**: the first step requests reasoning, and the second step formats the answer into the expected code format for grading. The official CritPt grading server is used to assess all responses.

CritPt contributes **6%** weight to the [[concepts/intelligence-index]] v4.1 (under the Scientific Reasoning category, alongside HLE at 12% and GPQA Diamond at 6%).

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | CritPt as a component of the Intelligence Index, two-step parsing, grading server, answer formats | 2026-07-21 |

## Key details

- **Questions:** 70 test-set challenges (challenge-level components; the example challenge is excluded)
- **Repeats:** 5
- **Scoring:** Pass@1 — aggregated across all 5 repeats × 70 challenges
- **Answer formats:**
  - Numerical values
  - Symbolic expressions in SymPy
  - Python functions (evaluated against test cases)
- **Grading:** Official CritPt grading server — not an LLM judge or regex extraction
- **Paper:** <https://arxiv.org/abs/2509.26574>
- **Website:** <https://critpt.com/>
- **Dataset:** <https://huggingface.co/datasets/CritPt-Benchmark/CritPt>
- **Repository:** <https://github.com/CritPt-Benchmark/CritPt>

### Two-Step Parsing
Models are called with a two-step approach:
1. **Reasoning step:** Model completes the challenge with full chain-of-thought reasoning
2. **Formatting step:** Model reformats its answer into the exact code format expected by the grading server (numerical values, SymPy expressions, or Python functions as appropriate)

Both steps count toward token usage and cost estimates. This ensures models aren't penalized for answer formatting while still requiring rigorous physics reasoning.

### Answer Format Types
| Format | Example | Evaluation |
|--------|---------|------------|
| Numerical | `3.14`, `2.7e-10` | Exact/near-exact match |
| SymPy expression | `x**2 + sin(y)` | Symbolic equivalence check |
| Python function | `def solve(x): return ...` | Test case execution |

### Testing Parameters
- **Temperature:** 0 (non-reasoning), 0.6 (reasoning)
- **Max output tokens:** 16,384 (non-reasoning) or maximum allowed (reasoning)
- **Environment:** Ubuntu 22.04 LTS, Python 3.12
- **Error handling:** Up to 30 retry attempts on API failures

## Relationships
- [[concepts/intelligence-index]] — CritPt contributes 6% weight to the Intelligence Index v4.1 (Scientific Reasoning category)
- [[concepts/humanitys-last-exam]] — Another Scientific Reasoning benchmark (12%), broader domain coverage, adversarially selected
- [[concepts/gpqa-diamond]] — Another Scientific Reasoning benchmark (6%), multiple choice format, biology/physics/chemistry
- [[concepts/scicode]] — Similar code-execution evaluation paradigm, but SciCode is general scientific computing; CritPt is specifically frontier physics reasoning
- [[entities/orgs/artificial-analysis]] — evaluator of CritPt within the Intelligence Index

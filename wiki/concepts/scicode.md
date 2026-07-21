---
type: concept
---

# SciCode

Benchmark evaluating scientific programming capability. Models must write **Python code** to solve scientific computing tasks across physics, chemistry, biology, and other scientific domains. The benchmark consists of 288 subproblems in the test set, each requiring the model to pass all associated unit tests. Scoring uses **pass@1 with sub-problem-level** granularity and **scientist-annotated background prompting** — background information from domain scientists is included in the prompt to ensure the model is tested on coding ability rather than memorized scientific facts.

SciCode contributes **8%** weight to the [[concepts/intelligence-index]] v4.1 (under the Coding category, alongside Terminal-Bench v2.1 at 16%).

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | SciCode as a component of the Intelligence Index, weight, and evaluation parameters | 2026-07-21 |

## Key details

- **Task:** Python programming for scientific computing problems
- **Test set size:** 288 subproblems
- **Repeats:** 3
- **Scoring:** Pass@1, sub-problem level — model must pass all unit tests for each subproblem on first attempt
- **Prompting:** Scientist-annotated background information included — the prompt provides domain context so models are tested on coding, not scientific recall
- **Response type:** Python code that must pass all associated unit tests
- **Evaluation:** Code execution with test suite verification
- **Paper:** <https://arxiv.org/abs/2407.13168>
- **Dataset:** <https://scicode-bench.github.io/>

### Testing Parameters
- **Temperature:** 0 for non-reasoning models, 0.6 for reasoning models
- **Max output tokens:** 16,384 (non-reasoning), or maximum allowed (reasoning)
- **Environment:** Ubuntu 22.04 LTS, Python 3.12
- **Error handling:** Up to 30 retry attempts on API failures

### Code Extraction
SciCode uses a regex-based extraction approach to isolate Python code blocks from model responses. The extracted code is then executed against the test suite for each subproblem. The prompt template includes scientist-annotated background information specific to each problem's scientific domain.

## Relationships
- [[concepts/intelligence-index]] — SciCode contributes 8% weight to the Intelligence Index v4.1 (Coding category)
- [[concepts/terminal-bench]] — The other Coding category benchmark (16% weight), focused on terminal-based software engineering
- [[concepts/capability-indices]] — SciCode is a component of the Coding Index and Engineering Index
- [[entities/orgs/artificial-analysis]] — evaluator of SciCode within the Intelligence Index

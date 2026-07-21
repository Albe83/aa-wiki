---
type: concept
---

# AA Intelligence Index v4.1

The Artificial Analysis Intelligence Index v4.1 is the primary composite metric for measuring general model intelligence. It aggregates 9 independent evaluations across 4 categories, each weighted according to its contribution: Agents (34%), Coding (24%), Scientific Reasoning (24%), and General (18%).

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Core methodology page defining index composition, testing parameters, and evaluation methodology | 2026-07-21 |
| [[sources/methodology]] | General AA methodology, definitions, and Cost per Task calculation tied to Intelligence Index weights | 2026-07-21 |

## Key details

### Composition and weights
| Evaluation | Category | Weight |
|------------|----------|--------|
| GDPval-AA v2 | Agents | 20% |
| τ³-Banking | Agents | 14% |
| Terminal-Bench v2.1 | Coding | 16% |
| SciCode | Coding | 8% |
| AA-LCR | General | 6% |
| AA-Omniscience (Accuracy) | General | 8% |
| AA-Omniscience (Non-Hallucination) | General | 4% |
| HLE | Scientific Reasoning | 12% |
| GPQA Diamond | Scientific Reasoning | 6% |
| CritPt | Scientific Reasoning | 6% |

**Category totals:** Agents 34% (GDPval-AA v2 + τ³-Banking), Coding 24% (Terminal-Bench v2.1 + SciCode), Scientific Reasoning 24% (HLE + GPQA Diamond + CritPt), General 18% (AA-LCR + AA-Omniscience Accuracy + AA-Omniscience Non-Hallucination).

### Tracking evaluations
GDPval-AA v2, HLE, GPQA Diamond, and CritPt act as "tracking evaluations" used to monitor improvement over time across provider offerings. They serve as the baseline against which model progress is measured.

### Scoring methodology
Pass@1 scoring is used for all evaluations. Temperature is set to 0 for non-reasoning models and 0.6 for reasoning models. Text-only, English-language evaluations. The index has a ~±1% 95% confidence interval.

### Elo-to-score normalization
For evaluations using Elo scoring (GDPval-AA v2), Elo scores are frozen and normalized as `clamp((Elo − 500) / 2000)` to produce a 0–1 score for the Intelligence Index.

## Relationships
- [[concepts/gdpval-aa]] — 20% weight, agentic knowledge work evaluation
- [[concepts/tau3-banking]] — 14% weight, agentic customer interaction evaluation
- [[concepts/terminal-bench]] — 16% weight, agentic terminal use evaluation
- [[concepts/aa-lcr]] — 6% weight, long context reasoning evaluation
- [[concepts/aa-omniscience]] — 12% total weight (8% accuracy + 4% non-hallucination)
- [[concepts/cost-per-task]] — Cost per Task is calculated using Intelligence Index weights
- [[concepts/capability-indices]] — all Capability Index components derive from Intelligence Index evaluations

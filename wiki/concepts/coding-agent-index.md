---
type: concept
---

# AA Coding Agent Index v1.2

The AA Coding Agent Index v1.2 is a composite benchmark that evaluates coding agents on end-to-end software engineering tasks. It aggregates 321 tasks across 3 components, measuring not only task success (pass@1) but also efficiency metrics: cost, token usage, and execution time. The index is distinct from the Coding Skill Index in the Capability Indices — the Coding Agent Index evaluates complete autonomous agents, while the Coding Skill Index evaluates atomic coding capabilities.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/coding-agents-benchmarking]] | Full methodology page covering index composition, scoring, and efficiency metrics | 2026-07-21 |

## Key details

### Index components (v1.2, July 2026)
| Evaluation | Field | Tasks | Repeats |
|------------|-------|-------|---------|
| DeepSWE | Long-Horizon Software Engineering | 113 | 3 |
| Terminal-Bench v2 | Agentic Terminal Use | 84* | 3 |
| SWE-Atlas-QnA | Repository Q&A | 124 | 3 |

*84 of 89 Terminal-Bench tasks (5 excluded for environment compatibility)

Total: 321 evaluated tasks.

### Scoring
- **Binary pass@1:** each task receives 1 for pass, 0 for fail
- **Per-evaluation score:** average of task-level pass@1 results across all 3 repeats
- **Index score:** composite average pass@1 across all 3 components (equal-weighted)

### Efficiency metrics
Beyond task success, the index reports:
- **Cost to run:** average pay-per-token API cost per task (provider pricing, not consumer plans)
- **Token usage:** average input, cache, cache-write, reasoning, and output tokens per task
- **Execution time:** average wall-clock runtime per task

These efficiency metrics are critical for practical deployment: an excellent but prohibitively expensive or slow coding agent has limited real-world utility.

### Version history
- **v1.2 (July 2026):** SWE-Atlas-QnA scoring changed to binary pass/fail (from non-binary)
- **v1.1 (June 2026):** Added DeepSWE, removed SWE-Bench-Pro-Hard-AA
- **v1.0 (May 2026):** Initial release

The rapid iteration (3 versions in 3 months) reflects the fast-moving coding agent landscape.

### Scoring verifiers
- **DeepSWE:** program verifier pass/fail
- **Terminal-Bench v2:** test suite pass/fail
- **SWE-Atlas-QnA:** strict resolve verifier (binary pass/fail as of v1.2)

## Relationships
- [[concepts/terminal-bench]] — 84 of 89 tasks used; one of three index components
- [[concepts/capability-indices]] — distinct from the Coding Skill Index; Coding Agent Index evaluates complete agents vs. atomic capabilities
- [[concepts/intelligence-index]] — Terminal-Bench appears in both indices, serving as a bridge between intelligence and coding agent evaluation

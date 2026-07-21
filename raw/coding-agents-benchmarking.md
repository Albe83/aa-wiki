# Coding Agent Index Methodology

**Source:** https://artificialanalysis.ai/methodology/coding-agents-benchmarking
**Fetched:** 2026-07-21

## Overview

Benchmarks coding agents on end-to-end software engineering tasks. Measures outcome, reliability, token usage, cost, and execution time.

## Index Components (v1.2, July 2026)

| Evaluation | Field | Tasks | Repeats | Scoring |
|------------|-------|-------|---------|---------|
| DeepSWE | Long-Horizon SE | 113 | 3 | Program verifier pass/fail, pass@1 |
| Terminal-Bench v2 | Agentic Terminal Use | 84* | 3 | Test suite pass/fail, pass@1 |
| SWE-Atlas-QnA | Repository Q&A | 124 | 3 | Strict resolve verifier, pass@1 |

*84 of 89 tasks (5 excluded for environment compatibility)

Total: 321 evaluated tasks across 3 components.

## Scoring

- Binary pass@1: task receives 1 for pass, 0 for fail
- Per-evaluation score: average of task-level pass@1 results (including repeats)
- Index: composite average pass@1 across all 3 components

## Efficiency Metrics

- **Cost to run:** Avg pay-per-token API cost per task (provider pricing, not consumer plans)
- **Token usage:** Avg input, cache, cache-write, reasoning, output tokens per task
- **Execution time:** Avg wall-clock runtime per task

## Version History

- **v1.2 (July 2026):** SWE-Atlas-QnA scoring changed to binary pass/fail
- **v1.1 (June 2026):** Added DeepSWE, removed SWE-Bench-Pro-Hard-AA
- **v1.0 (May 2026):** Initial release

---
type: source
date: 2026-07-21
source_file: raw/coding-agents-benchmarking.md
status: processed
---

# Coding Agent Index Methodology

**Source:** https://artificialanalysis.ai/methodology/coding-agents-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing Artificial Analysis's Coding Agent Index, a benchmark that evaluates coding agents on end-to-end software engineering tasks. The index (v1.2, July 2026) aggregates 321 tasks distributed across 3 components: DeepSWE (113 long-horizon tasks), Terminal-Bench v2 (84 agentic terminal-usage tasks), and SWE-Atlas-QnA (124 repository Q&A tasks). Each task is run 3 times with binary pass@1 scoring.

Beyond quality, the index measures efficiency metrics: API cost per task (based on pay-per-token pricing), token usage (input, cache, cache-write, reasoning, output), and wall-clock execution time. The page also documents the index's evolution through three versions.

## Key points

- 321 total tasks across 3 components: DeepSWE (113), Terminal-Bench v2 (84), SWE-Atlas-QnA (124)
- Binary pass@1 scoring: 1 for pass, 0 for fail, averaged across 3 repeats per task
- Composite index: equally weighted average of the 3 components' pass@1
- Efficiency metrics: API cost, token usage, execution time
- v1.2 (July 2026): SWE-Atlas-QnA converted to binary scoring
- v1.1 (June 2026): added DeepSWE, removed SWE-Bench-Pro-Hard-AA
- v1.0 (May 2026): first release
- 5 Terminal-Bench tasks excluded due to environment incompatibility

## Entities mentioned

_none_

## Concepts mentioned

- [[concepts/coding-agent-index]] — composite agentic coding index
- [[concepts/terminal-bench]] — Terminal-Bench v2: agentic terminal-usage component

## Related sources

- [[sources/methodology]] — general AA methodology
- [[sources/intelligence-benchmarking]] — Intelligence Index (includes Terminal-Bench)
- [[sources/capability-indices]] — Coding Index as a separate Skill Index

## My notes

- The Coding Agent Index is distinct from the Coding Index (Skill) of the Capability Indices: the former evaluates complete agents, the latter evaluates atomic capabilities
- The rapid evolution (3 versions in 3 months) reflects the speed of the coding agents field
- The cost metric is particularly relevant: an excellent but prohibitively expensive coding agent has limited practical utility

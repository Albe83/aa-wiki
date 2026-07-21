---
type: concept
---

# DeepSWE

DeepSWE is a long-horizon software engineering benchmark used as a component of the Artificial Analysis [[concepts/coding-agent-index|Coding Agent Index]]. It evaluates coding agents on complex, multi-step software engineering tasks that require sustained reasoning and code modification over extended trajectories, in contrast to single-shot code generation benchmarks.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/coding-agents-benchmarking]] | AA Coding Agent Index v1.2 component: 113 tasks, 3 repeats, program verifier pass/fail | 2026-07-21 |

## Key details

- **113 evaluated tasks** covering real-world software engineering workflows
- **3 repeats** per task for statistical robustness
- **Scoring:** Program verifier pass/fail, binary pass@1 — the agent's code patch or repository changes must satisfy an automated verification suite
- **Field:** Long-Horizon Software Engineering
- **Agent harness:** Each agent variant is evaluated independently; settings reflect default reasoning configurations
- Added to the Coding Agent Index in v1.1 (June 2026), replacing SWE-Bench-Pro-Hard-AA

## Sample tasks

Tasks span diverse repositories and languages, including:
- Add iterable collection combinators, rolling statistics, and deterministic data structures
- Fix HTTP body read lifecycle, PromQL label sorting, and merge conflict handling
- Add circuit breaker patterns, policy-based alerting, and dead-letter queues
- Implement GraphQL incremental delivery with @defer and @stream
- Add typed variable bindings, CSS Grid layout, and SSE streaming endpoints

## Relationships

- [[concepts/coding-agent-index]] — DeepSWE is one of three index components (1/3 weight, equally weighted)
- [[concepts/terminal-bench]] — complementary component evaluating agentic terminal use (84 tasks)
- [[concepts/swatlas-qna]] — complementary component evaluating repository Q&A (124 tasks)

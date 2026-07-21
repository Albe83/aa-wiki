---
type: concept
---

# SWE-Atlas-QnA

SWE-Atlas-QnA is a repository question-and-answer benchmark used as a component of the Artificial Analysis [[concepts/coding-agent-index|Coding Agent Index]]. It tests coding agents' ability to answer questions about code repositories by reasoning over code structure, dependencies, and behavior — a capability distinct from code generation or terminal-based task execution.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/coding-agents-benchmarking]] | AA Coding Agent Index v1.2 component: 124 tasks, 3 repeats, strict resolve verifier | 2026-07-21 |

## Key details

- **124 evaluated tasks** requiring agents to answer questions about real code repositories
- **3 repeats** per task for statistical robustness
- **Scoring:** Strict resolve verifier — all test cases must pass for a task to be marked correct. Binary pass@1 (0 or 1).
- **Field:** Repository Q&A
- Included in the Coding Agent Index since v1.0 (May 2026)

## Scoring change (v1.2, July 2026)

SWE-Atlas-QnA was originally scored using a rubric reward system. In v1.2, scoring was changed to **binary pass/fail** requiring all test cases to pass. This stricter scoring better distinguishes agent capability levels.

## Relationships

- [[concepts/coding-agent-index]] — SWE-Atlas-QnA is one of three index components (1/3 weight, equally weighted)
- [[concepts/deepswe]] — complementary component evaluating long-horizon software engineering (113 tasks)
- [[concepts/terminal-bench]] — complementary component evaluating agentic terminal use (84 tasks)

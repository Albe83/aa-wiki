---
type: concept
---

# Terminal-Bench v2.1

Terminal-Bench v2.1 is an agentic coding benchmark developed by Stanford University and the Laude Institute. It evaluates models on their ability to use a terminal environment to solve complex tasks across multiple domains. It contributes 16% to the AA Intelligence Index v4.1 and is also a component of the AA Coding Agent Index v1.2.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Core evaluation in the Intelligence Index v4.1 at 16% weight | 2026-07-21 |
| [[sources/coding-agents-benchmarking]] | Component of the Coding Agent Index v1.2 (84 of 89 tasks, 3 repeats) | 2026-07-21 |
| [[sources/capability-indices]] | Component of the Coding Index (Skill) at 50% weight | 2026-07-21 |

## Key details

### Task design
89 tasks spanning 5 domains:
- Software Engineering
- System Administration
- Data Processing
- Model Training
- Security

### Scoring
pass@1 averaged over 3 repeats. Tasks pass only if **all tests pass** — partial credit is not awarded. In the Coding Agent Index, 84 of 89 tasks are used (5 excluded for environment compatibility).

### Agent harness
Uses the **Terminus 2** agent harness operating inside an E2B sandbox. Agents interact exclusively through a terminal interface, mimicking real-world developer workflows.

### Technical parameters
- Maximum 250 episodes per task
- 2-hour timeout per task
- 3 repeats for pass@1 averaging
- E2B sandbox execution environment
- Terminal-only interaction (no GUI, no structured API)

## Relationships
- [[concepts/intelligence-index]] — 16% weight in the Intelligence Index
- [[concepts/coding-agent-index]] — 84 of 89 tasks used; one of three components in the Coding Agent Index v1.2
- [[concepts/capability-indices]] — 50% of the Coding Index (Skill), 5% of Engineering Index (Industry)
- [[entities/orgs/stanford]] — co-developer alongside the Laude Institute

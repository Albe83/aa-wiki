---
type: concept
---

# GDPval-AA v2

GDPval-AA v2 is Artificial Analysis's implementation of OpenAI's GDPval dataset, designed to evaluate agentic task completion on real-world occupational tasks. It is the single largest component of the AA Intelligence Index v4.1 at 20% weight. Models must navigate file-based outputs, tool use, and multi-step reasoning to complete 220 tasks spanning 44 occupations.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Core evaluation in the Intelligence Index v4.1; described as agentic knowledge work evaluation | 2026-07-21 |
| [[sources/capability-indices]] | Component in the Agentic Index (50%) and all six Industry Indices except Coding | 2026-07-21 |

## Key details

### Task design
220 tasks across 44 occupations. Each task requires agentic task completion with file outputs — models must produce concrete artifacts, not just text responses. Represents real-world knowledge work scenarios.

### Scoring: pairwise comparison (Elo)
Tasks are scored via pairwise comparison using a panel of 3 frontier LLM judges: GPT-5.5, Gemini 3.1 Pro, and Claude Opus 4.8. Results are anchored to human expert performance at 1000 Elo. Elo scores are then frozen and normalized as `clamp((Elo − 500) / 2000)` for use in the Intelligence Index.

### Agent harness
Uses the **Stirrup** harness with 6 tools available to the model:
- Web Fetch — retrieve web content
- Web Search — search the internet
- View Image — inspect images
- Code Exec — execute code in a sandboxed environment
- Finish — signal task completion
- Abandon — give up on a task

### Technical parameters
- Maximum 250 turns per task
- E2B sandbox for code execution
- Models work independently on each task

## Relationships
- [[concepts/intelligence-index]] — 20% weight, largest single component
- [[concepts/capability-indices]] — 50% of Agentic Index, present in all industry indices except Coding
- [[concepts/tau3-banking]] — paired in the Agentic Index as the two agentic evaluations
- [[concepts/aa-briefcase]] — related agentic knowledge work benchmark using the same Stirrup harness but with longer-horizon tasks

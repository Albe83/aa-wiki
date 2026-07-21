---
type: concept
---

# AA-LCR (Long Context Reasoning)

AA-LCR is a long context reasoning benchmark developed by Artificial Analysis. It evaluates models' ability to answer hard text-based questions requiring synthesis across ~100K tokens of context per question. It contributes 6% to the AA Intelligence Index v4.1 and appears in 4 of the 6 Industry Capability Indices.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Core evaluation in the Intelligence Index v4.1 at 6% weight | 2026-07-21 |
| [[sources/capability-indices]] | Component in Finance, Strategy & Ops, Legal, and Economics industry indices | 2026-07-21 |

## Key details

### Dataset
100 hard text questions requiring deep comprehension and synthesis. Documents span 7 categories:
- Company Reports
- Industry Reports
- Government Consultations
- Academia
- Legal
- Marketing
- Survey Reports

~230 unique documents providing ~3 million unique input tokens across the full dataset.

### Context requirements
- ~100,000 tokens of input per question (measured with cl100k_base tokenizer)
- Requires models to support a 128K context window to fit the full document set
- Questions are designed to be unanswerable without integrating information across the full context

### Scoring
pass@1 scoring using **Qwen3 235B A22B** as the equality checker. The equality checker determines whether the model's answer matches the reference answer, accounting for acceptable variations in phrasing and formatting.

### Role in Capability Indices
AA-LCR contributes to 4 industry indices:
- Finance & Accounting: 5%
- Strategy & Ops: 5%
- Legal: 10%
- Economics: 15%

Economics places the highest weight on AA-LCR (15%), reflecting the importance of long-document analysis in economic research.

## Relationships
- [[concepts/intelligence-index]] — 6% weight, part of the General category
- [[concepts/capability-indices]] — appears in 4 industry indices, highest weight in Economics (15%)

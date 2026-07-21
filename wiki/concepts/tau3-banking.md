---
type: concept
---

# τ³-Banking

τ³-Banking is a fintech customer-support benchmark derived from Sierra's τ-Knowledge framework. It evaluates agentic tool use for customer interaction scenarios, contributing 14% to the AA Intelligence Index v4.1. Agents must coordinate knowledge retrieval across a large policy document corpus with multi-step tool calls to resolve customer queries, scored against backend database state rather than conversational quality.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Core evaluation in the Intelligence Index v4.1; benchmark of agentic tool use for customer interaction | 2026-07-21 |
| [[sources/capability-indices]] | Component in the Agentic Index (50%) and appears in 6 of 8 Capability Indices | 2026-07-21 |

## Key details

### Task design
97 tasks with 5 repeats each across fintech customer-support scenarios. Agents interact with a backend system's database state — correctness is determined by whether the agent's actions produce the correct database state, not by conversational quality or tone.

### Policy document corpus
~700 policy documents totaling ~195,000 tokens, covering 21 product categories. Agents must coordinate knowledge retrieval by searching and reading policy documents to find the information needed to resolve each customer request.

### Agent architecture
Agents use multi-step tool calls to:
1. Search the policy corpus for relevant documents
2. Read specific policy sections
3. Execute actions against the backend system
4. Verify their work against policy requirements

### Scoring
pass@1 scoring. The evaluation uses **GPT-5.4 Mini** as both user simulator and judge. The user simulator generates customer queries, and the judge evaluates whether the agent's backend database state changes correctly resolved the request.

### Technical parameters
- BM25 + grep retrieval mode for document search
- Maximum 200 steps per task
- 10 tool-execution error allowance per task
- 5 repeats per task for reliability

## Relationships
- [[concepts/intelligence-index]] — 14% weight, second-largest agentic component
- [[concepts/gdpval-aa]] — paired in the Agentic Index (50% each); complementary agentic evaluation
- [[concepts/capability-indices]] — 50% of Agentic Index, present in Strategy & Ops (30%), Finance (10%), Legal (5%), Healthcare (10%)
- [[entities/orgs/sierra]] — developer of the τ-Knowledge framework underlying τ³-Banking

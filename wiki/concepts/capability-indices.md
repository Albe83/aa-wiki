---
type: concept
---

# AA Capability Indices

AA Capability Indices are composite metrics that measure model performance on specific use cases and industries. Unlike the general-purpose Intelligence Index, Capability Indices are targeted: they aggregate Intelligence Index evaluation scores with weights tuned to particular skills or professions. There are 2 Skill Indices and 6 Industry Indices, all composed from subsets of the 9 Intelligence Index evaluations.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/capability-indices]] | Full methodology page describing all 8 indices, their compositions, and weighting rationale | 2026-07-21 |
| [[sources/intelligence-benchmarking]] | Source of all component evaluations used in the Capability Indices | 2026-07-21 |

## Key details

### Skill Indices (equal-weighted)
Cross-domain capabilities, each component weighted equally:

**Agentic Index:**
- 50% GDPval-AA v2 — Agentic Knowledge Work
- 50% τ³-Banking — Agentic Customer Interaction

**Coding Index:**
- 50% Terminal-Bench v2.1 — Agentic Terminal Use
- 50% SciCode — Code Generation

### Industry Indices (O*NET-weighted)
Profession-specific indices where component weights reflect real-world task frequency derived from O*NET-style occupation taxonomies:

**Finance & Accounting Index** (6 components):
- 30% Business Knowledge (AA-Omniscience)
- 30% Agentic Knowledge Work (GDPval-AA v2)
- 20% Reasoning (HLE)
- 10% Agentic Customer Interaction (τ³-Banking)
- 5% Long-Context (LCR)
- 5% Non-Hallucination (AA-Omniscience)

**Strategy & Ops Index** (5 components):
- 30% Business Knowledge (AA-Omniscience)
- 30% Agentic Knowledge Work (GDPval-AA v2)
- 30% Agentic Customer Interaction (τ³-Banking)
- 5% Instruction Following (IFBench)
- 5% Long-Context (LCR)

**Legal Index** (6 components):
- 35% Legal Knowledge (AA-Omniscience)
- 25% Agentic Knowledge Work (GDPval-AA v2)
- 15% Reasoning (HLE)
- 10% Long-Context (LCR)
- 10% Non-Hallucination (AA-Omniscience)
- 5% Agentic Customer Interaction (τ³-Banking)

**Healthcare & Medical Index** (5 components):
- 35% Medical & Health Knowledge (AA-Omniscience)
- 25% Agentic Knowledge Work (GDPval-AA v2)
- 15% Non-Hallucination (AA-Omniscience)
- 15% Reasoning (HLE)
- 10% Agentic Customer Interaction (τ³-Banking)

**Engineering Index** (4 components):
- 35% Engineering Knowledge (AA-Omniscience)
- 35% Reasoning (HLE, GPQA Diamond, CritPt)
- 25% Agentic Knowledge Work (GDPval-AA v2)
- 5% Agentic Terminal Use (Terminal-Bench v2.1)

**Economics Index** (4 components):
- 35% Economics Knowledge (AA-Omniscience)
- 35% Reasoning (HLE)
- 15% Agentic Knowledge Work (GDPval-AA v2)
- 15% Long-Context (LCR)

### Cross-index patterns
- AA-Omniscience is the most broadly used component: appears in all 6 industry indices
- GDPval-AA v2 appears in all indices except the Coding Index
- τ³-Banking appears in 6 of 8 indices (absent from Engineering and Economics)
- HLE appears in 5 indices as a general reasoning component
- AA-LCR appears in 4 indices: Finance, Strategy & Ops, Legal, Economics

### Weighting rationale
Skill Indices use equal weighting because cross-domain skills don't have occupation-specific task frequencies. Industry Indices use O*NET-derived weights to reflect how often each type of task is actually performed in each profession — for example, Legal weights AA-Omniscience legal knowledge heavily (35%) while Engineering weights reasoning tasks heavily (35% total across HLE, GPQA Diamond, CritPt).

## Relationships
- [[concepts/intelligence-index]] — source of all component evaluations
- [[concepts/gdpval-aa]] — present in 7 of 8 indices
- [[concepts/tau3-banking]] — present in 6 of 8 indices
- [[concepts/aa-omniscience]] — present in all 6 industry indices
- [[concepts/aa-lcr]] — present in 4 industry indices
- [[concepts/terminal-bench]] — present in Coding Index and Engineering Index
- [[concepts/coding-agent-index]] — distinct from the Coding Skill Index; evaluates agents vs. atomic capabilities

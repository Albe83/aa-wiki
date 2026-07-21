# Artificial Analysis Capability Indices Methodology

**Source:** https://artificialanalysis.ai/methodology/capability-indices
**Fetched:** 2026-07-21

## Overview

Capability Indices measure model performance on specific use cases/industries. Two types:
- **Skill indices:** Cross-domain capabilities (Coding, Agentic). Equal-weighted average of components.
- **Industry indices:** Single profession (Legal, Healthcare, Finance). Weighted by real-world task frequency (O*NET-style taxonomy).

## Index Breakdowns

### Agentic Index (Skill)
- 50% Agentic Knowledge Work (GDPval-AA v2)
- 50% Agentic Customer Interaction (τ³-Banking)

### Coding Index (Skill)
- 50% Agentic Terminal Use (Terminal-Bench v2.1)
- 50% Code Generation (SciCode)

### Finance & Accounting Index (Industry)
- 30% Business Knowledge (AA-Omniscience)
- 30% Agentic Knowledge Work (GDPval-AA v2)
- 20% Reasoning (HLE)
- 10% Agentic Customer Interaction (τ³-Banking)
- 5% Long-Context (LCR)
- 5% Non-Hallucination (AA-Omniscience)

### Strategy & Ops Index (Industry)
- 30% Business Knowledge (AA-Omniscience)
- 30% Agentic Knowledge Work (GDPval-AA v2)
- 30% Agentic Customer Interaction (τ³-Banking)
- 5% Instruction Following (IFBench)
- 5% Long-Context (LCR)

### Legal Index (Industry)
- 35% Legal Knowledge (AA-Omniscience)
- 25% Agentic Knowledge Work (GDPval-AA v2)
- 10% Long-Context (LCR)
- 10% Non-Hallucination (AA-Omniscience)
- 5% Agentic Customer Interaction (τ³-Banking)
- 15% Reasoning (HLE)

### Healthcare & Medical Index (Industry)
- 35% Medical & Health Knowledge (AA-Omniscience)
- 25% Agentic Knowledge Work (GDPval-AA v2)
- 15% Non-Hallucination (AA-Omniscience)
- 15% Reasoning (HLE)
- 10% Agentic Customer Interaction (τ³-Banking)

### Engineering Index (Industry)
- 35% Engineering Knowledge (AA-Omniscience)
- 35% Reasoning (HLE, GPQA Diamond, CritPt)
- 25% Agentic Knowledge Work (GDPval-AA v2)
- 5% Agentic Terminal Use (Terminal-Bench v2.1)

### Economics Index (Industry)
- 35% Economics Knowledge (AA-Omniscience)
- 35% Reasoning (HLE)
- 15% Agentic Knowledge Work (GDPval-AA v2)
- 15% Long-Context (LCR)

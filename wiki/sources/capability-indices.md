---
type: source
date: 2026-07-21
source_file: raw/capability-indices.md
status: processed
---

# Artificial Analysis Capability Indices Methodology

**Source:** https://artificialanalysis.ai/methodology/capability-indices
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing Artificial Analysis's Capability Indices, composite metrics that measure model performance on specific use cases and industries. They fall into two categories: Skill Indices (cross-domain competencies) and Industry Indices (specific professions). Skill Indices use an equally weighted average of components, while Industry Indices weight components based on real-world professional task frequency (according to an O*NET taxonomy).

The page lists 8 indices: 2 Skill (Agentic, Coding) and 6 Industry (Finance & Accounting, Strategy & Ops, Legal, Healthcare & Medical, Engineering, Economics). Each index is broken down into its components with their percentage weights, all derived from Intelligence Index evaluations.

## Key points

- 2 Skill Indices: Agentic Index (GDPval-AA v2 + τ³-Banking) and Coding Index (Terminal-Bench v2.1 + SciCode)
- 6 Industry Indices: Finance, Strategy & Ops, Legal, Healthcare, Engineering, Economics
- Industry Indices weight components by real task frequency, not equally
- AA-Omniscience is the most cross-cutting component: it appears in all 6 Industry Indices
- GDPval-AA v2 appears in all indices except the Coding Index
- τ³-Banking appears in 6 of the 8 indices
- HLE appears in 5 indices as a source of general reasoning
- AA-LCR appears in 4 indices (Finance, Strategy & Ops, Legal, Economics)

## Entities mentioned

_none_

## Concepts mentioned

- [[concepts/capability-indices]] — definition and structure of capability indices
- [[concepts/intelligence-index]] — source of component evaluations
- [[concepts/gdpval-aa]] — agentic knowledge work component
- [[concepts/tau3-banking]] — agentic customer interaction component
- [[concepts/terminal-bench]] — agentic coding component
- [[concepts/scicode]] — scientific code generation component
- [[concepts/aa-omniscience]] — knowledge and anti-hallucination component
- [[concepts/humanitys-last-exam]] — reasoning component
- [[concepts/aa-lcr]] — long-context reasoning component
- [[concepts/ifbench]] — instruction following component

## Related sources

- [[sources/methodology]] — general AA methodology
- [[sources/intelligence-benchmarking]] — Intelligence Index from which all components are derived

## My notes

- The Skill vs Industry distinction is fundamental: Skill Indices are cross-domain and equally weighted, Industry Indices are calibrated to real professional task frequencies
- AA-Omniscience is the most versatile building block: sector knowledge + hallucination metric in a single benchmark
- The Engineering Index is the most reasoning-heavy (35% across HLE, GPQA Diamond, and CritPt)
- Strategy & Ops is the only index where τ³-Banking has equal weight to GDPval-AA v2 (30% each)

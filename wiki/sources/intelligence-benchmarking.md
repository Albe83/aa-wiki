---
type: source
date: 2026-07-21
source_file: raw/intelligence-benchmarking.md
status: processed
---

# Artificial Analysis Intelligence Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/intelligence-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing the composition of Artificial Analysis's Intelligence Index v4.1, the composite index that measures general model intelligence. The index aggregates multiple independent evaluations covering agentic knowledge work, customer interaction, terminal usage, code generation, scientific reasoning, long-context reasoning, multidisciplinary knowledge, and hallucination prevention.

Beyond the core Intelligence Index evaluations, the page describes additional benchmarks such as AA-Briefcase (long-horizon knowledge work), Harvey LAB-AA and APEX-Agents-AA (legal and agentic benchmarks developed with partners), AutomationBench-AA, EnterpriseOps-Gym-AA, ITBench-AA, LiveCodeBench, IFBench, MMLU-Pro, Global MMLU-Lite, and MMMU-Pro. Testing parameters, prompts, and evaluation methodology are specified.

## Key points

- Intelligence Index v4.1 is the main composite index for measuring AA model intelligence
- Core evaluations include: GDPval-AA v2, τ³-Banking, Terminal-Bench v2.1, SciCode, AA-LCR, AA-Omniscience, HLE, GPQA Diamond, CritPt
- Additional benchmarks cover specialized domains: legal (Harvey LAB-AA), agentic (APEX-Agents-AA, AutomationBench-AA), enterprise IT (EnterpriseOps-Gym-AA, ITBench-AA)
- Extended knowledge work evaluations with AA-Briefcase
- Additional coding benchmarks: LiveCodeBench
- Instruction following benchmark: IFBench
- Multidisciplinary benchmarks: MMLU-Pro, Global MMLU-Lite, MMMU-Pro

## Entities mentioned

- [[entities/orgs/openai]] — GDPval dataset uses tiktoken for tokenization
- [[entities/orgs/sierra]] — developer of the τ-bench benchmark (τ³-Banking)
- [[entities/orgs/stanford]] — developer of Terminal-Bench

## Concepts mentioned

- [[concepts/intelligence-index]] — composite intelligence index v4.1
- [[concepts/gdpval-aa]] — GDPval-AA v2: benchmark on real-world work tasks
- [[concepts/tau3-banking]] — τ³-Banking: agentic tool use benchmark for customer interaction
- [[concepts/terminal-bench]] — Terminal-Bench v2.1: agentic coding benchmark via terminal
- [[concepts/scicode]] — SciCode: scientific code generation benchmark
- [[concepts/aa-lcr]] — AA-LCR: long context reasoning benchmark
- [[concepts/aa-omniscience]] — AA-Omniscience: knowledge and hallucination benchmark
- [[concepts/humanitys-last-exam]] — HLE: extreme reasoning benchmark
- [[concepts/gpqa-diamond]] — GPQA Diamond: scientific reasoning benchmark
- [[concepts/critpt]] — CritPt: critical reasoning benchmark
- [[concepts/aa-briefcase]] — AA-Briefcase: long-horizon knowledge work benchmark
- [[concepts/harvey-lab-aa]] — Harvey LAB-AA: legal benchmark developed with Harvey
- [[concepts/apex-agents-aa]] — APEX-Agents-AA: agentic benchmark
- [[concepts/automationbench-aa]] — AutomationBench-AA: automation benchmark
- [[concepts/enterpriseops-gym-aa]] — EnterpriseOps-Gym-AA: enterprise IT operations benchmark
- [[concepts/itbench-aa]] — ITBench-AA: IT benchmark
- [[concepts/livecodebench]] — LiveCodeBench: live coding benchmark
- [[concepts/ifbench]] — IFBench: instruction following benchmark
- [[concepts/mmlu-pro]] — MMLU-Pro: advanced multidisciplinary benchmark
- [[concepts/global-mmlu-lite]] — Global MMLU-Lite: global multidisciplinary benchmark
- [[concepts/mmmu-pro]] — MMMU-Pro: advanced multimodal benchmark

## Related sources

- [[sources/methodology]] — general AA methodology
- [[sources/capability-indices]] — capability indices derived from these benchmarks
- [[sources/coding-agents-benchmarking]] — specific methodology for coding agents

## My notes

- Intelligence Index v4.1 is AA's central benchmark: all Cost per Task values are calculated on the weights of this index
- The list of additional benchmarks is notable: AA has developed proprietary benchmarks (AA-Briefcase, AA-LCR, AA-Omniscience) and partnerships (Harvey LAB-AA, APEX-Agents-AA)
- Terminal-Bench appears in both the Intelligence Index and the Coding Agent Index — it is a bridge benchmark between the two areas

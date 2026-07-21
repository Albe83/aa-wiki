---
type: source
date: 2026-07-21
source_file: raw/agentperf.md
status: processed
---

# AA-AgentPerf Methodology

**Source:** https://artificialanalysis.ai/methodology/agentperf
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing AA-AgentPerf, Artificial Analysis's hardware benchmark that measures how many active agents an inference deployment can support simultaneously while meeting SLOs (Service Level Objectives) for agent performance. Unlike API benchmarks that measure isolated prompts, AgentPerf uses real multi-turn agentic trajectories with interleaved reasoning, tool calls, and variable context.

The benchmark defines SLO tiers derived from AA's serverless API benchmarking data, with different thresholds for different models. It uses a dataset of real trajectories collected with the OpenCode harness (DeepSeek V3.2, GLM 4.7, Kimi K2.5), with inputs ranging from ~5K to 131K tokens. The test uses binary search after exponential ramp-up, with each phase lasting at least 10 minutes at steady state. Results are normalized per accelerator, per system, and per MW.

## Key points

- Measures supportable active agents, not raw token throughput
- Real multi-turn agentic trajectories: coding sessions with tool calls and variable context
- SLO tiers derived from the market: based on performance observed in AA serverless APIs
- 2 reference models with different tiers: DeepSeek V4 Pro (max) with 3 tiers, gpt-oss-120b (high) with 4 tiers
- Dataset from OpenCode harness: input ~5K-131K tokens (mean ~27K), 12+ languages
- Realistic tool call delays: 0.1s-5s (median ~1s)
- Binary search after exponential ramp-up; ≥30 trajectories completed per phase
- Multi-level normalization: per accelerator, system, MW
- Continuously updated with new hardware/software

## Entities mentioned

_none_

## Concepts mentioned

- [[concepts/aa-agentperf]] — hardware benchmark for agentic deployments
- [[concepts/output-speed]] — SLO metrics: P25 Output Speed and P95 TTFT

## Related sources

- [[sources/methodology]] — general AA methodology
- [[sources/performance-benchmarking]] — API performance benchmark from which SLO tiers are derived
- [[sources/system-load-test]] — complementary system load benchmark

## My notes

- AgentPerf bridges the gap between API benchmarks (single-user experience) and system benchmarks (raw throughput): it measures real agentic capacity
- Using real trajectories (not synthetic) with realistic tool call delays is a methodological strength
- Per-MW normalization enables energy efficiency comparisons across deployments
- Differentiated SLO tiers per model reflect that performance expectations depend on the model used

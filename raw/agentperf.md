# AA-AgentPerf Methodology

**Source:** https://artificialanalysis.ai/methodology/agentperf
**Fetched:** 2026-07-21

## Overview

Hardware benchmark measuring how many active agents an inference deployment can support under realistic agentic workloads while meeting per-agent performance SLOs (TTFT and output speed).

Key features:
- **Real agentic trajectories:** Multi-turn coding sessions with interleaved reasoning, tool calls, variable context
- **Sustained concurrent load:** Simulated agents maintain continuous in-flight requests
- **Market-derived SLO tiers:** Based on AA serverless API benchmarking data
- **Continuously updated** as new hardware/software becomes available

## Dataset

Real agentic trajectories from OpenCode harness using DeepSeek V3.2, GLM 4.7, Kimi K2.5. Input lengths ~5K-131K tokens (mean ~27K). 12+ programming languages. Tool call delays: 0.1s-5s (median ~1s).

## SLO Tiers

| Model | SLO Tier | P25 Output Speed | P95 TTFT |
|-------|----------|-----------------|----------|
| DeepSeek V4 Pro (max) | SLO #1 | 20 t/s | 10s |
| DeepSeek V4 Pro (max) | SLO #2 | 60 t/s | 5s |
| DeepSeek V4 Pro (max) | SLO #3 | 180 t/s | 3s |
| gpt-oss-120b (high) | SLO #1 | 100 t/s | 5s |
| gpt-oss-120b (high) | SLO #2 | 250 t/s | 3s |
| gpt-oss-120b (high) | SLO #3 | 500 t/s | 2s |
| gpt-oss-120b (high) | SLO #4 | 2,000 t/s | 1s |

## Test Execution

Binary search after exponential ramp. Each phase: ≥30 trajectories completed, ≥3 trajectories per agent, ≥10 min steady state. Results normalized per accelerator, per system, and per MW.

---
type: concept
---

# AA-AgentPerf

AA-AgentPerf is a hardware benchmark that measures how many active agents an inference deployment can support simultaneously while meeting per-agent performance SLOs (Service Level Objectives). It bridges the gap between standard API benchmarks (single-user experience) and system load tests (raw throughput) by evaluating realistic multi-turn agentic workloads with variable context, reasoning, and tool call delays.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/agentperf]] | Full methodology page covering dataset, SLO tiers, and test execution protocol | 2026-07-21 |
| [[sources/performance-benchmarking]] | Source of serverless API benchmarking data used to derive SLO tiers | 2026-07-21 |
| [[sources/system-load-test]] | Complementary benchmark — AA-SLT measures raw throughput, AgentPerf measures agentic throughput | 2026-07-21 |

## Key details

### Dataset: real agentic trajectories
Trajectories collected from the **OpenCode** harness using three models:
- DeepSeek V3.2
- GLM 4.7
- Kimi K2.5

Trajectory characteristics:
- Multi-turn coding sessions with interleaved reasoning, tool calls, and variable context
- Input lengths: ~5K to 131K tokens (mean ~27K)
- 12+ programming languages
- Tool call delays: 0.1s to 5s (median ~1s) — realistic, not instantaneous

### Market-derived SLO tiers
SLO thresholds are derived from AA serverless API benchmarking data, reflecting what real serverless users experience:

**DeepSeek V4 Pro (max) tiers:**
| SLO Tier | P25 Output Speed | P95 TTFT |
|----------|-----------------|----------|
| SLO #1 | 20 t/s | 10s |
| SLO #2 | 60 t/s | 5s |
| SLO #3 | 180 t/s | 3s |

**gpt-oss-120b (high) tiers:**
| SLO Tier | P25 Output Speed | P95 TTFT |
|----------|-----------------|----------|
| SLO #1 | 100 t/s | 5s |
| SLO #2 | 250 t/s | 3s |
| SLO #3 | 500 t/s | 2s |
| SLO #4 | 2,000 t/s | 1s |

Different SLO tier counts for different models reflect their distinct performance profiles. gpt-oss-120b's 4 tiers (vs. DeepSeek V4 Pro's 3) indicate a wider range of achievable performance levels.

### Test execution protocol
1. **Exponential ramp:** concurrency increases exponentially to find the approximate ceiling
2. **Binary search:** narrows to the exact maximum concurrent agents that meet SLOs
3. **Per-phase requirements:** ≥30 trajectories completed, ≥3 trajectories per agent, ≥10 minutes steady state
4. **Sustained concurrent load:** agents maintain continuous in-flight requests throughout

### Normalization
Results are normalized across three dimensions:
- **Per accelerator** — efficiency per hardware unit
- **Per system** — total system capacity
- **Per MW** — energy efficiency, enabling carbon-aware deployment comparisons

### Continuous updates
The benchmark is continuously updated as new hardware and software become available, ensuring relevance to current deployment options.

## Relationships
- [[concepts/aa-slt]] — complementary benchmark; AA-SLT measures raw API throughput, AA-AgentPerf measures agentic workload capacity
- [[concepts/output-speed]] — SLO tiers defined by P25 Output Speed and P95 TTFT
- [[sources/performance-benchmarking]] — source of SLO tier data from serverless API benchmarks

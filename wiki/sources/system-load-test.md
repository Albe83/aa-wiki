---
type: source
date: 2026-07-21
source_file: raw/system-load-test.md
status: processed
---

# System Load Test (AA-SLT) Methodology

**Source:** https://artificialanalysis.ai/methodology/system-load-test
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing the AA-SLT (System Load Test), Artificial Analysis's benchmark for measuring system performance under sustained load. Unlike standard API performance benchmarks that measure single prompts or fixed batches, the AA-SLT maintains a constant number of parallel queries: when one finishes, another starts immediately, ensuring stable load with minimal variance.

The test proceeds in 3-minute phases at increasing concurrency (1, 2, 4, 8, 16, 32, 64, then +64 increments) until reaching the system's maximum throughput. Each query uses 1,000 input tokens and 1,000 output tokens with streaming enabled. Key metrics are aggregate throughput, response rate, end-to-end latency, and output speed per query.

## Key points

- Sustained load: queries replaced immediately upon completion to maintain constant concurrency
- 3-minute phases at increasing concurrency: 1, 2, 4, 8, 16, 32, 64, then +64
- Standardized workload: 1,000 input tokens, 1,000 output tokens, streaming enabled
- 4 key metrics: System Output Throughput, Response Rate, End-to-End Latency, Output Speed per Query
- Test scales until system saturation to find the throughput ceiling
- Phased approach with ramp-up and cool-down excluded from measurements

## Entities mentioned

_none_

## Concepts mentioned

- [[concepts/aa-slt]] — Artificial Analysis system load benchmark
- [[concepts/output-speed]] — output speed and latency metrics under load

## Related sources

- [[sources/methodology]] — general AA methodology
- [[sources/performance-benchmarking]] — standard API performance benchmarks (single and parallel load)
- [[sources/agentperf]] — hardware benchmark for sustained agentic workloads

## My notes

- AA-SLT is complementary to standard performance benchmarks: those measure single-user experience, this measures system capacity
- The "replaced query" methodology is more realistic than a fixed batch because it simulates a continuous user flow
- Interesting comparison with agentperf: both measure load, but AA-SLT is for serverless APIs, agentperf for dedicated deployments

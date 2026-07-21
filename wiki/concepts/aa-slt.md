---
type: concept
---

# AA System Load Test (AA-SLT)

The AA System Load Test (AA-SLT) is a benchmark that measures AI inference system performance under sustained concurrent load. Unlike AA's standard API performance benchmarks (which measure single or fixed-batch prompt performance), AA-SLT maintains constant parallel query pressure to find a system's throughput ceiling. It is designed for evaluating dedicated inference deployments and systems, not serverless API endpoints.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/system-load-test]] | Full methodology page covering phased approach, metrics, and technical parameters | 2026-07-21 |
| [[sources/performance-benchmarking]] | Complementary benchmark — measures single-user and 10-parallel experience vs. system saturation | 2026-07-21 |
| [[sources/methodology]] | General AA methodology, included as one of 13 detailed methodology areas | 2026-07-21 |

## Key details

### Methodology: sustained load
When a query finishes, another is immediately sent — ensuring a fixed number of parallel queries at all times with minimal variance. This simulates a continuous stream of users rather than a single batch, providing more realistic system load measurements.

### Phased concurrency scaling
The test proceeds through phases of increasing concurrency:
- **Phases:** 1, 2, 4, 8, 16, 32, 64
- **Beyond 64:** increments of +64 until the throughput ceiling is reached
- **Phase duration:** 3 minutes per phase (excluding ramp-up and cool-down)
- **Termination:** test runs until throughput plateaus — indicating the system's maximum capacity

### Workload specification
- 1,000 input tokens per query
- 1,000 output tokens per query
- Streaming enabled
- Standardized workload ensures comparability across systems

### Key metrics
1. **System Output Throughput:** average aggregate output tokens per second across all concurrent requests — the primary capacity metric
2. **Response Rate:** proportion of queries that receive responses (≥1 output token) — measures system reliability under load
3. **End-to-End Latency per Query:** median end-to-end response time per concurrency phase — shows latency degradation as load increases
4. **Output Speed per Query:** median output tokens per second after the first token, per concurrency phase — shows per-query throughput degradation under load

### Throughput ceiling
The test runs until throughput stops scaling with additional concurrency. The throughput ceiling is the maximum sustained output rate the system can achieve, after which adding more parallel queries only increases latency without increasing total throughput.

## Relationships
- [[concepts/aa-agentperf]] — complementary benchmark; AA-SLT measures raw API throughput capacity, AA-AgentPerf measures agentic workload capacity
- [[concepts/output-speed]] — key metrics include Output Speed per Query and System Output Throughput
- [[sources/performance-benchmarking]] — standard API performance benchmarks measure single-user experience; AA-SLT measures system capacity

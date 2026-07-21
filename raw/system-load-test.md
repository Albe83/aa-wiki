# System Load Test (AA-SLT) Methodology

**Source:** https://artificialanalysis.ai/methodology/system-load-test
**Fetched:** 2026-07-21

## Overview

Measures system performance by maintaining fixed numbers of parallel queries. When a query finishes, another is immediately sent, ensuring stable load with minimal variance.

Phased approach: each phase runs 3 minutes, concurrency scales (1, 2, 4, 8, 16, 32, 64, then +64 increments) until throughput ceiling is reached.

## Key Specifications

- **Phase duration:** 3 minutes (excluding ramp-up/cool-down)
- **Concurrency levels:** 1, 2, 4, 8, 16, 32, 64, then increments of 64
- **Workload:** 1,000 input tokens, 1,000 output tokens per query
- **Streaming:** Enabled

## Key Metrics

- **System Output Throughput:** Average aggregate output tokens/second across all concurrent requests
- **Response rate:** Proportion of queries receiving responses (≥1 output token)
- **End-to-End Latency per Query:** Median end-to-end response time per concurrency phase
- **Output Speed per Query:** Median output tokens/second after first token, per concurrency phase

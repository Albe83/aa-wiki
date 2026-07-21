---
type: source
date: 2026-07-21
source_file: raw/performance-benchmarking.md
status: processed
---

# Artificial Analysis Language Model API Performance Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/performance-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing how Artificial Analysis measures language model API performance. The guiding principle is to measure the end-to-end experience of the end user: prompt sent, response received. Diversified workloads are used (1K, 10K, 100K input tokens, vision) and two load scenarios (single prompt, 10 parallel prompts), with tests repeated regularly (up to 8 times per day).

The methodology covers key definitions (TTFT, Output Speed, Response Time), technical details (us-central1 server, API parameters, o200k_base tokenization), representation metrics (P50 median over 72 hours), and known limitations. It also includes integrity terms that prohibit providers from treating AA traffic differently from ordinary users.

## Key points

- 4 workload types: 1K input tokens, 10K (default), 100K, vision (1MP image)
- 2 load scenarios: single prompt, 10 simultaneous parallel prompts
- Test frequency: every 3 hours for main workloads, 1x/day for parallel, 1x/week for 100K
- Unique prompts at each test run to avoid caching effects and measure real output speed variations
- P50 median over 72 hours as the representative metric (14 days for 100K workload)
- Servers in Google Cloud us-central1-a; mix of anonymous, authenticated, and benchmark key accounts
- Temperature 0.6 for reasoning models, 0 for non-reasoning; top_p 1
- o200k_base tokenization for performance benchmarking; provider-reported for Intelligence Index costs
- Integrity: providers must not detect or treat AA traffic differently

## Entities mentioned

- [[entities/orgs/openai]] — OpenAI Python library used for compatible providers; o200k_base tokenizer

## Concepts mentioned

- [[concepts/output-speed]] — TTFT, Time to First Answer Token, Output Speed, Response Time
- [[concepts/token]] — o200k_base vs native token tokenization; tokenizer efficiency
- [[concepts/cost-per-task]] — relationship with pricing via provider-reported tokens

## Related sources

- [[sources/methodology]] — general AA methodology, standard definitions
- [[sources/intelligence-benchmarking]] — intelligence metrics to which costs are related

## My notes

- v2.2.0 (March 2026) moved the default workload from 1K to 10K input tokens: a signal that real prompts are getting longer
- The TTFT / Time to First Answer Token distinction is critical for reasoning models — without it, reasoning time would be confused with response latency
- Integrity terms are stringent: no dedicated hardware, priority queues, or non-public configurations for AA traffic

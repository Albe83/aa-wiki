---
type: source
date: 2026-07-21
source_file: raw/guide.md
status: processed
---

# Using Artificial Analysis — Guide

**Source:** https://artificialanalysis.ai/guide
**Ingested:** 2026-07-21
**Type:** article

## Summary

Practical guide to using Artificial Analysis for model and provider selection. AA outlines a three-step decision process: (1) start from the use case, (2) choose the model, (3) choose the provider. The emphasis is on trade-offs between quality, speed, price, latency, and context window.

The concrete example is a low-ARPU consumer website: high output speed, low latency, and low price are needed. The Intelligence Index is presented as a generalist quality indicator, to be complemented with use-case-specific testing.

## Key points

- The AA decision process: use case → model → provider (in this order)
- The Intelligence Index is a generalist indicator; for final decisions, custom tests on the use case are needed
- Model selection precedes provider selection because providers vary in the models they host
- When choosing a provider, what matters: price, throughput, latency, OpenAI compatibility, rate limits, context window
- Key trade-off: quality vs speed vs price vs latency vs context window

## Entities mentioned

- [[entities/orgs/deepseek]] — DeepSeek V4 Pro used as an example on the providers page

## Concepts mentioned

- [[concepts/intelligence-index]] — generalist indicator of response quality
- [[concepts/model-selection-framework]] — use case → model → provider process
- [[concepts/cost-per-task]] — relevant for the quality/price trade-off
- [[concepts/output-speed]] — relevant for the speed/quality trade-off

## Related sources

- [[sources/methodology]] — defines the metrics the selection process is based on

## My notes

- Short but pragmatic guide. The "use-case first" framework is the organizing principle of the entire AA site
- The advice to develop a shortlist and test on the specific use case is an important caveat: AA benchmarks are a compass, not a replacement for testing

---
type: source
date: 2026-07-21
source_file: raw/methodology.md
status: processed
---

# Artificial Analysis Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology
**Ingested:** 2026-07-21
**Type:** article

## Summary

Official Artificial Analysis methodology page. Defines the scope of AA benchmarking (intelligence, quality, performance, price) and the standard terminology used throughout the site. The guiding principle is to measure real user experience, not theoretical maximum performance on specific hardware.

The page lists 13 detailed methodology areas (LLM intelligence, API performance, capability indices, system load test, coding agents, agent perf, text-to-image, video, music, STT, TTS, speech-to-speech, openness index) and 17 key definitions that form the core vocabulary for interpreting all of the site's data.

## Key points

- AA benchmarks both proprietary and open weights models, API endpoints and dedicated systems
- Performance is measured end-to-end as real customer experience, not theoretical maximum
- Serverless endpoints are defined as pay-per-use (price per token), not flat-rate
- OpenAI Tokens (tiktoken o200k_base) are the standard unit for speed comparisons
- Prices are expressed in native tokens; blended price assumes a 7:2:1 ratio (cache hit : input : output)
- Cost per Task is weighted on the relative weights of benchmarks in the Intelligence Index
- For reasoning models, a distinction is made between Time to First Token (first reasoning token) and Time to First Answer Token (first response token)
- Average Reasoning Tokens is calculated over 60 varied prompts (personal, commercial, coding, math, science) from MMLU Pro, AIME 2025, LiveCodeBench

## Entities mentioned

- [[entities/orgs/openai]] — cited as an example of Model Creator and Provider (GPT-4)
- [[entities/orgs/meta]] — cited as an example of Model Creator (Llama 3)
- [[entities/orgs/aws]] — cited as an example of Provider (AWS Bedrock)
- [[entities/orgs/together-ai]] — cited as an example of Provider

## Concepts mentioned

- [[concepts/model-ecosystem]] — Model, Model Creator, Endpoint, Provider, System distinction
- [[concepts/token]] — OpenAI Tokens vs Native Tokens, tokenizer
- [[concepts/cost-per-task]] — weighted cost per task calculation in the Intelligence Index
- [[concepts/output-speed]] — performance metrics: TTFT, Output Speed, Response Time
- [[concepts/open-weights]] — definition and distinction from open-source
- [[concepts/serverless]] — definition in the context of LLM APIs
- [[concepts/blended-price]] — 7:2:1 ratio for blended price calculation

## Related sources

_(none at this time — first ingested source)_

## My notes

- This is the foundational source: it defines the core vocabulary for interpreting every other AA page
- The 13 linked methodology areas are potential future sources to download and ingest
- The Model/Endpoint/Provider distinction is crucial for understanding API provider performance graphs

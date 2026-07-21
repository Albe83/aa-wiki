# Artificial Analysis Language Model API Performance Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/performance-benchmarking
**Fetched:** 2026-07-21

## Overview

Measuring LLM performance requires sending the LLM a prompt and measuring the characteristics of its output. We use a variety of test workloads to test and measure LLM performance.

### Workload Types

| Type | Description |
|------|-------------|
| 1k input token | Approximately 1,000 input tokens, at least 1,000 answer tokens |
| 10k input token | Approximately 10,000 input tokens, at least 1,500 answer tokens (default benchmark) |
| 100k input token | Approximately 100,000 input tokens, at least 2,000 answer tokens |
| Vision workload | A single 1 megapixel image and approximately 1,000 input tokens, 1,000 output tokens |

### Load Scenarios

| Scenario | Description |
|----------|-------------|
| Single prompt | One prompt is sent to the model's API at a time |
| Parallel prompts | 10 prompts are sent to the model's API simultaneously |

### Testing Frequency

- 1k, 10k, vision: 8 times per day (~every 3 hours)
- Parallel workload: once per day at random time (10 concurrent requests of 1k input)
- 100k input: once per week

### Prompt Generation

Every test run uses a unique prompt, combining long-form input content (articles) with varied tasks (explanation/summarization, Q&A, comparative analysis, translation, visual artifact generation). Prompt diversity is important because techniques like speculative decoding cause variation in output speeds depending on output type.

### Measurement Representation

Median (P50) over past 72 hours for sustained performance. Exception: 100k workload uses median over past 14 days.

## Key Definitions

- **Time to First Token:** Seconds between sending request and receiving first token. For reasoning models = first reasoning token.
- **Time to First Answer Token:** Seconds to first answer token after reasoning phase.
- **Output Speed:** Average tokens per second after first token received.
- **Total Response Time for 100 Output Tokens:** Synthetic metric from TTFT + Output Speed.
- **End-to-End Response Time:** Total time including input processing, reasoning, and answer generation.
- **Average Reasoning Tokens:** Avg reasoning tokens across 60 diverse prompts (MMLU Pro, AIME 2025, LiveCodeBench). Default 2k if not available.

## Technical Details

- **Server Location:** Google Cloud us-central1-a
- **Test Accounts:** Mix of anonymous accounts, credited accounts, and provider-provided benchmark keys. Independent validation accounts ensure no performance manipulation.
- **API Libraries:** OpenAI Python library for OpenAI-compatible providers; provider-recommended clients otherwise.
- **API Parameters:** temperature 0.6 (reasoning) / 0 (non-reasoning), top_p 1
- **Token Measurement:** o200k_base for performance benchmarking; provider-reported tokens for Intelligence Index cost
- **Output Speed Calculation (reasoning models):** Last 80% of answer chunks for models that don't expose reasoning tokens

## Known Limitations

- **Tokenizer Efficiency:** Different tokenizers mean pricing not directly comparable
- **Quantization:** May affect quality; moving toward full disclosure
- **Server Location and TTFT:** us-central1 may advantage/disadvantage certain providers

## Version History

**v2.2.0 (March 2026):** Upgraded prompts with broader content; default workload changed to 10k input tokens (was 1k); deprecated 100-token workload.

## Integrity Terms

- AA traffic must be served on same publicly available configuration as any ordinary developer
- Providers must not detect/fingerprint AA traffic or serve it differently
- No dedicated hardware, capacity pools, priority queues, or non-public configurations
- Violations may result in delisting, suspension, or public disclosure
- Regular consistency checks with independent test accounts

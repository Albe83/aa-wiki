---
type: concept
---

# Output Speed and Performance Metrics

Performance metrics for LLM inference APIs defined by Artificial Analysis.

## Definitions

### Time to First Token (TTFT)
Time (seconds) between sending the request and receiving the first token. For reasoning models, this is the first reasoning token.

### Time to First Answer Token
Time (seconds) between sending the request and the first response token (after any reasoning phase).

### Output Speed (output tokens per second)
Average number of tokens received per second, after receiving the first token. Measured in OpenAI tokens.

### Total Response Time for 100 Output Tokens
Time to generate 100 output tokens, computed synthetically from TTFT + Output Speed.

### End-to-End Response Time
Total time to receive a complete response, including input processing, reasoning, and response generation.

### Average Reasoning Tokens
Average number of reasoning tokens produced by reasoning models before the response. Computed over 60 varied prompts (personal, commercial, coding, math, science) from MMLU Pro, AIME 2025, LiveCodeBench. If unavailable, 2k reasoning tokens are assumed.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Official AA definitions of performance metrics | 2026-07-21 |

## Current synthesis

AA metrics measure real user experience, not maximum theoretical throughput. The distinction between TTFT and Time to First Answer Token is especially relevant for reasoning models, where the "thinking" phase can last seconds before the actual response begins.

## Relationships
- [[concepts/token]] — speed metrics use OpenAI Tokens as the standard unit

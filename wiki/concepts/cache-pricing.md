---
type: concept
---

# Cache Pricing

Pricing models for prompt caching in LLM APIs, which vary significantly across providers.

## Models by provider

| Provider | Cache Hit | Cache Write | Cache Storage |
|----------|-----------|-------------|---------------|
| Anthropic | Sì | Sì (separata, diversa per TTL 5min/1h) | No |
| Google (Vertex/Gemini) | Sì | No | Sì (per ora) |
| OpenAI, DeepSeek, altri | Sì | No | No |

## Impact on blended price

The AA [[concepts/blended-price|blended price]] assumes a 7:2:1 ratio (cache hit : input : output), but the actual cost depends on the provider and specific use case.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definition of caching models by provider | 2026-07-21 |
| [[sources/performance-benchmarking]] | Token measurement uses provider-reported counts for the Intelligence Index | 2026-07-21 |

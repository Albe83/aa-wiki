---
type: concept
---

# Cache Pricing

Modelli di pricing per il caching dei prompt nelle API LLM, che variano significativamente tra provider.

## Modelli per provider

| Provider | Cache Hit | Cache Write | Cache Storage |
|----------|-----------|-------------|---------------|
| Anthropic | Sì | Sì (separata, diversa per TTL 5min/1h) | No |
| Google (Vertex/Gemini) | Sì | No | Sì (per ora) |
| OpenAI, DeepSeek, altri | Sì | No | No |

## Impatto sul blended price

Il [[concepts/blended-price|blended price]] AA assume un rapporto 7:2:1 (cache hit : input : output), ma il costo reale dipende dal provider e dal caso d'uso specifico.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizione dei modelli di caching per provider | 2026-07-21 |
| [[sources/performance-benchmarking]] | Token measurement usa provider-reported counts per l'Intelligence Index | 2026-07-21 |

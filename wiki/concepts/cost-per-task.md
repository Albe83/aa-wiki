---
type: concept
---

# Cost per Task and Pricing

Cost metric developed by Artificial Analysis to compare the real cost of using models.

## Definitions

### Price (Input/Output)
The price charged by a provider per input token sent and per output token received. Prices are the currently declared provider rates.

### Blended Price
Combined price assuming a 7:2:1 ratio of cache hit, input, and output tokens, to facilitate comparison.

### Cost per Task
Weighted average cost (USD) to complete an Intelligence Index task. Calculated as:

```
Cost per Task = Σ (prezzo_input × token_input + prezzo_cache × token_cache + prezzo_output × token_output) × peso_benchmark / numero_task
```

The cost reflects actual token consumption: models that produce longer responses or more reasoning tokens have a higher cost per task, even at the same per-token price.

### Cost to Run Intelligence Index
Total cost (USD) to run all Intelligence Index evaluations, calculated at first-party provider prices.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Official AA pricing and cost definitions | 2026-07-21 |

## Current synthesis

Cost per Task is the most realistic metric for comparing model costs because it incorporates verbosity. Two models with the same per-token price can have very different Cost per Task if one produces longer responses.

## Relationships
- [[concepts/blended-price]] — the 7:2:1 ratio used for blended price calculation
- [[concepts/cache-pricing]] — detail on cache pricing models by provider

---
type: concept
---

# Model Selection Framework

Decision-making process recommended by Artificial Analysis for choosing models and API providers.

## The three steps

1. **Start from the use case** — Identify which dimensions to optimize: quality, speed, price, latency, context window. Example: a low-ARPU consumer site prioritizes speed and low price over maximum quality.

2. **Choose the model** — Use the [[concepts/intelligence-index|Intelligence Index]] as a generalist indicator, then develop a shortlist of candidate models to test on the specific use case. Custom testing is essential: AA benchmarks point the way but do not replace validation.

3. **Choose the provider** — Once the model is chosen, compare providers on: price, throughput, latency, OpenAI compatibility, rate limits, context window. Performance between providers can vary significantly.

## Rationale

Models and providers present inevitable trade-offs. The use case → model → provider order avoids locking into a provider before identifying the right model, since providers do not host all models.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/guide]] | Official AA framework for model and provider selection | 2026-07-21 |

## Current synthesis

The framework is the organizing principle of the entire AA site. Every chart and leaderboard is designed to support one of these three decision steps.

# Text to Speech Benchmarking Methodology

**Source:** https://artificialanalysis.ai/text-to-speech/methodology
**Fetched:** 2026-07-21

## Scope

Benchmarks TTS models on quality, performance, and price. Serverless endpoints only.

## Key Metrics

- **Quality Elo:** From TTS Arena user votes (Bradley-Terry MLE, similar to LMSYS Chatbot Arena)
- **Price per 1M Characters:** Normalized across pricing models (per-char, subscription, token-based, output duration, per-byte, inference time). No temporary discounts.
- **Generation Time:** Median over trailing 14 days, 4x daily at random times, ~500 char prompts, batch size 1, includes URL download.

## Controlled Voices Arena

Uses voice cloning to standardize 8 reference voices (2 US female, 2 US male, 2 UK female, 2 UK male). Separates voice preference from model quality (naturalness, audio quality, pronunciation, pacing, prosody).

## Provider Voices Arena

Evaluates models using their own publicly available voices (8 voices: male/female x US/UK combinations). Reflects typical user experience.

## Independence

No compensation from providers.

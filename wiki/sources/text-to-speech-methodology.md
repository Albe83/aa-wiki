---
type: source
date: 2026-07-21
source_file: raw/text-to-speech-methodology.md
status: processed
---

# Text to Speech Benchmarking Methodology

**Source:** https://artificialanalysis.ai/text-to-speech/methodology
**Ingested:** 2026-07-21
**Type:** article

## Summary

Artificial Analysis benchmarks text-to-speech (TTS) models on quality, performance, and price, evaluating only [[concepts/serverless]] endpoints. Quality is measured via Elo scores from the [[concepts/text-to-speech-arena]] using blind pairwise user votes (Bradley-Terry MLE, following the LMSYS Chatbot Arena model). Two complementary arena tracks isolate different quality dimensions: the Controlled Voices Arena uses voice cloning to standardize 8 reference voices (2 male × 2 female × US/UK), isolating model quality from voice preference; the Provider Voices Arena evaluates models using their own native voices to reflect typical user experience.

Performance metrics include Price per 1M Characters (normalized across per-character, subscription, token-based, output-duration, per-byte, and inference-time pricing) and Generation Time (median over trailing 14 days, 4× daily sampling, ~500 character prompts, batch size 1, including URL download time). Neither temporary discounts nor provider compensation is accepted.

## Key points

- Two TTS Arena tracks: Controlled Voices (isolates model quality) and Provider Voices (real-world experience)
- 8 reference voices standardized across gender and accent (US/UK) for controlled testing
- Quality Elo from Bradley-Terry MLE pairwise human preference voting
- Price normalized across 6+ billing models per million characters
- Generation Time sampled 4× daily, batch size 1, includes full pipeline to URL download
- [[concepts/serverless]] endpoints only — excludes dedicated-instance deployments
- No temporary pricing discounts or provider compensation accepted

## Entities mentioned

- [[entities/orgs/artificial-analysis]] — benchmarking platform

## Concepts mentioned

- [[concepts/text-to-speech-arena]] — blind pairwise human preference voting arena for TTS
- [[concepts/serverless]] — deployment model required for TTS benchmarks
- [[concepts/bradley-terry]] — statistical model for deriving Elo scores from pairwise votes

## Related sources

- [[sources/methodology]] — parent methodology page

## My notes

The Controlled vs Provider Voices split is a well-designed methodological choice. By cloning voices across models, the Controlled Arena removes the confound of whether users prefer a specific voice rather than the model's synthesis quality. The Provider Arena then adds ecological validity. Together they give a fuller picture than either alone.

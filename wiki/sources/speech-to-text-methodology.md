---
type: source
date: 2026-07-21
source_file: raw/speech-to-text-methodology.md
status: processed
---

# Speech to Text Benchmarking Methodology

**Source:** https://artificialanalysis.ai/speech-to-text/methodology
**Ingested:** 2026-07-21
**Type:** article

## Summary

Artificial Analysis benchmarks speech-to-text (STT) models using its proprietary [[concepts/aa-wer]] metric suite. The primary quality metric is Word Error Rate (WER), computed as (Substitutions + Insertions + Deletions) / Words in Reference. Three datasets compose AA-WER v2.2 (~8 hours total audio): a proprietary held-out voice agent dataset (AA-AgentTalk, 50% weight), cleaned EU parliamentary speech (VoxPopuli-Cleaned-AA, 25%), and cleaned corporate earnings calls (Earnings22-Cleaned-AA, 25%).

Performance metrics include Speed Factor (audio duration / API response time, where >1 means faster than real-time), Streaming Latency (Time to Final Transcript and Time to First Partial Transcript), and Price per 1,000 Minutes. Streaming evaluation sends audio in 20ms chunks with two transcript types (Partials and Finals), using SileroVAD for forced endpointing. Transcripts are normalized via the OpenAI Whisper normalizer plus custom rules covering contractions, numbers, punctuation, currency, IDs, UK/US spelling, and more.

## Key points

- Word Error Rate is the core quality metric: (S+I+D) / reference word count
- AA-WER v2.2: 3 datasets, ~8 hours, weighted 50/25/25 toward voice agent use cases
- AA-AgentTalk is proprietary and held-out, focused on voice agent scenarios
- Speed Factor >1 means faster than real-time processing
- Streaming: 20ms audio chunks, partial + final transcripts, SileroVAD endpointing
- Price normalized across billing models (duration, tokens, subscription, processing time)
- Custom text normalization built on OpenAI Whisper normalizer

## Entities mentioned

- [[entities/orgs/artificial-analysis]] — benchmarking platform

## Concepts mentioned

- [[concepts/aa-wer]] — proprietary word error rate benchmark suite for STT evaluation
- [[concepts/speech-to-text]] — the STT task space being benchmarked
- [[concepts/word-error-rate]] — core metric formula: substitutions + insertions + deletions over reference words
- [[concepts/streaming-latency]] — time to first partial and final transcript, critical for real-time use

## Related sources

- [[sources/methodology]] — parent methodology page

## My notes

The v2.0 shift to a voice-agent-focused benchmark (AA-AgentTalk at 50% weight) reflects the market pivot from transcription to conversational AI. The streaming evaluation with partial transcripts is notable — many STT benchmarks only measure final transcript quality, missing the latency dimension that matters for real-time interactions.

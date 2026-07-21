---
type: concept
---

# AA Speech-to-Text

Artificial Analysis's benchmarking framework for speech recognition (ASR) models. Covers both **batch transcription** and **streaming transcription** evaluation. The primary quality metric is the **AA-WER Index** (Word Error Rate), computed as (Substitutions + Insertions + Deletions) / Words in Reference. Performance is measured through Speed Factor (batch) and Streaming Latency (Time to Final Transcript and Time to First Partial Transcript). Price is normalized across diverse billing models per 1,000 minutes of audio.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | Full specification: WER datasets, normalization rules, streaming evaluation, pricing normalization | 2026-07-21 |

## Key details

### AA-WER Index v2.2 (May 2026+)
Three datasets, ~8 hours total audio, weighted toward voice agent use cases:

| Dataset | Duration | Samples | Weight | Description |
|---------|----------|---------|--------|-------------|
| AA-AgentTalk | ~250 min | 469 | 50% | Proprietary held-out dataset, voice agent focused |
| VoxPopuli-Cleaned-AA | ~119 min | 628 | 25% | Cleaned EU parliamentary speech |
| Earnings22-Cleaned-AA | ~115 min | 6 | 25% | Cleaned corporate earnings calls |

### WER Calculation
- Formula: (Substitutions + Insertions + Deletions) / Words in Reference
- Lower is better
- Transcripts normalized via OpenAI Whisper normalizer + custom AA rules covering contractions, numbers, punctuation, currency, IDs, time formatting, UK/US spelling, codes/symbols

### Speed Factor (Batch)
- Audio Duration / API Response Time
- Speed Factor > 1 means faster than real-time processing
- Higher is better for throughput-oriented workloads

### Streaming Latency
- Audio streamed in **20ms chunks**
- Two transcript types: Partials (unconfirmed, evolving) and Finals (confirmed, stable)
- Forced endpointing via SileroVAD
- Separate WER reported for final and partial transcripts
- **Time to Final Transcript:** Complete utterance latency
- **Time to First Partial Transcript:** First-unconfirmed-output latency, critical for real-time display

### Price Normalization
- Price per 1,000 minutes of audio
- Normalized across billing models: per-duration, per-token, per-processing-time, subscription
- No temporary discounts accepted

### Version History
- **v2.2 (May 2026):** Additional normalization rules; launched streaming STT evaluation
- **v2.1 (Apr 2026):** Expanded normalization (IDs, ranges, codes)
- **v2.0 (Feb 2026):** Added AA-AgentTalk; cleaned transcripts; removed AMI SDM
- **v1.0 (Sep 2025):** Initial release with AMI SDM, VoxPopuli, Earnings22

## Relationships
- [[concepts/aa-wer]] — The core word error rate benchmark suite for STT v2.2
- [[concepts/word-error-rate]] — The foundational metric: substitutions + insertions + deletions over reference word count
- [[concepts/streaming-latency]] — Key performance dimension for real-time STT use cases
- [[concepts/speech-to-speech-index]] — Complementary benchmark for the reverse direction (audio-to-audio synthesis)
- [[entities/orgs/artificial-analysis]] — developer of AA-WER and the STT benchmarking framework

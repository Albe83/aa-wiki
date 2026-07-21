---
type: concept
---

# AA-WER Index v2.2

The AA-WER Index v2.2 is Artificial Analysis's proprietary Word Error Rate benchmark for speech-to-text (STT) models. It evaluates transcription quality across three datasets weighted toward voice agent use cases, with a custom normalization pipeline and streaming evaluation support. WER is calculated as (Substitutions + Insertions + Deletions) / Words in Reference.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | Full methodology page covering datasets, normalization, streaming eval, and pricing | 2026-07-21 |

## Key details

### Dataset composition (v2.2, May 2026+)
Total: ~8 hours of audio (~250 min AgentTalk + ~119 min VoxPopuli + ~115 min Earnings22).

| Dataset | Duration | Samples | Weight | Description |
|---------|----------|---------|--------|-------------|
| AA-AgentTalk | ~250 min | 469 | 50% | Proprietary, held-out; voice agent focused scenarios |
| VoxPopuli-Cleaned-AA | ~119 min | 628 | 25% | EU parliamentary speech, cleaned transcripts |
| Earnings22-Cleaned-AA | ~115 min | 6 | 25% | Corporate earnings calls, cleaned transcripts |

The 50% weight on AA-AgentTalk reflects the market shift from general transcription to conversational AI and voice agent use cases.

### Normalization pipeline
Transcripts are normalized before WER calculation using:
- **OpenAI Whisper normalizer** as the base
- **Custom rules** for: contractions, numbers (written vs. numeric), punctuation, currency formatting, IDs, time formatting, UK/US spelling variants, codes and symbols

This multi-layer normalization ensures fair comparisons by standardizing formatting differences that don't affect semantic correctness.

### Streaming evaluation
Audio is streamed in **20ms chunks** with two transcript types:
- **Partials:** unconfirmed interim transcripts — critical for real-time UX
- **Finals:** confirmed segments — the definitive transcription

Forced endpointing is handled by **SileroVAD** (Voice Activity Detection). Separate WER is reported for final and partial transcripts, with partial WER capturing the accuracy of real-time display.

### Performance metrics (reported alongside WER)
- **Speed Factor:** Audio Duration / API Response Time. >1 means faster than real-time processing.
- **Streaming Latency:** Time to Final Transcript and Time to First Partial Transcript — critical for real-time conversational use.
- **Price per 1,000 Minutes:** Normalized across diverse billing models (duration-based, processing time, per-token, subscription).

### Version history
- **v2.2 (May 2026):** Additional normalization rules; launched streaming STT evaluation
- **v2.1 (April 2026):** Expanded normalization (IDs, ranges, codes, etc.)
- **v2.0 (February 2026):** Added AA-AgentTalk; cleaned transcripts for VoxPopuli/Earnings22; removed AMI SDM dataset
- **v1.0 (September 2025):** Initial release with AMI SDM, VoxPopuli, Earnings22

The v2.0 transition replaced meeting-transcription (AMI SDM) with voice-agent audio (AA-AgentTalk), reflecting the market pivot from transcription to conversational AI.

## Relationships
- [[concepts/word-error-rate]] — core metric formula: (S+I+D) / reference word count
- [[concepts/streaming-latency]] — time to first partial and final transcript metrics
- [[concepts/speech-to-text]] — the STT task space being benchmarked

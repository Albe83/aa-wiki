# Speech to Text Benchmarking Methodology

**Source:** https://artificialanalysis.ai/speech-to-text/methodology
**Fetched:** 2026-07-21

## Key Metrics

- **AA-WER Index:** Word Error Rate = (Substitutions + Insertions + Deletions) / Words in Reference
- **Speed Factor (batch):** Audio Duration / API Response Time. >1 = faster than real-time
- **Streaming Latency:** Time to Final Transcript, Time to First Partial Transcript
- **Price per 1,000 Minutes:** Normalized across billing models (duration, processing time, tokens, subscription)

## WER Evaluation

### Datasets (AA-WER v2.2, May 2026+)
- **AA-AgentTalk** (proprietary, held-out): ~250 min, 469 samples, voice agent focused — 50% weight
- **VoxPopuli-Cleaned-AA:** ~119 min, 628 samples, EU parliamentary — 25% weight
- **Earnings22-Cleaned-AA:** ~115 min, 6 samples, corporate earnings calls — 25% weight

Total: ~8 hours audio. Weighted: 50% AgentTalk, 25% VoxPopuli, 25% Earnings22.

### Normalization
OpenAI Whisper normalizer + custom rules: contractions, numbers, punctuation, currency, IDs, time formatting, UK/US spelling, codes/symbols, etc.

### Streaming
Audio streamed in 20ms chunks. Two transcript types: Partials (unconfirmed) and Finals (confirmed). Forced endpointing via SileroVAD. Separate WER reported for final and partial transcripts.

## Version History

- **v2.2 (May 2026):** Additional normalization rules; launched streaming STT evaluation
- **v2.1 (April 2026):** Expanded normalization (IDs, ranges, codes, etc.)
- **v2.0 (Feb 2026):** Added AA-AgentTalk; cleaned transcripts for VoxPopuli/Earnings22; removed AMI SDM
- **v1.0 (Sep 2025):** Initial release with AMI SDM, VoxPopuli, Earnings22

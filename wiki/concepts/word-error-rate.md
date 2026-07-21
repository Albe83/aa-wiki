---
type: concept
---

# Word Error Rate (WER)

Standard metric for evaluating speech-to-text transcription accuracy. Measures the distance between the model transcription (hypothesis) and the human reference transcription (reference).

## Formula

```
WER = (Substitutions + Insertions + Deletions) / Words in Reference
```

Based on Levenshtein distance: the minimum number of substitutions, insertions, and deletions to transform the hypothesis into the reference.

## AA-WER Index

The [[concepts/aa-wer|AA-WER Index v2.2]] computes WER across 3 datasets (~8 hours total): AA-AgentTalk (50%), VoxPopuli-Cleaned-AA (25%), Earnings22-Cleaned-AA (25%). Results are aggregated as an audio-duration-weighted average.

Normalization uses the OpenAI Whisper normalizer with additional rules to handle equivalent formatting variants (numbers, dates, currencies, IDs, UK/US spelling, etc.).

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | Complete AA-WER v2.2 methodology | 2026-07-21 |

## Relationships
- [[concepts/aa-wer]] — AA's implementation of the WER benchmark
- [[concepts/speech-to-text]] — broader STT benchmarking context

---
type: concept
---

# VoxPopuli-Cleaned-AA

VoxPopuli-Cleaned-AA is a cleaned subset of the English VoxPopuli test dataset, released by Artificial Analysis as part of AA-WER v2.0. It carries a 25% weight in the [[concepts/aa-wer|AA-WER Index]].

**Public dataset:** https://huggingface.co/datasets/ArtificialAnalysis/VoxPopuli-Cleaned-AA

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | AA-WER v2.2 methodology: 628 samples, ~119 min, 25% weight | 2026-07-21 |

## Dataset properties

| Property | Value |
|----------|-------|
| Source | European Parliament proceedings (English) |
| Samples | 628 |
| Sample duration range | 5–38 seconds |
| Total duration | ~119 minutes |
| Language | English |
| License | Apache-2.0 |

## Motivation for cleaning

Reference transcripts in the original VoxPopuli test set contained inaccuracies — misspellings, misheard words, incorrect contractions. These errors penalized models that correctly transcribed the audio, artificially inflating WER scores. After cleaning, model WER on VoxPopuli went down by an average of **3.5 percentage points**.

## Correction methodology

- **Incorrect words:** Misspellings, misheard words, incorrect contractions corrected
- **Missed words:** Verbatim repetitions retained
- **Partial stuttering:** Incomplete word fragments removed (inherently ambiguous)
- **Grammar/tense:** Verbatim words kept even when grammatically incorrect

Elements already handled by the Whisper normalizer (capitalization, punctuation, filler words) were left unchanged.

## Relationships

- [[concepts/aa-wer]] — VoxPopuli-Cleaned-AA contributes 25% weight to AA-WER v2.0+
- [[concepts/aa-agenttalk]] — companion dataset (50% weight, voice agent speech)
- [[concepts/earnings22-cleaned-aa]] — companion dataset (25% weight, corporate earnings calls)
- [[concepts/speech-to-text]] — broader STT benchmarking context
- [[concepts/word-error-rate]] — core metric used for evaluation

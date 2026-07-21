---
type: concept
---

# Earnings22-Cleaned-AA

Earnings22-Cleaned-AA is a cleaned subset of the English Earnings-22 test dataset, released by Artificial Analysis as part of AA-WER v2.0. It carries a 25% weight in the [[concepts/aa-wer|AA-WER Index]] and represents the most challenging acoustic domain in the benchmark — corporate earnings calls with diverse speakers, accents, and technical financial language.

**Public dataset:** https://huggingface.co/datasets/ArtificialAnalysis/Earnings22-Cleaned-AA

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | AA-WER v2.2 methodology: 6 samples, ~115 min, 25% weight | 2026-07-21 |

## Dataset properties

| Property | Value |
|----------|-------|
| Source | Corporate earnings calls (global companies, diverse nationalities/accents) |
| Samples | 6 |
| Sample duration range | ~14–22 minutes |
| Total duration | ~115 minutes |
| Language | English |
| License | Apache-2.0 |

## Motivation for cleaning

Reference transcripts in the original Earnings22 test set contained significant inaccuracies. After cleaning, model WER on Earnings22 went down by an average of **5.6 percentage points** — the largest improvement among the three datasets. No models had higher WER after cleaning, confirming that corrections were universally beneficial.

## Correction methodology

- **Incorrect words:** Misspellings, misheard words, incorrect contractions corrected
- **Missed words:** Verbatim repetitions retained
- **Partial stuttering:** Incomplete word fragments removed
- **Grammar/tense:** Verbatim words kept even when grammatically incorrect

## Long-form audio handling

Due to their length (~14-22 minutes), Earnings22 samples may require chunking for models with input length limits. AA chunks Earnings22 starting with ~9-minute segments and reduces to ~30-second chunks only if needed, placing boundaries at speech pauses. Chunked results are concatenated and WER is computed on the combined transcript against the parent-call ground truth.

## Relationships

- [[concepts/aa-wer]] — Earnings22-Cleaned-AA contributes 25% weight to AA-WER v2.0+
- [[concepts/aa-agenttalk]] — companion dataset (50% weight, voice agent speech)
- [[concepts/voxpopuli-cleaned-aa]] — companion dataset (25% weight, parliamentary speech)
- [[concepts/speech-to-text]] — broader STT benchmarking context
- [[concepts/word-error-rate]] — core metric used for evaluation

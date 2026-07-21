---
type: source
date: 2026-07-21
source_file: raw/aa-wer-v2.md
status: processed
---

# AA-WER v2.0: Speech to Text Accuracy Benchmark

**Source:** https://artificialanalysis.ai/articles/aa-wer-v2
**Ingested:** 2026-07-21
**Type:** article

## Summary

Announcement article for AA-WER v2.0 (February 2026), a major update to Artificial Analysis's speech-to-text accuracy benchmark. Introduces AA-AgentTalk, a new proprietary held-out dataset focused on voice agent speech, alongside cleaned ground truth transcripts for VoxPopuli and Earnings22. Five key changes: new proprietary dataset (50% weighting), cleaned transcripts for public datasets, removal of AMI-SDM, improved text normalizer, and new evaluation weighting.

## Key points

- AA-AgentTalk: 469 samples (~250 min), 6 content categories, 17 accent groups, proprietary and held-out
- VoxPopuli-Cleaned-AA: 628 samples (~119 min), parliamentary speech, WER improved 3.5 pp after cleaning
- Earnings22-Cleaned-AA: 6 samples (~115 min), corporate earnings calls, WER improved 5.6 pp after cleaning
- New weighting: 50% AA-AgentTalk, 25% VoxPopuli-Cleaned-AA, 25% Earnings22-Cleaned-AA
- ElevenLabs Scribe v2 led at 2.3% AA-WER overall
- Cleaned datasets released publicly on Hugging Face under Apache-2.0

## Entities mentioned

- [[entities/orgs/artificial-analysis]] — developed and released the benchmark and datasets

## Concepts mentioned

- [[concepts/aa-wer]] — the benchmark this article introduces v2.0 of
- [[concepts/aa-agenttalk]] — new proprietary dataset, 50% weight
- [[concepts/voxpopuli-cleaned-aa]] — cleaned parliamentary dataset, 25% weight
- [[concepts/earnings22-cleaned-aa]] — cleaned earnings calls dataset, 25% weight
- [[concepts/word-error-rate]] — core accuracy metric
- [[concepts/speech-to-text]] — broader STT domain

## Related sources

- [[sources/speech-to-text-methodology]] — current AA-WER v2.2 methodology
- [[sources/methodology]] — general AA methodology

## My notes

- The shift to a voice-agent-focused benchmark (AA-AgentTalk at 50%) reflects the market pivot from transcription to conversational AI. This is a forward-looking methodological choice.
- Releasing cleaned datasets publicly on Hugging Face demonstrates AA's commitment to transparency and community contribution.
- The fact that no model had higher WER after cleaning validates that the corrections were genuinely fixing ground truth errors, not introducing bias.

---
type: concept
---

# Streaming Latency (STT)

Latency metrics for speech-to-text transcription in streaming mode, defined by Artificial Analysis.

## Metrics

- **Time to Final Transcript:** time from end-of-speech detection (via SileroVAD) to receiving the first transcript marked as Final by the model.
- **Time to First Partial Transcript:** time from end-of-speech detection to receiving the first Partial transcript.

## Mechanics

Audio is streamed in 20ms chunks. Streaming STT models return two types of transcripts:
- **Partials:** not yet confirmed, subject to changes
- **Finals:** confirmed, no longer modifiable

Forced endpointing uses SileroVAD to detect the end of speech and force generation of a final transcript. For models that do not support forced endpointing, the first natural Final within 2 seconds of end-of-speech is used.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | AA's streaming STT methodology | 2026-07-21 |

## Relationships
- [[concepts/aa-wer]] — streaming evaluation is part of AA-WER v2.2
- [[concepts/speech-to-text]] — broader context
- [[concepts/word-error-rate]] — WER for final and partial transcripts are reported separately

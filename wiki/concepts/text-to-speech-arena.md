---
type: concept
---

# AA TTS Arena

Blind pairwise human preference voting arena for evaluating text-to-speech (TTS) model quality. Elo scores are derived via Bradley-Terry MLE, following the LMSYS Chatbot Arena model. The arena is split into **two complementary tracks** designed to isolate different quality dimensions.

The **Controlled Voices Arena** uses voice cloning to standardize 8 reference voices (2 US female, 2 US male, 2 UK female, 2 UK male) across all models. This isolates the model's synthesis quality — naturalness, audio quality, pronunciation, pacing, and prosody — from voice preference.

The **Provider Voices Arena** evaluates models using their own publicly available voices (8 voices: male/female × US/UK combinations), reflecting the typical user experience.

All tests use [[concepts/serverless]] endpoints only, approximately 500-character prompts, batch size 1, and 22.05 kHz output. Performance is sampled 4× daily and reported as median over trailing 14 days.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/text-to-speech-methodology]] | Full specification of the two-track arena design, voice cloning, Elo calculation, and performance benchmarking | 2026-07-21 |

## Key details

### Two-Track Arena Design
| Track | Voices | What it measures |
|-------|--------|-----------------|
| Controlled Voices | 8 reference voices via cloning (2M×2F × US/UK) | Pure model quality, isolated from voice preference |
| Provider Voices | 8 provider-offered voices per model (M/F × US/UK) | Real-world user experience |

The Controlled Arena removes the confound of whether users prefer a specific voice rather than the model's synthesis quality. The Provider Arena adds ecological validity. Together they give a fuller picture than either alone.

### Quality Dimensions Evaluated
- Naturalness of speech
- Audio quality (artifacts, clarity)
- Pronunciation accuracy
- Pacing and rhythm
- Prosody and intonation

### Elo Calculation
- Bradley-Terry MLE from blind pairwise human preference votes
- Separate Elo pools for Controlled Voices and Provider Voices arenas

### Performance Benchmarks
- **Price per 1M Characters:** Normalized across per-character, subscription, token-based, output-duration, per-byte, and inference-time pricing models. No temporary discounts accepted.
- **Generation Time:** Median over trailing 14 days, sampled 4× daily at random times, ~500 character prompts, batch size 1, includes URL download time (full pipeline).
- **Audio format:** 22.05 kHz sample rate

### Endpoint Requirements
- [[concepts/serverless]] endpoints only — dedicated-instance deployments excluded
- No temporary pricing discounts or provider compensation accepted

## Relationships
- [[concepts/speech-to-speech-index]] — Related speech modality evaluated under a different framework (composite index, not arena)
- [[concepts/speech-to-text]] — Complementary speech benchmark (ASR direction), uses AA-WER metric
- [[concepts/bradley-terry]] — Statistical model underlying Elo score calculation
- [[concepts/serverless]] — Deployment model required for TTS benchmarks
- [[entities/orgs/artificial-analysis]] — operator of the TTS Arena

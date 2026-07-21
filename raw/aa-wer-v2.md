# AA-WER v2.0: Speech to Text Accuracy Benchmark

**Source:** https://artificialanalysis.ai/articles/aa-wer-v2
**Fetched:** 2026-07-21
**Date:** February 17, 2026

[Content saved from full article — see fetched version for complete details]

## Key summary

AA-WER v2.0 introduced AA-AgentTalk (new proprietary dataset, 50% weight), cleaned VoxPopuli and Earnings22 transcripts (25% each), removed AMI-SDM, and improved the text normalizer.

### AA-AgentTalk
- 469 samples, ~250 minutes, 8-109 second duration
- 6 content categories (Voice Agents 40%, AI Agent Interaction 20%, Industry Jargon 15%, Meetings 10%, Consumer 10%, Media 5%)
- 17 accent groups, 8 speaking styles
- 75% natural voice, 70% quiet indoor, 30% background noise
- Proprietary, held-out dataset to prevent overfitting

### VoxPopuli-Cleaned-AA
- 628 samples, ~119 minutes, 5-38 second duration
- European Parliament proceedings
- On average, model WER went down 3.5 pp after cleaning

### Earnings22-Cleaned-AA
- 6 samples, ~115 minutes, ~14-22 minute duration
- Corporate earnings calls with diverse speakers/accents
- On average, model WER went down 5.6 pp after cleaning

### Top results (February 2026)
ElevenLabs Scribe v2 led at 2.3% AA-WER, followed by Gemini 3 Pro (2.9%), Voxtral Small (3.0%), Gemini 2.5 Pro (3.1%), Gemini 3 Flash (3.2%).

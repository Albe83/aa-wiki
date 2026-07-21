---
type: source
date: 2026-07-21
source_file: raw/speech-to-speech-methodology.md
status: processed
---

# Speech to Speech Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/speech-to-speech-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Artificial Analysis evaluates native audio-to-audio models through the [[concepts/speech-to-speech-index]], a composite metric weighted equally (33.3% each) across three dimensions. The first, Speech Reasoning, uses [[concepts/big-bench-audio]] — 1,000 audio questions from Big Bench Hard categories (Formal Fallacies, Navigate, Object Counting, Web of Lies), generated with 23 synthetic voices from top-ranked TTS models and evaluated by a judge model for correctness. The second, Conversational Dynamics, applies the Full Duplex Bench (v1 + v1.5) covering four conversational skills: Pause Handling, Turn Taking, User Interruption Handling, and Backchannel Handling. The third, Agentic Performance, uses [[concepts/tau-voice]] with 278 customer service scenarios across airline (50), retail (114), and telecom (114) domains, evaluated via pass@1 with database state verification and 7 voice personas (2 control, 5 regular with diverse accents).

Performance metrics include Price per Hour of input/output audio and Time to First Audio (TTFA). The S2S Index launched in June 2026 at v1.0 with the 33/33/33 weighting; Big Bench Audio has seen several judge model updates, most recently switching to an updated judge for verbose responses (v1.2, May 2026).

## Key points

- Three equal-weighted dimensions (33.3% each): Speech Reasoning, Conversational Dynamics, Agentic Performance
- Big Bench Audio: 1,000 questions across 4 BBH categories, 23 synthetic TTS voices
- Full Duplex Bench tests 4 conversational skills: pauses, turns, interruptions, backchannels
- τ-Voice agentic benchmark: 278 scenarios, 7 voice personas, pass@1 with DB state verification
- TTFA (Time to First Audio) measures latency to first audio token output
- Launched June 2026 (v1.0); BBA judge model updated through v1.2 in May 2026
- Evaluates native audio-to-audio models — not cascaded STT→LLM→TTS pipelines

## Entities mentioned

- [[entities/orgs/artificial-analysis]] — benchmarking platform

## Concepts mentioned

- [[concepts/speech-to-speech-index]] — composite benchmark with 33/33/33 weighting across reasoning, conversation, and agentic dimensions
- [[concepts/big-bench-audio]] — audio adaptation of BBH for testing speech reasoning in audio-native models
- [[concepts/tau-voice]] — agentic voice benchmark with customer service scenarios and database state verification
- [[concepts/full-duplex]] — conversational dynamics benchmark covering pause handling, turn taking, interruptions, backchannels

## Related sources

- [[sources/methodology]] — parent methodology page

## My notes

This is the most architecturally ambitious of the AA benchmarks. The three-dimensional design reflects the understanding that speech-to-speech models need to reason (BBA), converse naturally (Full Duplex), and accomplish tasks (τ-Voice). The focus on native audio-to-audio models (not cascaded pipelines) is a forward-looking methodological choice as the field moves toward end-to-end speech models. The use of TTS-generated voices for BBA also cleverly controls for input quality variation.

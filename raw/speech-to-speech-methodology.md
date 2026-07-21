# Speech to Speech Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/speech-to-speech-benchmarking
**Fetched:** 2026-07-21

## Overview

Evaluates native audio-to-audio models across three dimensions (equal weighting 33.3% each):

### Speech Reasoning (Big Bench Audio)
1,000 audio questions from Big Bench Hard categories:
- Formal Fallacies (250): Deductive validity of informal arguments
- Navigate (250): Whether navigation steps return to start
- Object Counting (250): Count items from a collection
- Web of Lies (250): Boolean truth evaluation in natural language

Generated using 23 synthetic voices from top-ranked TTS models. Judge model evaluates correctness.

### Conversational Dynamics (Full Duplex Bench v1 + v1.5)
- **Pause Handling:** Model does not interrupt during natural pauses
- **Turn Taking:** Model correctly takes conversational turn
- **User Interruption Handling:** Model addresses mid-conversation interruptions
- **Backchannel Handling:** Model continues after backchannels ("yeah", "mm-hmm")

### Agentic Performance (τ-Voice)
Customer service tasks across 3 domains:
- Airline (50 scenarios): flight changes, rebooking
- Retail (114): disputes, returns
- Telecom (114): billing, troubleshooting

Voice personas: 2 control + 5 regular (diverse accents/profiles). Evaluation: pass@1 with database state verification.

## Price & Speed
- Price per hour of input/output audio
- Time to First Audio (TTFA): seconds to first audio token

## Version History
- **v1.0 (June 2026):** Launched Speech to Speech Index (33/33/33 weighting)
- **BBA v1.2 (May 2026):** Updated judge model for verbose responses
- **BBA v1.1 (Mar 2026):** Claude Sonnet 4.6 judge, counts non-answers
- **BBA v1.0 (Dec 2024):** Initial, only non-error responses counted

---
type: concept
---

# AA Speech-to-Speech Index

Composite benchmark for evaluating native audio-to-audio (speech-to-speech) models — not cascaded STT→LLM→TTS pipelines. The index is a **weighted average of three dimensions**, each contributing **33.3%**: Speech Reasoning (Big Bench Audio), Conversational Dynamics (Full Duplex Bench), and Agentic Performance (τ-Voice). Launched in June 2026 at v1.0 with this equal weighting, the index represents the most architecturally ambitious of the AA benchmarks, reflecting the understanding that speech models must reason, converse naturally, and accomplish tasks.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-speech-methodology]] | Full specification of the three-dimension index, benchmarks used, version history | 2026-07-21 |

## Key details

### Speech Reasoning (33.3%) — Big Bench Audio
- **1,000 audio questions** drawn from 4 Big Bench Hard categories (250 each):
  - **Formal Fallacies:** Deductive validity of informal arguments
  - **Navigate:** Whether navigation steps return to starting point
  - **Object Counting:** Count items from a collection
  - **Web of Lies:** Boolean truth evaluation in natural language
- Generated using 23 synthetic voices from top-ranked TTS models to control for input quality variation
- Evaluated by a judge model for correctness
- Judge model version history: v1.0 (Dec 2024, only non-error responses), v1.1 (Mar 2026, Claude Sonnet 4.6 judge, counts non-answers), v1.2 (May 2026, updated judge for verbose responses)

### Conversational Dynamics (33.3%) — Full Duplex Bench (v1 + v1.5)
- **Pause Handling:** Model does not interrupt during natural pauses in user speech
- **Turn Taking:** Model correctly takes conversational turn at appropriate moment
- **User Interruption Handling:** Model appropriately addresses mid-conversation interruptions
- **Backchannel Handling:** Model continues naturally after backchannel cues ("yeah", "mm-hmm")

### Agentic Performance (33.3%) — τ-Voice
- **278 customer service scenarios** across 3 domains:
  - Airline (50 scenarios): flight changes, rebooking
  - Retail (114): disputes, returns
  - Telecom (114): billing, troubleshooting
- 7 voice personas: 2 control + 5 regular with diverse accents and profiles
- Evaluation: pass@1 with database state verification

### Performance Metrics
- **Price:** Per hour of input/output audio
- **TTFA (Time to First Audio):** Seconds to first audio token output — key latency metric

### Version History
- **v1.0 (June 2026):** Launched Speech to Speech Index with 33/33/33 weighting
- **BBA v1.2 (May 2026):** Updated judge model for verbose responses
- **BBA v1.1 (Mar 2026):** Claude Sonnet 4.6 judge, counts non-answers
- **BBA v1.0 (Dec 2024):** Initial release, only non-error responses counted

## Relationships
- [[concepts/big-bench-audio]] — The Speech Reasoning component, adapting BBH for audio-native models
- [[concepts/full-duplex]] — The Conversational Dynamics component, covering pause handling, turn taking, interruptions, backchannels
- [[concepts/tau-voice]] — The Agentic Performance component, customer service scenarios with DB state verification
- [[concepts/speech-to-text]] — Complementary benchmark for ASR (the other speech direction)
- [[concepts/text-to-speech-arena]] — Related speech modality, evaluated via arena rather than composite index
- [[entities/orgs/artificial-analysis]] — developer of the Speech-to-Speech Index

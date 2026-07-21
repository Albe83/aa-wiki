---
type: concept
---

# Full Duplex

Conversation mode where both participants can speak simultaneously, without rigid turn-taking. In the context of speech-to-speech models, a full duplex model handles interruptions, pauses, and backchannel naturally.

## AA Evaluation

The Conversational Dynamics benchmark in the [[concepts/speech-to-speech-index|AA Speech-to-Speech Index]] evaluates 4 full duplex skills based on Full Duplex Bench (Lin et al., 2025):

- **Pause Handling:** the model does not interrupt during the user's natural pauses
- **Turn Taking:** the model takes the turn when appropriate
- **User Interruption Handling:** the model handles mid-conversation interruptions
- **Backchannel Handling:** the model continues after backchannel ("yeah", "mm-hmm")

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-speech-methodology]] | AA implementation of Full Duplex Bench v1 and v1.5 | 2026-07-21 |

## Relationships
- [[concepts/speech-to-speech-index]] — Conversational Dynamics is 1/3 of the S2S index

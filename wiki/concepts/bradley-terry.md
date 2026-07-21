---
type: concept
---

# Bradley-Terry Model

The Bradley-Terry model is a statistical method for estimating the probability that one option is preferred over another in pairwise comparisons. Used by Artificial Analysis to calculate Elo scores across all arenas (Image, Video, Music, TTS).

## How it works

The model estimates a "strength" parameter for each contender. The probability that A is preferred over B is:

```
P(A > B) = strength_A / (strength_A + strength_B)
```

Using Maximum Likelihood Estimation (MLE), the model finds strength values that maximize the probability of observing the actual votes. Scores are then rescaled to the Elo scale for readability.

## Sources in AA

AA uses Bradley-Terry in Image Arena, Video Arena, Music Arena, and TTS Arena. The 95% confidence interval is reported alongside each Elo score.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/image-methodology]] | Image Arena Elo via Bradley-Terry MLE | 2026-07-21 |
| [[sources/video-methodology]] | Video Arena Elo via Bradley-Terry MLE, ricalcolato ogni ora | 2026-07-21 |
| [[sources/music-methodology]] | Music Arena Elo via Bradley-Terry MLE, con 95% CI | 2026-07-21 |
| [[sources/text-to-speech-methodology]] | TTS Arena Elo simile a LMSYS Chatbot Arena | 2026-07-21 |

---
type: concept
---

# Modello di Bradley-Terry

Il modello di Bradley-Terry è un metodo statistico per stimare la probabilità che un'opzione venga preferita a un'altra in confronti a coppie. Usato da Artificial Analysis per calcolare i punteggi Elo in tutte le arene (Image, Video, Music, TTS).

## Funzionamento

Il modello stima un parametro di "forza" per ogni contendente. La probabilità che A sia preferito a B è:

```
P(A > B) = strength_A / (strength_A + strength_B)
```

Usando la Maximum Likelihood Estimation (MLE), il modello trova i valori di strength che massimizzano la probabilità di osservare i voti reali. I punteggi vengono poi riscalati in scala Elo per leggibilità.

## Fonti in AA

AA usa Bradley-Terry in Image Arena, Video Arena, Music Arena e TTS Arena. L'intervallo di confidenza al 95% è riportato accanto a ogni punteggio Elo.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/image-methodology]] | Image Arena Elo via Bradley-Terry MLE | 2026-07-21 |
| [[sources/video-methodology]] | Video Arena Elo via Bradley-Terry MLE, ricalcolato ogni ora | 2026-07-21 |
| [[sources/music-methodology]] | Music Arena Elo via Bradley-Terry MLE, con 95% CI | 2026-07-21 |
| [[sources/text-to-speech-methodology]] | TTS Arena Elo simile a LMSYS Chatbot Arena | 2026-07-21 |

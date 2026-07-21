---
type: concept
---

# Word Error Rate (WER)

Metrica standard per la valutazione dell'accuratezza della trascrizione speech-to-text. Misura la distanza tra la trascrizione del modello (hypothesis) e la trascrizione umana di riferimento (reference).

## Formula

```
WER = (Substitutions + Insertions + Deletions) / Words in Reference
```

Basata sulla distanza di Levenshtein: numero minimo di sostituzioni, inserimenti e cancellazioni per trasformare l'hypothesis nella reference.

## AA-WER Index

L'[[concepts/aa-wer|AA-WER Index v2.2]] calcola il WER su 3 dataset (~8 ore totali): AA-AgentTalk (50%), VoxPopuli-Cleaned-AA (25%), Earnings22-Cleaned-AA (25%). I risultati sono aggregati come media pesata per durata audio.

La normalizzazione usa il normalizer Whisper di OpenAI con regole aggiuntive per gestire varianti di formattazione equivalenti (numeri, date, valute, ID, ortografia UK/US, ecc.).

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | Metodologia completa AA-WER v2.2 | 2026-07-21 |

## Relationships
- [[concepts/aa-wer]] — implementazione AA del benchmark WER
- [[concepts/speech-to-text]] — contesto più ampio del benchmarking STT

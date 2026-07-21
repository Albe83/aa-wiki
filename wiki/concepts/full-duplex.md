---
type: concept
---

# Full Duplex

Modalità di conversazione in cui entrambi i partecipanti possono parlare simultaneamente, senza alternanza rigida dei turni. Nel contesto dei modelli speech-to-speech, un modello full duplex gestisce interruzioni, pause e backchannel in modo naturale.

## Valutazione AA

Il benchmark Conversational Dynamics nell'[[concepts/speech-to-speech-index|AA Speech-to-Speech Index]] valuta 4 abilità full duplex basate su Full Duplex Bench (Lin et al., 2025):

- **Pause Handling:** il modello non interrompe durante le pause naturali dell'utente
- **Turn Taking:** il modello prende il turno quando appropriato
- **User Interruption Handling:** il modello gestisce interruzioni mid-conversazione
- **Backchannel Handling:** il modello continua dopo backchannel ("yeah", "mm-hmm")

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-speech-methodology]] | Implementazione AA di Full Duplex Bench v1 e v1.5 | 2026-07-21 |

## Relationships
- [[concepts/speech-to-speech-index]] — la Conversational Dynamics è 1/3 dell'indice S2S

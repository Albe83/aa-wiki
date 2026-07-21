---
type: concept
---

# Streaming Latency (STT)

Metriche di latenza per la trascrizione speech-to-text in modalità streaming, definite da Artificial Analysis.

## Metriche

- **Time to Final Transcript:** tempo dal rilevamento di fine parlato (via SileroVAD) alla ricezione del primo transcript marcato come Final dal modello.
- **Time to First Partial Transcript:** tempo dal rilevamento di fine parlato alla ricezione del primo transcript Partial.

## Meccanica

L'audio viene streamato in chunk da 20ms. I modelli STT streaming restituiscono due tipi di transcript:
- **Partials:** non ancora confermati, soggetti a modifiche
- **Finals:** confermati, non più modificabili

Il forced endpointing usa SileroVAD per rilevare la fine del parlato e forzare la generazione di un transcript finale. Per i modelli che non supportano forced endpointing, si usa il primo Final naturale entro 2 secondi dalla fine del parlato.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | Metodologia streaming STT di AA | 2026-07-21 |

## Relationships
- [[concepts/aa-wer]] — la valutazione streaming è parte di AA-WER v2.2
- [[concepts/speech-to-text]] — contesto più ampio
- [[concepts/word-error-rate]] — WER per final e partial transcript sono riportati separatamente

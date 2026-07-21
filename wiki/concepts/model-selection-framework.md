---
type: concept
---

# Model Selection Framework

Processo decisionale raccomandato da Artificial Analysis per scegliere modelli e provider API.

## I tre passi

1. **Partire dallo use-case** — Identificare quali dimensioni ottimizzare: qualità, velocità, prezzo, latenza, context window. Esempio: un sito consumer a basso ARPU privilegia velocità e prezzo basso sulla qualità massima.

2. **Scegliere il modello** — Usare l'[[concepts/intelligence-index|Intelligence Index]] come indicatore generalista, poi sviluppare una short-list di modelli candidati da testare sullo use-case specifico. I test custom sono essenziali: i benchmark AA indicano la direzione ma non sostituiscono la validazione.

3. **Scegliere il provider** — Una volta scelto il modello, confrontare i provider su: prezzo, throughput, latenza, compatibilità OpenAI, rate limits, context window. Le performance tra provider possono variare significativamente.

## Razionale

Modelli e provider presentano trade-off inevitabili. L'ordine use-case → modello → provider evita di vincolarsi a un provider prima di aver identificato il modello giusto, dato che i provider non ospitano tutti i modelli.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/guide]] | Framework ufficiale AA per la selezione di modelli e provider | 2026-07-21 |

## Current synthesis

Il framework è il principio organizzatore dell'intero sito AA. Ogni grafico e leaderboard è progettato per supportare uno di questi tre passi decisionali.

---
type: concept
---

# Output Speed e Metriche di Performance

Metriche di performance per API di inferenza LLM definite da Artificial Analysis.

## Definizioni

### Time to First Token (TTFT)
Tempo (secondi) tra l'invio della richiesta e la ricezione del primo token. Per i reasoning models, è il primo token di reasoning.

### Time to First Answer Token
Tempo (secondi) tra l'invio della richiesta e il primo token di risposta (dopo l'eventuale fase di reasoning).

### Output Speed (output tokens per second)
Numero medio di token ricevuti al secondo, dopo la ricezione del primo token. Misurato in OpenAI tokens.

### Total Response Time for 100 Output Tokens
Tempo per generare 100 token di output, calcolato sinteticamente da TTFT + Output Speed.

### End-to-End Response Time
Tempo totale per ricevere una risposta completa, includendo input processing, reasoning e generazione della risposta.

### Average Reasoning Tokens
Numero medio di token di reasoning prodotti dai reasoning models prima della risposta. Calcolato su 60 prompt vari (personali, commerciali, coding, math, scienza) da MMLU Pro, AIME 2025, LiveCodeBench. Se non disponibile, si assume 2k reasoning tokens.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizioni ufficiali AA delle metriche di performance | 2026-07-21 |

## Current synthesis

Le metriche AA misurano l'esperienza reale dell'utente, non il throughput massimo teorico. La distinzione tra TTFT e Time to First Answer Token è particolarmente rilevante per i reasoning models, dove la fase di "thinking" può durare secondi prima che inizi la risposta vera e propria.

## Relationships
- [[concepts/token]] — le metriche di velocità usano OpenAI Tokens come unità standard

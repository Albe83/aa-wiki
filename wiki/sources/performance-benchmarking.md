---
type: source
date: 2026-07-21
source_file: raw/performance-benchmarking.md
status: processed
---

# Artificial Analysis Language Model API Performance Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/performance-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica che descrive come Artificial Analysis misura le performance delle API dei modelli linguistici. Il principio guida è misurare l'esperienza end-to-end dell'utente finale: prompt inviato, risposta ricevuta. Vengono utilizzati workload diversificati (1K, 10K, 100K input token, vision) e due scenari di carico (prompt singolo, 10 prompt paralleli), con test ripetuti regolarmente (fino a 8 volte al giorno).

La metodologia copre definizioni chiave (TTFT, Output Speed, Response Time), dettagli tecnici (server us-central1, parametri API, tokenizzazione o200k_base), metriche di rappresentazione (mediana P50 su 72 ore) e limitazioni note. Include anche termini di integrità che vietano ai provider di trattare il traffico AA in modo diverso da quello degli utenti ordinari.

## Key points

- 4 tipi di workload: 1K token input, 10K (default), 100K, vision (1MP image)
- 2 scenari di carico: prompt singolo, 10 prompt paralleli simultanei
- Frequenza test: ogni 3 ore per workload principali, 1 volta/giorno per parallelo, 1 volta/settimana per 100K
- Prompt unici a ogni test run per evitare caching effects e misurare variazioni reali di output speed
- Mediana P50 su 72 ore come metrica rappresentativa (14 giorni per workload 100K)
- Server in Google Cloud us-central1-a; mix di account anonimi, accreditati e benchmark key
- Temperature 0.6 per reasoning models, 0 per non-reasoning; top_p 1
- Tokenizzazione o200k_base per performance benchmarking; provider-reported per costi Intelligence Index
- Integrità: i provider non devono rilevare o trattare diversamente il traffico AA

## Entities mentioned

- [[entities/orgs/openai]] — libreria Python OpenAI usata per provider compatibili; tokenizer o200k_base

## Concepts mentioned

- [[concepts/output-speed]] — TTFT, Time to First Answer Token, Output Speed, Response Time
- [[concepts/token]] — tokenizzazione o200k_base vs native token; efficienza del tokenizer
- [[concepts/cost-per-task]] — relazione con pricing via token provider-reported

## Related sources

- [[sources/methodology]] — metodologia generale AA, definizioni standard
- [[sources/intelligence-benchmarking]] — metriche di intelligenza a cui si rapportano i costi

## My notes

- v2.2.0 (Marzo 2026) ha spostato il workload default da 1K a 10K input token: segnale che i prompt reali stanno diventando più lunghi
- La distinzione TTFT / Time to First Answer Token è critica per i reasoning models — senza, il tempo di ragionamento verrebbe confuso con latenza di risposta
- I termini di integrità sono stringenti: niente hardware dedicato, code di priorità o configurazioni non pubbliche per il traffico AA

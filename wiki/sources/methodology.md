---
type: source
date: 2026-07-21
source_file: raw/methodology.md
status: processed
---

# Artificial Analysis Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica ufficiale di Artificial Analysis. Definisce lo scope del benchmarking AA (intelligence, qualità, performance, prezzo) e la terminologia standard usata in tutto il sito. Il principio guida è misurare l'esperienza reale degli utenti, non le performance teoriche massime su hardware specifico.

La pagina elenca 13 aree metodologiche dettagliate (intelligence LLM, performance API, capability indices, system load test, coding agents, agent perf, text-to-image, video, musica, STT, TTS, speech-to-speech, openness index) e 17 definizioni chiave che costituiscono il vocabolario base per interpretare tutti i dati del sito.

## Key points

- AA benchmarka sia modelli proprietari che open weights, endpoint API e sistemi dedicati
- Le performance sono misurate end-to-end come esperienza reale del cliente, non massimo teorico
- Gli endpoint serverless sono definiti come pay-per-use (prezzo per token), non a tariffa fissa
- OpenAI Tokens (tiktoken o200k_base) sono l'unità standard per i confronti di velocità
- I prezzi sono espressi in native token; il blended price assume rapporto 7:2:1 (cache hit : input : output)
- Il Cost per Task è pesato sui pesi relativi dei benchmark nell'Intelligence Index
- Per i reasoning models, si distinguono Time to First Token (primo token di reasoning) e Time to First Answer Token (primo token di risposta)
- L'Average Reasoning Tokens è calcolato su 60 prompt vari (personali, commerciali, coding, math, scienza) da MMLU Pro, AIME 2025, LiveCodeBench

## Entities mentioned

- [[entities/orgs/openai]] — citato come esempio di Model Creator e Provider (GPT-4)
- [[entities/orgs/meta]] — citato come esempio di Model Creator (Llama 3)
- [[entities/orgs/aws]] — citato come esempio di Provider (AWS Bedrock)
- [[entities/orgs/together-ai]] — citato come esempio di Provider

## Concepts mentioned

- [[concepts/model-ecosystem]] — distinzione Model, Model Creator, Endpoint, Provider, System
- [[concepts/token]] — OpenAI Tokens vs Native Tokens, tokenizer
- [[concepts/cost-per-task]] — calcolo del costo pesato per task nell'Intelligence Index
- [[concepts/output-speed]] — metriche di performance: TTFT, Output Speed, Response Time
- [[concepts/open-weights]] — definizione e distinzione da open-source
- [[concepts/serverless]] — definizione nel contesto delle API LLM
- [[concepts/blended-price]] — rapporto 7:2:1 per il calcolo del prezzo combinato

## Related sources

_(nessuna al momento — prima fonte ingerita)_

## My notes

- Questa è la fonte fondativa: definisce il vocabolario base per interpretare ogni altra pagina di AA
- Le 13 aree metodologiche linkate sono potenziali fonti future da scaricare e ingerire
- La distinzione Model/Endpoint/Provider è cruciale per capire i grafici di performance API provider

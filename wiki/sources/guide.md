---
type: source
date: 2026-07-21
source_file: raw/guide.md
status: processed
---

# Using Artificial Analysis — Guide

**Source:** https://artificialanalysis.ai/guide
**Ingested:** 2026-07-21
**Type:** article

## Summary

Guida pratica all'uso di Artificial Analysis per la selezione di modelli e provider. AA delinea un processo decisionale in tre passi: (1) partire dallo use-case, (2) scegliere il modello, (3) scegliere il provider. L'enfasi è sui trade-off tra qualità, velocità, prezzo, latenza e finestra di contesto.

L'esempio concreto è un sito consumer a basso ARPU: servono alta velocità di output, bassa latenza e prezzo contenuto. L'Intelligence Index è presentato come indicatore generalista della qualità, da affiancare a test specifici sullo use-case.

## Key points

- Il processo decisionale AA: use-case → modello → provider (in quest'ordine)
- L'Intelligence Index è un indicatore generalista; per decisioni finali servono test custom sullo use-case
- La scelta del modello precede quella del provider perché i provider variano nei modelli che ospitano
- Nella scelta del provider contano: prezzo, throughput, latenza, compatibilità OpenAI, rate limits, context window
- Trade-off chiave: qualità vs velocità vs prezzo vs latenza vs context window

## Entities mentioned

- [[entities/orgs/deepseek]] — DeepSeek V4 Pro usato come esempio nella pagina dei provider

## Concepts mentioned

- [[concepts/intelligence-index]] — indicatore generalista di qualità delle risposte
- [[concepts/model-selection-framework]] — processo use-case → modello → provider
- [[concepts/cost-per-task]] — rilevante per il trade-off qualità/prezzo
- [[concepts/output-speed]] — rilevante per il trade-off velocità/qualità

## Related sources

- [[sources/methodology]] — definisce le metriche su cui si basa il processo di selezione

## My notes

- Guida breve ma pragmatica. Il framework "use-case first" è il principio organizzatore di tutto il sito AA
- Il consiglio di sviluppare una short-list e testare sullo use-case specifico è un caveat importante: i benchmark AA sono una bussola, non un sostituto dei test

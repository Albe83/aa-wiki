---
type: source
date: 2026-07-21
source_file: raw/coding-agents-benchmarking.md
status: processed
---

# Coding Agent Index Methodology

**Source:** https://artificialanalysis.ai/methodology/coding-agents-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica che descrive il Coding Agent Index di Artificial Analysis, un benchmark che valuta i coding agent su task end-to-end di software engineering. L'indice (v1.2, Luglio 2026) aggrega 321 task distribuiti su 3 componenti: DeepSWE (113 task long-horizon), Terminal-Bench v2 (84 task di uso agentico del terminale) e SWE-Atlas-QnA (124 task di Q&A su repository). Ogni task viene eseguito 3 volte con scoring pass@1 binario.

Oltre alla qualità, l'indice misura metriche di efficienza: costo API per task (basato su pricing pay-per-token), utilizzo token (input, cache, cache-write, reasoning, output) e tempo di esecuzione wall-clock. La pagina documenta anche l'evoluzione dell'indice attraverso tre versioni.

## Key points

- 321 task totali su 3 componenti: DeepSWE (113), Terminal-Bench v2 (84), SWE-Atlas-QnA (124)
- Scoring pass@1 binario: 1 per pass, 0 per fail, media tra i 3 repeat per task
- Indice composito: media equipesata dei pass@1 delle 3 componenti
- Metriche di efficienza: costo API, utilizzo token, tempo di esecuzione
- v1.2 (Luglio 2026): SWE-Atlas-QnA convertito a scoring binario
- v1.1 (Giugno 2026): aggiunto DeepSWE, rimosso SWE-Bench-Pro-Hard-AA
- v1.0 (Maggio 2026): prima release
- 5 task di Terminal-Bench esclusi per incompatibilità d'ambiente

## Entities mentioned

_nessuna_

## Concepts mentioned

- [[concepts/coding-agent-index]] — indice composito di coding agentico
- [[concepts/terminal-bench]] — Terminal-Bench v2: componente di uso agentico del terminale

## Related sources

- [[sources/methodology]] — metodologia generale AA
- [[sources/intelligence-benchmarking]] — Intelligence Index (include Terminal-Bench)
- [[sources/capability-indices]] — Coding Index come Skill Index separato

## My notes

- Il Coding Agent Index è distinto dal Coding Index (Skill) dei Capability Indices: il primo valuta agent completi, il secondo valuta capacità atomiche
- L'evoluzione rapida (3 versioni in 3 mesi) riflette la velocità del campo coding agentico
- La metrica di costo è particolarmente rilevante: un coding agent eccellente ma proibitivamente costoso ha utilità pratica limitata

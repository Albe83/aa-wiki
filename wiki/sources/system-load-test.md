---
type: source
date: 2026-07-21
source_file: raw/system-load-test.md
status: processed
---

# System Load Test (AA-SLT) Methodology

**Source:** https://artificialanalysis.ai/methodology/system-load-test
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica che descrive l'AA-SLT (System Load Test), il benchmark di Artificial Analysis per misurare le performance di sistema sotto carico sostenuto. A differenza dei benchmark di performance API standard che misurano prompt singoli o batch fissi, l'AA-SLT mantiene un numero costante di query parallele: quando una finisce, un'altra parte immediatamente, garantendo carico stabile con varianza minima.

Il test procede per fasi di 3 minuti a concorrenza crescente (1, 2, 4, 8, 16, 32, 64, poi incrementi di 64) fino a raggiungere il throughput massimo del sistema. Ogni query usa 1.000 token input e 1.000 token output con streaming abilitato. Le metriche chiave sono throughput aggregato, tasso di risposta, latenza end-to-end e output speed per query.

## Key points

- Carico sostenuto: query rimpiazzate immediatamente al completamento per mantenere concorrenza costante
- Fasi di 3 minuti a concorrenza crescente: 1, 2, 4, 8, 16, 32, 64, poi +64
- Workload standardizzato: 1.000 token input, 1.000 token output, streaming abilitato
- 4 metriche chiave: System Output Throughput, Response Rate, End-to-End Latency, Output Speed per Query
- Il test scala fino a saturazione del sistema per trovare il throughput ceiling
- Approccio a fasi con ramp-up e cool-down esclusi dalle misurazioni

## Entities mentioned

_nessuna_

## Concepts mentioned

- [[concepts/aa-slt]] — benchmark di carico sistema di Artificial Analysis
- [[concepts/output-speed]] — metriche di output speed e latenza sotto carico

## Related sources

- [[sources/methodology]] — metodologia generale AA
- [[sources/performance-benchmarking]] — benchmark di performance API standard (carico singolo e parallelo)
- [[sources/agentperf]] — benchmark hardware per carichi agentici sostenuti

## My notes

- L'AA-SLT è complementare ai benchmark di performance standard: quelli misurano l'esperienza del singolo utente, questo misura la capacità del sistema
- La metodologia a "query rimpiazzate" è più realistica di un batch fisso perché simula un flusso continuo di utenti
- Interessante il confronto con agentperf: entrambi misurano carico, ma AA-SLT è per API serverless, agentperf per deployment dedicati

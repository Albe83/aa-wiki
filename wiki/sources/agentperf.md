---
type: source
date: 2026-07-21
source_file: raw/agentperf.md
status: processed
---

# AA-AgentPerf Methodology

**Source:** https://artificialanalysis.ai/methodology/agentperf
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica che descrive AA-AgentPerf, il benchmark hardware di Artificial Analysis che misura quanti agenti attivi un deployment di inferenza può supportare simultaneamente, rispettando SLO (Service Level Objectives) di performance per agente. A differenza dei benchmark API che misurano prompt isolati, AgentPerf usa traiettorie agentiche reali multi-turno con ragionamento interleaved, tool call e contesto variabile.

Il benchmark definisce SLO tier derivati dai dati di benchmarking API serverless di AA, con soglie diverse per modelli diversi. Usa un dataset di traiettorie reali raccolte con l'harness OpenCode (DeepSeek V3.2, GLM 4.7, Kimi K2.5), con input tra ~5K e 131K token. Il test usa binary search dopo ramp esponenziale, con ogni fase di almeno 10 minuti a regime. I risultati sono normalizzati per acceleratore, per sistema e per MW.

## Key points

- Misura agenti attivi supportabili, non throughput di token grezzo
- Traiettorie agentiche reali multi-turno: coding session con tool call e contesto variabile
- SLO tier derivati dal mercato: basati sulle performance osservate nelle API serverless AA
- 2 modelli di riferimento con tier diversi: DeepSeek V4 Pro (max) con 3 tier, gpt-oss-120b (high) con 4 tier
- Dataset da OpenCode harness: input ~5K-131K token (media ~27K), 12+ linguaggi
- Tool call delay realistici: 0.1s-5s (mediana ~1s)
- Binary search dopo ramp esponenziale; ≥30 traiettorie completate per fase
- Normalizzazione multi-livello: per acceleratore, sistema, MW
- Continuamente aggiornato con nuovo hardware/software

## Entities mentioned

_nessuna_

## Concepts mentioned

- [[concepts/aa-agentperf]] — benchmark hardware per deployment agentici
- [[concepts/output-speed]] — metriche SLO: P25 Output Speed e P95 TTFT

## Related sources

- [[sources/methodology]] — metodologia generale AA
- [[sources/performance-benchmarking]] — benchmark di performance API da cui derivano gli SLO tier
- [[sources/system-load-test]] — benchmark di carico sistema complementare

## My notes

- AgentPerf colma il gap tra benchmark API (esperienza singolo utente) e benchmark di sistema (throughput grezzo): misura capacità agentica reale
- L'uso di traiettorie reali (non sintetiche) con tool call delay realistici è un punto di forza metodologico
- La normalizzazione per MW permette confronti di efficienza energetica tra deployment
- I SLO tier differenziati per modello riflettono che le aspettative di performance dipendono dal modello usato

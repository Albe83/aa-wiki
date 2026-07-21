---
type: source
date: 2026-07-21
source_file: raw/capability-indices.md
status: processed
---

# Artificial Analysis Capability Indices Methodology

**Source:** https://artificialanalysis.ai/methodology/capability-indices
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica che descrive i Capability Indices di Artificial Analysis, metriche composite che misurano la performance dei modelli su specifici casi d'uso e industrie. Si dividono in due categorie: Skill Indices (competenze cross-dominio) e Industry Indices (professioni specifiche). Gli Skill Indices usano una media equipesata dei componenti, mentre gli Industry Indices pesano i componenti in base alla frequenza reale dei task professionali (secondo una tassonomia O*NET).

La pagina elenca 8 indici: 2 Skill (Agentic, Coding) e 6 Industry (Finance & Accounting, Strategy & Ops, Legal, Healthcare & Medical, Engineering, Economics). Ogni indice è scomposto nei suoi componenti con i relativi pesi percentuali, tutti derivati dalle valutazioni dell'Intelligence Index.

## Key points

- 2 Skill Indices: Agentic Index (GDPval-AA v2 + τ³-Banking) e Coding Index (Terminal-Bench v2.1 + SciCode)
- 6 Industry Indices: Finance, Strategy & Ops, Legal, Healthcare, Engineering, Economics
- Gli Industry Indices pesano i componenti per frequenza reale dei task, non equamente
- AA-Omniscience è il componente più trasversale: compare in tutti e 6 gli Industry Indices
- GDPval-AA v2 compare in tutti gli indici tranne il Coding Index
- τ³-Banking compare in 6 degli 8 indici
- HLE compare in 5 indici come fonte di ragionamento generale
- AA-LCR compare in 4 indici (Finance, Strategy & Ops, Legal, Economics)

## Entities mentioned

_nessuna_

## Concepts mentioned

- [[concepts/capability-indices]] — definizione e struttura degli indici di capacità
- [[concepts/intelligence-index]] — fonte delle valutazioni componenti
- [[concepts/gdpval-aa]] — componente di knowledge work agentico
- [[concepts/tau3-banking]] — componente di interazione clienti agentica
- [[concepts/terminal-bench]] — componente di coding agentico
- [[concepts/scicode]] — componente di generazione codice scientifico
- [[concepts/aa-omniscience]] — componente di conoscenza e non-allucinazione
- [[concepts/humanitys-last-exam]] — componente di ragionamento
- [[concepts/aa-lcr]] — componente di long-context reasoning
- [[concepts/ifbench]] — componente di instruction following

## Related sources

- [[sources/methodology]] — metodologia generale AA
- [[sources/intelligence-benchmarking]] — Intelligence Index da cui derivano tutti i componenti

## My notes

- La distinzione Skill vs Industry è fondamentale: gli Skill Index sono cross-dominio e equipesati, gli Industry Index sono tarati su frequenze reali di task professionali
- AA-Omniscience è il mattone più versatile: conoscenza settoriale + metrica di allucinazione in un unico benchmark
- Engineering Index è il più pesante sul ragionamento (35% tra HLE, GPQA Diamond e CritPt)
- Strategy & Ops è l'unico indice dove τ³-Banking pesa tanto quanto GDPval-AA v2 (30% ciascuno)

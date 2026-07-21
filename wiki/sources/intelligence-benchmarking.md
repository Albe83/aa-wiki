---
type: source
date: 2026-07-21
source_file: raw/intelligence-benchmarking.md
status: processed
---

# Artificial Analysis Intelligence Benchmarking Methodology

**Source:** https://artificialanalysis.ai/methodology/intelligence-benchmarking
**Ingested:** 2026-07-21
**Type:** article

## Summary

Pagina metodologica che descrive la composizione dell'Intelligence Index v4.1 di Artificial Analysis, l'indice composito che misura l'intelligenza generale dei modelli. L'indice aggrega molteplici valutazioni indipendenti che coprono knowledge work agentico, interazione con clienti, uso del terminale, generazione di codice, ragionamento scientifico, long-context reasoning, conoscenza multidisciplinare e prevenzione delle allucinazioni.

Oltre alle valutazioni principali dell'Intelligence Index, la pagina descrive benchmark aggiuntivi come AA-Briefcase (knowledge work di lungo periodo), Harvey LAB-AA e APEX-Agents-AA (benchmark legali e agentici sviluppati con partner), AutomationBench-AA, EnterpriseOps-Gym-AA, ITBench-AA, LiveCodeBench, IFBench, MMLU-Pro, Global MMLU-Lite e MMMU-Pro. Vengono specificati parametri di testing, prompt e metodologia di valutazione.

## Key points

- Intelligence Index v4.1 è l'indice composito principale per misurare l'intelligenza dei modelli AA
- Le valutazioni core includono: GDPval-AA v2, τ³-Banking, Terminal-Bench v2.1, SciCode, AA-LCR, AA-Omniscience, HLE, GPQA Diamond, CritPt
- Benchmark aggiuntivi coprono domini specializzati: legale (Harvey LAB-AA), agentico (APEX-Agents-AA, AutomationBench-AA), enterprise IT (EnterpriseOps-Gym-AA, ITBench-AA)
- Valutazioni di knowledge work esteso con AA-Briefcase
- Benchmark di coding aggiuntivi: LiveCodeBench
- Benchmark di instruction following: IFBench
- Benchmark multidisciplinari: MMLU-Pro, Global MMLU-Lite, MMMU-Pro

## Entities mentioned

- [[entities/orgs/openai]] — dataset GDPval usa tiktoken per la tokenizzazione
- [[entities/orgs/sierra]] — sviluppatore del benchmark τ-bench (τ³-Banking)
- [[entities/orgs/stanford]] — sviluppatore di Terminal-Bench

## Concepts mentioned

- [[concepts/intelligence-index]] — indice composito di intelligenza v4.1
- [[concepts/gdpval-aa]] — GDPval-AA v2: benchmark su task lavorativi reali
- [[concepts/tau3-banking]] — τ³-Banking: benchmark di tool use agentico per interazione clienti
- [[concepts/terminal-bench]] — Terminal-Bench v2.1: benchmark di coding agentico via terminale
- [[concepts/scicode]] — SciCode: benchmark di generazione codice scientifico
- [[concepts/aa-lcr]] — AA-LCR: benchmark di long context reasoning
- [[concepts/aa-omniscience]] — AA-Omniscience: benchmark di conoscenza e allucinazione
- [[concepts/humanitys-last-exam]] — HLE: benchmark di ragionamento estremo
- [[concepts/gpqa-diamond]] — GPQA Diamond: benchmark di ragionamento scientifico
- [[concepts/critpt]] — CritPt: benchmark di ragionamento critico
- [[concepts/aa-briefcase]] — AA-Briefcase: benchmark di knowledge work di lungo periodo
- [[concepts/harvey-lab-aa]] — Harvey LAB-AA: benchmark legale sviluppato con Harvey
- [[concepts/apex-agents-aa]] — APEX-Agents-AA: benchmark agentico
- [[concepts/automationbench-aa]] — AutomationBench-AA: benchmark di automazione
- [[concepts/enterpriseops-gym-aa]] — EnterpriseOps-Gym-AA: benchmark enterprise IT operations
- [[concepts/itbench-aa]] — ITBench-AA: benchmark IT
- [[concepts/livecodebench]] — LiveCodeBench: benchmark di coding live
- [[concepts/ifbench]] — IFBench: benchmark di instruction following
- [[concepts/mmlu-pro]] — MMLU-Pro: benchmark multidisciplinare avanzato
- [[concepts/global-mmlu-lite]] — Global MMLU-Lite: benchmark multidisciplinare globale
- [[concepts/mmmu-pro]] — MMMU-Pro: benchmark multimodale avanzato

## Related sources

- [[sources/methodology]] — metodologia generale AA
- [[sources/capability-indices]] — capability indices derivati da questi benchmark
- [[sources/coding-agents-benchmarking]] — metodologia specifica per coding agents

## My notes

- Intelligence Index v4.1 è il benchmark centrale di AA: tutti i Cost per Task sono calcolati sui pesi di questo indice
- La lista di benchmark aggiuntivi è notevole: AA ha sviluppato benchmark proprietari (AA-Briefcase, AA-LCR, AA-Omniscience) e collaborazioni (Harvey LAB-AA, APEX-Agents-AA)
- Terminal-Bench compare sia nell'Intelligence Index che nel Coding Agent Index — è un benchmark ponte tra le due aree

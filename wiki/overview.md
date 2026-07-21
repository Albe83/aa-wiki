---
type: overview
---

# Artificial Analysis — Panoramica

Artificial Analysis è una piattaforma indipendente di analisi e benchmarking dell'AI. Valuta modelli linguistici, agenti, modelli di generazione media (immagini, video, speech) e provider API, offrendo metriche oggettive su **intelligenza**, **velocità** e **costo**.

## Metodologia

AA benchmarka sia modelli proprietari che open weights. Il principio guida è misurare l'**esperienza reale dell'utente**, non le performance teoriche massime su hardware specifico. Vedi [[sources/methodology]] per i dettagli completi.

### Standard di misurazione
- **Velocità**: misurata in [[concepts/token|OpenAI Tokens]] (tiktoken o200k_base) per confronti equi tra modelli
- **Prezzi**: espressi in native token; il [[concepts/blended-price|blended price]] assume rapporto 7:2:1 (cache hit : input : output)
- **Costo reale**: il [[concepts/cost-per-task|Cost per Task]] è pesato sui benchmark dell'Intelligence Index — incorpora la verbosità del modello
- **Performance**: misurata come esperienza end-to-end del cliente, non throughput massimo teorico

### Terminologia chiave
La distinzione [[concepts/model-ecosystem|Model → Model Creator → Endpoint → Provider → System]] è fondamentale per interpretare i dati AA.

### Valutazioni dell'Intelligence Index v4.1

L'[[concepts/intelligence-index|Intelligence Index v4.1]] aggrega 9 valutazioni indipendenti in 4 categorie (peso totale 100%):

**Agenti (34%)**
- **GDPval-AA v2 (20%)**: task di knowledge work agentico su dataset proprietario — è la valutazione a peso singolo più elevato
- **τ³-Banking (14%)**: interazione cliente agentica nel dominio fintech, 97 task, sviluppato da [[entities/orgs/sierra|Sierra AI]]

**Coding (24%)**
- **Terminal-Bench v2.1 (16%)**: task di terminale e system administration, sviluppato da [[entities/orgs/stanford|Stanford/Laude Institute]], 89 task
- **SciCode (8%)**: generazione di codice scientifico

**Ragionamento scientifico (24%)**
- **HLE — Humanity's Last Exam (12%)**: ragionamento estremo su domande di frontiera
- **GPQA Diamond (6%)**: ragionamento scientifico avanzato
- **CritPt (6%)**: ragionamento critico e valutazione di argomentazioni

**Generale (18%)**
- **AA-Omniscience (12%)**: conoscenza multidisciplinare (8% accuracy + 4% non-hallucination)
- **AA-LCR (6%)**: long context reasoning

Tutte le valutazioni usano scoring pass@1, temperatura 0 (modelli non-reasoning) o 0.6 (reasoning). Intervallo di confidenza ~±1%.

## Framework di selezione

AA propone un processo decisionale in tre passi: **use-case → modello → provider**. Vedi [[concepts/model-selection-framework]] e [[sources/guide]].

## Aree coperte

### Intelligence (modelli linguistici)
- **Intelligence Index v4.1**: indice composito basato su 9 valutazioni indipendenti
- **Valutazioni**: [[concepts/gdpval-aa|GDPval-AA v2]], [[concepts/tau3-banking|τ³-Banking]], [[concepts/terminal-bench|Terminal-Bench v2.1]], SciCode, Humanity's Last Exam, GPQA Diamond, CritPt, [[concepts/aa-omniscience|AA-Omniscience]], [[concepts/aa-lcr|AA-LCR]]
- **[[concepts/aa-briefcase|AA-Briefcase]]**: benchmark agentico per knowledge work di lungo periodo
- **Capability Indices**: indici settoriali (Agentic, Coding, Finance & Accounting, Strategy & Ops, Legal, Healthcare, Engineering, Economics)

### Agenti e coding
- **Coding Agent Index**: performance, costo e tempo di esecuzione su task di software engineering end-to-end
- **AA-Agentic Index**: tool use, pianificazione, autonomia, problem solving complesso

### Velocità e latenza
- [[concepts/output-speed|Output speed]] in token al secondo, tempo per task, latenza end-to-end
- Confronto tra provider API (first-party e terze parti)

### Prezzo e costo
- [[concepts/cost-per-task|Costo per task]] pesato sull'Intelligence Index
- Prezzi per input, output, cache hit, cache write
- [[concepts/cache-pricing|Modelli di pricing della cache]] per provider

### Media
- **Image Arena**: text-to-image, image editing (Elo da voti ciechi)
- **Video Arena**: text-to-video, image-to-video, video editing
- **Speech**: Text-to-Speech Arena, Speech-to-Text (AA-WER Index), Speech-to-Speech

### Apertura
- **[[concepts/openness-index|Openness Index]]**: trasparenza dei dati di training, metodologia, disponibilità dei pesi

### Provider API
- Performance e pricing comparati tra provider per modelli open-weight
- Provider monitorati: [[entities/orgs/openai|OpenAI]], Anthropic, Google, [[entities/orgs/aws|AWS Bedrock]], Azure, [[entities/orgs/together-ai|Together AI]], Fireworks, Groq, DeepInfra, Cerebras, SambaNova e altri

## Laboratori e creatori di modelli monitorati

[[entities/orgs/openai|OpenAI]], Anthropic, Google (Gemini), [[entities/orgs/meta|Meta]] (Llama/Muse), DeepSeek, Mistral, Kimi (Moonshot AI), SpaceXAI, MiniMax, NVIDIA, Alibaba (Qwen), Xiaomi, Z AI, Thinking Machines, Cohere, MBZUAI, Tencent

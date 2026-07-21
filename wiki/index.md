# Index

## Overview
- [[overview]] — Panoramica di Artificial Analysis: piattaforma indipendente di benchmarking AI

## Sources
- [[sources/guide]] — Guida all'uso di AA: come scegliere modello e provider | ingested 2026-07-21
- [[sources/methodology]] — Metodologia ufficiale AA: scope, definizioni, standard di misurazione | ingested 2026-07-21
- [[sources/intelligence-benchmarking]] — Intelligence Index v4.1: composizione e benchmark | ingested 2026-07-21
- [[sources/performance-benchmarking]] — Performance API: workload, metriche, integrità | ingested 2026-07-21
- [[sources/capability-indices]] — Skill e Industry Indices: composizione e pesi | ingested 2026-07-21
- [[sources/system-load-test]] — AA-SLT: benchmark di carico sistema | ingested 2026-07-21
- [[sources/coding-agents-benchmarking]] — Coding Agent Index v1.2: 321 task su 3 componenti | ingested 2026-07-21
- [[sources/agentperf]] — AA-AgentPerf: benchmark hardware per deployment agentici | ingested 2026-07-21
- [[sources/image-methodology]] — Benchmark generazione immagini: qualità, velocità, prezzo | ingested 2026-07-21
- [[sources/music-methodology]] — Music Arena: blind pairwise voting per musica | ingested 2026-07-21
- [[sources/openness-index-methodology]] — Openness Index: trasparenza pesi, dati, metodologia | ingested 2026-07-21
- [[sources/speech-to-speech-methodology]] — Speech-to-Speech Index: 3 dimensioni (33/33/33) | ingested 2026-07-21
- [[sources/speech-to-text-methodology]] — AA-WER v2.2: STT con streaming evaluation | ingested 2026-07-21
- [[sources/text-to-speech-methodology]] — TTS Arena: Controlled vs Provider Voices | ingested 2026-07-21
- [[sources/video-methodology]] — Video Arena: 6 modalità, Elo orario | ingested 2026-07-21

## Entities

### Organizations
- [[entities/orgs/artificial-analysis]] — Piattaforma indipendente di benchmarking AI, creatore di tutti i benchmark AA
- [[entities/orgs/aws]] — Amazon Web Services / Bedrock, provider cloud
- [[entities/orgs/openai]] — Laboratorio AI, creatore di GPT, standard di tokenizzazione AA
- [[entities/orgs/meta]] — Meta AI, creatore di Llama e Muse
- [[entities/orgs/together-ai]] — Provider di inferenza per modelli open-weight
- [[entities/orgs/anthropic]] — Laboratorio AI, creatore di Claude (Opus)
- [[entities/orgs/google]] — Google DeepMind / Gemini
- [[entities/orgs/deepseek]] — Laboratorio AI cinese, modelli open-weight
- [[entities/orgs/mistral]] — Laboratorio AI francese, modelli open-weight
- [[entities/orgs/kimi]] — Moonshot AI, creatore di Kimi K3
- [[entities/orgs/spacexai]] — xAI di Elon Musk (Grok)
- [[entities/orgs/minimax]] — Laboratorio AI cinese
- [[entities/orgs/nvidia]] — NVIDIA AI
- [[entities/orgs/alibaba]] — Alibaba Cloud / Qwen
- [[entities/orgs/xiaomi]] — Xiaomi AI
- [[entities/orgs/z-ai]] — Z AI
- [[entities/orgs/thinking-machines]] — Thinking Machines (Inkling)
- [[entities/orgs/cohere]] — Cohere AI
- [[entities/orgs/mbzuai]] — MBZUAI Institute of Foundation Models
- [[entities/orgs/tencent]] — Tencent AI (Hy)
- [[entities/orgs/sierra]] — Sviluppatore del benchmark τ-bench (τ³-Banking)
- [[entities/orgs/stanford]] — Stanford University, sviluppatore di Terminal-Bench

## Concepts
- [[concepts/lufs-normalization]] — Normalizzazione loudness ITU-R BS.1770 per la Music Arena
- [[concepts/model-selection-framework]] — Processo AA: use-case → modello → provider
- [[concepts/blended-price]] — Prezzo combinato 7:2:1 (cache hit : input : output)
- [[concepts/cost-per-task]] — Costo medio pesato per task nell'Intelligence Index
- [[concepts/model-ecosystem]] — Distinzione Model, Model Creator, Endpoint, Provider, System
- [[concepts/open-weights]] — Modelli a pesi pubblici vs proprietari, classificazione AA
- [[concepts/output-speed]] — Metriche di performance: TTFT, Output Speed, Response Time
- [[concepts/serverless]] — Pay-per-use nel contesto delle API LLM
- [[concepts/streaming-latency]] — Metriche di latenza per STT streaming: final e partial transcript
- [[concepts/token]] — OpenAI Tokens vs Native Tokens, standard di misurazione AA
- [[concepts/intelligence-index]] — Artificial Analysis Intelligence Index: indice composito di intelligenza
- [[concepts/gdpval-aa]] — GDPval-AA v2: benchmark su task lavorativi reali
- [[concepts/tau3-banking]] — τ³-Banking: benchmark di tool use agentico
- [[concepts/terminal-bench]] — Terminal-Bench: benchmark di coding agentico
- [[concepts/aa-omniscience]] — AA-Omniscience: benchmark di conoscenza e allucinazione
- [[concepts/aa-briefcase]] — AA-Briefcase: benchmark di knowledge work di lungo periodo
- [[concepts/aa-lcr]] — AA-LCR: benchmark di long context reasoning
- [[concepts/openness-index]] — Openness Index: indice di apertura e trasparenza dei modelli
- [[concepts/bradley-terry]] — Modello statistico per ranking da confronti a coppie (usato in tutte le arene AA)
- [[concepts/word-error-rate]] — Metrica WER: formula, normalizzazione, distanza di Levenshtein
- [[concepts/cache-pricing]] — Modelli di pricing della cache: cache hit, write, storage
- [[concepts/full-duplex]] — Conversazione bidirezionale simultanea nei modelli speech-to-speech
- [[concepts/scicode]] — SciCode: benchmark di generazione codice scientifico
- [[concepts/humanitys-last-exam]] — HLE: benchmark di ragionamento estremo
- [[concepts/gpqa-diamond]] — GPQA Diamond: benchmark di ragionamento scientifico
- [[concepts/critpt]] — CritPt: benchmark di ragionamento critico
- [[concepts/harvey-lab-aa]] — Harvey LAB-AA: benchmark legale sviluppato con Harvey
- [[concepts/apex-agents-aa]] — APEX-Agents-AA: benchmark agentico
- [[concepts/automationbench-aa]] — AutomationBench-AA: benchmark di automazione
- [[concepts/enterpriseops-gym-aa]] — EnterpriseOps-Gym-AA: benchmark enterprise IT ops
- [[concepts/itbench-aa]] — ITBench-AA: benchmark IT
- [[concepts/livecodebench]] — LiveCodeBench: benchmark di coding live
- [[concepts/ifbench]] — IFBench: benchmark di instruction following
- [[concepts/mmlu-pro]] — MMLU-Pro: benchmark multidisciplinare avanzato
- [[concepts/global-mmlu-lite]] — Global MMLU-Lite: benchmark multidisciplinare globale
- [[concepts/mmmu-pro]] — MMMU-Pro: benchmark multimodale avanzato
- [[concepts/capability-indices]] — Indici di capacità per skill e industrie
- [[concepts/coding-agent-index]] — Indice composito di coding agentico
- [[concepts/aa-slt]] — System Load Test: benchmark di carico sistema AA
- [[concepts/aa-agentperf]] — AgentPerf: benchmark hardware per deployment agentici
- [[concepts/image-arena]] — Arena di valutazione qualitativa per generazione immagini
- [[concepts/music-arena]] — Arena di valutazione qualitativa per generazione musicale
- [[concepts/speech-to-speech-index]] — Indice composito S2S: ragionamento, conversazione, agentico
- [[concepts/speech-to-text]] — Benchmark STT: AA-WER Index + streaming evaluation
- [[concepts/text-to-speech-arena]] — Arena TTS: Controlled Voices vs Provider Voices
- [[concepts/video-arena]] — Arena di valutazione qualitativa per generazione video
- [[concepts/aa-wer]] — Word Error Rate benchmark v2.2 per speech-to-text
- [[concepts/big-bench-audio]] — Adattamento audio di Big Bench Hard per speech reasoning
- [[concepts/tau-voice]] — Benchmark agentico voice con 278 scenari customer service

## Comparisons

## Questions

---
type: entity
entity_type: org
---

# Artificial Analysis

Artificial Analysis è una piattaforma indipendente di benchmarking e analisi dell'AI. Valuta modelli linguistici, agenti, modelli di generazione media e provider API con metriche oggettive di intelligenza, velocità e costo.

## Mentions across sources

| Source | What's said | Date |
|--------|-------------|------|
| [[sources/methodology]] | AA definisce il proprio scope e terminologia standard | 2026-07-21 |
| [[sources/guide]] | AA fornisce un framework decisionale use-case → modello → provider | 2026-07-21 |
| [[sources/intelligence-benchmarking]] | AA sviluppa e mantiene l'Intelligence Index v4.1 con 9 valutazioni indipendenti | 2026-07-21 |
| [[sources/performance-benchmarking]] | AA misura performance API in modo indipendente con integrity terms | 2026-07-21 |

## Key facts

- Fondata come piattaforma indipendente: nessun compenso dai provider per listing o risultati favorevoli
- Server di testing primario: Google Cloud us-central1-a
- Standard di misurazione: OpenAI Tokens (tiktoken o200k_base) per velocità, native tokens per prezzi
- Integrity terms: i provider non devono distinguere o trattare diversamente il traffico AA
- Copre: LLM, coding agents, generazione immagini/video/musica, STT, TTS, speech-to-speech, hardware
- Metodologia completamente pubblica e trasparente (prompt, parametri, scoring)
- Dataset proprietari: AA-AgentTalk (STT), AA-Briefcase (knowledge work), GDPval-AA (implementazione di GDPval)

## Relationships

- [[concepts/intelligence-index]] — l'indice composito di punta sviluppato da AA
- [[concepts/model-selection-framework]] — il framework decisionale promosso da AA
- Tutti i concept e le valutazioni nella wiki sono derivative del lavoro di AA

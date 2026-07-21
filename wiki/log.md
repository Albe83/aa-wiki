# Log

## [2026-07-21] setup | Wiki initialized
- Created: initial directory structure, schema (`AGENTS.md`), index, log
- Notes: wiki ready for first source ingest

## [2026-07-21] setup | Seeded domain overview
- Created: [[overview]] — sintesi del dominio Artificial Analysis basata sul sito web
- Updated: [[index]] — aggiunte voci per org, concept e valutazioni chiave
- Notes: le pagine entity e concept elencate nell'index sono placeholder (link rotti) — verranno create durante gli ingest successivi di fonti da `raw/`

## [2026-07-21] ingest | Artificial Analysis Benchmarking Methodology
- Created: [[sources/methodology]]
- Created: [[concepts/model-ecosystem]], [[concepts/token]], [[concepts/cost-per-task]], [[concepts/output-speed]], [[concepts/open-weights]], [[concepts/serverless]], [[concepts/blended-price]]
- Created: [[entities/orgs/openai]], [[entities/orgs/meta]], [[entities/orgs/aws]], [[entities/orgs/together-ai]]
- Updated: [[overview]], [[index]]
- Notes: prima fonte ingerita. Definisce il vocabolario base AA (OpenAI Tokens come standard, blended price 7:2:1, distinzione Model/Endpoint/Provider). 7 concept e 4 entity create.

## [2026-07-21] ingest | Using Artificial Analysis — Guide
- Created: [[sources/guide]]
- Created: [[concepts/model-selection-framework]], [[entities/orgs/deepseek]]
- Updated: [[overview]], [[index]]
- Notes: framework decisionale use-case → modello → provider. Creato DeepSeek (citato come esempio).

## [2026-07-21] ingest | Intelligence Benchmarking Methodology
- Created: [[sources/intelligence-benchmarking]]
- Updated: [[index]] — aggiunte 20 concept e 2 entity
- Notes: Intelligence Index v4.1 + benchmark aggiuntivi. Creati placeholder per tutti i benchmark nel Concepts index.

## [2026-07-21] ingest | Performance Benchmarking Methodology
- Created: [[sources/performance-benchmarking]]
- Updated: [[index]]
- Notes: v2.2.0 ha spostato workload default a 10K input token. Integrità: i provider non devono distinguere il traffico AA.

## [2026-07-21] ingest | Capability Indices Methodology
- Created: [[sources/capability-indices]]
- Updated: [[index]]
- Notes: 2 Skill Indices + 6 Industry Indices. AA-Omniscience è il componente più trasversale.

## [2026-07-21] ingest | System Load Test (AA-SLT) Methodology
- Created: [[sources/system-load-test]]
- Updated: [[index]]
- Notes: Carico sostenuto a concorrenza crescente fino a throughput ceiling. Complementare ai benchmark API standard.

## [2026-07-21] ingest | Coding Agent Index Methodology
- Created: [[sources/coding-agents-benchmarking]]
- Updated: [[index]]
- Notes: 321 task, 3 componenti, scoring pass@1. Tre versioni in tre mesi — campo in rapida evoluzione.

## [2026-07-21] ingest | AA-AgentPerf Methodology
- Created: [[sources/agentperf]]
- Updated: [[index]]
- Notes: Benchmark hardware per deployment agentici con SLO tier. Traiettorie reali OpenCode, normalizzazione per MW.

## [2026-07-21] ingest | Image Generation Benchmarking Methodology
- Created: [[sources/image-methodology]]
- Updated: [[index]]
- Notes: Image Arena con Bradley-Terry MLE. Classificazione Standard/Modified per endpoint.

## [2026-07-21] ingest | Methodology sub-pages (7 pages)
- Created: [[sources/music-methodology]], [[sources/openness-index-methodology]], [[sources/speech-to-speech-methodology]], [[sources/speech-to-text-methodology]], [[sources/text-to-speech-methodology]], [[sources/video-methodology]]
- Created: [[entities/orgs/sierra]], [[entities/orgs/stanford]]
- Updated: [[overview]], [[index]]
- Notes: Bulk ingest of remaining methodology sub-pages. Complete AA evaluation framework now documented. Added Intelligence Index v4.1 breakdown to overview.

## [2026-07-21] lint | Health check and fix broken links
- Created: [[entities/orgs/artificial-analysis]], [[concepts/bradley-terry]], [[concepts/cache-pricing]], [[concepts/word-error-rate]], [[concepts/streaming-latency]], [[concepts/full-duplex]], [[concepts/lufs-normalization]]
- Updated: [[index]]
- Notes: Lint found 56 broken links from 21 missing pages. Fixed 7 high-priority concept pages + 1 entity (Artificial Analysis itself). Remaining 14 broken links are placeholder orgs in index — intentional, will be created when cited by sources.

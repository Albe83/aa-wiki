# Log

## [2026-07-21] setup | Wiki initialized
- Created: initial directory structure, schema (`AGENTS.md`), index, log
- Notes: wiki ready for first source ingest

## [2026-07-21] setup | Seeded domain overview
- Created: [[overview]] — Artificial Analysis domain synthesis based on the website
- Updated: [[index]] — added entries for key orgs, concepts, and evaluations
- Notes: entity and concept pages listed in the index are placeholders (broken links) — they will be created during subsequent source ingests from `raw/`

## [2026-07-21] ingest | Artificial Analysis Benchmarking Methodology
- Created: [[sources/methodology]]
- Created: [[concepts/model-ecosystem]], [[concepts/token]], [[concepts/cost-per-task]], [[concepts/output-speed]], [[concepts/open-weights]], [[concepts/serverless]], [[concepts/blended-price]]
- Created: [[entities/orgs/openai]], [[entities/orgs/meta]], [[entities/orgs/aws]], [[entities/orgs/together-ai]]
- Updated: [[overview]], [[index]]
- Notes: first source ingested. Defines the AA base vocabulary (OpenAI Tokens as standard, 7:2:1 blended price, Model/Endpoint/Provider distinction). 7 concepts and 4 entities created.

## [2026-07-21] ingest | Using Artificial Analysis — Guide
- Created: [[sources/guide]]
- Created: [[concepts/model-selection-framework]], [[entities/orgs/deepseek]]
- Updated: [[overview]], [[index]]
- Notes: use-case → model → provider decision framework. Created DeepSeek (cited as example).

## [2026-07-21] ingest | Intelligence Benchmarking Methodology
- Created: [[sources/intelligence-benchmarking]]
- Updated: [[index]] — added 20 concepts and 2 entities
- Notes: Intelligence Index v4.1 + additional benchmarks. Created placeholders for all benchmarks in the Concepts index.

## [2026-07-21] ingest | Performance Benchmarking Methodology
- Created: [[sources/performance-benchmarking]]
- Updated: [[index]]
- Notes: v2.2.0 moved default workload to 10K input tokens. Integrity: providers must not distinguish AA traffic.

## [2026-07-21] ingest | Capability Indices Methodology
- Created: [[sources/capability-indices]]
- Updated: [[index]]
- Notes: 2 Skill Indices + 6 Industry Indices. AA-Omniscience is the most cross-cutting component.

## [2026-07-21] ingest | System Load Test (AA-SLT) Methodology
- Created: [[sources/system-load-test]]
- Updated: [[index]]
- Notes: Sustained load at increasing concurrency up to throughput ceiling. Complementary to standard API benchmarks.

## [2026-07-21] ingest | Coding Agent Index Methodology
- Created: [[sources/coding-agents-benchmarking]]
- Updated: [[index]]
- Notes: 321 tasks, 3 components, pass@1 scoring. Three versions in three months — rapidly evolving field.

## [2026-07-21] ingest | AA-AgentPerf Methodology
- Created: [[sources/agentperf]]
- Updated: [[index]]
- Notes: Hardware benchmark for agentic deployments with SLO tiers. Real OpenCode trajectories, normalization per MW.

## [2026-07-21] ingest | Image Generation Benchmarking Methodology
- Created: [[sources/image-methodology]]
- Updated: [[index]]
- Notes: Image Arena with Bradley-Terry MLE. Standard/Modified endpoint classification.

## [2026-07-21] ingest | Methodology sub-pages (7 pages)
- Created: [[sources/music-methodology]], [[sources/openness-index-methodology]], [[sources/speech-to-speech-methodology]], [[sources/speech-to-text-methodology]], [[sources/text-to-speech-methodology]], [[sources/video-methodology]]
- Created: [[entities/orgs/sierra]], [[entities/orgs/stanford]]
- Updated: [[overview]], [[index]]
- Notes: Bulk ingest of remaining methodology sub-pages. Complete AA evaluation framework now documented. Added Intelligence Index v4.1 breakdown to overview.

## [2026-07-21] lint | Health check and fix broken links
- Created: [[entities/orgs/artificial-analysis]], [[concepts/bradley-terry]], [[concepts/cache-pricing]], [[concepts/word-error-rate]], [[concepts/streaming-latency]], [[concepts/full-duplex]], [[concepts/lufs-normalization]]
- Updated: [[index]]
- Notes: Lint found 56 broken links from 21 missing pages. Fixed 7 high-priority concept pages + 1 entity (Artificial Analysis itself). Remaining 14 broken links are placeholder orgs in index — intentional, will be created when cited by sources.

## [2026-07-21] ingest | AA-WER v2.0 article + missing concept pages
- Created: [[sources/aa-wer-v2]], [[concepts/deepswe]], [[concepts/swatlas-qna]], [[concepts/aa-agenttalk]], [[concepts/voxpopuli-cleaned-aa]], [[concepts/earnings22-cleaned-aa]]
- Updated: [[index]]
- Notes: Filled gaps found during lint. DeepSWE and SWE-Atlas-QnA are Coding Agent Index components. AA-AgentTalk, VoxPopuli-Cleaned-AA, Earnings22-Cleaned-AA are the 3 datasets composing AA-WER v2.0+. Saved authoritative source: AA-WER v2.0 blog post and HuggingFace dataset cards to raw/.

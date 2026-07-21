---
type: overview
---

# Artificial Analysis — Overview

Artificial Analysis is an independent AI analysis and benchmarking platform. It evaluates language models, agents, media generation models (images, video, speech), and API providers, offering objective metrics on **intelligence**, **speed**, and **cost**.

## Methodology

AA benchmarks both proprietary and open-weight models. The guiding principle is to measure the **real user experience**, not theoretical maximum performance on specific hardware. See [[sources/methodology]] for full details.

### Measurement standards
- **Speed**: measured in [[concepts/token|OpenAI Tokens]] (tiktoken o200k_base) for fair comparisons across models
- **Pricing**: expressed in native tokens; the [[concepts/blended-price|blended price]] assumes a 7:2:1 ratio (cache hit : input : output)
- **Real cost**: [[concepts/cost-per-task|Cost per Task]] is weighted across Intelligence Index benchmarks — incorporates model verbosity
- **Performance**: measured as end-to-end customer experience, not theoretical maximum throughput

### Key terminology
The [[concepts/model-ecosystem|Model → Model Creator → Endpoint → Provider → System]] distinction is fundamental to interpreting AA data.

### Intelligence Index v4.1 evaluations

The [[concepts/intelligence-index|Intelligence Index v4.1]] aggregates 9 independent evaluations across 4 categories (total weight 100%):

**Agents (34%)**
- **GDPval-AA v2 (20%)**: agentic knowledge work tasks on a proprietary dataset — the highest single-weight evaluation
- **τ³-Banking (14%)**: agentic customer interaction in the fintech domain, 97 tasks, developed by [[entities/orgs/sierra|Sierra AI]]

**Coding (24%)**
- **Terminal-Bench v2.1 (16%)**: terminal and system administration tasks, developed by [[entities/orgs/stanford|Stanford/Laude Institute]], 89 tasks
- **SciCode (8%)**: scientific code generation

**Scientific reasoning (24%)**
- **HLE — Humanity's Last Exam (12%)**: extreme reasoning on frontier questions
- **GPQA Diamond (6%)**: advanced scientific reasoning
- **CritPt (6%)**: critical reasoning and argument evaluation

**General (18%)**
- **AA-Omniscience (12%)**: multidisciplinary knowledge (8% accuracy + 4% non-hallucination)
- **AA-LCR (6%)**: long context reasoning

All evaluations use pass@1 scoring, temperature 0 (non-reasoning models) or 0.6 (reasoning). Confidence interval ~±1%.

## Selection framework

AA proposes a three-step decision process: **use-case → model → provider**. See [[concepts/model-selection-framework]] and [[sources/guide]].

## Areas covered

### Intelligence (language models)
- **Intelligence Index v4.1**: composite index based on 9 independent evaluations
- **Evaluations**: [[concepts/gdpval-aa|GDPval-AA v2]], [[concepts/tau3-banking|τ³-Banking]], [[concepts/terminal-bench|Terminal-Bench v2.1]], SciCode, Humanity's Last Exam, GPQA Diamond, CritPt, [[concepts/aa-omniscience|AA-Omniscience]], [[concepts/aa-lcr|AA-LCR]]
- **[[concepts/aa-briefcase|AA-Briefcase]]**: agentic benchmark for long-duration knowledge work
- **Capability Indices**: sector-specific indices (Agentic, Coding, Finance & Accounting, Strategy & Ops, Legal, Healthcare, Engineering, Economics)

### Agents and coding
- **Coding Agent Index**: performance, cost, and execution time on end-to-end software engineering tasks
- **AA-Agentic Index**: tool use, planning, autonomy, complex problem solving

### Speed and latency
- [[concepts/output-speed|Output speed]] in tokens per second, time per task, end-to-end latency
- Comparison across API providers (first-party and third-party)

### Price and cost
- [[concepts/cost-per-task|Cost per task]] weighted across the Intelligence Index
- Pricing for input, output, cache hit, cache write
- [[concepts/cache-pricing|Cache pricing models]] per provider

### Media
- **Image Arena**: text-to-image, image editing (Elo from blind votes)
- **Video Arena**: text-to-video, image-to-video, video editing
- **Speech**: Text-to-Speech Arena, Speech-to-Text (AA-WER Index), Speech-to-Speech

### Openness
- **[[concepts/openness-index|Openness Index]]**: training data transparency, methodology, weight availability

### API providers
- Performance and pricing compared across providers for open-weight models
- Monitored providers: [[entities/orgs/openai|OpenAI]], Anthropic, Google, [[entities/orgs/aws|AWS Bedrock]], Azure, [[entities/orgs/together-ai|Together AI]], Fireworks, Groq, DeepInfra, Cerebras, SambaNova, and others

## Model labs and creators monitored

[[entities/orgs/openai|OpenAI]], Anthropic, Google (Gemini), [[entities/orgs/meta|Meta]] (Llama/Muse), DeepSeek, Mistral, Kimi (Moonshot AI), SpaceXAI, MiniMax, NVIDIA, Alibaba (Qwen), Xiaomi, Z AI, Thinking Machines, Cohere, MBZUAI, Tencent

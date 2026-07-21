---
type: concept
---

# AA-AgentTalk

AA-AgentTalk is a proprietary, held-out speech dataset developed by Artificial Analysis for evaluating speech-to-text models on voice agent use cases. It is the largest component (50% weight) of the [[concepts/aa-wer|AA-WER Index v2.0+]], introduced in February 2026.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/speech-to-text-methodology]] | AA-WER v2.2 methodology: 469 samples, ~250 min, 50% weight | 2026-07-21 |

## Dataset composition

| Property | Value |
|----------|-------|
| Samples | 469 |
| Total duration | ~250 minutes |
| Sample duration range | 8–109 seconds |
| Speakers | Multiple participants with diverse accents |
| Type | Proprietary, held-out, scripted prompts read aloud |

## Content categories

| Category | Share | Description |
|----------|-------|-------------|
| Voice Agents & Call Centers | 40% | Customer and internal support, complex inquiries, scheduling |
| AI Agent Prompting & Interaction | 20% | Coding agents, research agents, writing, data analysis |
| Industry Jargon | 15% | Financial services, healthcare, insurance, legal, engineering |
| Meetings & Collaboration | 10% | Client meetings, technical meetings, cross-functional |
| Consumer & Personal | 10% | Personal assistant, shopping, smart home, productivity |
| Media | 5% | Interviews, podcasts, panel shows, sports commentary |

## Recording characteristics

- **17 accent groups** represented
- **8 speaking styles:** natural (75%), fast, quiet, slow, loud, tired, alternating volume, out of breath
- **70% quiet indoor**, 30% with background noise
- Recorded on participants' own devices in natural environments

## Design rationale

As a proprietary, held-out dataset, AA-AgentTalk mitigates the risk of models being trained or fine-tuned to perform well on public test sets — a growing concern with widely-used STT benchmarks. The focus on voice agent speech reflects market shift from general transcription to conversational AI.

## Relationships

- [[concepts/aa-wer]] — AA-AgentTalk is the primary dataset in AA-WER v2.0+, weighted at 50%
- [[concepts/voxpopuli-cleaned-aa]] — companion dataset (25% weight, parliamentary speech)
- [[concepts/earnings22-cleaned-aa]] — companion dataset (25% weight, corporate earnings calls)
- [[concepts/speech-to-text]] — broader STT benchmarking context

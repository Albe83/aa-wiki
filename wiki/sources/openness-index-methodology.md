---
type: source
date: 2026-07-21
source_file: raw/openness-index.md
status: processed
---

# Openness Index Methodology

**Source:** https://artificialanalysis.ai/methodology/openness-index
**Ingested:** 2026-07-21
**Type:** article

## Summary

The [[concepts/openness-index]] is a composite metric measuring how openly available and transparently documented AI models are. It evaluates three dimensions: Model Availability (weights access, 0-3 points), Model Transparency — Data (pre- and post-training data disclosure, averaged for max 6 points), and Model Transparency — Methodology (technical disclosure and code availability, 0-3 points). The maximum raw score is 18, normalized to a 0-100 scale.

Each dimension uses a 4-point scale (0-3) combining access and licensing criteria. For weights: 0 = closed/no API through 3 = [[concepts/open-weights]] with no meaningful limitations. For data: 0 = no disclosure through 3 = full data shared. For methodology: 0 = no disclosure through 3 = full technical details with pipeline code and commercial use allowed. The index intentionally separates data transparency (pre- and post-training) from methodology transparency to prevent conflating distinct aspects of openness. A detailed specification is available as a PDF download.

## Key points

- Three dimensions: Weights Availability (0-3), Data Transparency (0-6, pre + post averaged), Methodology Transparency (0-3)
- Raw score max 18, normalized to 0-100
- Each sub-score combines access level with license permissiveness
- Data dimension is double-weighted: averaging pre-training and post-training data disclosure
- Distinguishes [[concepts/open-weights]] from full openness — open weights alone score 3/18 (16.7)
- Detailed specification available as PDF download
- No compensation accepted from providers

## Entities mentioned

- [[entities/orgs/artificial-analysis]] — benchmarking platform

## Concepts mentioned

- [[concepts/openness-index]] — composite 0-100 metric for AI model openness
- [[concepts/open-weights]] — a specific level on the index; open weights alone yield only ~17/100

## Related sources

- [[sources/methodology]] — parent methodology page

## My notes

The index's key insight is that "open weights" is a narrow slice of openness. A model with open weights but no data or methodology disclosure scores only 3/18 (16.7/100). The double-weighting of data transparency (averaging pre- and post-training) reflects the reality that data is the most contested and opaque aspect of modern AI development. The emphasis on license permissiveness alongside raw access is also notable — availability without usable licensing is not meaningful openness.

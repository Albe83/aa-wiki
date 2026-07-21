---
type: concept
---

# AA Openness Index

Composite metric (0-100) measuring how openly available and transparently documented AI models are. The index evaluates three dimensions: Model Availability (weights access + license, 0-3 points), Model Transparency — Data (pre-training and post-training disclosure averaged, max 6 points), and Model Transparency — Methodology (technical disclosure + code license, 0-3 points). The maximum raw score is 18, normalized to a 0-100 scale. A model with [[concepts/open-weights]] but no data or methodology transparency scores 3/18 (≈17/100), illustrating that true openness requires all three dimensions.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/openness-index-methodology]] | Full specification of the three-dimension composition, scoring tiers, and normalization | 2026-07-21 |

## Key details

### Model Availability — Weights (0-3)
| Score | Access | License |
|-------|--------|---------|
| 0 | Closed weights, no API | Closed or no commercial use |
| 1 | Closed weights, API with limits | Commercial use, attribution required |
| 2 | Closed weights, API available | Commercial use, no attribution |
| 3 | [[concepts/open-weights]] | No meaningful limitations |

### Model Transparency — Data (0-6, pre + post averaged)
| Score | Access | License |
|-------|--------|---------|
| 0 | No/limited disclosure | No commercial use |
| 1 | Partial data source detail | Commercial use, attribution |
| 2 | Full data mix, substantial shared | Commercial use, no attribution |
| 3 | Full data shared | No meaningful limitations |

Both pre-training and post-training data are scored separately (0-3 each), then averaged together for a max of 6 points in this dimension.

### Model Transparency — Methodology (0-3)
| Score | Disclosure | License |
|-------|------------|---------|
| 0 | No/limited disclosure | No code disclosed |
| 1 | Model architecture disclosed | Frameworks open, commercial use |
| 2 | Limited general technical disclosure | Training pipeline code/guide released |
| 3 | Full technical details disclosed | Pipeline code + commercial use allowed |

### Score Calculation
- Three components summed → max raw score of 18
- Normalized to 0-100 scale
- Data transparency is double-weighted (averaging pre- and post-training) reflecting the reality that data is the most contested and opaque aspect of modern AI development
- Detailed specification available as PDF download

## Relationships
- [[concepts/open-weights]] — Open weights alone yield only ≈17/100 on the Openness Index; the index intentionally separates "weights available" from full transparency
- [[concepts/intelligence-index]] — Complementary dimension: Intelligence Index measures capability, Openness Index measures transparency
- [[entities/orgs/artificial-analysis]] — developer and maintainer of the Openness Index

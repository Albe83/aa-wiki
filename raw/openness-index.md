# Openness Index Methodology

**Source:** https://artificialanalysis.ai/methodology/openness-index
**Fetched:** 2026-07-21

## Overview

Composite metric measuring how openly available and transparently documented AI models are. Covers weight availability and transparency of data/methodology.

## Index Composition (max raw score 18)

### 1. Model Availability — Weights
| Score | Access | License |
|-------|--------|---------|
| 0 | Closed weights, no API | Closed or no commercial use |
| 1 | Closed weights, API limits tokens | Commercial use, attribution required |
| 2 | Closed weights, API available | Commercial use, no attribution |
| 3 | Open weights | No meaningful limitations |

### 2. Model Transparency — Data (Pre & Post Training, averaged)
| Score | Access | License |
|-------|--------|---------|
| 0 | No/limited disclosure | No commercial use |
| 1 | Partial data source detail | Commercial use, attribution |
| 2 | Full data mix, substantial shared | Commercial use, no attribution |
| 3 | Full data shared | No meaningful limitations |

### 3. Model Transparency — Methodology
| Score | Disclosure | License |
|-------|------------|---------|
| 0 | No/limited disclosure | No code disclosed |
| 1 | Model architecture disclosed | Frameworks open, commercial use |
| 2 | Limited general technical disclosure | Training pipeline code/guide released |
| 3 | Full technical details disclosed | Pipeline code + commercial use allowed |

## Score Calculation
- Data components averaged (pre + post training) → max 6 points
- All components summed → max raw 18
- Normalized to 0-100 scale

Detailed spec available as PDF download.

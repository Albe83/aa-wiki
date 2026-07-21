---
type: concept
---

# AA Image Arena

Blind pairwise human preference voting arena for evaluating image generation quality. Users are shown two images side-by-side (anonymized) and vote on which is better. Elo scores are derived via Bradley-Terry Maximum Likelihood Estimation, yielding quality rankings. The arena covers two separate modalities, each with its own independent Elo pool: **Text-to-Image** (generate from text prompt) and **Image Editing** (edit an existing image). All images are generated at each model's highest supported resolution, then downscaled to 1024×1024 for consistent comparison. Fixed parameters: 1 image per prompt, 1:1 aspect ratio, seed 42.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/image-methodology]] | Arena mechanics, resolution standardization, endpoint classification, pairwise MLE Elo | 2026-07-21 |

## Key details

### Elo Calculation
- Bradley-Terry MLE from blind pairwise human preference votes
- Separate Elo pools for Text-to-Image and Image Editing modalities
- Follows the same statistical approach as LMSYS Chatbot Arena

### Standardized Generation Parameters
- **Resolution:** Highest supported by each model, downscaled to 1024×1024 for arena display
- **Images per prompt:** 1
- **Aspect ratio:** 1:1
- **Seed:** 42
- Inference steps and guidance scale: published defaults

### Endpoint Classification
- **Standard:** Native model at full fidelity — the model's intended output quality
- **Modified:** Altered for speed/cost reasons — labeled distinctly and may be hidden by default

### Performance Metrics (from benchmarking, not arena)
- **Price per 1,000 Images:** Provider's published per-image rate × 1000
- **Generation Time:** Median over trailing 14 days, sampled 4× daily at random times, includes URL download time (simulates real user experience)

### Independence
No compensation accepted from providers. Strict independence maintained.

## Relationships
- [[concepts/video-arena]] — Same blind pairwise voting approach, different modality (video generation)
- [[concepts/music-arena]] — Same approach applied to music generation
- [[concepts/bradley-terry]] — Statistical model underlying Elo score calculation
- [[entities/orgs/artificial-analysis]] — operator of the Image Arena

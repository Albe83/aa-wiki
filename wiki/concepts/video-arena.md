---
type: concept
---

# AA Video Arena

Blind pairwise human preference voting arena for evaluating video generation quality. Users are shown two videos side-by-side (anonymized) and vote on which is better. Elo scores are derived via Bradley-Terry MLE, calculated separately per modality and **recalculated hourly** as new votes come in. The arena covers **six video modalities**: Text-to-Video, Image-to-Video, Video Editing, and each of these with Audio variants. Generation uses standardized defaults: 1080p, 24 FPS, 10 seconds duration, 16:9 aspect ratio, seed 42.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/video-methodology]] | Full specification of six video modalities, arena Elo mechanics, standardized generation parameters | 2026-07-21 |

## Key details

### Six Modalities
Each modality has its own independent Elo pool:
1. **Text-to-Video** — Generate video from text prompt
2. **Image-to-Video** — Generate video from a reference image (PNG lossless, 1920×1080)
3. **Video Editing** — Edit an existing video
4-6. Each of the above **with Audio** variants

### Elo Calculation
- Bradley-Terry MLE from blind pairwise human preference votes
- Recalculated hourly (more frequent than other arenas due to high vote velocity)
- Separate Elo pools for each of the 6 modalities

### Standardized Generation Parameters
- **Resolution:** 1080p
- **Frame rate:** 24 FPS
- **Duration:** 10 seconds
- **Aspect ratio:** 16:9
- **Seed:** 42
- **Prompt enhancement:** Enabled when recommended by model creator
- **CFG/guidance and inference steps:** Provider defaults

### Image-to-Video Specifics
- Reference images: PNG (lossless), 1920×1080, 16:9
- Upload time counted toward total Generation Time

### Performance Metrics (from benchmarking)
- **Price per Minute of Video:** Provider's published per-minute rate
- **Generation Time:** Median over trailing 14 days. Includes upload, queue, inference, and download — not just model inference time

### Independence
No compensation accepted from providers.

## Relationships
- [[concepts/image-arena]] — Same blind pairwise approach, applied to image generation
- [[concepts/music-arena]] — Same approach for music generation
- [[concepts/bradley-terry]] — Statistical model for Elo score derivation
- [[entities/orgs/artificial-analysis]] — operator of the Video Arena

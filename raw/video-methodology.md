# Video Generation Benchmarking Methodology

**Source:** https://artificialanalysis.ai/video/methodology
**Fetched:** 2026-07-21

## Scope

Benchmarks video generation models. Six modalities: Text to Video, Image to Video, Video Editing, and each with Audio variants.

## Default Settings

- Resolution: 1080p, Frame rate: 24 FPS, Duration: 10s, Aspect ratio: 16:9, Seed: 42
- Prompt enhancement: on when recommended by creator
- CFG/guidance and inference steps: provider default

## Key Metrics

- **Quality Elo:** From Video Arena user votes (Bradley-Terry MLE), separately per modality. Recalculated hourly.
- **Price per Minute of Video:** Provider's published per-minute rate
- **Generation Time:** Median over trailing 14 days. Text to Video: 1x daily. Includes upload, queue, inference, download.

## Image to Video specifics

Reference images: PNG (lossless), 1920x1080, 16:9. Upload time counted toward Generation Time.

## Independence

No compensation from providers. Strict independence.

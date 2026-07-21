---
type: source
date: 2026-07-21
source_file: raw/video-methodology.md
status: processed
---

# Video Generation Benchmarking Methodology

**Source:** https://artificialanalysis.ai/video/methodology
**Ingested:** 2026-07-21
**Type:** article

## Summary

Artificial Analysis benchmarks video generation models across six modalities: Text to Video, Image to Video, Video Editing, and each of these with Audio variants. Quality is measured via Elo scores derived from [[concepts/video-arena]] user votes (Bradley-Terry MLE), calculated separately per modality and recalculated hourly. Performance is tracked through Price per Minute of Video and Generation Time (median over 14 trailing days), which includes full pipeline latency — upload, queue, inference, and download.

All evaluations use standardized defaults: 1080p, 24 FPS, 10s duration, 16:9 aspect ratio, seed 42. Image-to-Video tests use lossless PNG reference images at 1920x1080. Prompt enhancement is enabled when recommended by the model creator, while CFG/guidance and inference steps use provider defaults.

## Key points

- Six video modalities benchmarked: Text-to-Video, Image-to-Video, Video Editing, each with Audio variants
- Quality measured via Video Arena Elo (Bradley-Terry MLE), recalculated hourly
- Generation Time includes upload, queue, inference, and download — not just model inference
- Standardized defaults: 1080p, 24 FPS, 10s, 16:9, seed 42
- Image-to-Video uses PNG lossless reference images (1920x1080)
- No compensation accepted from providers

## Entities mentioned

- [[entities/orgs/artificial-analysis]] — operator of the benchmarking platform and Video Arena

## Concepts mentioned

- [[concepts/video-arena]] — human preference voting arena for video generation, source of Elo quality scores
- [[concepts/bradley-terry]] — statistical model used to derive Elo scores from pairwise votes

## Related sources

- [[sources/methodology]] — parent methodology page

## My notes

Video Arena is the primary quality signal, following the LMSYS Chatbot Arena model of blind pairwise human preference voting. The six-modality structure covers the emerging video generation landscape comprehensively, with audio as a cross-cutting dimension rather than a separate pipeline.

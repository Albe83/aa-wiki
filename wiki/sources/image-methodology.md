---
type: source
date: 2026-07-21
source_file: raw/image-methodology.md
status: processed
---

# Image Generation Benchmarking Methodology

**Source:** https://artificialanalysis.ai/image/methodology
**Ingested:** 2026-07-21
**Type:** article

## Summary

Methodological page describing how Artificial Analysis benchmarks image generation models across three dimensions: quality, speed, and price. It covers two modalities — Text to Image and Image Editing — with standardized settings (maximum supported resolution, 1 image per prompt, 1:1 aspect ratio, seed 42) and metrics derived from both automatic evaluations and human votes in the Image Arena.

Quality is measured via Elo derived from user votes in the Image Arena (Bradley-Terry MLE), separately for each modality. Speed and price are measured with tests repeated 4 times per day, with medians over 14 days. Endpoints are classified as Standard (native model at full fidelity) or Modified (altered for speed/cost).

## Key points

- Two modalities: Text to Image, Image Editing
- Maximum resolution supported by each model, downscaled to 1024x1024 for the Arena
- Fixed parameters: 1 image per prompt, 1:1 aspect ratio, seed 42
- Quality: Elo from Image Arena (user votes, Bradley-Terry MLE)
- Price: provider-published rate per image × 1000
- Generation time: median over 14 days, 4 tests/day at random times, includes URL download
- Endpoint classification: Standard (native) vs Modified (optimized for speed/cost)
- Rigorous independence: no compensation from providers

## Entities mentioned

_none_

## Concepts mentioned

- [[concepts/image-arena]] — qualitative evaluation system based on human votes

## Related sources

- [[sources/methodology]] — general AA methodology

## My notes

- The Image Arena uses the same philosophy as the Chatbot Arena (LMSYS): human preferences aggregated with Bradley-Terry
- The Standard/Modified classification is important: some providers offer accelerated versions that sacrifice quality
- Including URL download in generation time makes the metric more realistic (simulates the complete user experience)
- 1024x1024 as the Arena's standard resolution enables fair comparisons between models with different native resolutions

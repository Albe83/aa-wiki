# Image Generation Benchmarking Methodology

**Source:** https://artificialanalysis.ai/image/methodology
**Fetched:** 2026-07-21

## Scope

Benchmarks image generation models on quality, speed, and price. Two modalities: Text to Image, Image Editing.

## Default Settings

- Highest resolution each model supports, downscaled to 1024x1024 for Arena
- 1 image per prompt, 1:1 aspect ratio, seed 42
- Published defaults for inference steps, guidance scale, negative prompts

## Key Metrics

- **Quality Elo:** From user votes in Image Arena (Bradley-Terry MLE), separately per modality
- **Price per 1,000 Images:** Provider's published per-image rate x 1000
- **Generation Time:** Median over trailing 14 days, 4x daily at random times, includes URL download

## Endpoint Classification

- **Standard:** Native model at full fidelity
- **Modified:** Altered for speed/cost (labeled and may be hidden by default)

## Independence

No compensation from providers. Strict independence.

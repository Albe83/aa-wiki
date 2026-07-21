---
type: concept
---

# LUFS Normalization

Audio loudness normalization standard used by Artificial Analysis in the Music Arena. LUFS (Loudness Units relative to Full Scale) measures perceived loudness according to the ITU-R BS.1770 standard.

## Application in the Music Arena

Before entering the Music Arena, each track is normalized:
- **Target:** -16 LUFS integrated loudness
- **Method:** single static gain (no compression, limiting, or EQ)
- **Ceiling:** -1 dBTP true-peak — if the track lacks sufficient headroom, it stops below the target
- **Final format:** 320 kbps MP3, 44.1 kHz

This ensures that Music Arena votes reflect musical quality, not volume differences.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/music-methodology]] | Audio normalization detail in the Music Arena | 2026-07-21 |

## Relationships
- [[concepts/music-arena]] — LUFS normalization is a mandatory step before voting

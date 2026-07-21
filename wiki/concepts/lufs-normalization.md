---
type: concept
---

# LUFS Normalization

Standard di normalizzazione del volume audio usato da Artificial Analysis nella Music Arena. LUFS (Loudness Units relative to Full Scale) misura il loudness percepito secondo lo standard ITU-R BS.1770.

## Applicazione nella Music Arena

Prima di entrare nella Music Arena, ogni traccia viene normalizzata:
- **Target:** -16 LUFS integrated loudness
- **Metodo:** singolo guadagno statico (no compressione, limiting o EQ)
- **Ceiling:** -1 dBTP true-peak — se la traccia non ha abbastanza headroom, si ferma sotto il target
- **Formato finale:** 320 kbps MP3, 44.1 kHz

Questo assicura che i voti nella Music Arena riflettano la qualità musicale, non differenze di volume.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/music-methodology]] | Dettaglio della normalizzazione audio nella Music Arena | 2026-07-21 |

## Relationships
- [[concepts/music-arena]] — la normalizzazione LUFS è un passaggio obbligatorio prima del voting

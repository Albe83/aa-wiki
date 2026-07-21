---
type: concept
---

# Blended Price

Prezzo combinato usato da Artificial Analysis per facilitare il confronto tra modelli, calcolato assumendo un rapporto **7:2:1** di:

- **Cache hit** (7 parti): token già in cache, prezzo scontato
- **Input** (2 parti): token di input non in cache, prezzo pieno
- **Output** (1 parte): token generati dal modello

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizione del blended price e del rapporto 7:2:1 | 2026-07-21 |

## Relationships
- [[concepts/cost-per-task]] — il blended price è una semplificazione; il Cost per Task è più accurato
- [[concepts/cache-pricing]] — i modelli di cache pricing variano per provider

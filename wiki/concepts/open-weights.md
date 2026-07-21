---
type: concept
---

# Open Weights

Modelli i cui pesi sono stati rilasciati pubblicamente dal creatore. Artificial Analysis usa "open weights" (o "open") anziché "open-source" perché molti LLM aperti sono rilasciati con licenze che non soddisfano la definizione completa di software open-source (es. restrizioni sull'uso commerciale).

## Classificazione AA

Nei grafici AA i modelli sono suddivisi in:
- **Proprietary**: pesi non rilasciati, accesso solo via API del creatore
- **Open Weights**: pesi pubblici, utilizzabili liberamente
- **Open Weights (Commercial Use Restricted)**: pesi pubblici ma uso commerciale limitato (tipicamente richiede licenza a pagamento)

## Fonti di performance per open weights

Per i modelli open weights, AA mostra tipicamente la mediana tra tutti i provider che li ospitano, non il dato di un singolo provider. Questo è rilevante perché speed e prezzo variano significativamente tra provider.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizione ufficiale AA di Open Weights | 2026-07-21 |

## Relationships
- [[concepts/model-ecosystem]] — gli open weights permettono a provider terzi di creare endpoint
- [[concepts/openness-index]] — l'Openness Index valuta anche trasparenza di dati e metodologia

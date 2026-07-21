---
type: concept
---

# Cost per Task e Pricing

Metrica di costo sviluppata da Artificial Analysis per confrontare il costo reale dell'uso dei modelli.

## Definizioni

### Price (Input/Output)
Il prezzo applicato da un provider per token di input inviato e per token di output ricevuto. I prezzi sono quelli correnti dichiarati dai provider.

### Blended Price
Prezzo combinato che assume un rapporto 7:2:1 di cache hit, input e output token, per facilitare il confronto.

### Cost per Task
Costo medio pesato (USD) per completare un task dell'Intelligence Index. Si calcola:

```
Cost per Task = Σ (prezzo_input × token_input + prezzo_cache × token_cache + prezzo_output × token_output) × peso_benchmark / numero_task
```

Il costo riflette l'effettivo consumo di token: modelli che producono risposte più lunghe o più reasoning token hanno un costo per task più alto, anche a parità di prezzo per token.

### Cost to Run Intelligence Index
Costo totale (USD) per eseguire tutte le valutazioni dell'Intelligence Index, calcolato sui prezzi del provider first-party.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizioni ufficiali AA di pricing e costo | 2026-07-21 |

## Current synthesis

Il Cost per Task è la metrica più realistica per confrontare il costo dei modelli perché incorpora la verbosità. Due modelli con lo stesso prezzo per token possono avere Cost per Task molto diversi se uno produce risposte più lunghe.

## Relationships
- [[concepts/blended-price]] — il rapporto 7:2:1 usato per il calcolo del prezzo combinato
- [[concepts/cache-pricing]] — dettaglio sui modelli di pricing della cache per provider

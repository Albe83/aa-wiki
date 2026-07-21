---
type: concept
---

# Token

Unità numeriche che rappresentano parole e caratteri su cui sono costruiti i moderni LLM. I modelli ricevono token in input e generano token in output.

## OpenAI Tokens vs Native Tokens

| Tipo | Descrizione | Uso in AA |
|------|-------------|-----------|
| **OpenAI Tokens** | Token prodotti dal tokenizer GPT-3.5/GPT-4 (tiktoken, o200k_base) | Unità standard per tutte le metriche di velocità (tokens/second) |
| **Native Tokens** | Token prodotti dal tokenizer nativo di ciascun LLM | Usati per i prezzi (USD per milione di token nativi) |

AA usa OpenAI Tokens come unità standard per permettere confronti equi tra modelli con tokenizer diversi. Un modello con tokenizer "avaro" (che produce meno token per lo stesso testo) apparirebbe artificialmente più veloce se misurato in native tokens.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizione ufficiale AA di Token, OpenAI Tokens, Native Tokens | 2026-07-21 |

## Current synthesis

La doppia unità di misura (OpenAI tokens per speed, native tokens per price) è una scelta pragmatica: permette confronti fair senza forzare tutti i provider a usare lo stesso tokenizer.

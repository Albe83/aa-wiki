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

Pagina metodologica che descrive come Artificial Analysis benchmarka i modelli di generazione immagini su tre dimensioni: qualità, velocità e prezzo. Copre due modalità — Text to Image e Image Editing — con impostazioni standardizzate (risoluzione massima supportata, 1 immagine per prompt, aspect ratio 1:1, seed 42) e metriche derivate sia da valutazioni automatiche che da voti umani nell'Image Arena.

La qualità è misurata tramite Elo derivato dai voti degli utenti nell'Image Arena (Bradley-Terry MLE), separatamente per ciascuna modalità. Velocità e prezzo sono misurati con test ripetuti 4 volte al giorno, con mediane su 14 giorni. Gli endpoint sono classificati come Standard (modello nativo a piena fedeltà) o Modified (alterato per velocità/costo).

## Key points

- Due modalità: Text to Image, Image Editing
- Risoluzione massima supportata da ciascun modello, downscalata a 1024x1024 per l'Arena
- Parametri fissi: 1 immagine per prompt, 1:1 aspect ratio, seed 42
- Qualità: Elo da Image Arena (voti utenti, Bradley-Terry MLE)
- Prezzo: tariffa pubblicata dal provider per immagine × 1000
- Tempo di generazione: mediana su 14 giorni, 4 test/giorno a orari casuali, include download URL
- Classificazione endpoint: Standard (nativo) vs Modified (ottimizzato per velocità/costo)
- Indipendenza rigorosa: nessun compenso dai provider

## Entities mentioned

_nessuna_

## Concepts mentioned

- [[concepts/image-arena]] — sistema di valutazione qualitativa basato su voti umani

## Related sources

- [[sources/methodology]] — metodologia generale AA

## My notes

- L'Image Arena usa la stessa filosofia delle Chatbot Arena (LMSYS): preferenze umane aggregate con Bradley-Terry
- La classificazione Standard/Modified è importante: alcuni provider offrono versioni accelerate che sacrificano qualità
- Il download URL incluso nel tempo di generazione rende la metrica più realistica (simula l'esperienza utente completa)
- 1024x1024 come risoluzione standard dell'Arena permette confronti equi tra modelli con risoluzioni native diverse

---
type: concept
---

# Model Ecosystem (Modello, Creatore, Endpoint, Provider, Sistema)

Distinzioni terminologiche fondamentali nell'ecosistema dei modelli linguistici, come definite da Artificial Analysis.

## Definizioni

| Termine | Definizione | Esempio |
|---------|-------------|---------|
| **Model** | Un large language model (LLM), proprietario o open weights | GPT-4, Llama 3, Claude |
| **Model Creator** | L'organizzazione che ha sviluppato e addestrato il modello | OpenAI per GPT-4, Meta per Llama 3 |
| **Endpoint** | Un'istanza hosted di un modello accessibile via API | GPT-4 su Azure, Llama 3 su Together |
| **System** | Ambiente di calcolo dedicato (es. VM) per eseguire modelli AI | VM con GPU per inference on-premise |
| **Provider** | Azienda che ospita e fornisce accesso a endpoint o sistemi | OpenAI, AWS Bedrock, Together.ai |

## Relazioni

- Uno stesso modello può avere endpoint multipli su provider diversi
- Un'azienda è spesso sia Model Creator che Provider (es. OpenAI, Google)
- I provider terze parti ospitano modelli open weights creati da altri (es. DeepInfra, Fireworks)

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Definizioni ufficiali AA dei termini dell'ecosistema | 2026-07-21 |

## Current synthesis

La distinzione Model/Endpoint/Provider è essenziale per interpretare correttamente i grafici AA. Quando AA confronta le performance API di un modello open-weight, mostra la varianza tra provider (output speed e prezzo possono differire drasticamente). Quando mostra l'Intelligence Index, il valore è unico per modello (l'intelligenza non cambia col provider).

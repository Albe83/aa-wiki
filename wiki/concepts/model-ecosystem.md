---
type: concept
---

# Model Ecosystem (Model, Creator, Endpoint, Provider, System)

Core terminological distinctions in the language model ecosystem, as defined by Artificial Analysis.

## Definitions

| Term | Definition | Example |
|------|------------|---------|
| **Model** | A large language model (LLM), proprietary or open weights | GPT-4, Llama 3, Claude |
| **Model Creator** | The organization that developed and trained the model | OpenAI for GPT-4, Meta for Llama 3 |
| **Endpoint** | A hosted instance of a model accessible via API | GPT-4 on Azure, Llama 3 on Together |
| **System** | Dedicated compute environment (e.g. VM) for running AI models | VM with GPU for on-premise inference |
| **Provider** | Company that hosts and provides access to endpoints or systems | OpenAI, AWS Bedrock, Together.ai |

## Relationships

- A single model can have multiple endpoints across different providers
- A company is often both Model Creator and Provider (e.g. OpenAI, Google)
- Third-party providers host open weights models created by others (e.g. DeepInfra, Fireworks)

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Official AA definitions of ecosystem terms | 2026-07-21 |

## Current synthesis

The Model/Endpoint/Provider distinction is essential for correctly interpreting AA charts. When AA compares the API performance of an open-weight model, it shows the variance across providers (output speed and price can differ drastically). When showing the Intelligence Index, the value is unique per model (intelligence does not change with the provider).

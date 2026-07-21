---
type: concept
---

# Token

Numerical units representing words and characters on which modern LLMs are built. Models receive tokens as input and generate tokens as output.

## OpenAI Tokens vs Native Tokens

| Type | Description | Use in AA |
|------|-------------|-----------|
| **OpenAI Tokens** | Tokens produced by the GPT-3.5/GPT-4 tokenizer (tiktoken, o200k_base) | Standard unit for all speed metrics (tokens/second) |
| **Native Tokens** | Tokens produced by each LLM's native tokenizer | Used for pricing (USD per million native tokens) |

AA uses OpenAI Tokens as the standard unit to enable fair comparisons between models with different tokenizers. A model with a "stingy" tokenizer (producing fewer tokens for the same text) would appear artificially faster if measured in native tokens.

## Sources

| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/methodology]] | Official AA definition of Token, OpenAI Tokens, Native Tokens | 2026-07-21 |

## Current synthesis

The dual unit of measurement (OpenAI tokens for speed, native tokens for price) is a pragmatic choice: it enables fair comparisons without forcing all providers to use the same tokenizer.

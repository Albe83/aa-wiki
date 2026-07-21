# wiki-llm

A pattern for building personal knowledge bases using LLMs. The LLM incrementally builds and maintains a persistent, interlinked wiki from curated source documents. You read and direct; the LLM does the bookkeeping.

## Structure

- `raw/` — Curated source documents (read-only for the LLM)
- `wiki/` — LLM-maintained markdown knowledge base
- `AGENTS.md` — Schema and workflows for the LLM agent

## Getting started

1. Drop source documents into `raw/`
2. Tell your LLM agent to "ingest [filename]"
3. Browse the results in Obsidian (or any markdown reader)
4. Ask questions, file answers, run lint checks

## License

MIT

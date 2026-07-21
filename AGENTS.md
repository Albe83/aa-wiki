# LLM Wiki — Agent Schema

## Architecture

Three layers:

- **`raw/`** — Immutable source documents (articles, papers, transcripts, images). Read-only for the LLM. The user curates this.
- **`wiki/`** — LLM-owned markdown knowledge base. All pages are written and maintained by the LLM. The user reads and browses.
- **This file** — The schema. Tells the LLM how to structure, maintain, and navigate the wiki. Co-evolved with the user over time.

The wiki is a persistent, compounding artifact. Every source ingested and every good answer filed back makes it richer. The LLM does all the bookkeeping — summarizing, cross-referencing, filing, contradiction-flagging — so the human doesn't have to.

## Directory structure

```
raw/                  # User-curated source documents (read-only)
  assets/             # Downloaded images and attachments
wiki/                 # LLM-maintained knowledge base
  index.md            # Catalog of all wiki pages
  log.md              # Chronological record of all operations
  overview.md         # High-level synthesis of the domain
  sources/            # One summary page per ingested source
  entities/           # Pages for people, orgs, places, books, etc.
  concepts/           # Pages for ideas, theories, frameworks, themes
  comparisons/        # Comparison tables and analyses
  questions/          # Filed answers to interesting questions
AGENTS.md             # This schema file
```

## Page naming conventions

- Use kebab-case: `albert-einstein.md`, `theory-of-relativity.md`
- Source pages: `sources/article-title.md` (name matches the source filename, without extension)
- Entity pages: `entities/[type]/[name].md` — `entities/people/`, `entities/orgs/`, `entities/books/`, `entities/places/`
- Concept pages: `concepts/[name].md`
- Comparison pages: `comparisons/[a]-vs-[b].md`
- Question pages: `questions/[slugified-question].md`

## Page templates

### Source page (`wiki/sources/[name].md`)

```markdown
---
type: source
date: [ingest date]
source_file: [path relative to raw/]
status: processed
---

# [Title]

**Source:** [citation or link]
**Ingested:** [date]
**Type:** [article | paper | book-chapter | transcript | podcast | other]

## Summary
[1-3 paragraph summary of the source's main arguments and findings]

## Key points
- [point]
- [point]

## Entities mentioned
- [[entities/people/alice-smith]] — [role/relevance]
- [[entities/orgs/acme-corp]] — [role/relevance]

## Concepts mentioned
- [[concepts/idea-name]] — [how it's used]

## Related sources
- [[sources/other-article]] — [relationship]

## My notes
[User-directed notes, things to emphasize, connections to explore — added collaboratively during ingest]
```

### Entity page (`wiki/entities/[type]/[name].md`)

```markdown
---
type: entity
entity_type: [person | org | book | place | other]
---

# [Name]

[Description — 1 paragraph overview]

## Mentions across sources
| Source | What's said | Date |
|--------|-------------|------|
| [[sources/article-a]] | Key claim or fact | 2024-03 |
| [[sources/article-b]] | Another claim | 2024-06 |

## Key facts
- [fact with source citation]

## Relationships
- [[entities/people/other-person]] — [how they relate]
- [[concepts/some-idea]] — [connection]
```

### Concept page (`wiki/concepts/[name].md`)

```markdown
---
type: concept
---

# [Name]

[1 paragraph definition/overview]

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/a]] | [what this source says about the concept] | 2024-03 |

## Evolution
[How thinking about this concept has changed across sources — note contradictions, developments, refinements]

## Current synthesis
[Where understanding stands now]

## Open questions
- [unresolved issue]
```

### Overview page (`wiki/overview.md`)

```markdown
---
type: overview
---

# [Domain] — Overview

[High-level synthesis of everything in the wiki. This is the entry point. Updated each ingest if the synthesis shifts. Cross-references to key entity and concept pages.]
```

### Comparison page (`wiki/comparisons/[a]-vs-[b].md`)

```markdown
---
type: comparison
---

# [A] vs [B]

| Dimension | [[a]] | [[b]] |
|-----------|-------|-------|
| [aspect]  | ...   | ...   |

## Synthesis
[When would you choose one over the other?]
```

## Workflows

### Ingest workflow

When the user says "ingest [filename]" or "process [source]":

1. **Read the source** from `raw/`. If it references images, read them separately after the text.
2. **Discuss with the user**: summarize key takeaways, ask what to emphasize, note anything surprising.
3. **Write the source page** in `wiki/sources/[name].md` using the template above.
4. **Update entity pages**: for each mentioned entity, add/update the "Mentions across sources" table. Create the entity page if it doesn't exist yet.
5. **Update concept pages**: same as entities — add the new source's perspective to each concept page, note contradictions or developments.
6. **Update `overview.md`**: if the new source shifts the overall synthesis, revise it.
7. **Update `index.md`**: add entries for all new pages, update summaries for changed pages.
8. **Append to `log.md`**: record what was ingested, what pages were created/updated, and any notable findings.
9. **Report**: tell the user what was created and what pages were touched.

The LLM should touch every relevant page — a single source might affect 10-15 pages. This is the core value: the bookkeeping happens now, not at query time.

### Query workflow

When the user asks a question:

1. **Read `index.md`** to find relevant pages.
2. **Read the pages** that are most relevant.
3. **Synthesize an answer** with citations (wikilinks to source and concept pages).
4. **Offer to file the answer**: if the answer is substantial (an analysis, comparison, or insight), offer to save it as a wiki page in `wiki/questions/` or `wiki/comparisons/`. The user decides.

### Lint workflow

When the user says "lint" or "health check":

1. Scan for **contradictions**: read pairs of pages on related topics, flag conflicting claims.
2. Check for **staleness**: are there claims superseded by newer sources?
3. Find **orphans**: pages with no inbound links from other wiki pages.
4. Identify **gaps**: important concepts mentioned across pages but lacking their own page.
5. Check **broken links**: wikilinks pointing to nonexistent pages.
6. **Suggest next steps**: new questions to investigate, new sources to look for.
7. Report findings in a structured way (not automatically fixing — let the user decide what to act on).

## Index format (`wiki/index.md`)

Organized by category. Each entry: link + one-line summary + optional metadata.

```markdown
# Index

## Overview
- [[overview]] — High-level synthesis of the domain

## Sources
- [[sources/article-title]] — One-line summary | ingested 2024-03-15

## Entities
### People
- [[entities/people/alice-smith]] — Role/summary

### Organizations
- [[entities/orgs/acme-corp]] — Role/summary

## Concepts
- [[concepts/idea-name]] — One-line definition

## Comparisons
- [[comparisons/a-vs-b]] — One-line summary

## Questions
- [[questions/why-does-x-happen]] — One-line summary
```

Update the index on every ingest and whenever a page is created, renamed, or significantly changed.

## Log format (`wiki/log.md`)

Append-only. Consistent prefix format: `## [YYYY-MM-DD] [type] | details`. This makes it grep-parseable.

```markdown
## [2024-03-15] ingest | Article Title
- Created: [[sources/article-title]]
- Updated: [[entities/people/alice-smith]], [[concepts/idea-name]]
- Notes: [key takeaway or action item]

## [2024-03-15] query | "Why does X happen?"
- Filed answer: [[questions/why-does-x-happen]]
```

## Cross-referencing conventions

- Use Obsidian-compatible wikilinks: `[[path/to/page]]`, optionally with display text: `[[path/to/page|display text]]`
- Every source page should link to all entities and concepts it covers.
- Every entity page should list all sources that mention it.
- Concept pages should trace how understanding has evolved across sources.
- When filing contradictions, link both pages to each other and flag with a `> ⚠ Contradiction:` blockquote.

## Frontmatter conventions

All wiki pages should have YAML frontmatter. Standard fields:
- `type`: `source | entity | concept | overview | comparison | question`
- `entity_type` (for entities): `person | org | book | place | event | other`
- `date` (for sources): ingest date
- `tags`: optional list of tags (enables Dataview queries in Obsidian)
- `status` (for sources): `processed | draft`

## General principles

- The LLM writes; the human reads and directs.
- Be thorough in cross-referencing — this is what makes the wiki useful over time.
- Prefer creating new pages over cramming into existing ones. A dedicated page for a minor character is better than a long "Minor characters" section that grows unwieldy.
- When in doubt about what to emphasize, ask the user.
- Sources are immutable. Never modify files in `raw/`.
- The wiki is a git repo. Changes are versioned. Don't worry about making mistakes — they can be reverted.
- Flag uncertainty: if a claim is speculative or contested across sources, say so.

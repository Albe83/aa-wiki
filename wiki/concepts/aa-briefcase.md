---
type: concept
---

# AA-Briefcase

AA-Briefcase is an agentic knowledge work benchmark that evaluates models on multi-week business projects with thousands of input source files. Unlike GDPval-AA v2 (shorter, single-session tasks), AA-Briefcase models sustained, complex knowledge work over extended horizons. It is an additional evaluation — not part of the core Intelligence Index — but provides deeper insight into models' capability for long-duration autonomous work.

## Sources
| Source | Perspective | Date |
|--------|-------------|------|
| [[sources/intelligence-benchmarking]] | Listed as an additional evaluation beyond the core Intelligence Index | 2026-07-21 |

## Key details

### Task design
Multi-week business projects. Each task involves thousands of input source files, requiring models to synthesize information across large document sets. Models complete each task independently from scratch — no incremental progress between tasks.

### Agent harness
Uses the **Stirrup** harness (same as GDPval-AA v2) with:
- Maximum 500 turns per task (double GDPval-AA's 250-turn limit)
- No internet access (all information is in the provided source files)
- Sandboxed code execution tool
- Finish tool to submit completed work

### Grading
Two complementary scoring methods:

**Binary rubric checks:** Pass/fail criteria evaluating whether specific deliverables were produced correctly. These are concrete, objective checks.

**Pairwise comparisons:** Models' outputs are compared head-to-head on two dimensions:
- **Analytical Quality** — depth, accuracy, and rigor of analysis
- **Presentation** — clarity, structure, and professionalism of the output

Judge panel: Claude Opus 4.8, GPT-5.5, and Gemini 3.1 Pro.

### Headline metric
The **AA-Briefcase Elo** combines three sub-scores into a single metric:
- Analytical Quality Elo
- Presentation Elo
- Rubric Pass Rate

This provides a holistic measure of multi-week autonomous knowledge work capability.

## Relationships
- [[concepts/intelligence-index]] — additional evaluation, not in core index
- [[concepts/gdpval-aa]] — related evaluation using the same Stirrup harness; GDPval-AA is shorter-horizon, AA-Briefcase is long-horizon

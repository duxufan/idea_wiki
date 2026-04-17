# Frontmatter Contract

## Source Note

Required fields:
- `source_id`
- `raw_path`
- `source_type`
- `ingested_at`
- `related_problem_spaces`
- `related_concepts`

Example:

```yaml
---
source_id: SRC-001
raw_path: raw/sources/example-llm-product-research.md
source_type: article
ingested_at: 2026-04-09
related_problem_spaces:
  - make-reading-compound-into-ideas
related_concepts:
  - selective-ingestion-preserves-signal
---
```

## Concept Page

Recommended fields:
- `concept_status`
- `source_refs`

## Problem-Space Page

Recommended fields:
- `problem_status`
- `related_sources`
- `related_concepts`
- `knowledge_gaps`
- `idea_seeds`

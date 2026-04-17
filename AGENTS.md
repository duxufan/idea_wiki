# Idea Wiki Operating Contract

This repository is a markdown-first framework for managing source-backed knowledge and idea-driven problem spaces together.

## Core model

- `raw/` stores immutable source materials and the provenance registry.
- `wiki/sources/` stores derived source notes.
- `wiki/concepts/` stores durable synthesis.
- `wiki/problems/` stores long-lived problem spaces that also carry `idea_seeds`.
- `wiki/index.md` is the content index.
- `wiki/log.md` is the chronological change log.

## Repository rules

- Raw files are immutable after arrival unless explicitly replaced.
- Every source note must reference one raw source via `source_id` and `raw_path`.
- Thoughts stay local by default; promote only when they create durable cross-source value.
- Every non-trivial cross-link needs explainable `Link Reasoning`.
- Problem-space pages may contain `idea_seeds` and `Knowledge To Acquire Next`, but they must not turn into execution-task checklists.

## Commands

- Ingest a source: follow `wiki/_workflows/ingest.md`.
- Evolve a problem space: follow `wiki/_workflows/query.md` plus `wiki/_templates/problem-space.md`.
- Recommend what to read next: follow `wiki/_workflows/recommend-reading.md`.
- Lint the repository: follow `wiki/_workflows/lint.md`.

# Ingest Workflow

## Purpose

Convert one raw source into derived wiki knowledge without mutating the raw file.

## Steps

1. Confirm the source exists under `raw/sources/`.
2. Confirm or create its `source_id` entry in [raw/_registry.md](../../raw/_registry.md).
3. Triage the source before creating notes:
   - If it is a high-overlap low-information duplicate, skip ingest and note the reason in `wiki/log.md`.
   - If it is unrelated to the current knowledge graph and there is no explicit user ingest command, skip ingest and ask for confirmation before linking it into the main wiki.
4. Read the raw source and create or update one source note under `wiki/sources/`.
5. Fill the source note with:
   - summary,
   - key claims,
   - embedded thought entries,
   - linked concepts/problem spaces,
   - link reasoning.
6. Apply [promotion-rules.md](../_schemas/promotion-rules.md) to decide which thoughts stay local and which get promoted.
7. Update any affected concept or problem-space pages.
8. Update [index.md](../index.md) if a new durable page was created.
9. Append an ingest entry to [log.md](../log.md).

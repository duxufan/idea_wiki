# Raw Sources

`raw/` is the immutable source-of-truth layer for this vault.

## Rules

- Put original files in `raw/sources/`.
- Do not rewrite or summarize raw files in place.
- If a source is superseded, add a new raw file and record the relationship in `raw/_registry.md`.
- Every ingested source must have a `source_id` and a registry entry before or during ingest.

## Workflow

1. Add the source file under `raw/sources/`.
2. Add or update the matching row in [raw/_registry.md](_registry.md).
3. Run the ingest workflow described in [ingest.md](../wiki/_workflows/ingest.md).

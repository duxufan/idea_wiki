# Idea Wiki

Idea Wiki is a markdown-first framework for managing **knowledge and ideas together**.

Instead of treating ideas as loose notes that sit beside research, this repository treats idea-driving problem spaces as first-class records. Sources feed notes, notes feed concepts, and problem-space pages collect the open questions, idea seeds, and next reading directions that keep learning moving.

You do not need Obsidian, OMX, or a separate app UI to use it. The repository is designed to stay useful as plain files in git, while still being structured enough for AI-assisted workflows.

## What this repository is for

Use it when you want a lightweight but opinionated loop for:

1. collecting raw materials without mutating them,
2. turning them into source-backed notes,
3. promoting durable concepts only when they earn it,
4. keeping long-lived problem spaces / idea tracks alive,
5. letting ideas drive what you read and study next.

## Core model

- `raw/` — immutable source materials plus provenance registry.
- `wiki/sources/` — source notes with summaries, claims, thought entries, and explicit link reasoning.
- `wiki/concepts/` — durable synthesis that survives beyond one source.
- `wiki/problems/` — problem-space pages that hold knowledge gaps and `idea_seeds`, so ideas can drive research.
- `wiki/_schemas/`, `wiki/_templates/`, `wiki/_workflows/` — the operating rules for keeping the graph consistent.
- `skills/` — bundled Codex-compatible skills for brainstorming, research intake, and source study.

## Included skills

This template bundles three reusable skills under `skills/`:

- `brainstorming` — clarify an idea, explore approaches, and write a design before implementation.
- `research-intake` — start from an idea/question, screen sources, pull high-value raw material into the repository, and prepare for ingest.
- `source-study` — study one local source deeply, then update the source note and linked graph conservatively.

These skills are repository-local copies so you can inspect, edit, and reuse them.

## Getting started

1. Add a source file to `raw/sources/`.
2. Register it in `raw/_registry.md`.
3. Follow `wiki/_workflows/ingest.md` to create or update a source note.
4. Promote only durable ideas into `wiki/concepts/` or `wiki/problems/`.
5. Use `Knowledge To Acquire Next` and `idea_seeds` to choose the next reading or study pass.

## Minimal example included

This repository ships with one example source, one source note, one concept page, and one problem-space page so you can see the workflow end to end without pulling in anyone's personal research history.

## Non-goals

- No task tracker disguised as a wiki.
- No automatic promotion of every thought into the global graph.
- No requirement to use a specific editor, note app, or orchestration runtime.
- No separate product UI unless you intentionally build one.

## Suggested public-repo hygiene

- Keep `raw/` immutable.
- Prefer explainable links over decorative cross-linking.
- Keep problem-space pages pre-executional: they should track understanding, idea pressure, and knowledge gaps, not shipping checklists.
- Remove personal exports, runtime state, and transient logs before publishing.

## Install bundled skills elsewhere

If you want to reuse the skills in another Codex setup, copy any directory from `skills/` into your local skills directory and adjust paths or wording as needed.

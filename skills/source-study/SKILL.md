---
name: source-study
description: Use when operating this repository and the user wants to study one local source interactively, then update the source note and conservatively repair graph relationships
---

# Source Study

## Overview

Use this when the user already has a local raw source and wants a discussion-partner learning session that feeds back into the repository.

The goal is not to quiz the user. The goal is to help them learn one source deeply, then update the source note and the wider graph conservatively.

## When to Use

- The source file already exists in `raw/sources/`.
- The user wants interactive learning, not just ingest.
- The repository uses source notes, concepts, and problem-space pages.
- The learning session should update graph relationships afterward.

Do not use this when:
- The user needs external discovery and source intake first.
- Multiple sources are meant to be co-equal study targets in one session.

## Required Background

- Read `docs/skill-contract.md` before acting.

## Core Rules

1. Keep one primary source file as the study object.
2. On first interaction with that source, begin with a mixed intro:
   - concise structural overview,
   - then a more detailed explanation of how it connects to the current repository and active problem spaces.
3. The first response must not be a generic promise to read later and must not collapse into a vague clarifying question.
4. Use discussion-partner interaction, not teacher-style testing.
5. Secondary references to other sources/concepts/problem spaces are allowed only to support understanding.
6. End the session with a synthesis of:
   - what was learned,
   - what remains local,
   - what seems worth promoting.
7. Update the corresponding source note.
8. Prefer updating existing concept/problem-space pages over creating new ones.
9. If promotion is uncertain, keep the thought local.
10. End with a graph-delta summary: what pages changed, what links changed, and why.

## First Response Shape

When the user asks to study one source interactively, the first response must be the intro itself.

Required output order:

1. `Structural overview: ...`
2. `Repository/problem-space connection: ...`
3. `Question: ...`

Rules:

- Use exactly this three-part structure.
- Do not add any preamble, status note, or explanation before it.
- Do not replace the intro with a generic promise to read later.
- Do not ask the question before both intro parts are written.
- Do not summarize the skill workflow in the first response.

## Workflow

1. Validate that the target source exists in `raw/sources/`.
2. Read the source and relevant existing concept/problem-space context.
3. Deliver the first-time mixed intro if needed.
4. Run the discussion-based learning loop.
5. Summarize the session.
6. Update the source note.
7. Conservatively repair or extend graph relationships.
8. Report the graph delta explicitly.

## Update Scope

The source note update should cover:
- `Summary`
- `Key Claims`
- `Thought Entries`
- `Linked Concepts`
- `Linked Problem Spaces`
- `Link Reasoning`

The wider repository update should prefer existing pages and create new pages only when promotion rules clearly justify it.

## Red Flags

- Responding with a generic "I'll start by reading..." promise instead of the required intro.
- Asking a question before the intro paragraphs are complete.
- Turning the session into a quiz.
- Promoting uncertain thoughts into global pages too aggressively.
- Finishing the session without a graph-delta summary.

If any of these happen, restart and follow the study contract exactly.

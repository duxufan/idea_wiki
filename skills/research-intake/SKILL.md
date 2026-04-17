---
name: research-intake
description: Use when operating this repository from one idea or question and you need external sources screened, ranked, downloaded into the raw layer, and prepared for ingest
---

# Research Intake

## Overview

Use this when a user has a question or idea but does not yet have local source material. This skill turns that need into a disciplined research-intake workflow for this repository.

The goal is not just to search. The goal is to bring high-value raw materials into the repository with provenance, then continue into ingest after user interaction.

## When to Use

- The user starts from one idea, problem, or research direction.
- The user wants external sources brought into the repository.
- The repository uses `raw/sources/`, `raw/_registry.md`, `wiki/sources/`, `wiki/concepts/`, and `wiki/problems/`.
- You need repository-specific discipline rather than generic web research behavior.

Do not use this when:
- The source file already exists locally and the user wants to study it.
- The user wants general brainstorming without source intake.

## Required Background

- Read `docs/skill-contract.md` before acting.

## Core Rules

1. Ask one clarification question at a time only when the research target is still ambiguous.
2. If the user already gave enough direction, do not fall back to a generic preference question.
3. When the target is already clear enough, start by restating the target and the ranking rule you will use.
4. Screen at least 5 candidate sources.
5. Rank candidates by:
   - relevance,
   - source quality,
   - novelty.
6. Report only the top 3 to the user.
7. If the top 3 are good enough, download only those 3 into `raw/sources/`.
8. Register downloaded sources in `raw/_registry.md`.
9. Do not download the 4th or 5th candidates unless the user explicitly asks.
10. After download, report back and interact with the user before ingesting.
11. After that interaction completes, continue automatically into ingest.

## First Response Shape

When the user already specified the problem clearly, the first response should:

1. Restate the research target in one sentence.
2. State the ranking rule you will use.
3. State that you will screen at least 5 candidates and report only the top 3.
4. Ask at most one narrow follow-up question if one is still needed.

## Workflow

1. Clarify the research need only if necessary.
2. Build a short internal research brief.
3. Search and screen at least 5 candidates.
4. Report the top 3 with explicit ranking rationale.
5. Download the qualifying top 3 into `raw/sources/`.
6. Update `raw/_registry.md`.
7. Interact with the user about the selected materials.
8. Continue into ingest automatically unless the user changes direction.

## Report Format

For each of the top 3, include:
- what it is,
- why it is relevant,
- why it outranks the other candidates,
- whether it was downloaded.

Also include:
- how many candidates were screened,
- why non-top-3 candidates were excluded from automatic download.

## Red Flags

- Asking a generic question but never committing to the `5 candidates minimum`.
- Reporting an unspecified number of links.
- Downloading into `raw/sources/` without updating `raw/_registry.md`.
- Downloading candidates 4 or 5 without explicit user approval.
- Downloading and then silently ingesting without a user interaction checkpoint.

If any of these happen, restart the workflow and follow the contract exactly.

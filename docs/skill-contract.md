# Idea Wiki Skill Contract

This document defines the repository-specific rules that bundled or custom skills should follow when operating on this framework.

## Raw Source Contract

- Original materials belong in `raw/sources/`.
- Every source must have a `source_id`.
- Every source must be registered in `raw/_registry.md`.
- Raw files are immutable after arrival unless explicitly replaced by the user.

## Derived Note Contract

- Source notes live in `wiki/sources/`.
- Source notes must preserve `source_id` and `raw_path`.
- Source notes should update `Thought Entries`, linked concepts, linked problem spaces, and `Link Reasoning` when understanding changes.

## Problem-Space / Idea Contract

- Problem-space pages live in `wiki/problems/`.
- They incubate ideas, questions, and knowledge gaps.
- They may include `idea_seeds` and `Knowledge To Acquire Next`.
- They must not drift into execution-task management.

## Promotion Contract

- Thoughts stay local by default.
- Promote only when they create durable, reusable, cross-source value or materially reshape a long-lived problem space.
- Prefer updating existing concept/problem-space pages over creating new global pages.

## Explainability Contract

- Every meaningful auto-created link must carry reasoning.
- Skills that change the graph must summarize what changed and why.

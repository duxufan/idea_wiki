# Idea Wiki Public Template Design

Date: 2026-04-17
Status: approved and executed

## Goal

Create a clean public repository named `idea_wiki` that preserves the framework of the current private working repo without exposing personal research history, runtime traces, or operator-specific branding.

## Approved decisions

- Publish a sibling standalone repository instead of nesting the public copy in the working repo.
- Keep the public repo minimal: one example raw source, one source note, one concept page, and one problem-space page.
- Position the template as a knowledge-plus-ideas framework, not an Obsidian-first or OMX-required setup.
- Keep idea handling in the existing `wiki/problems/` / `idea_seeds` model.
- Bundle repo-local skills: `brainstorming`, `research-intake`, and `source-study`.
- Remove legacy private-repo branding from the two custom skills.

## Public repo boundaries

Keep:
- markdown structure and workflow docs,
- minimal examples,
- skill contract,
- bundled skills.

Remove:
- `.omx/`, `output/`, personal PDFs, current research graph, and temporary files.

# README Rewrite and OneFav Publish Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `README.md` into a Chinese, idea-driven research manifesto/workflow document, add `MIT` licensing, and publish the repository to `OneFav/idea-wiki`.

**Architecture:** Keep the repository structure unchanged. Replace the current README with a Chinese narrative that leads with the necessity of combining ideas and learning, explains the research loop and AI alignment role, then maps that loop onto the existing repository structure and bundled skills. Add a standard `LICENSE` file and publish the same repository contents to a second GitHub remote under the OneFav account.

**Tech Stack:** Markdown, Git, GitHub CLI (`gh`)

---

## File Structure

- Modify: `README.md` — replace the current English repo-description README with the approved Chinese workflow-first README.
- Create: `LICENSE` — add standard MIT license text.
- Create: `.git/config` entries via git commands — add/publish `onefav` remote or create target repo as needed.
- Reference only: `docs/superpowers/specs/2026-04-17-readme-rewrite-design.md` — source of truth for messaging and publication target.

### Task 1: Rewrite README content

**Files:**
- Modify: `README.md`
- Reference: `docs/superpowers/specs/2026-04-17-readme-rewrite-design.md`

- [ ] **Step 1: Read the approved design spec**

Run: `Get-Content docs/superpowers/specs/2026-04-17-readme-rewrite-design.md`
Expected: spec confirms Chinese README, workflow-first structure, light emoji use, target publication to `OneFav/idea-wiki`, and MIT licensing.

- [ ] **Step 2: Replace README with approved structure**

Write a new `README.md` that includes these sections in order:

```markdown
# idea-wiki

> [one-sentence positioning line]

## 💡 为什么要把想法和学习放在一起
## 🧭 这套框架在做什么
## 🤖 AI 在这里扮演什么角色
## 🧱 这个仓库如何承载这个闭环
## 🛠️ 内置技能
## 🚫 这不是什么
## 🚀 如何开始
## License
```
```

Content requirements:
- Explain why knowledge-only systems and idea-only systems both break.
- Present the loop `idea -> structure -> research -> alignment -> synthesis -> new idea`.
- Define AI as a research alignment tool, not a generic summarizer.
- Explain `raw/`, `wiki/sources/`, `wiki/concepts/`, `wiki/problems/`, and `skills/` in workflow terms.
- Mention bundled skills: `brainstorming`, `research-intake`, `source-study`.
- Use Chinese as the primary language.
- Use a small number of emoji only at section headers or key anchors.

- [ ] **Step 3: Run a readability/self-check on README**

Checklist:
- First screen states this is not a generic knowledge base.
- The necessity of combining ideas and learning appears before file structure.
- The AI role is explicit and non-hype.
- No Obsidian/OMX requirement language appears.
- Emoji are present but not excessive.

- [ ] **Step 4: Verify branding/path hygiene in README**

Run: `Select-String -Path README.md -Pattern 'llm_wiki|llm-wiki|[A-Za-z]:\\|/Users/|/home/'`
Expected: no matches.

### Task 2: Add MIT license

**Files:**
- Create: `LICENSE`

- [ ] **Step 1: Create standard MIT license text**

Write standard MIT license text into `LICENSE`.

- [ ] **Step 2: Verify the license file exists**

Run: `Test-Path LICENSE`
Expected: `True`

- [ ] **Step 3: Mention the license in README**

Ensure the rewritten `README.md` has a short `License` section that states the repository is released under MIT.

### Task 3: Verify repository state before publication

**Files:**
- Modify: none
- Verify: `README.md`, `LICENSE`

- [ ] **Step 1: Check git status**

Run: `git status --short --branch`
Expected: modified files are limited to `README.md`, `LICENSE`, and any deliberate plan/spec artifacts.

- [ ] **Step 2: Scan the repository for old branding and local paths**

Run: `Get-ChildItem -Recurse -File | Select-String -Pattern 'llm_wiki|llm-wiki-research-intake|llm-wiki-source-study|[A-Za-z]:\\|/Users/|/home/'`
Expected: no matches in published content.

- [ ] **Step 3: Commit the content changes**

Run:
```bash
git add README.md LICENSE docs/superpowers/plans/2026-04-17-readme-rewrite-and-onefav-publish.md
git commit -m "Present idea-wiki as a Chinese idea-driven research workflow

Constraint: Public README should prioritize method and workflow over generic repo description
Constraint: Target publication is OneFav/idea-wiki under MIT
Rejected: Keep the English structure-only README | weaker explanation of the research loop and alignment logic
Confidence: high
Scope-risk: narrow
Reversibility: clean
Directive: Keep future README edits aligned to the idea -> research -> alignment loop
Tested: README self-review, branding/path scan, file existence checks
Not-tested: Cross-device rendering on GitHub mobile"
```
Expected: commit succeeds.

### Task 4: Publish to OneFav/idea-wiki

**Files:**
- Modify: `.git/config` via git/gh commands

- [ ] **Step 1: Switch GitHub CLI active account to OneFav**

Run: `gh auth switch -u OneFav`
Expected: `gh auth status` shows `OneFav` as active.

- [ ] **Step 2: Check whether `OneFav/idea-wiki` already exists**

Run: `gh repo view OneFav/idea-wiki --json name -q .name`
Expected: returns the name if it exists, or fails with not found.

- [ ] **Step 3: Create the target repository if missing**

Run: `gh repo create OneFav/idea-wiki --public --description "Idea-driven research workflow for aligning personal intuition with existing knowledge."`
Expected: repository is created.

- [ ] **Step 4: Add or update a dedicated remote for the OneFav repo**

Run one of:
```bash
git remote add onefav https://github.com/OneFav/idea-wiki.git
```
or
```bash
git remote set-url onefav https://github.com/OneFav/idea-wiki.git
```
Expected: `git remote -v` includes `onefav`.

- [ ] **Step 5: Push main branch to OneFav**

Run: `git push -u onefav main`
Expected: push succeeds and sets upstream tracking for `onefav/main` or reports branch pushed.

- [ ] **Step 6: Verify the published repository metadata**

Run: `gh repo view OneFav/idea-wiki --json url,isPrivate,defaultBranchRef -q '{"url": .url, "private": .isPrivate, "defaultBranch": .defaultBranchRef.name}'`
Expected: public repo URL, `private=false`, default branch `main`.

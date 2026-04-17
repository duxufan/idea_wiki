[English](./README.md) | [简体中文](./README.zh.md)

# idea-wiki

> An idea-driven research workflow for turning personal intuition into structured inquiry, aligned research, and durable knowledge. 💡

`idea-wiki` is not just a note repository, and it is not just an idea dump.
It is a workflow for a more specific problem:

> **How do you take a vague idea in your head, turn it into something researchable, compare it against existing work, and gradually align your own understanding with what is already known?**

This repository works best when you use it with a **CLI code agent** that can read and edit the repo directly. 🤖

---

## 🚀 How to use

### Recommended setup

The intended usage is:

- keep this repository locally;
- work with a **CLI code agent** (for example, Codex CLI, Claude Code, or a comparable local agent);
- let the agent help you structure ideas, intake sources, study materials, and update the repository.

Why CLI agents?
Because this workflow is file-native. The agent should be able to:

- read your current `problems`, `concepts`, and `sources`;
- write new notes and cross-links back into the repo;
- keep raw sources, derived notes, and problem spaces in one continuous loop.

### Recommended loop

1. Start from a question, intuition, or half-formed idea.
2. Use `brainstorming` to turn it into a clearer problem framing.
3. Use `research-intake` to find and bring in relevant sources.
4. Use `source-study` to deeply study one source and repair the graph around it.
5. Promote only durable insights into `concepts` or `problems`.
6. Let new questions and `idea_seeds` drive the next research cycle.

In other words, don’t use this repo as passive storage.
Use it as a working loop for **idea -> research -> alignment -> synthesis -> next idea**.

---

## 💡 Why ideas and learning need to stay together

A knowledge system by itself is often not enough.
You can collect papers, notes, summaries, and references for months without actually advancing the question that matters to you.

An idea system by itself is also not enough.
You can collect intuitions, hypotheses, and possible directions, but without sustained learning and external correction, those ideas often remain subjective and under-tested.

That creates two common failure modes:

- **Knowledge without direction**: you learn a lot, but your learning does not really move your own inquiry forward. 📚
- **Ideas without correction**: you imagine a lot, but you do not know where those ideas stand relative to existing work. 🤔

`idea-wiki` exists to connect those two halves:

- let **ideas drive learning**, instead of collecting knowledge without a live question;
- let **learning correct ideas**, instead of leaving them at the level of personal intuition.

The real goal is not “remembering more.”
The goal is:

> **to make your original ideas progressively clearer, better grounded, and better aligned with reality and existing work.**

---

## 🧭 What this workflow does

This repository is built around a repeating loop, not a one-off note-taking action:

```text
idea -> structure -> research -> alignment -> synthesis -> new idea
```

Each stage does something distinct:

1. **idea**  
   Start with a question, intuition, hunch, or direction—even if it is still vague.

2. **structure**  
   Turn that vague thought into something discussable and researchable: what is the actual question, what is missing, and what kind of problem space is this?

3. **research**  
   Bring in papers, cases, examples, and external material so the idea is no longer only private intuition.

4. **alignment**  
   Compare “how I currently think about this” with “how existing work actually frames this.” This is where gaps, mismatches, and blind spots become visible.

5. **synthesis**  
   Once an understanding survives beyond one source, promote it into concepts, problem pages, and reusable knowledge relationships.

6. **new idea**  
   Good synthesis does not end the process. It produces sharper follow-up questions, new angles, and better next ideas.

So the point of `idea-wiki` is not just to store information.
It is:

> **to give a person’s ideas a path into research, and give research a path back into the person’s thinking.**

---

## 🤖 What AI is doing here

In this framework, AI is not supposed to replace judgment.
And it is not just a generic summarizer.

Its more useful role is as a **research aligner**:

- it helps turn vague ideas into researchable objects;
- it helps identify what knowledge is missing next;
- it helps map private language into more stable research language;
- it helps expose the gap between what you think you are asking and what the field is actually discussing. 🧠

A lot of research friction does not come from “not reading enough.”
It comes from:

- asking an unclear question,
- researching in a diffuse way,
- using private language that does not match the literature,
- and failing to route new material back into the original problem.

AI is most useful here when it helps bridge those breaks.
Not when it pretends to think for you.

---

## 🧱 How this repository holds the loop

The directory structure exists to support that workflow, not just to classify files.

### `raw/`
This is the raw input layer.
Original materials live here and should stay as unpolluted as possible.
Your later summaries, interpretations, and concepts should not overwrite the source layer.

### `wiki/sources/`
These are source notes.
They turn a source into a reusable research node: summary, claims, local thoughts, and explainable links to the wider graph.

### `wiki/concepts/`
These are durable concepts.
A concept belongs here only when it holds beyond a single source and becomes reusable in the wider system.

### `wiki/problems/`
This is one of the most important layers.
These pages are not task lists—they are **problem spaces / idea spaces**:

- what long-running question actually matters,
- what knowledge is still missing,
- what `idea_seeds` are emerging,
- what should be read next to sharpen the picture.

This is where the system keeps the connection between inquiry and learning alive.

### `skills/`
These are not random utilities.
They are workflow entry points that help you move through different stages of the loop.

---

## 🛠️ Bundled skills

This repository currently bundles three skills:

### `brainstorming`
Use it before implementation or before prematurely locking into a solution.
It helps transform a vague direction into a clearer design or problem framing.

### `research-intake`
Use it when you have a question or idea but still need to bring in external material.
It handles candidate screening, intake discipline, and source acquisition. 🔎

### `source-study`
Use it when one local source deserves deeper attention.
It helps study that source, update the note, and repair the surrounding graph conservatively.

Together, these skills support the workflow rather than replacing it.

---

## 🚫 What this is not

To avoid confusion, `idea-wiki` is **not**:

- a generic note archive;
- a task manager;
- a “save every source” dumping ground;
- an autonomous system where AI is supposed to make final judgments for you.

It is better understood as a research operating style:

> **a way to keep personal ideas, AI-assisted structuring, external knowledge, and long-term synthesis inside one coherent loop.**

---

## 📚 Repository quick map

- `raw/` — immutable raw materials plus registry
- `wiki/sources/` — source notes
- `wiki/concepts/` — durable synthesis
- `wiki/problems/` — long-running problem spaces with `idea_seeds`
- `skills/` — workflow skills for brainstorming, intake, and study

---

## 🙌 Inspiration

This project is **inspired by Andrej Karpathy’s `llm_wiki`**.

The difference is that `idea-wiki` tries to push the pattern one step further:
not only organizing knowledge, but also explicitly organizing **ideas**, **problem spaces**, and the alignment process between a person’s private intuition and the field’s existing understanding.

In that sense, you can think of it as an idea-augmented extension of the original `llm_wiki` direction.

---

## License

This repository is released under the **MIT License**.

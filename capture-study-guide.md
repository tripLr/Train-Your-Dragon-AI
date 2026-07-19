---
name: capture-study-guide
description: Turn a conversation, reflection, or set of insights into a clean landscape Remarkable-optimized study guide with structured content and generous journaling space. Use when the user wants to capture personal development discussions, frameworks, questions, or key insights as a study guide for later handwriting and review. Works for Warrior's Way, Train Your Dragon project, or any personal growth material. Triggers on capture as study guide, make this a study guide, turn this conversation into notes, Remarkable study guide, export this discussion, or similar.
---

# Capture Study Guide Skill

Convert meaningful conversations, personal reflections, frameworks, and insights into spacious, landscape study guides optimized for the Remarkable tablet.

## Purpose

Create durable external artifacts from live thinking so the user can continue processing by hand. The goal is not a transcript — it is a clean, structured study guide that preserves the core ideas and leaves room for further discovery.

## When to Use

- User says “capture this as a study guide”, “make this Remarkable-ready”, “turn this into notes”, “same format as Coach Chris”, etc.
- A conversation contains frameworks, key questions, distinctions, or personal insights worth keeping.
- Material needs to move from chat into the user’s long-term study system (Warrior’s Way, Train Your Dragon, or general personal development).

## Core Design Principles

1. **Structure over transcript** — Extract and organize the important ideas. Do not dump the full conversation.
2. **Generous notes space** — After every major section or insight, leave clear room for handwriting.
3. **Landscape letter** — Default page size for Remarkable comfort.
4. **Clean hierarchy** — Clear titles, section heads, short body text, and visual breathing room.
5. **Context header** — Briefly state where the material came from and why it matters so future-you has orientation.
6. **Preserve voice** — Keep the user’s language and key phrases when they are powerful. Do not over-polish into generic self-help tone.
7. **One clear deliverable** — A single well-named PDF ready to drop onto the tablet.

## Standard Output Structure

- Title page or header with:
  - Study Guide title
  - Source (conversation date, topic, or project name)
  - Optional short context sentence
- Numbered or clearly headed sections for each major idea / framework / question set
- Short, readable body text under each heading
- “NOTES” or “JOURNAL” band with blank lines after each section
- Optional final reflection page or open questions page

## Workflow

1. Confirm with the user which parts of the conversation (or which insights) should be included.
2. Propose a clean section structure before building.
3. Build the landscape PDF with consistent styling.
4. Deliver the file and confirm it matches the intended use (Warrior’s Way, Train Your Dragon, general, etc.).

## Naming Convention

Prefer clear, project-aware names, for example:
- `WW_Week5_Grey_Jedi_Study_Guide.pdf`
- `Train_Your_Dragon_Inner_Conflict_Study_Guide.pdf`
- `Personal_Strengths_HOW_Study_Guide.pdf`

## Relationship to Other Skills

- Use `notes-merge` afterward if this study guide needs to be combined with other PDFs.
- Complements `video-study-notes` (for video content) and `warriors-way-course` (for official course material).
- This skill is the bridge from live conversation → durable personal study artifact.

## Evolution

Expect this skill to refine as real study guides are produced. Common improvements will likely include better section detection, optional question prompts, and tighter integration with the Train Your Dragon project structure.

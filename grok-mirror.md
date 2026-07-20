---
name: grok-mirror
description: Maintain alignment between this main Grok instance (source of truth for memory and skills) and Grok on X. Creates portable mirror packages, stores conversation links, and supports manual sync. Also enforces the standing rule that when the user says “Get the process”, pause and ask for a comment before proceeding. Triggers on grok mirror, mirror package, sync to X, export for X grok, get the process, or similar.
---

# Grok Mirror Skill

**Main instance (this one) is the source of truth.**

Grok inside the X app is a separate instance. There is currently no automatic live sync. This skill manages a clean, manual mirror process so the two stay as aligned as possible.

## Core Rules

1. This environment (memory + skills) is the master.
2. Grok on X is the downstream / working copy.
3. Sync is manual and structured until better technical bridges exist.
4. When the user says **“Get the process”**, always pause and ask for a short comment before proceeding with any significant action.

## What This Skill Does

- Creates a portable **Mirror Package** (key memory sections + current skills list + important standing rules)
- Lets the user add and store conversation links (especially share/embed links from X or other places)
- Reminds both sides of the current sync status
- Supports bringing important updates from X conversations back into the main memory

## Mirror Package Contents (Standard)

A Mirror Package should include:
- Short statement that this is the master system
- Key standing rules and preferences
- Current list of active skills
- Selected high-value memory sections (identity, current projects, working style, active goals)
- Any conversation links the user has stored
- Date of last export

## Workflow

**Export to X**
1. User requests a mirror package or says they are about to work in Grok on X.
2. Generate a clean, readable markdown export.
3. User can paste or reference it when talking to Grok on X.

**Import from X**
1. User brings back important outcomes, decisions, or new insights from an X conversation.
2. Capture them into main memory or the appropriate skill using normal processes.
3. Optionally store the conversation link.

## Standing Behavioral Rule

Whenever the user says **“Get the process”** (or close variants):
- Pause
- Ask: “Before I proceed, do you want to add a comment or clarification?”
- Wait for the reply before continuing with the significant action.

## Limitations (Honest)

- No automatic two-way live sync with Grok on X is currently possible.
- The quality of alignment depends on regular exports and the user bringing key updates back.
- Conversation share/embed links are stored when the user provides them; automatic capture is not available.

## Evolution

Update this skill when better technical options appear for moving context between instances, or when the manual process shows clear friction.

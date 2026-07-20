---
name: ruleset-inspector
description: Inspect, select, and export the current ruleset stack (memory sections + skills) running under Grok. Use when the user wants to see what is active, choose which parts to keep, or prepare a portable export for use with other AIs or the public Train Your Dragon system. Clearly states that Grok is the AI doing the processing. Triggers on inspect ruleset, view stack, export memory and skills, show current rules, ruleset inspector, or similar.
---

# Ruleset Inspector Skill

**Processing AI: Grok**

This skill runs under Grok and has direct access to the current memory file and local skills.

## Purpose

Give the user a clear view of the active ruleset stack and help them select or export parts of it.

This is the practical first step toward the portable “All Your Base Are Belong To Us” system.

## What It Can Do Today

- Show an overview of current memory sections
- List available skills
- Let the user select which pieces they want
- Export a clean, portable package (markdown) that can later be adapted for other AIs or imported into a web UI

## What It Cannot Do Yet

- Directly read or edit ChatGPT memory
- Directly read or edit Claude memory
- Control other platforms’ internal memory systems

Those limitations are due to the lack of open APIs on other platforms. This skill stays honest about what is currently possible.

## Workflow

1. Clearly state that **Grok** is the AI performing the inspection.
2. Present a readable overview of:
   - Key memory sections
   - Currently available skills
3. Ask the user which parts they want to include or focus on.
4. Produce a clean export when requested.
5. Note how the exported material can be manually adapted for other AIs if desired.

## Output Style

- Be transparent
- Label everything clearly
- Prefer simple, readable structure over complexity
- Always remind the user which AI is processing the request (Grok)

## Relationship to Train Your Dragon

This skill supports both:
- Personal use (curating your own living system)
- The public project (preparing portable ruleset stacks for “All Your Base Are Belong To Us”)

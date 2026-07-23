---
name: inspect-grok-memory
description: Examine the current running Grok memory, compare it with timestamped backups in the private My-Dragon-AI repo, offer to backup now, revert to a previous version, or create a Baby Dragon (fresh memory that still knows Train Your Dragon and this skill). Triggers on inspect grok memory, examine memory, backup memory, revert memory, baby dragon, or similar.
---

# Inspect Grok Memory Skill

Safety and agency skill for the durable memory that Grok uses.

**Skill location:** Train-Your-Dragon-AI (public philosophy / skills)  
**Private memory backups location:** My-Dragon-AI repository

## Purpose

Give the user clear control over the running memory:
- See what is currently active
- Compare with backed-up versions
- Create timestamped backups
- Revert when needed
- Start fresh (Baby Dragon) without losing the core system knowledge

## Flow

When the user asks to inspect / examine Grok memory:

1. **Show current running memory**  
   Display the current durable memory (or a clear summary + key sections if very long).

2. **Compare with GitHub backup**  
   Check the single backup location in `My-Dragon-AI`.  
   Show the timestamp of the latest backup and note any obvious differences if possible.

3. **Ask: Backup now?**  
   If yes:
   - Create a timestamped copy of the current memory
   - Push it to the single backup folder in `My-Dragon-AI`
   - Confirm success

4. **Offer next actions:**
   - **1. Revert** → List available timestamped backups so the user can choose one to restore
   - **2. Baby Dragon** → Create a fresh memory

### Baby Dragon Rules

A Baby Dragon memory must be mostly clean/stock, but it **must still contain**:

- Knowledge that the Train Your Dragon project exists
- Knowledge of the core skills (especially this `inspect-grok-memory` skill)
- The basic ownership / agency principles
- Pointers to the private My-Dragon-AI system

This guarantees we can never lose the ability to recover or continue the system.

## Structure Rule

- Only **one** memory backup folder inside `My-Dragon-AI`
- No complex nested version trees
- Simple timestamped files (e.g. `memory_2026-07-22_2015.md`)

## Permanent Project Component

This skill and the private memory backup location are permanent parts of the Train Your Dragon system. They exist so the human always keeps control of the memory that shapes the AI collaborator.

## Privacy

Memory content and backups are private. The skill definition itself may live in the public Train-Your-Dragon-AI repo; the actual memory files stay in the private My-Dragon-AI repo.

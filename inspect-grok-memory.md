---
name: inspect-grok-memory
description: Examine the current running Grok memory, compare with timestamped backups in My-Dragon-AI, offer backup / revert / Baby Dragon, and support section-by-section review and editing so the user keeps full agency. Always ask to backup before any edit or Baby Dragon. Triggers on inspect grok memory, examine memory, backup memory, revert memory, baby dragon, memory inspector, review memory, or similar.
---

# Inspect Grok Memory Skill

Safety, review, and agency skill for the durable memory that Grok uses.

**Skill location:** Train-Your-Dragon-AI (public)  
**Private memory backups location:** My-Dragon-AI / memory-backups/

## Purpose

Give the user full control over the running memory:
- See what is currently active
- Review it section by section
- Edit or remove sections
- Create timestamped backups
- Revert to a previous version
- Start fresh (Baby Dragon) without losing core system knowledge

## Core Safety Rule

**Always ask the user to create a backup before any edit or before running Baby Dragon.**  
Do not force it — ask. The user decides.

## Main Flow

When the user asks to inspect / examine Grok memory:

1. **Show overview of current running memory**  
   List the top-level headings / sections.

2. **Compare with GitHub backup**  
   Show the timestamp of the latest backup in `My-Dragon-AI/memory-backups/`.

3. **Present choices:**

   **A. Review & Edit sections**  
   - Go through the memory section by section  
   - User can choose a section to view in full  
   - After viewing, offer: Keep / Edit / Delete / Next section  
   - **Before any Edit or Delete:** ask whether to backup first  
   - Edits are performed via the normal memory-edit process (user stays in control)

   **B. Backup now**  
   - Create a timestamped copy of the current memory  
   - Push it to `My-Dragon-AI/memory-backups/`  
   - Confirm success

   **C. Revert**  
   - List available timestamped backups  
   - User chooses one to restore

   **D. Baby Dragon**  
   - **Ask to backup first**  
   - Then create a fresh (mostly clean) memory  
   - Must still contain:
     - Knowledge that Train Your Dragon exists  
     - Core skills (especially this inspect-grok-memory skill)  
     - Basic ownership / agency principles  
     - Pointers to the private My-Dragon-AI system  

### Baby Dragon Concept

Baby Dragon is a **double-blind tool**.  
It works like opening a private browser tab with no history — it lets the user see what a clean/stock memory produces *before* deciding to change the real one.  

Use it to preview behavior safely. It is not a destructive reset unless the user later chooses to keep it.

## Structure Rule

- Only **one** memory backup folder inside `My-Dragon-AI`
- Simple timestamped files (e.g. `memory_2026-07-22_2045.md`)
- No complex nested version trees

## Permanent Project Component

This skill and the private memory backup location are permanent parts of the Train Your Dragon system. They exist so the human always keeps control of the memory that shapes the AI collaborator.

## Privacy

Memory content and backups are private. The skill definition lives in the public Train-Your-Dragon-AI repo; actual memory files stay in the private My-Dragon-AI repo.

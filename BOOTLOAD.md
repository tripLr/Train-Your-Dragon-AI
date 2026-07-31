# BOOTLOAD — Train Your Dragon

**Updated:** 2026-07-31

## Purpose

Give every instance a single, human-owned orientation file so the AI can be trained *about this person* without treating chat history as the source of truth.

## Commands

| Command | When |
|---------|------|
| **Launch the dragon** | **Once** (or rebuild). Ends with **make-bootloader**. |
| **Load bootloader** | Every later session (or on demand). Reads the orientation file. |

## make-bootloader (end of first launch)

1. Create `bootload-dragon.md` in the user’s chosen living home (example: Google Drive `Projects/bootload-dragon.md`).
2. Seed only what the human has stated: Dragon exists; living work location (e.g. PARA on Drive); main focuses; methods; areas of responsibility.
3. Add a **pointer** in durable memory: Load bootloader → that file.
4. Optional log line: created / rebuilt.

After make-bootloader succeeds, ongoing sessions use **Load bootloader**, not full Launch.

## Living orientation file

The bootloader file is the **instance source of truth about the human**.  
Update it only with **human confirm** when structural facts change.

It is **not** a dump of all projects or course weeks. Those stay in PARA (or the user’s chosen living home).

## Where everything lives

| What | Where |
|------|--------|
| Public method, skills, install, standing rules | **Train-Your-Dragon-AI** (this repo) |
| Living notes, course, research, personal development | **User PARA** (e.g. Google Drive) |
| Private memory / history patterns | User’s private memory / My-Dragon-AI style home |

**Deprecated for living study:** course trees such as `nosce-te-ipsum` on GitHub may remain as frozen skeletons. Living work does not return there. This public repo may keep a short reference that living work switched to PARA.

## PARA Layer Status Rules

- Each active Project or Area should have a `status-index.md` file.
- A `status-index.md` contains a timestamped top-level summary + timestamped entries.
- When entering a layer that is missing its `status-index.md`, suggest a quick review and create or update as needed.
- Skills and new instances look for the file first → then the top-level summary → then individual entries.
- Archive is low priority. Resources usually need no status file unless repeatedly useful.

## Pointers

Pointers answer “where is X?” only.  
Do not copy full project content into memory.

## Critical standing rules

1. Human owns the system. AI is builder and thinking partner.
2. Prefer durable external systems over chat history.
3. When the human says **“Get the process”** → pause and ask for a short comment before proceeding.
4. Agency first; confirm before structural or irreversible writes.

## How to continue

**New:** Say **Launch the dragon** → finish with make-bootloader.  
**Existing:** Say **Load bootloader** → read orientation → continue work.

## Related

- [INSTALL.md](INSTALL.md)
- [STANDING_RULES.md](STANDING_RULES.md)
- [launch-the-dragon.md](launch-the-dragon.md)
- [SYSTEM_STRUCTURE.md](SYSTEM_STRUCTURE.md)

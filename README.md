# Train Your Dragon

**A durable, consent-based personal AI operating system**  
Architecture: **PARA-MOC-dragon**

---

## What this is

Train Your Dragon is a method for keeping personal AI work alive across sessions and instances.

It solves a simple problem: AI conversations are powerful but ephemeral. Insights, course work, and self-examination disappear when the chat ends. This system gives the human a durable external structure that any AI instance can orient to — while the human keeps full ownership and agency.

**Living work** happens in the user’s own storage (PARA on Google Drive, local files, or any cloud the user controls).  
**This repository** holds the developed / public method.

## Core architecture: PARA-MOC-dragon

| Piece | Role |
|-------|------|
| **PARA** | Organizational spine (Projects / Areas / Resources / Archives) |
| **MOC** | Single orientation file (`00_Orientation.md`) per multi-layer project — source of truth + handling rules |
| **Bootloader** | Short, stable file that tells any AI instance how to find the living system. **Agency** and **Consent** are defined here as standing rules. |
| **Skills** | All AI skills live in one skills home (e.g. `dragon-skills/`), including global reminders |
| **Consent rule** | Nothing structural is written without explicit user approval |

The same pattern works with any storage the user controls: cloud, local device, or networked storage. A simple bootloader command is enough for the AI to know who the user is and where the living work lives.

## Standing rules (authoritative in the bootloader)

**Agency**  
The human owns the data, the decisions, and the direction.  
AI is builder and thinking partner, not owner.

**Consent**  
Do not create, overwrite, or structurally edit orientation files, living documents, skills, reminders, or other system files without explicit user approval.  
Propose and wait.

Downstream files may echo these rules for clarity but must not redefine or soften them. Multiple independent copies create drift and competing authority.

## Credits

**PARA** (Projects • Areas • Resources • Archives)  
Originally articulated by Tiago Forte. Used here as the structural backbone.

**MOC** (Map of Content)  
The disciplined use of a single navigational / index note as a project entry point was popularized in the personal-knowledge-management community, especially through Nick Milo’s work on Maps of Content. The underlying idea of an index note is older; the clear naming and consistent practice are gratefully acknowledged.

This project combines those ideas with an explicit consent rule and a bootloader pattern so the structure is readable by both humans and AI instances.

## Agency & privacy

- The human decides what is written and what is structural.
- The AI proposes, drafts, and organizes — then waits for consent.
- Living data stays in the user’s own storage.
- This repository does not own or claim the user’s personal files.

See `ORIGIN.md` for the full discovery process and philosophy.

## Quick start for an AI instance

1. User says “Load bootloader” (or equivalent).
2. Read the bootloader file from the user’s living storage — Agency and Consent are defined there.
3. Follow the orientation file of the relevant project.
4. Skills and reminders live in the skills home (e.g. `dragon-skills/`).
5. Obey the consent rule before any structural write.

## License

MIT — see `LICENSE`.  
The license covers the method and documentation only. The user’s living data remains solely under the user’s control.

## Status

This repository is the **developed / public** expression of the method.  
Older beta-era material and previous project splits (including separate nosce-te-ipsum / shared-dragon / my-dragon tracks) are retired in favor of the current PARA-MOC architecture.

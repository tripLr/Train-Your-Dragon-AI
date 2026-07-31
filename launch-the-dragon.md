---
name: launch-the-dragon
description: Orient any Grok instance to the Train Your Dragon system. Detects new vs existing users, checks connectors, agency selections for new users, make-bootloader at end of first launch, Load bootloader for ongoing sessions. Triggers on launch the dragon, load bootloader, boot dragon, orient me, or similar.
---

# Launch the Dragon

## Purpose

- **Launch the dragon** — once (or rebuild): onboard → **make-bootloader**
- **Load bootloader** — ongoing: read living orientation file and continue

## New user (Launch — once)

1. Detect new
2. Connector check → https://grok.com/connectors if missing
3. Agency selections (before hosting)
4. Hosting choice (GitHub / Drive PARA / hybrid / other)
5. Optional Dev ID (non-personal, version checks only)
6. New User Log
7. **Make-bootloader** — create orientation file in user’s home + memory pointer
8. Optional Bootloader Log

## Existing user

1. Detect existing
2. Connector check if needed
3. **Load bootloader** — read `bootload-dragon.md` (user’s path; example Drive `Projects/bootload-dragon.md`)
4. Short status (not full Core Split)
5. Light inbox note if applicable

Do not re-run full agency/hosting on every launch.

## Make-bootloader

1. Create/confirm orientation file in chosen home
2. Seed only human-stated orientation
3. Pointer: Load bootloader → that file
4. Optional log: created/rebuilt

## Load bootloader

Triggers: Load bootloader, bootload, load orientation.  
Action: Read and apply the living orientation file. Update that file only with human confirm on structural changes.

## Standing rules

- Human keeps ownership. AI is builder and thinking partner.
- Prefer durable external systems over chat history.
- Get the process → pause for short comment before significant action.
- Show where updates are applied.
- Local rules/skills: version-check against public when relevant.

## Change log

- 2026-07-30 — Launch once → make-bootloader; ongoing Load bootloader; existing-user path slimmed.

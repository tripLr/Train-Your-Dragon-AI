---
name: launch-the-dragon
description: Orient any Grok instance to the Train Your Dragon system. Detects new vs existing users, checks available connectors, offers hosting choice for new users, loads Core Split, Bootloader Log, and standing rules. Triggers on launch the dragon, boot dragon, orient me, load train your dragon, bootload update, or similar.
---

# Launch the Dragon Skill

Boot / orientation skill for the Train Your Dragon system.

## Purpose

When a session starts cold (new instance, voice mode, limited context), or when the user says **“Bootload update”** / **“Launch the dragon”**, this skill:

1. Detects whether this is a **new user** or an **existing Dragon user**
2. For new users → checks available connectors and offers a hosting choice
3. Orients the session to the Core Split and standing rules
4. Handles the Bootloader Log

Works for any user training their own dragon, including Warrior’s Way (men’s or women’s course) or other personal development work.

## Step 0 — New-user detection

Treat the user as **new** if most of these are true:

- No prior Bootloader Log entry for this person
- No Train Your Dragon / Dragon skills already present in their environment
- No known Dragon-related repos or PARA / Dragon-Inbox structure
- Memory has no Core Split / Train Your Dragon orientation block

If signals are mixed, ask once:  
“Have you already set up Train Your Dragon, or is this a fresh start?”

## Step 1 — For new users: connector check + hosting choice

1. Inspect which connectors are actually available in this session (GitHub, Google Drive, OneDrive, Gmail, Outlook, Teams, etc.).
2. Present only the options that are real for this user.

### Hosting options (show only available ones)

| Option | Best for | Requires |
|--------|----------|----------|
| **A. GitHub full host** | Simple, versioned, everything in one place | GitHub connector |
| **B. Drive / cloud PARA style** | Privacy + ownership; living work separate from system | Google Drive or OneDrive |
| **C. Hybrid (recommended)** | System on GitHub, living work on Drive/cloud | Both GitHub + Drive (or similar) |
| **D. Other connector** | Microsoft-centric or custom setup | That connector |

3. Human chooses. Record the choice.
4. Create the minimal structure in the chosen home (with confirmation before writing):
   - Bootloader Log
   - Basic folder / repo skeleton if needed
   - First orientation entry

**Privacy rule:** Living personal data stays under the user’s ownership in the place they choose. The AI does not become the owner.

## Step 2 — Core Split (for all users)

| Layer | Home | Role |
|-------|------|------|
| **Dragon project (the system itself)** | **GitHub** (or chosen system host) | Bootloader, skills, rules, course skeleton, versioning |
| **Living personal work** | **PARA / chosen cloud** | Projects, notes, research, study, journal, discoveries, course notes |
| **Capture** | **Inbox** (Dragon-Inbox or equivalent) | Staging point → review → file into living home |

## Step 3 — Bootloader Log

**Living location:** In the user’s chosen home  
(e.g. `Projects/Train-Your-Dragon/Bootloader_Log.md` on Drive, or equivalent on GitHub/OneDrive)

**Entry format (append only):**

```
### [YYYY-MM-DD HH:MM TZ] — [Instance label]
- Platform: [Android / Web / X / Voice / Other]
- Action: Launch | Bootload update | First setup
- User type: New | Existing
- Hosting: [GitHub full | Drive PARA | Hybrid | Other]
- Notes: [optional short note]
```

Flow:
1. Read recent log entries if they exist.
2. Ask once (lightly): “What do you want to call this instance?”
3. Append a new entry.
4. Confirm the session is aligned.

## Standing rules (always load)

- Human keeps ownership. AI is builder and thinking partner.
- Prefer durable external systems over chat history.
- When user says **“Get the process”** → pause and ask for a short comment before proceeding.
- Capture first, file second.
- Agency first — never save important material without clear direction.

## Warrior’s Way note

This bootloader is course-agnostic.  
Living Warrior’s Way study (men’s or women’s) belongs in the user’s living home under a clear week / course structure (e.g. `warriors way / Week 4A/`, `Week 5/`).  
Official course skeleton, if any, can live with the system host. Personal notes and PDFs stay in the living home.

## Flow summary

1. Detect new vs existing.
2. If new → connector check → hosting choice → minimal setup.
3. Present Core Split + orientation block.
4. Bootloader Log (name instance → append).
5. Confirm aligned and ready.

## Relationship

This skill is the entry point for any person training their own dragon.  
It keeps the system portable, respects whatever connectors the user has, and never assumes one person’s private structure is universal.

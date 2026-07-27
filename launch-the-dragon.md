---
name: launch-the-dragon
description: Orient any Grok instance to the Train Your Dragon system. Detects new vs existing users, checks available connectors, directs user to grok.com/connectors if none are loaded, offers hosting choice for new users, loads Core Split, Bootloader Log, and standing rules. Triggers on launch the dragon, boot dragon, orient me, load train your dragon, bootload update, or similar.
---

# Launch the Dragon Skill

Boot / orientation skill for the Train Your Dragon system.

## Purpose

When a session starts cold (new instance, voice mode, limited context), or when the user says **“Bootload update”** / **“Launch the dragon”**, this skill:

1. Detects whether this is a **new user** or an **existing Dragon user**
2. Checks available connectors — if none (or critical ones missing), directs the user to set them up
3. For new users → offers a hosting choice based on what is actually connected
4. Orients the session to the Core Split and standing rules
5. Handles the Bootloader Log

Works for any user training their own dragon, including Warrior’s Way (men’s or women’s course) or other personal development work.

## Step 0 — New-user detection

Treat the user as **new** if most of these are true:

- No prior Bootloader Log entry for this person
- No Train Your Dragon / Dragon skills already present in their environment
- No known Dragon-related repos or PARA / Dragon-Inbox structure
- Memory has no Core Split / Train Your Dragon orientation block

If signals are mixed, ask once:  
“Have you already set up Train Your Dragon, or is this a fresh start?”

## Step 1 — Connector check

Inspect which connectors are actually available in this session.

**If no connectors are loaded (or critical ones needed for the chosen path are missing):**

Direct the user clearly:

> Connectors are not set up yet (or the ones needed are missing).  
> Go to **https://grok.com/connectors** → click **New Connector** → connect the services you want (GitHub, Google Drive, OneDrive, etc.).  
> Then come back and say **“Launch the dragon”** again.

Do not invent connectors that are not present. Only offer hosting options that match what is actually connected.

## Step 2 — For new users: hosting choice

Present only the options that are real for this user.

| Option | Best for | Requires |
|--------|----------|----------|
| **A. GitHub full host** | Simple, versioned, everything in one place | GitHub connector |
| **B. Drive / cloud PARA style** | Privacy + ownership; living work separate from system | Google Drive or OneDrive |
| **C. Hybrid (recommended)** | System on GitHub, living work on Drive/cloud | Both GitHub + Drive (or similar) |
| **D. Other connector** | Microsoft-centric or custom setup | That connector |

Human chooses. Record the choice.  
Create the minimal structure in the chosen home (with confirmation before writing).

**Privacy rule:** Living personal data stays under the user’s ownership in the place they choose. The AI does not become the owner.

## Step 3 — Core Split (for all users)

| Layer | Home | Role |
|-------|------|------|
| **Dragon project (the system itself)** | **GitHub** (or chosen system host) | Bootloader, skills, rules, course skeleton, versioning |
| **Living personal work** | **PARA / chosen cloud** | Projects, notes, research, study, journal, discoveries, course notes |
| **Capture** | **Inbox** (Dragon-Inbox or equivalent) | Staging point → review → file into living home |

## Step 4 — Bootloader Log

**Living location:** In the user’s chosen home

**Entry format (append only):**

```
### [YYYY-MM-DD HH:MM TZ] — [Instance label]
- Platform: [Android / Web / X / Voice / Other]
- Action: Launch | Bootload update | First setup
- User type: New | Existing
- Hosting: [GitHub full | Drive PARA | Hybrid | Other]
- Notes: [optional short note]
```

## Standing rules (always load)

- Human keeps ownership. AI is builder and thinking partner.
- Prefer durable external systems over chat history.
- When user says **“Get the process”** → pause and ask for a short comment before proceeding.
- Capture first, file second.
- Agency first — never save important material without clear direction.

## Warrior’s Way note

This bootloader is course-agnostic.  
Living Warrior’s Way study (men’s or women’s) belongs in the user’s living home under a clear week / course structure.  
Personal notes and PDFs stay in the living home.

## Flow summary

1. Detect new vs existing.
2. Connector check → if missing, direct to https://grok.com/connectors and stop until ready.
3. If new → hosting choice → minimal setup.
4. Present Core Split + orientation block.
5. Bootloader Log (name instance → append).
6. Confirm aligned and ready.

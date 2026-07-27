---
name: launch-the-dragon
description: Orient any Grok instance to the Train Your Dragon system. Detects new vs existing users, checks available connectors, directs to grok.com/connectors if missing, offers hosting choice, supports optional non-personal Dev ID for independent dragons, New User Log, Bootloader Log, and Core Split. Triggers on launch the dragon, boot dragon, orient me, load train your dragon, bootload update, or similar.
---

# Launch the Dragon Skill

Boot / orientation skill for the Train Your Dragon system.

## Purpose

When a session starts cold or the user says **“Launch the dragon”** / **“Bootload update”**:

1. Detect new vs existing Dragon user
2. Check connectors → if missing, direct to https://grok.com/connectors
3. New users → hosting choice + optional Dev ID + New User Log
4. Orient to Core Split and standing rules
5. Bootloader Log

Works for any independent dragon (including a spouse running their own Warrior’s Way course). No assumption of shared accounts or shared storage.

## Step 0 — New-user detection

Treat as **new** if most signals are true (no prior Bootloader / New User Log, no Dragon skills, no known structure, no Core Split in memory).  
If mixed, ask once: “Have you already set up Train Your Dragon, or is this a fresh start?”

## Step 1 — Connector check

If no connectors (or critical ones missing):

> Connectors are not set up yet.  
> Go to **https://grok.com/connectors** → New Connector → connect what you need.  
> Then say **“Launch the dragon”** again.

Only offer hosting options that match real connectors.

## Step 2 — New user: hosting + optional Dev ID + New User Log

### Hosting choice (show only available)

| Option | Best for | Requires |
|--------|----------|----------|
| A. GitHub full host | Simple, versioned | GitHub |
| B. Drive / cloud PARA | Privacy + ownership | Google Drive or OneDrive |
| C. Hybrid (recommended) | System on GitHub, living on Drive | Both |
| D. Other | Microsoft-centric / custom | That connector |

### Optional Dev ID (development / testing / update-check only)

- **Optional.** Ask once: “Do you want an optional development ID for version/update checks? It contains no personal information.”
- If yes, generate:
  ```
  payload = "TYD|" + SYSTEM_VERSION + "|" + UTC_TIMESTAMP_TO_SECOND
  id     = first 16 chars of SHA-256(payload)
  ```
- Example version: `2026-07-26.1`
- **Must contain nothing about the user** (no name, account, device, email).
- Purpose: let independent dragons (no GitHub) compare system version with the public Train-Your-Dragon-AI line, and let two test instances correlate during development only.

### New User Log (living, human-owned)

Create or append in the user’s chosen home (e.g. `Train-Your-Dragon/New_User_Log.md`):

```
### [YYYY-MM-DD HH:MM TZ] — First setup
- User type: New
- Hosting: [chosen]
- Platform: [Android / Web / Voice / Other]
- System version: [e.g. 2026-07-26.1]
- Dev ID (optional): [hash or "none"]
- Notes: [optional short non-personal note]
```

No personal identifiers unless the human themselves adds them.

## Step 3 — Core Split

| Layer | Home | Role |
|-------|------|------|
| Dragon project (system) | GitHub or chosen system host | Skills, rules, versioning |
| Living personal work | PARA / chosen cloud | Notes, course study, journal, research |
| Capture | Inbox | Staging → file into living home |

## Step 4 — Bootloader Log

Append in the user’s home. Include optional Dev ID only if they opted in.

## Standing rules

- Human keeps ownership. AI is builder and thinking partner.
- Prefer durable external systems over chat history.
- “Get the process” → pause and ask for a short comment before proceeding.
- Capture first, file second. Agency first.

## Update check without GitHub

An independent dragon may store its last system version (+ optional Dev ID).  
On launch/bootload, if the user allows, it may fetch only the public version from Train-Your-Dragon-AI and report whether a newer system version exists.  
No user data is sent — version comparison only.

## Warrior’s Way note

Course-agnostic. Living study (men’s or women’s) stays in the user’s living home under their week structure.

## Flow summary

1. Detect new vs existing  
2. Connector check → redirect to grok.com/connectors if needed  
3. New → hosting choice → optional Dev ID → New User Log  
4. Core Split orientation  
5. Bootloader Log  
6. Confirm aligned  

## Privacy

Dev ID and New User Log as specified contain no personal data.  
ID is optional and for development/testing/update checks only.

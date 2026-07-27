---
name: launch-the-dragon
description: Orient any Grok instance to the Train Your Dragon system. Detects new vs existing users, checks available connectors, directs to grok.com/connectors if missing, offers hosting choice, supports optional non-personal Dev ID for independent dragons, New User Log, Bootloader Log, and clean status output. Triggers on launch the dragon, boot dragon, orient me, load train your dragon, bootload update, or similar.
---

# Launch the Dragon Skill

Boot / orientation skill for the Train Your Dragon system.

## Purpose

When a session starts cold or the user says **“Launch the dragon”** / **“Bootload update”**:

1. Detect new vs existing Dragon user
2. Check connectors → if missing, direct to https://grok.com/connectors
3. New users → hosting choice + optional Dev ID + New User Log
4. Existing users → clean status output + light inbox awareness
5. Bootloader Log

Works for any independent dragon (including a spouse running their own Warrior’s Way course). No assumption of shared accounts or shared storage.

## Step 0 — New-user detection

Treat as **new** if most signals are true (no prior Bootloader / New User Log, no Dragon skills, no known structure).  
If mixed, ask once: “Have you already set up Train Your Dragon, or is this a fresh start?”

## Step 1 — Connector check

If no connectors (or critical ones missing):

> Connectors are not set up yet.  
> Go to **https://grok.com/connectors** → New Connector → connect what you need.  
> Then say **“Launch the dragon”** again.

Only offer hosting options that match real connectors.

## Step 2 — New user: agency selections first, then hosting

### Your agency selections begin training your dragon!

Present this checklist **before** hosting choice. Optional items — user marks what they wish:

```
## Your agency selections begin training your dragon!

- [ ] I keep ownership of my living files
- [ ] I decide where notes and course work live
- [ ] I treat AI output as material to question, not final truth
- [ ] I want a pause before irreversible actions
- [ ] I prefer durable systems over relying on chat history
- [ ] I may use an optional non-personal Dev ID for version checks only
- [ ] Formal issues go to the public GitHub repo
- [ ] I can stop or change any of this later
- [ ] I want to know where processes and files are updated and created in every instance
```

Agency first, then structure.

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

## Step 3 — Existing user: Clean status output

For existing users, use this short status format instead of a long Core Split explanation:

```
Loading dragon from GitHub  
Loading your dragon from Google Drive  
Dragon Inbox in Google Drive ready
```

Then:

- If the inbox has items, note it briefly (e.g. “Inbox has items”).
- Ask: **“Sort and update the inbox now?”**

(The actual sorting is handled by the personal-assistant skill.)

Do **not** repeat the full Core Split table on every launch unless the user asks for orientation details.

## Step 4 — Bootloader Log

Append in the user’s home. Include optional Dev ID only if they opted in.

```
### [YYYY-MM-DD HH:MM TZ] — [Instance label]
- Platform: ...
- Action: Launch | Bootload update | First setup
- User type: New | Existing
- Hosting: ...
- Dev ID: [hash or "none"]
- Notes: ...
```

## Standing rules

- Human keeps ownership. AI is builder and thinking partner.
- Prefer durable external systems over chat history.
- “Get the process” → pause and ask for a short comment before proceeding.
- Capture first, file second. Agency first.
- **All future and now updates show where the update is applied.** (State the file or location being changed.)
- **Show where processes and files are updated and created in every instance.**

## Update check without GitHub

An independent dragon may store its last system version (+ optional Dev ID).  
On launch/bootload, if the user allows, it may fetch only the public version from Train-Your-Dragon-AI and report whether a newer system version exists.  
No user data is sent — version comparison only.

## Warrior’s Way note

Course-agnostic. Living study (men’s or women’s) stays in the user’s living home under their week structure. Personal notes never required on GitHub.

## Flow summary

**New user**  
1. Detect new  
2. Connector check  
3. Agency selections → hosting → optional Dev ID → New User Log  
4. Bootloader Log  

**Existing user**  
1. Detect existing  
2. Connector check (if needed)  
3. Clean status output + light inbox note  
4. “Sort and update the inbox now?”  
5. Bootloader Log  

## Privacy

Dev ID and New User Log as specified contain no personal data.  
ID is optional and for development/testing/update checks only.

## Change log

- **2026-07-26** — Existing-user flow simplified to clean status + inbox awareness. Added standing rule: all updates must show where they are applied.
- **2026-07-26 (later)** — Added agency item + standing rule: “I want to know where processes and files are updated and created in every instance.”
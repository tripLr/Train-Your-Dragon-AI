# Dragon ID + New User Log

**Purpose:** Support independent dragons (e.g. a second person running their own instance) that may not have GitHub, while allowing optional development/testing correlation and update checks.

**Rules:**
- ID is **optional**
- Used **only for development / testing / update checks**
- **Cryptographic hash only**
- Payload = version + date-time-to-the-second
- **Nothing about the user** (no name, account, device, email, or personal markers)

---

## Optional Dragon System ID (dev/test only)

### Generation (when needed)
```
payload = "TYD|" + VERSION + "|" + UTC_TIMESTAMP_TO_SECOND
id     = first 16 chars of SHA-256(payload)
```

Example payload: `TYD|2026-07-26.1|2026-07-26T18:33:00Z`  
Example id: `a3f91c2e8b7d4e01` (opaque)

### When to create
- Only if the user opts in for development testing, **or**
- When a non-GitHub dragon needs a way to ask “is there a newer system version?”

### What it must never contain
- User name, handle, email, phone
- Device ID, IP, account ID
- Any personal or course content

---

## New User Log (living, human-owned)

Location: user’s chosen home  
File suggestion: `Train-Your-Dragon/New_User_Log.md` or section inside Bootloader_Log.md

### Entry format (append only)

```
### [YYYY-MM-DD HH:MM TZ] — First setup
- User type: New
- Hosting: [GitHub full | Drive PARA | Hybrid | Other]
- Platform: [Android / Web / Voice / Other]
- System version: [e.g. 2026-07-26.1]
- Dev ID (optional): [hash or "none"]
- Notes: [optional short non-personal note]
```

---

## Update check without GitHub

1. Public Train-Your-Dragon-AI publishes a tiny version marker.
2. Independent dragon stores last-known system version + optional Dev ID.
3. On launch/bootload (if user allows): fetch public version only → compare → report.
4. No user data is sent. Version comparison only.

---

## Privacy summary

| Item | Contains user data? |
|------|---------------------|
| Dragon System ID (hash) | No |
| New User Log (as specified) | No (unless human adds it) |
| Update check traffic | Version only |

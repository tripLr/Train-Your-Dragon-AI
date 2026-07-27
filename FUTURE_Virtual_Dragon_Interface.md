# Future Track — Virtual Dragon Interface

**Status:** Concept / next development track  
**Date noted:** 2026-07-26  
**Origin:** Train Your Dragon beta planning (paid services + private journals)

---

## Problem

Many useful services are paid or private and have no official Grok connector:

- Discord servers
- Coach Chris journal / forgeworks-style sites
- Other membership portals, private journals, course platforms

Grok cannot natively log in with the user’s credentials and read those systems.

---

## Concept: Virtual Dragon Interface

A thin web layer (or MCP server) that:

1. The user authenticates to once (their credentials stay with them / the interface)
2. Maintains an authenticated session to the paid/private service
3. Exposes only the data the user chooses (read journal entries, list channels, etc.) back to Grok via MCP or a controlled API
4. Never stores the user’s password in Grok itself

Think of it as a **personal authenticated bridge** — closer to a controlled VPN + session proxy for AI than to giving the AI raw login details.

---

## What already exists in the market (research snapshot)

| Approach | Examples | Notes |
|----------|----------|-------|
| **Remote MCP + OAuth** | Truthifi, Massive, Claude custom connectors | Service owner builds OAuth; user authorizes; AI never sees password. Best when the service cooperates. |
| **Cloud browser + authenticated profiles** | Browserbase, Browserless Authenticated Profiles | User logs in once in a controlled browser; agent reuses the session. Good for sites with no API. |
| **Credential proxy / agent keys** | agentkeys, OneCLI-style gateways | Inject credentials at request time with allow-lists; keep secrets out of the model. |
| **Local / self-hosted browser agents** | Playwright + local CDP, various open projects | Full control, higher ops burden. |

Closest analogues to “Virtual Dragon Interface”:

- **Browserbase / Browserless authenticated profiles** — login once, reuse session for agents
- **Custom remote MCP with OAuth** — cleanest when the target service supports it
- **Self-hosted bridge page** that holds the session and exposes a narrow MCP surface to Grok

---

## Design principles for Train Your Dragon

1. **User owns the credentials and the bridge.** Grok never becomes the password store.
2. **Narrow surface** — only the data the user explicitly allows is visible to the AI.
3. **Revocable** — user can kill the session / bridge at any time.
4. **Optional and explicit** — never required for core Dragon use.
5. **Fits Core Split** — the interface is infrastructure the user controls; living data still lands in their PARA / chosen home.

---

## Possible first targets (when built)

- Discord (selected servers / channels)
- Coach Chris / forgeworks-style journal
- Other membership or course portals the user already pays for

---

## Next steps (when this track is opened)

1. Decide self-hosted vs managed browser service vs pure MCP-OAuth path.
2. Prototype one narrow use case (e.g. read-only journal entries).
3. Document security model and threat assumptions clearly.
4. Keep it optional — core bootloader and PARA flow must work without it.

---

*Recorded as a future development track. Not implemented yet.*

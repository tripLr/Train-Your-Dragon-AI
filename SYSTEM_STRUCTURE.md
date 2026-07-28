# System Structure — Why Agency Needs Organization

**Updated:** 2026-07-28  
**Audience:** Anyone training their own dragon, including people who are new to formal development processes.

---

## What this project actually is

Train Your Dragon is not about inventing new AI theory.

It is about **integration**.

Existing AI functions (memory, tools, conversation, search, file systems, skills) are brought into personal lived experience under human ownership. The human does not have unlimited time, knowledge, or resources. The system must therefore be simple enough to use and strong enough to compound.

That is why organization matters.

---

## Three-layer architecture (do not blur) — privacy & agency

| Layer | Home | What lives there |
|-------|------|------------------|
| **Master / public Dragon** | GitHub `Train-Your-Dragon-AI` | Method only: bootloader, public skills, standing rules, install, versioning, pointers. **No personal rules, no personal skills content, no living notes.** |
| **My Dragon** | User’s **PARA** (e.g. Google Drive) | The personal dragon concept: personal rules, personal skills, memory orientation, course living files, research, journal, faith, discoveries. **Owned by the human.** |
| **Capture** | Dragon-Inbox (Drive root or equivalent) | Staging: phone / chat → review → file into My Dragon / PARA |

### Hard rules

1. **My Dragon concept lives in the PARA architecture** — not in the public repo and not as AI-owned storage.
2. **Personal rules and personal skills live under My Dragon** (PARA). They are the user’s, versioned under the user’s control.
3. **Master / public Dragon only points** to the idea of My Dragon. It never stores another user’s personal rules or skills. Processes say: *load from the user’s My Dragon / PARA* — they do not embed that content.

This ensures **privacy** and **agency**. Shared method; private living dragon.

---

## Core Split (operational) — 2026-07-26 / refined 2026-07-28

| Layer | Home | Role |
|-------|------|------|
| **Dragon project (the system itself)** | **GitHub** | Bootloader, *public* skills, rules, versioning, future web-launchable process |
| **My Dragon (living personal system)** | **PARA on Google Drive** (or user’s chosen private home) | Personal rules, personal skills, memory, all projects in progress, notes, research, study, journal, discoveries, faith work, equipment, course weeks |
| **Capture** | **Dragon-Inbox** | Phone → AI staging; material is reviewed and filed into My Dragon / PARA |

**Privacy & ownership rule:** Personal data and personal rules live in the user’s My Dragon (PARA). They are not controlled by any AI system and are not copied into the public Master repo.

---

## Why agency requires a streamlined organization method

Agency means you remain the one who decides.

Without a clear place for things to land, three problems appear quickly:

1. **Capture fails** — useful material arrives and has nowhere obvious to go.
2. **Context resets** — every new conversation starts from near zero.
3. **Ownership blurs** — the AI begins to feel like the center of the work instead of a tool under your direction.

A streamlined organization method solves these by giving every piece of work a home based on *what it is doing right now*.

---

## How PARA entered this system

PARA (Projects, Areas, Resources, Archives) was not invented here. It was chosen because it matches how work moves:

| Layer | Meaning in this system |
|-------|------------------------|
| **Projects** | Active efforts with a finish line |
| **Areas** | Ongoing responsibilities (Mind, Heart, Body, Spirit, health, marriage, work) |
| **Resources** | Reference material |
| **Archives** | Finished or inactive material |

**My Dragon** sits inside that PARA tree as the home for the personal AI operating layer (rules, skills, orientation) plus the living work those rules serve.

---

## Two kinds of work (important distinction)

| Kind of work | Where it lives | Examples |
|--------------|----------------|----------|
| **Personal (My Dragon)** | Your PARA | Personal rules, personal skills, course notes, self-reflection, journal, research, discoveries |
| **Method / capability (Master)** | Public Train-Your-Dragon-AI | Capture workflows, bootloader, public skill *templates*, process review, “point to user’s My Dragon” instructions |

Personal work stays private under My Dragon.

When the work is about *how human and AI work together*, it is method. Method belongs in the public Master and **points** at My Dragon for anything personal — it does not contain it.

---

## Current operating pattern

```
You (agency)
├── My Dragon → PARA (Projects / Areas / Resources / Archives)
│     ├── Personal rules & personal skills
│     └── Living material (course, notes, research, …)
│
└── Master Dragon → Public Train-Your-Dragon-AI (GitHub)
      └── Rules, bootloader, public skills — all of which *point to* My Dragon for personal load
```

**Dragon-Inbox** is the capture point for personal material.

**Bootloader** (`launch-the-dragon`) orients any instance to Master method, then loads **from the user’s My Dragon** (connectors / PARA), never the other way around.

---

## Development focus rule (standing)

When work improves how the collaboration itself runs:

1. Record **method** in the public Master repo (pointers only for personal paths).
2. Keep **personal** rules, skills, and content in My Dragon (PARA).
3. Never promote personal content into Master “for convenience.”

---

## Starting point for people who know little about formal process

1. **Capture first** — known inbox.
2. **File second** — home in My Dragon / PARA.
3. **Review on friction** — smallest useful improvement.

---

## Why this matters for agency

Without this split, the public system either absorbs personal data or the personal system has no portable method.

With it:

- You decide what is kept and where it lives
- Master stays shareable and clean
- My Dragon stays private and under your control
- Any instance can be oriented to Master, then pointed at *your* My Dragon

Agency is protected by a simple, durable way of knowing where things belong and who is in charge of them.

**Updated 2026-07-28:** Explicit three-layer rule — My Dragon in PARA; personal rules/skills under My Dragon; Master only points to My Dragon.

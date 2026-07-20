# Train Your Dragon AI

Public principles and starter skills for training a personal AI collaborator.

## Why this exists

Most AI conversations start from zero every time. Chat history becomes noisy or disappears.

This project captures a practical alternative that emerged from real use: build durable external systems (clear skills + a well-structured memory file). The AI becomes a consistent thinking partner instead of a forgetful tool.

Private, highly personal, or course-specific skills stay outside this public repo.

## How this collaboration model works

The goal is not a smarter chatbot. The goal is a reliable thinking partner that compounds over time.

Core operating pattern:

1. Prefer durable external systems (skills + a structured memory file) over relying on chat history.
2. Do not attempt to design the perfect system up front. Use the current version → notice friction → improve the smallest useful piece.
3. Keep ownership with the human. The AI is a builder and thinking partner; the human decides what matters and what gets kept.
4. Build deliberate **versioning** and review into the system itself.

### Why versioning matters

Healthy human societies do not treat beliefs, laws, institutions, or personal identities as permanently fixed. They allow revision, debate, and reversion when something becomes rigid, outdated, or harmful. The same principle applies to AI collaboration.

Versioning in this system means:

- Skills and major preferences are treated as living versions, not final truth.
- When a review trigger is hit (roadblock, approximately 6 months, or meaningful model improvement), the human can examine the current version and, if needed, revert to a previous one or evolve it.
- Deep self-reflection is stored as dated versions so earlier reasoning remains available and can be questioned later.

Without versioning, both human and AI risk locking in temporary conclusions as permanent identity or unchangeable rules. Versioning keeps the system humble, adaptable, and aligned with how healthy human learning and culture actually work.

## Skills and core files in this repo

- [principles.md](principles.md) — Foundational rules that guide everything else
- [personal-assistant.md](personal-assistant.md) — Lightweight day-to-day support (to-dos, reminders, light organization)
- [research-skill.md](research-skill.md) — Research that moves from evidence toward understanding
- [memory-skill.md](memory-skill.md) — How to build and maintain a durable, versioned personal memory system
- [public-update-process.md](public-update-process.md) — Required checklist for any change to this public repository (human review before push)
- [ORIGIN.md](ORIGIN.md) — Permanent public record of how the versioning approach was created and why it exists
- [FUTURE.md](FUTURE.md) — Open future goals that others are welcome to pick up
- [LICENSE](LICENSE) — MIT License with permanent credit and history-preservation requirement

## Private Conversation Archive Pattern

In addition to a structured memory file, many users benefit from a **private conversation archive** on GitHub.

This is a separate private repository that stores cleaned conversation exports. It gives you an external, durable record that is not dependent on any AI model’s internal memory.

Recommended structure:

```
my-dragon-memory/          (or any name you choose)
├── README.md
├── INDEX.md               # Master index of conversations
├── conversations/         # Full cleaned exports
└── subjects/              # Tiny pointer system by topic
```

This pattern supports a simple skill that can later say “check our conversations” and look up prior durable discussion under your control.

Keep the archive private. Be selective about what you store.

## Example of a personal working-style entry (for your private memory)

This is the kind of short, dated entry that belongs in *your own* private memory file — never in a public skill:

```
- Preferred working style [YYYY-MM-DD]: Builds durable external systems (skills + memory) instead of relying on chat history. Prefers refining through real-time iteration. Keeps ownership — AI is builder and partner, not owner. Prefers usable progress over premature perfection. Review on roadblock, after ~6 months, or when the model improves.
```

Copy the pattern. Fill in what is actually true for you.

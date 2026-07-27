# Public Update Process

This document covers both directions of working with **Dragon Master** (the public source of truth).

See also: [DRAGON_MASTER.md](DRAGON_MASTER.md)

The goal is simple: keep personal information out of the public record, keep the system versionable, and keep agency with the human.

---

## 1. Contributing *to* Dragon Master

**Standard interface: GitHub Issues**

### Required Checklist (every contribution)

1. **Strip all personal references**  
   Remove names, private dates, specific life details, private preferences, and anything that belongs only in private memory or private skills.

2. **Check against the standing rules and principles**  
   Especially ownership, usable progress, built-in review, and deliberate versioning.

3. **Update the skill list in README.md** if a new skill is added or removed (when the change is later implemented).

4. **Write a clear description** of the intent of the change.

5. **Human review**  
   The human must look at the final content and explicitly approve before it is submitted.

### How to submit

- **Preferred path for everyone:** Open a GitHub Issue on the Dragon Master repo with the clean proposal.
- **Owner (repo owner) options:**  
  When proposing a change, choose:  
  A. Update the dragon directly (after this checklist)  
  B. Create an Issue for later review  
  C. Cancel
- **Developers who forked:** May open a Pull Request if preferred, but Issues remain the simple standard path.
- **Users without GitHub:** System produces a clean package that can be pasted into an Issue or sent another way.

### Why this process exists

Versioning only works if the public record stays clean.  
A single personal detail that leaks becomes permanent public history.  
Requiring human review *before* submission is the practical safeguard that keeps the system humble and reversible.

---

## 2. Updating *from* Dragon Master (Pull)

1. Compare local skills/rules against the public versions.
2. Show a clear summary of differences.
3. Human chooses what to accept (all / selected / none).
4. Apply only after confirmation.
5. Log the update (what changed, from which commit).

This applies to the owner, forkers, non-GitHub users, and future apps.

---

## Versioning of this process

This process itself is versioned. Review it when it hits friction, after ~6 months, or when the model improves.

**Change log**
- **2026-07-26** — Expanded to cover both directions. GitHub Issues set as the standard contribution interface. Linked to new DRAGON_MASTER.md.

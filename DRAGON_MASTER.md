# Dragon Master

**Dragon Master** is the public source of truth for the Train Your Dragon system.

It currently consists of:
- `tripLr/Train-Your-Dragon-AI` (core principles, standing rules, skills, process)
- `tripLr/Shared-Dragon-AI` (shareable skills)

This is the public method layer. Living personal work stays private (PARA / Drive / local).

---

## Two Directions

### 1. Update *from* Dragon Master (Pull)

Anyone can receive improvements from the public source.

**Process:**
1. Compare local skills/rules against the public versions on Dragon Master.
2. Show a clear summary of differences.
3. Human chooses: accept all, accept selected, or skip.
4. Apply only after confirmation.
5. Log what was updated and from which commit.

**Commands / triggers:**
- “Update from Dragon Master”
- “Check Dragon Master for updates”
- Optional check during “Launch the dragon” / “Bootload update”

**For different users:**
| User type | How it works |
|-----------|--------------|
| Owner | Same process + option to review via Issue |
| Forker | Pull latest into fork, then decide what to keep |
| No GitHub | System fetches public version when online → shows differences → updates local/Drive files only with approval |
| Future app | Same flow via API |

### 2. Contribute *to* Dragon Master (Push / Propose)

**Standard interface: GitHub Issues**

This keeps one simple path for everyone.

**Process:**
1. Prepare the change (skill, rule, documentation, etc.).
2. Run the public-update checklist (strip personal data, check principles, etc.).
3. Create a clean contribution package.
4. Open a **GitHub Issue** on the Dragon Master repo with the proposal.
5. Owner reviews the Issue and decides whether to implement.

**Owner (you) special options:**
When you propose something to Dragon Master, the system will ask:

> You own this Dragon Master.  
> Do you want to:  
> A. Update the dragon directly (after checklist)  
> B. Create an Issue for later review  
> C. Cancel

**For other users:**
- Developers who forked → can still open a Pull Request if they prefer, but Issues are the recommended simple path.
- Users with no GitHub → system produces a clean package they can paste into an Issue or send another way.

---

## Why GitHub Issues as the single interface

- One consistent place for proposals
- Works for owner, forkers, and non-GitHub users
- Easy to review, discuss, and track
- Compatible with future web app or phone app (via GitHub API)
- Keeps the public record clean and versioned

---

## Relationship to local / private dragons

- **Dragon Master** = public method, rules, skills, process
- **My dragon** = your private instance + living work (memory, notes, PARA, private skills)

You train your own dragon. Dragon Master supplies the shared, improved method. You decide what to pull in and what to keep private.

---

## Version checking

Local rules and skills must be version-checked against Dragon Master.  
When differences exist, the human is shown them and stays in control of which version is active.

See also: [STANDING_RULES.md](STANDING_RULES.md) and [public-update-process.md](public-update-process.md).

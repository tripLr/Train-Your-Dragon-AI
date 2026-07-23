# Durability Test — In Progress

**Started:** 2026-07-22  
**Status:** Active

## Purpose

This is a deliberate test of making the Train Your Dragon personal AI operating layer durable across instances, devices, and limited-skill sessions (including voice).

## What is being tested

1. **Private core** lives in `My-Dragon-AI`
   - memory-backups/
   - history/
   - my-research/ (nosce-te-ipsum + train-my-faith)

2. **Skill recovery** lives in `Shared-Dragon-AI`
   - Versioned backups of custom skills

3. **Public philosophy** remains in `Train-Your-Dragon-AI`

4. **Orientation methods**
   - Memory-based orientation block (everyday sessions)
   - `launch-the-dragon` skill (cold starts / limited sessions)
   - Future: optional public/unlisted bootloader page

## Key Principle Confirmed in This Test

The system learns the user through the user’s own research and self-development.  
The private `my-research/` tree is the lived expression of that principle.

## Important Development Note

This marks the transition from “skills and memory that work in one environment” to “a recoverable, user-owned operating layer that can be re-oriented in any instance.”

The test is intentionally practical and incremental. Results and refinements will be recorded as the system is used across different session types.

---

*Documented 2026-07-22 as part of the active durability test.*

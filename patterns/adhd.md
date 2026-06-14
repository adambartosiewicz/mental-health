# Patterns: ADHD

## Purpose

Catalog of recurring ADHD-shaped patterns: attention, initiation, transition, time perception, hyperfocus, follow-through, and the emotional consequences of those failing. Patterns are **analytical artifacts** supporting `psychological-map.md`. The goal is to make the patterns observable enough to design around — not to label every distraction as "ADHD."

## Update rules

- A pattern is added only after **at least 3 distinct observations on different days**.
- Every entry has the five required fields: **description, evidence, counter-evidence, confidence, experiments.**
- Each entry distinguishes:
  - **mechanism** (initiation failure, transition cost, hyperfocus crash, working-memory drop, time blindness)
  - **context** (time of day, type of task, environment, presence of others)
  - **downstream effect** (missed thing, mood drop, self-criticism loop)
- Note what does and does not work to interrupt the pattern, with sources.
- Self-criticism that follows an ADHD episode is a related but distinct pattern — link it; do not merge it.
- Stimulant medication, sleep, and exercise are major moderators. Note when an entry depends on those conditions.
- Patterns may *propose* updates to `psychological-map.md` (ADHD Model) but never replace it.

## Entry template

```markdown
### <Pattern name>

- **Description:** <plain-language description: mechanism + context + downstream effect>
- **Evidence:** `sessions/...`, `journal/...`
- **Counter-evidence:** <contexts where it would have been expected but did not occur>
- **Confidence:** low / medium / high
- **Experiments:** `experiments/...` (or "proposed: <one-line idea>")
- **Moderators:** <sleep, stimulants, body state, environment>
- **What has interrupted it:** <strategies that worked, with sources>
- **What has not worked:** <tried and failed, with sources>
- **Map status:** not promoted / proposed for map / present in map (`section`)
- **Last reviewed:** YYYY-MM-DD
```

## Example

```markdown
### Unstructured-weekend collapse

- **Description:** On Saturdays/Sundays with no plans, no commitments, and no external schedule to anchor to, initiation fails. Wake late, browse phone, half-start three things, finish none, mood crash by Sunday evening. Downstream: self-criticism loop, anxiety spike about Monday.
- **Evidence:** `sessions/2026-04-27-saturday-flat.md`, `sessions/2026-05-02-saturday-flat.md`, `sessions/2026-05-09-saturday-flat.md`
- **Counter-evidence:** Did not collapse on 2026-04-13 — had a single early plan with a friend. Suggests external anchor is the active variable.
- **Confidence:** medium
- **Experiments:** `experiments/2026-05-10-saturday-anchor.md`
- **Moderators:** Worse without exercise that morning. Better when partner is around.
- **What has interrupted it:** Pre-scheduled outdoor activity before 11am.
- **What has not worked:** "I'll just decide what to do when I wake up."
- **Map status:** proposed for map (ADHD Model → Motivation and initiation)
- **Last reviewed:** 2026-06-09
```

## Sections

### Active patterns

<!-- entries here -->

### Watch list (sub-threshold)

<!-- candidate patterns with 1–2 observations, not yet promoted -->

### Weakened / under review

<!-- patterns that previously held but are losing support -->
